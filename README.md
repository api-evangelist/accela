# Accela

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Accela is a San Ramon, California govtech company whose cloud Civic Platform runs permitting, planning,
licensing, code enforcement, inspections, asset management and citizen service requests for state and local
government agencies. This profile covers its public developer surface.

## What Accela publishes

- **Accela Construct API (V4)** — 417 operations across **fifteen Swagger 2.0 documents** served from
  `developer.accela.com/api/v4/*.json` and rendered through ReDoc on the developer portal. Base host
  `https://apis.accela.com`, every path prefixed `/v4`. Harvested verbatim into `openapi/_original/` and
  serialized to YAML in `openapi/`.
- **OAuth 2.0 authorization server** at `auth.accela.com` — authorization code, implicit and
  password-credential grants, with agency- and environment-bound tokens and a 32-scope permission registry
  that Accela declares inline in each operation's description (`scopes/`).
- **A dated changelog** — 63 release entries from May 2014 to August 2026, current release 4.6.5.4, which the
  live API host self-reports at `https://apis.accela.com/`.
- **A published sandbox** with credentials printed in the docs (`sandbox/`).
- **An llms.txt** at `https://www.accela.com/llms.txt` (marketing index, no API content).
- **CivicData.com**, Accela's free CKAN 2.9.9 open-data platform for agencies — live today, **end of life
  30 June 2026, removal after 31 December 2026**.
- **Compliance**: annual SSAE18 SOC 2 Type 2, HIPAA HITECH, PCI-DSS SAQ-D and CCPA audits.

## What it does not

- **No idempotency, no dry-run, no restore.** 168 mutating operations, 39 of them DELETEs, against a
  government system of record, with no replay protection and no undo. Only two reversal paths exist
  (`Void Payment`, `Void Record Part Transactions`) and neither states a window.
- **No event surface.** No webhooks, no AsyncAPI, no streaming — polling only.
- **No MCP server**, despite heavy AI marketing and an acquired AI agent suite.
- **No A2A agent card**, no `security.txt`, no vulnerability disclosure policy, no OAuth/OIDC discovery
  metadata on the authorization server, and no public status page.
- **No published pricing.** Sold to agencies through procurement.
- **Abandoned SDKs.** The developer portal's "SDKs and Samples" link goes to a GitHub org where all fifteen
  public repos are archived and none is an API client. The first-party Node client last shipped in 2019; the
  first-party .NET SDK, still titled "for Windows & Windows Phone", last shipped in **October 2014**.

## Two findings worth flagging to Accela

1. **`status.accela.com` is a stale CNAME.** It resolves to `status.springbrooksoftware.com` and serves the
   status page of Springbrook Software — a business Accela owned from 2015 and sold to Accel-KKR in 2020.
   Anyone monitoring the obvious status hostname is watching a divested company's incidents.
2. **Four of the fifteen published specs do not parse as strict JSON** as served: trailing commas in
   `api-auth.json`, `v4-documents.json` and `v4-reports.json`, an invalid escape in `v4-payments.json`, and
   `v4-citizens.json` is not valid UTF-8. Each repair is recorded in that file's
   `x-api-evangelist-provenance` block; the untouched originals are in `openapi/_original/`.
