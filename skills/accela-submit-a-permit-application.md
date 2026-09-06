---
name: accela-submit-a-permit-application
description: Create a permit or licence record in an Accela agency, attach the applicant, address and plan documents, and confirm it landed — with the retry and rollback caveats this API's lack of idempotency forces on you.
api: Accela Construct API (V4)
generated: '2026-09-06'
method: generated
source: openapi/accela-records-openapi.yml, openapi/accela-settings-openapi.yml, openapi/accela-documents-openapi.yml
base_url: https://apis.accela.com/v4
scopes: [records, settings, documents, addresses, contacts]
operations:
  - oauth2.token
  - v4.get.serverProperties
  - v4.get.settings.records.types
  - v4.get.records.describe.create
  - v4.post.records
  - v4.post.records.recordId.addresses
  - v4.post.records.recordId.contacts
  - v4.post.records.recordId.documents
  - v4.get.records.ids
  - v4.get.records.recordId.workflowTasks
safety: write — irreversible, non-idempotent
---

# Submit a permit application

**Read this before the steps.** This flow writes to a government system of record. The Accela Construct API has **no idempotency key**, **no dry-run mode**, and **no restore operation**. If `POST /v4/records` times out you cannot tell a retry from a duplicate filing, and if you delete the duplicate it is gone permanently. Treat every write here as requiring a human decision, and treat a timeout as *unknown*, never as *failed*.

## Steps

1. **Get a token.** `oauth2.token` — `POST https://auth.accela.com/oauth2/token`, `Content-Type: application/x-www-form-urlencoded`, `x-accela-appid` header. The token is bound to an agency, an environment and a scope list. Request the `records` scope.
2. **Check the agency's platform version.** `v4.get.serverProperties` — `GET /v4/serverProperties`. Every operation declares a minimum Civic Platform version in its description; agencies upgrade on their own schedule, so an operation in the published contract may not exist at this agency.
3. **Learn the agency's own record types.** `v4.get.settings.records.types` — `GET /v4/settings/records/types`. Never hard-code a type string learned from another agency.
4. **Ask what this record type needs.** `v4.get.records.describe.create` — `GET /v4/records/describe/create`. This returns the required attributes, including agency-defined custom forms and custom tables. Skipping it is how you get `data_validation_error`.
5. **Create the record.** `v4.post.records` — `POST /v4/records`.
   - Record the request you sent before you send it, so a timeout can be reconciled by hand.
   - On success, keep the returned `id` (shaped `AGENCY-YYCAP-NNNNN-NNNXX`) and `customId`.
   - **Check the body even on HTTP 200.** Agency-authored EMSE scripts run after this transaction; an after-event script failure returns 200 with `code: emse_error`. The record was created and an agency script attached to it was not. Surface that to a human — it is an agency configuration problem, not something to retry.
   - On HTTP 500, a *before*-event EMSE script cancelled the transaction. The record was not created.
6. **Attach the address.** `v4.post.records.recordId.addresses` — `POST /v4/records/{recordId}/addresses`.
7. **Attach the applicant.** `v4.post.records.recordId.contacts` — `POST /v4/records/{recordId}/contacts`.
8. **Upload plans.** `v4.post.records.recordId.documents` — `POST /v4/records/{recordId}/documents`.
9. **Confirm.** `v4.get.records.ids` for the record, and `v4.get.records.recordId.workflowTasks` to see where it sits in the agency's review workflow.

## Recovery

There is no undo. `v4.delete.records.ids` removes the record permanently and no restore operation exists anywhere in the 417-operation contract. If a duplicate is filed, the correct action is to contact the agency, not to delete.
