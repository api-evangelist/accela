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

Accela is a San Ramon, California govtech company whose cloud Civic Platform runs permitting, planning, licensing, code enforcement, inspections, asset management and citizen service requests for state and local government agencies worldwide. Its public developer surface is the Accela Construct API (V4) — a 417-operation REST API served from apis.accela.com and documented as fifteen Swagger 2.0 documents on the Accela Developer Portal, covering records, inspections, contacts and professionals, addresses/parcels/owners, assets and assessments, documents, payments and shopping carts, reports, search, citizens, CivicID and platform settings. Access is OAuth 2.0 against auth.accela.com with agency- and environment-scoped tokens, and every request is bound to a specific government tenant through the x-accela-agency and x-accela-environment headers.

**Areas:** GovTech · Government · Permitting · Licensing · Code Enforcement · Inspection · Asset Management · Citizen Engagement · Land Management · Civic Platform · Public Sector · Software-as-a-Service

## Accela on APIs.io

Everything profiled for Accela is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/accela/](https://apis.io/providers/accela/)** — or go straight to one of the APIs or properties below.

### APIs (109)

- [CivicData Open Data API (CKAN) — END OF LIFE](https://apis.io/apis/accela/civicdata-open-data-api-ckan-end-of-life/) — CivicData.com is Accela's free open-data platform for government agencies, described on its own site as "a free open data platform built by Accela" and…
- [Accela AA Version API](https://apis.io/apis/accela/accela-aa-version-api/) — This is to return the version number of the AA server that is running, which allows the mobile app to make decisions as to what API's they have available.
- [Accela Addresses API](https://apis.io/apis/accela/accela-addresses-api/) — An address provides details about the physical location of a parcel, building, contact, and so forth. An address is part of a property's APO (address,…
- [Accela Agencies API](https://apis.io/apis/accela/accela-agencies-api/) — The Agencies API from Accela — 5 operation(s) for agencies.
- [Accela Announcements API](https://apis.io/apis/accela/accela-announcements-api/) — The **announcements** API endpoints allow apps to get agency and public announcements, and mark them as read announcements.
- [Accela App Settings API](https://apis.io/apis/accela/accela-app-settings-api/) — App settings are defined when a developer registers the app on [Accela Developer Portal](https://developer.accela.com). These settings include app name, ID,…
- [Accela Assessments API](https://apis.io/apis/accela/accela-assessments-api/) — In Civic Platform, an assessment is synonymous to an asset condition assessment. An asset condition assessment is a scheduled maintenance review and/or a…
- [Accela Assessments/Attributes API](https://apis.io/apis/accela/accela-assessments-attributes-api/) — An agency can define custom attributes for each type of assessment.
- [Accela Assessments/Documents API](https://apis.io/apis/accela/accela-assessments-documents-api/) — Inspectors can attach documents and photos as needed to the asset condition assessment record, and record the assignments and costs that occur on the…
- [Accela Assessments/Observations API](https://apis.io/apis/accela/accela-assessments-observations-api/) — During an assessment, an inspector may make observations about the condition of the asset. For example, he may go to a certain area to look at the condition…
- [Accela Assessments/Work Orders API](https://apis.io/apis/accela/accela-assessments-work-orders-api/) — Asset assessments often alert agencies to problems that need attention. A work order is the starting point in the repair process. Associating a work order…
- [Accela Assets API](https://apis.io/apis/accela/accela-assets-api/) — Assets can be any object that an agency owns or maintains. Assets have standard properties such as date of service, start value, current value, depreciation…
- [Accela Assets/Assessments API](https://apis.io/apis/accela/accela-assets-assessments-api/) — Condition assessments apply to assets that change or deteriorate over time. These assets may require a visual condition assessment to effectively manage…
- [Accela Assets/Attributes API](https://apis.io/apis/accela/accela-assets-attributes-api/) — In addition to these asset properties, assets can also have custom attributes which are customized characteristics of assets, structures, and…
- [Accela Assets/Documents API](https://apis.io/apis/accela/accela-assets-documents-api/) — Document collaterals can be attached to assets.
- [Accela Assets/Records API](https://apis.io/apis/accela/accela-assets-records-api/) — Assets can be associated to transactional records when an asset assessment necessitates a service work order or if an application pertains to an agency asset.
- [Accela Batch API](https://apis.io/apis/accela/accela-batch-api/) — API for batch API requests.
- [Accela Citizen Access Delegate Invitations API](https://apis.io/apis/accela/accela-citizen-access-delegate-invitations-api/) — A citizen user designates a delegate by first sending them an invitation. The invited citizen users can accept or reject invitations. When the invited…
- [Accela Citizen Access Delegate Management API](https://apis.io/apis/accela/accela-citizen-access-delegate-management-api/) — description here
- [Accela Citizen Access Self-Registration API](https://apis.io/apis/accela/accela-citizen-access-self-registration-api/) — The **citizenaccess** API endpoints allow a logged-in Citizen Access user to register and manage his or her own account profile, status, and contacts.
- [Accela Citizen Access User Management API](https://apis.io/apis/accela/accela-citizen-access-user-management-api/) — description here
- [Accela Civic ID API](https://apis.io/apis/accela/accela-civicid-api/) — The CivicId API from Accela — 3 operation(s) for civicid.
- [Accela Conditions API](https://apis.io/apis/accela/accela-conditions-api/) — **Conditions** The system provides standard conditions for different record types(permits, licenses, inspections, and so forth). Depending on the condition,…
- [Accela Contacts/Addresses API](https://apis.io/apis/accela/accela-contacts-addresses-api/) — The Contacts/Addresses API from Accela — 2 operation(s) for contacts/addresses.
- [Accela Contacts API](https://apis.io/apis/accela/accela-contacts-api/) — A reference contact captures information about people or organizations involved in a business process. Contacts include licensed professionals, such as…
- [Accela Contacts/Conditions API](https://apis.io/apis/accela/accela-contacts-conditions-api/) — The Contacts/Conditions API from Accela — 2 operation(s) for contacts/conditions.
- [Accela Contacts/Custom Forms API](https://apis.io/apis/accela/accela-contacts-custom-forms-api/) — The Contacts/Custom Forms API from Accela — 3 operation(s) for contacts/custom forms.
- [Accela Contacts/Custom Tables API](https://apis.io/apis/accela/accela-contacts-custom-tables-api/) — The Contacts/Custom Tables API from Accela — 3 operation(s) for contacts/custom tables.
- [Accela Contacts/Records API](https://apis.io/apis/accela/accela-contacts-records-api/) — The Contacts/Records API from Accela — 1 operation(s) for contacts/records.
- [Accela Documents API](https://apis.io/apis/accela/accela-documents-api/) — The Documents API enables apps to upload and download documents, and attach a document to a record or inspection.
- [Accela Filters API](https://apis.io/apis/accela/accela-filters-api/) — Filters are user queries that are stored in Civic Platform and enable users to find information easily. Filters are configured in Civic Platform's Data…
- [Accela Geocoding API](https://apis.io/apis/accela/accela-geocoding-api/) — The Geocoding API provides geo-coded address information based on map services configured on [Construct Admin Portal](https://admin.accela.com) > Agencies >…
- [Accela Gis API](https://apis.io/apis/accela/accela-gis-api/) — The Gis API from Accela — 1 operation(s) for gis.
- [Accela Inspections API](https://apis.io/apis/accela/accela-inspections-api/) — The Inspections API from Accela — 15 operation(s) for inspections.
- [Accela Inspections/Checklists API](https://apis.io/apis/accela/accela-inspections-checklists-api/) — The Inspections/Checklists API from Accela — 2 operation(s) for inspections/checklists.
- [Accela Inspections/Checklists/Checklist Items API](https://apis.io/apis/accela/accela-inspections-checklists-checklist-items-api/) — The Inspections/Checklists/Checklist Items API from Accela — 6 operation(s) for inspections/checklists/checklist items.
- [Accela Inspections/Checklists/Checklist Items/Custom Forms API](https://apis.io/apis/accela/accela-inspections-checklists-checklist-items-custom-forms-api/) — The Inspections/Checklists/Checklist Items/Custom Forms API from Accela — 3 operation(s) for inspections/checklists/checklist items/custom forms.
- [Accela Inspections/Checklists/Checklist Items/Custom Tables API](https://apis.io/apis/accela/accela-inspections-checklists-checklist-items-custom-tables-api/) — The Inspections/Checklists/Checklist Items/Custom Tables API from Accela — 4 operation(s) for inspections/checklists/checklist items/custom tables.
- [Accela Inspections/Condition Approvals API](https://apis.io/apis/accela/accela-inspections-condition-approvals-api/) — The Inspections/Condition Approvals API from Accela — 3 operation(s) for inspections/condition approvals.
- [Accela Inspections/Conditions API](https://apis.io/apis/accela/accela-inspections-conditions-api/) — The Inspections/Conditions API from Accela — 4 operation(s) for inspections/conditions.
- [Accela Inspections/Documents API](https://apis.io/apis/accela/accela-inspections-documents-api/) — The Inspections/Documents API from Accela — 2 operation(s) for inspections/documents.
- [Accela Inspections/Time Accounting API](https://apis.io/apis/accela/accela-inspections-time-accounting-api/) — The Inspections/Time Accounting API from Accela — 3 operation(s) for inspections/time accounting.
- [Accela Inspectors API](https://apis.io/apis/accela/accela-inspectors-api/) — The Inspectors API from Accela — 2 operation(s) for inspectors.
- [Accela Invoices API](https://apis.io/apis/accela/accela-invoices-api/) — An invoice fee can either be generated manually in the Civic Platform's Payment Processing portlet or automatically if configured in Civic Platform…
- [Accela Mileage API](https://apis.io/apis/accela/accela-mileage-api/) — API for tracking vehicle mileage associated with inspections.
- [Accela Owners API](https://apis.io/apis/accela/accela-owners-api/) — An owner defines an individual or entity related to a parcel so that the owner becomes the responsible party and point of contact for the parcel. The parcel…
- [Accela Parcels API](https://apis.io/apis/accela/accela-parcels-api/) — A parcel defines a piece of land with a specific location and legally defined boundaries. The county assessor's office typically maintains information about…
- [Accela Payments API](https://apis.io/apis/accela/accela-payments-api/) — Payments represent the acceptance of monetary funds submitted to the agency in relation to a transactional record. The system uses payments to invoice for…
- [Accela Professionals API](https://apis.io/apis/accela/accela-professionals-api/) — A professional is a contractor, architect, engineer, developer, or associated organization. The system requires that all professionals be licensed. Similar…
- [Accela Professionals/Conditions API](https://apis.io/apis/accela/accela-professionals-conditions-api/) — The Professionals/Conditions API from Accela — 1 operation(s) for professionals/conditions.
- [Accela Professionals/Records API](https://apis.io/apis/accela/accela-professionals-records-api/) — The Professionals/Records API from Accela — 1 operation(s) for professionals/records.
- [Accela Records/Activities API](https://apis.io/apis/accela/accela-records-activities-api/) — Activities related to a record can be assigned to a staff member when the activities require further action, such as a follow-up inspection or service…
- [Accela Records/Addresses API](https://apis.io/apis/accela/accela-records-addresses-api/) — A record can have at least one associated address, such as the address of the application contact or the location of a permit application, service request,…
- [Accela Records/Addresses/Custom Forms API](https://apis.io/apis/accela/accela-records-addresses-custom-forms-api/) — The Records/Addresses/Custom Forms API from Accela — 2 operation(s) for records/addresses/custom forms.
- [Accela Records API](https://apis.io/apis/accela/accela-records-api/) — A record is a fundamental Civic Platform object that captures an agency's daily process tranactions, such as applications, permits, cases, licenses, service…
- [Accela Records/Assets API](https://apis.io/apis/accela/accela-records-assets-api/) — A work order record is linked to assets that require inspection, repair service, or any kind of task that needs to be performed and tracked in the system.
- [Accela Records/Comments API](https://apis.io/apis/accela/accela-records-comments-api/) — A staff user can add comments regarding the record, or can choose from standard comments that have been configured for the agency.
- [Accela Records/Condition Approvals API](https://apis.io/apis/accela/accela-records-condition-approvals-api/) — The Records/Condition Approvals API from Accela — 3 operation(s) for records/condition approvals.
- [Accela Records/Conditions API](https://apis.io/apis/accela/accela-records-conditions-api/) — A condition is a requirement that you can apply to an application (or component of an application), that the application must fulfill to qualify for…
- [Accela Records/Contacts API](https://apis.io/apis/accela/accela-records-contacts-api/) — One or more reference contacts can be associated to an application or service request.
- [Accela Records/Contacts/Custom Forms API](https://apis.io/apis/accela/accela-records-contacts-custom-forms-api/) — The Records/Contacts/Custom Forms API from Accela — 3 operation(s) for records/contacts/custom forms.
- [Accela Records/Contacts/Custom Tables API](https://apis.io/apis/accela/accela-records-contacts-custom-tables-api/) — The Records/Contacts/Custom Tables API from Accela — 3 operation(s) for records/contacts/custom tables.
- [Accela Records/Costs API](https://apis.io/apis/accela/accela-records-costs-api/) — The Records/Costs API from Accela — 2 operation(s) for records/costs.
- [Accela Records/Custom Forms API](https://apis.io/apis/accela/accela-records-custom-forms-api/) — The Records/Custom Forms API from Accela — 3 operation(s) for records/custom forms.
- [Accela Records/Custom Tables API](https://apis.io/apis/accela/accela-records-custom-tables-api/) — The Records/Custom Tables API from Accela — 4 operation(s) for records/custom tables.
- [Accela Records/Documents API](https://apis.io/apis/accela/accela-records-documents-api/) — The Records/Documents API from Accela — 3 operation(s) for records/documents.
- [Accela Records/Fees API](https://apis.io/apis/accela/accela-records-fees-api/) — The Records/Fees API from Accela — 2 operation(s) for records/fees.
- [Accela Records/Inspections API](https://apis.io/apis/accela/accela-records-inspections-api/) — The Records/Inspections API from Accela — 2 operation(s) for records/inspections.
- [Accela Records/Invoices API](https://apis.io/apis/accela/accela-records-invoices-api/) — The Records/Invoices API from Accela — 1 operation(s) for records/invoices.
- [Accela Records/Owners API](https://apis.io/apis/accela/accela-records-owners-api/) — The Records/Owners API from Accela — 3 operation(s) for records/owners.
- [Accela Records/Parcels API](https://apis.io/apis/accela/accela-records-parcels-api/) — The Records/Parcels API from Accela — 3 operation(s) for records/parcels.
- [Accela Records/Part Transactions API](https://apis.io/apis/accela/accela-records-part-transactions-api/) — The Records/Part Transactions API from Accela — 2 operation(s) for records/part transactions.
- [Accela Records/Payments API](https://apis.io/apis/accela/accela-records-payments-api/) — The Records/Payments API from Accela — 2 operation(s) for records/payments.
- [Accela Records/Professionals API](https://apis.io/apis/accela/accela-records-professionals-api/) — The Records/Professionals API from Accela — 3 operation(s) for records/professionals.
- [Accela Records/Trust Accounts API](https://apis.io/apis/accela/accela-records-trust-accounts-api/) — The Records/Trust Accounts API from Accela — 1 operation(s) for records/trust accounts.
- [Accela Records/Votes API](https://apis.io/apis/accela/accela-records-votes-api/) — The Records/Votes API from Accela — 2 operation(s) for records/votes.
- [Accela Records/Workflows API](https://apis.io/apis/accela/accela-records-workflows-api/) — The Records/Workflows API from Accela — 7 operation(s) for records/workflows.
- [Accela Reports API](https://apis.io/apis/accela/accela-reports-api/) — Civic Platform provides a set of standard reports, developed with reporting tools such as Crystal Reports, Microsoft Reporting Services. The Reports API…
- [Accela Search API](https://apis.io/apis/accela/accela-search-api/) — The Search API from Accela — 13 operation(s) for search.
- [Accela Settings/Activities API](https://apis.io/apis/accela/accela-settings-activities-api/) — The Settings/Activities API from Accela — 3 operation(s) for settings/activities.
- [Accela Settings/Addresses API](https://apis.io/apis/accela/accela-settings-addresses-api/) — The Settings/Addresses API from Accela — 7 operation(s) for settings/addresses.
- [Accela Settings/Assessments API](https://apis.io/apis/accela/accela-settings-assessments-api/) — The Settings/Assessments API from Accela — 1 operation(s) for settings/assessments.
- [Accela Settings/Asset Types API](https://apis.io/apis/accela/accela-settings-asset-types-api/) — The Settings/Asset Types API from Accela — 5 operation(s) for settings/asset types.
- [Accela Settings/Assets API](https://apis.io/apis/accela/accela-settings-assets-api/) — The Settings/Assets API from Accela — 3 operation(s) for settings/assets.
- [Accela Settings/Comments API](https://apis.io/apis/accela/accela-settings-comments-api/) — The Settings/Comments API from Accela — 2 operation(s) for settings/comments.
- [Accela Settings/Conditions API](https://apis.io/apis/accela/accela-settings-conditions-api/) — The Settings/Conditions API from Accela — 4 operation(s) for settings/conditions.
- [Accela Settings/Contacts API](https://apis.io/apis/accela/accela-settings-contacts-api/) — The Settings/Contacts API from Accela — 7 operation(s) for settings/contacts.
- [Accela Settings/Costs API](https://apis.io/apis/accela/accela-settings-costs-api/) — The Settings/Costs API from Accela — 6 operation(s) for settings/costs.
- [Accela Settings/Departments API](https://apis.io/apis/accela/accela-settings-departments-api/) — The Settings/Departments API from Accela — 2 operation(s) for settings/departments.
- [Accela Settings/Documents API](https://apis.io/apis/accela/accela-settings-documents-api/) — The Settings/Documents API from Accela — 6 operation(s) for settings/documents.
- [Accela Settings/Drilldowns API](https://apis.io/apis/accela/accela-settings-drilldowns-api/) — The Settings/Drilldowns API from Accela — 1 operation(s) for settings/drilldowns.
- [Accela Settings/Inspections API](https://apis.io/apis/accela/accela-settings-inspections-api/) — The Settings/Inspections API from Accela — 12 operation(s) for settings/inspections.
- [Accela Settings/Modules API](https://apis.io/apis/accela/accela-settings-modules-api/) — The Settings/Modules API from Accela — 1 operation(s) for settings/modules.
- [Accela Settings/Owners API](https://apis.io/apis/accela/accela-settings-owners-api/) — The Settings/Owners API from Accela — 1 operation(s) for settings/owners.
- [Accela Settings/Parcels API](https://apis.io/apis/accela/accela-settings-parcels-api/) — The Settings/Parcels API from Accela — 1 operation(s) for settings/parcels.
- [Accela Settings/Parts API](https://apis.io/apis/accela/accela-settings-parts-api/) — The Settings/Parts API from Accela — 2 operation(s) for settings/parts.
- [Accela Settings/Pick Lists API](https://apis.io/apis/accela/accela-settings-pick-lists-api/) — The Settings/Pick Lists API from Accela — 2 operation(s) for settings/pick lists.
- [Accela Settings/Priorities API](https://apis.io/apis/accela/accela-settings-priorities-api/) — The Settings/Priorities API from Accela — 1 operation(s) for settings/priorities.
- [Accela Settings/Professsionals API](https://apis.io/apis/accela/accela-settings-professsionals-api/) — The Settings/Professsionals API from Accela — 3 operation(s) for settings/professsionals.
- [Accela Settings/Records API](https://apis.io/apis/accela/accela-settings-records-api/) — The Settings/Records API from Accela — 8 operation(s) for settings/records.
- [Accela Settings/Reports API](https://apis.io/apis/accela/accela-settings-reports-api/) — The Settings/Reports API from Accela — 3 operation(s) for settings/reports.
- [Accela Settings/Time Accounting API](https://apis.io/apis/accela/accela-settings-time-accounting-api/) — The Settings/Time Accounting API from Accela — 2 operation(s) for settings/time accounting.
- [Accela Shopping Carts API](https://apis.io/apis/accela/accela-shopping-carts-api/) — Shopping carts allow public users to add and manage multiple record payment transactions.A shopping cart contains attributes indicating the payment…
- [Accela Time Accounting API](https://apis.io/apis/accela/accela-time-accounting-api/) — For general time accounting, Civic Platform provides the ability for employees to record the amount of time spent in performing their daily tasks, the…
- [Accela Trust Accounts API](https://apis.io/apis/accela/accela-trust-accounts-api/) — Agency customers can deposit money into a trust account that the customer can drawn from when they need to pay fees for an application. This is helpful for…
- [Accela Users API](https://apis.io/apis/accela/accela-users-api/) — **Agency Users** Although "users" is a broad and general term, the Accela API's User object (user API resource) represents the agency user. An agency user…
- [Accela Workflows API](https://apis.io/apis/accela/accela-workflows-api/) — **Workflow Tasks** A workflow is a sequence of tasks that agency users follow to process a record. When a user submits a new application, the system creates…
- [Accela Oauth2 API](https://apis.io/apis/accela/accela-oauth2-api/) — The Oauth2 API from Accela — 3 operation(s) for oauth2.
- [Accela Document Review API](https://apis.io/apis/accela/accela-document-review-api/) — The Document Review API supports integration of the Civic Platform's Electronic Document Review ("EDR") feature with third-party document review tools.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [accela-mcp.yml](https://apis.io/servers/accela/accela-mcp-yml/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Accela Records Overlay](https://apis.io/overlays/accela/accela-records-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Accela Authentication](https://apis.io/security/accela/accela-authentication/)
- [Accela Domain Security](https://apis.io/security/accela/accela-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Accela Scopes](https://apis.io/scopes/accela/accela-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Accela Plans Pricing](https://apis.io/plans/accela/accela-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Accela Rate Limits](https://apis.io/rate-limits/accela/accela-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.accela.com/)
- [Documentation](https://developer.accela.com/docs/)
- [Getting started](https://developer.accela.com/docs/construct-gettingStarted.html)
- [API reference](https://developer.accela.com/docs/api_reference/api-index.html)
- [Sign up](https://developer.accela.com/Register/Register)
- [Support](https://www.accela.com/services/technical-support/)
- [Changelog](https://developer.accela.com/docs/construct_api_v4_rel_notes.html)
- [Blog](https://www.accela.com/blog/)
- [Compliance](https://www.accela.com/civic-platform/security/)
- [Terms of service](https://www.accela.com/terms-of-use/)
- [Privacy policy](https://www.accela.com/privacy-policy/)
- [GitHub](https://github.com/Accela-Inc)

## API Evangelist rating

**Kin Score 51.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 45.0 |
| Contract governance | 18.2 |
| Operational transparency | 18.4 |
| Developer ergonomics | 73.2 |
| Access clarity | 42.1 |

**Agent readiness 39.9** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 47.1** — Government & Public Sector

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/accela/](https://apis.io/providers/accela/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Accela: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/accela/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
