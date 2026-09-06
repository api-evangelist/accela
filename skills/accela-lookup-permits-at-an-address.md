---
name: accela-lookup-permits-at-an-address
description: Find every permit, licence, inspection and open case attached to a street address in an Accela-run government agency, read-only and safe to run without approval.
api: Accela Construct API (V4)
generated: '2026-09-06'
method: generated
source: openapi/accela-addresses-parcels-owners-openapi.yml, openapi/accela-records-openapi.yml, openapi/accela-agencies-openapi.yml
base_url: https://apis.accela.com/v4
scopes: [addresses, records, parcels, inspections, agencies]
operations:
  - v4.get.agencies
  - v4.get.agencies.name.environments
  - v4.get.addresses
  - v4.get.addresses.id
  - v4.get.addresses.id.parcels
  - v4.get.addresses.id.records
  - v4.get.records.ids
  - v4.get.records.recordId.inspections
  - v4.get.parcels.id.records
safety: read-only
---

# Look up permits at an address

Every call is read-only. Nothing here writes to a government system of record.

## Before you start

You cannot call this API "for Accela". You call it **for one agency**. Decide which one first.

1. `v4.get.agencies` — `GET /v4/agencies` lists agencies. `v4.get.agencies.name.environments` gives the environment names for one.
2. Send `x-accela-agency` and `x-accela-environment` on every request, or use an access token that embeds them. If you send both a token and the headers, the values must match or you get `invalid_token`.
3. If you have no agency, stop. There is no cross-Accela address search.

Read-only address and record lookups are among the 34 operations whose authorization type is **No authorization required**, so a citizen app can make them with `x-accela-appid` + `x-accela-agency` + `x-accela-environment` and no user token. What comes back is whatever that agency has granted its anonymous user — a `forbidden` here is an agency permission setting, not a bug.

## Steps

1. **Find the address.** `v4.get.addresses` — `GET /v4/addresses` with the street filters. Take the `id`.
2. **Get the records.** `v4.get.addresses.id.records` — `GET /v4/addresses/{id}/records`. This is the answer to "what has happened at this property": permits, licences, code cases, service requests.
3. **Widen to the parcel if the address is thin.** `v4.get.addresses.id.parcels` then `v4.get.parcels.id.records`. Work recorded against the parcel rather than the street address will only appear this way.
4. **Read record detail.** `v4.get.records.ids` — `GET /v4/records/{ids}`, comma-delimited, so batch them into one call rather than looping.
5. **Get inspection history per record.** `v4.get.records.recordId.inspections`.

## Conventions that will bite you

- **Pagination is offset/limit.** Default `limit` is 25, max is 1000, and the response carries `page.hasMore`. A property with a long permit history will silently truncate at 25 if you do not page.
- **Trim the payload with `fields`.** `?fields=status,openedDate` returns only those first-level fields under `result`. `id` always comes back. Field names are case-sensitive.
- **Record type vocabulary is agency-specific.** "Permit/SingleFamilyHouse/Roof/Final" in one agency is "Building/Residential/SingleFamily/RoofFinal" in the next. Call `v4.get.settings.records.types` for the agency's own list rather than pattern-matching strings you learned elsewhere.
- **Errors.** `{status, code, message, more, traceId}`. Branch on `code`, not on the message. Quote `traceId` to support.
- **Rate limits.** Per-app, agency-configured, enforced since Construct 4.6.5.3 (June 2026). Watch `X-RateLimit-Remaining` and back off on 429 using `X-RateLimit-Reset`. No operation declares 429 in the spec, so a generated client will not handle it.
