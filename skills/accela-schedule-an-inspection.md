---
name: accela-schedule-an-inspection
description: Check whether an inspection type can be booked against a permit in an Accela agency, find an available date, and schedule it.
api: Accela Construct API (V4)
generated: '2026-09-06'
method: generated
source: openapi/accela-inspections-openapi.yml, openapi/accela-settings-openapi.yml
base_url: https://apis.accela.com/v4
scopes: [inspections, records, settings]
operations:
  - v4.get.records.ids
  - v4.get.settings.inspections.types
  - v4.get.inspections.checkAvailability
  - v4.get.inspections.availableDates
  - v4.post.inspections.schedule
  - v4.get.records.recordId.inspections
  - v4.get.inspections.ids
  - v4.put.inspections.id
safety: write — non-idempotent
---

# Schedule an inspection

Inspections are the largest sub-tree in the Construct contract (56 operations) and the flow is unusually well
supported: unlike most of this API, it gives you two real pre-flight checks before the write.

## Steps

1. **Confirm the record.** `v4.get.records.ids` — `GET /v4/records/{ids}`. The record must exist and be in a
   status the agency allows inspections against.
2. **Get this agency's inspection types.** `v4.get.settings.inspections.types` — `GET /v4/settings/inspections/types`.
   Inspection type names are agency-configured.
3. **Check it can be booked.** `v4.get.inspections.checkAvailability` — `GET /v4/inspections/checkAvailability`.
   This is the closest thing to a dry-run anywhere in this API. Use it.
4. **Find a date.** `v4.get.inspections.availableDates` — `GET /v4/inspections/availableDates`.
5. **Schedule.** `v4.post.inspections.schedule` — `POST /v4/inspections/schedule`. Non-idempotent: a retry after
   a timeout can double-book. Confirm with step 6 before retrying.
6. **Confirm.** `v4.get.records.recordId.inspections` — `GET /v4/records/{recordId}/inspections`.

## Changing or cancelling

`v4.put.inspections.id` updates a scheduled inspection. `v4.delete.inspections.ids` deletes one, permanently
and with no restore path. Accela publishes no cancellation window, so do not assert one to a user — check the
agency's own rules.

## Notes

- Two operations added in Construct 4.6.5 (January 2026) govern who may see what:
  `GET /v4/inspections/permissions` and `GET /v4/records/types/security`. If field-staff permissions matter to
  your integration, check the agency is on 4.6.5 or later via `v4.get.serverProperties`.
- Inspection results hang off checklists: `/v4/inspections/{inspectionId}/checklists` and then
  `/checklistItems`, each with their own custom forms and custom tables.
