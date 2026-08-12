# L2 Microsoft 365 & SharePoint Developer / Support Engineer

## 400 Interview Questions & Answers

> **Coverage:** SharePoint Online | Microsoft 365 Apps | Excel | Word | PowerPoint | Outlook | Teams
>
> **Format:** Easy ✦ Intermediate ✦ Tough | Troubleshooting & Root Cause Analysis (RCA)

---

## Document Overview

| Item | Details |
|---|---|
| Total Questions | 400 |
| Difficulty | Easy + Tough |
| Sections | 7 |
| Format | RCA / Q&A |
| SharePoint / Microsoft 365 | 120 questions |
| Excel / Word / PowerPoint | 150 questions |
| Outlook | 70 questions |
| Teams | 60 questions |

---

## Table of Contents

| # | Section | Questions | Pages |
|---:|---|---|---:|
| 1 | SharePoint Online Developer (L2) | Q1–Q80 | 3–14 |
| 2 | M365 Administration & Development | Q81–Q120 | 14–20 |
| 3 | Excel Troubleshooting — RCA | Q121–Q180 | 20–30 |
| 4 | Word Troubleshooting — RCA | Q181–Q220 | 30–38 |
| 5 | PowerPoint Troubleshooting — RCA | Q221–Q270 | 38–47 |
| 6 | Outlook Troubleshooting — RCA | Q271–Q340 | 47–59 |
| 7 | Teams Troubleshooting — RCA | Q341–Q400 | 59–70 |

> **EASY** = Foundational / Common Interview Questions
>
> **TOUGH** = Advanced / RCA / Scenario-Based Questions

---

## Section 1 — SharePoint Online Developer (L2) — Q1 to Q80

### Q1. What is SharePoint Online and how does it differ from SharePoint On-Premises? [EASY]

**Answer:** SharePoint Online (SPO) is a cloud-based collaboration platform hosted by Microsoft as part of M365.

It differs from On-Premises in that infrastructure is managed by Microsoft, updates are automatic, it scales elastically, and uses modern authentication (Azure AD). On-Premises gives full server control but requires manual patching, hardware management, and custom CA.

### Q2. What is a SharePoint Site Collection? [EASY]

**Answer:** A Site Collection is a top-level grouping of sites that share common settings, permissions, content

types, and a single recycle bin. It has one root site and can contain multiple subsites. Each collection is isolated with its own administration.

### Q3. Explain the difference between Classic and Modern SharePoint experience. [EASY]

**Answer:** Classic uses server-side rendering with master pages and page layouts; it supports full-trust solutions.

Modern uses client-side rendering (React-based), SPFx web parts, responsive design, and is incompatible with server-side code.

### Q4. What are SharePoint Framework (SPFx) web parts? [EASY]

**Answer:** SPFx web parts are client-side components built using TypeScript/React that run in the browser. They

are deployed to the App Catalog and can be added to modern pages. They use Microsoft Graph and REST APIs for data access.

### Q5. What is the SharePoint App Catalog? [EASY]

**Answer:** The App Catalog is a special site collection where SharePoint add-ins and SPFx solutions are uploaded

for deployment. Apps can be tenant-wide or site-collection scoped.

### Q6. Explain SharePoint permissions levels. [EASY]

**Answer:** Permissions levels include: Full Control, Design, Edit, Contribute, Read, View Only. They can be

customized. Permission inheritance flows from site to list to item, and can be broken at any level.

### Q7. What is Content Type in SharePoint? [EASY]

**Answer:** A Content Type is a reusable collection of metadata (columns), workflows, and other settings for a

category of items. They enforce consistent structure across lists and libraries.

### Q8. What is PnP PowerShell and when do you use it? [EASY]

**Answer:** PnP PowerShell is an open-source module for managing SharePoint and M365 resources via

PowerShell. Used for bulk operations, provisioning, tenant administration, and automation scripts.

### Q9. What is Microsoft Graph API? [EASY]

**Answer:** Microsoft Graph is a unified REST API endpoint (graph.microsoft.com) for accessing M365 services

including SharePoint, Teams, Outlook, OneDrive, and Azure AD. It supports both delegated and application permissions.

### Q10. Explain SharePoint Search architecture. [EASY]

**Answer:** SharePoint Search uses a crawl component that indexes content, a query processing component that

handles search requests, an analytics component, and a search index. In SPO, it's managed by Microsoft.

### Q11. What are SharePoint Managed Metadata and Term Stores? [EASY]

**Answer:** Managed Metadata is a centrally managed set of terms organized in term sets within a Term Store. It

ensures consistent tagging across sites and supports hierarchical taxonomy.

### Q12. What is a SharePoint Hub Site? [EASY]

**Answer:** A Hub Site connects related SharePoint sites, allowing shared navigation, branding, and rollup of

news/activity. It promotes flat site architecture over deep subsites.

### Q13. Explain SharePoint REST API basics. [EASY]

**Answer:** SharePoint exposes a REST API at /_api/. Resources are addressed as URLs. Common endpoints:

/_api/web (site info), /_api/lists, /_api/lists/getbytitle('name')/items. Supports GET, POST, PATCH, DELETE operations with JSON payloads.

### Q14. What is the difference between SharePoint list and document library? [EASY]

**Answer:** A List stores structured data (rows/columns similar to a table). A Document Library stores files with

metadata columns. Libraries have additional features like version control, check-in/check-out, and file previews.

### Q15. What are SharePoint webhooks? [EASY]

**Answer:** Webhooks are HTTP callbacks that notify an external service when changes occur in a SharePoint list

or library. They replace remote event receivers for cloud-hosted apps and require a publicly accessible HTTPS endpoint.

### Q16. What is CSOM (Client-Side Object Model)? [EASY]

**Answer:** CSOM is a .NET/JavaScript/Silverlight API for interacting with SharePoint without server-side code. It

batches requests to the server. SharePoint's JavaScript CSOM (SP.js) is used in classic pages; modern apps prefer REST or Graph.

### Q17. Explain SharePoint Online throttling. [EASY]

**Answer:** SPO throttles requests when usage exceeds limits to protect service stability. HTTP 429 (Too Many

Requests) is returned. Best practice: implement exponential backoff using Retry-After header. PnP libraries handle this automatically.

### Q18. What is SharePoint Syntex? [EASY]

**Answer:** SharePoint Syntex is an AI-based service that uses machine teaching to automatically classify

documents and extract metadata using trained models (form processing, document understanding). It integrates with content types.

### Q19. What are Power Automate flows and how do they replace SharePoint Designer workflows?

[EASY]

**Answer:** Power Automate (formerly Flow) is Microsoft's workflow automation tool. It replaces SharePoint

Designer workflows (deprecated) and offers cloud connectors, approvals, and scheduled triggers with a no-code/low-code interface.

### Q20. What is a SharePoint site template? [EASY]

**Answer:** Site templates define the structure, features, and content of a site at creation. Modern templates

include Communication Site and Team Site. Custom templates can be created and applied via PnP provisioning.

### Q21. Explain SharePoint column validation. [EASY]

**Answer:** Column validation uses formulas to enforce data constraints. Example: =LEN([Title])>5 ensures Title

has more than 5 characters. Validation runs on item save and displays a custom error message on failure.

### Q22. What is the SharePoint Recycle Bin and its stages? [EASY]

**Answer:** Items deleted go to the user's first-stage Recycle Bin (93-day retention). Site collection admins can

restore from the second-stage Recycle Bin. After 93 days, items are permanently deleted.

### Q23. What are SharePoint Information Rights Management (IRM) policies? [EASY]

**Answer:** IRM policies encrypt documents at the library level, restricting download, print, and copy operations on

sensitive content. They integrate with Azure Information Protection / Microsoft Purview.

### Q24. Explain Content Query vs. Content Search Web Part. [EASY]

**Answer:** CQWP (classic) queries within a site collection using SharePoint object model — no crawl needed.

CSWP queries the search index across site collections — requires content to be crawled. CSWP is faster and more scalable.

### Q25. What is SharePoint Online Data Loss Prevention (DLP)? [EASY]

**Answer:** DLP policies in Microsoft Purview detect and protect sensitive information (e.g., credit card numbers,

SSNs) in SharePoint/OneDrive. They can block sharing or notify users when sensitive content is found.

### Q26. Explain SPFx extension types. [TOUGH]

**Answer:** SPFx Extensions include: Application Customizers (add custom scripts/elements to header/footer),

Field Customizers (customize field rendering in list views), Command Sets (add buttons to list view command bar).

### Q27. How do you deploy an SPFx solution tenant-wide? [TOUGH]

**Answer:** In the App Catalog upload the .sppkg file, check 'Make this solution available to all sites' during

deployment. For Application Customizers, you still need to add the extension to sites via PowerShell or API.

### Q28. Explain SharePoint Framework property pane types. [TOUGH]

**Answer:** Property pane types: PropertyPaneTextField, PropertyPaneCheckbox, PropertyPaneDropdown,

PropertyPaneSlider, PropertyPaneToggle, PropertyPaneLink, PropertyPaneChoiceGroup. Defined in getPropertyPaneConfiguration().

### Q29. What is the difference between isolated and non-isolated SPFx web parts? [TOUGH]

**Answer:** Non-isolated web parts share the same page DOM and JavaScript context. Isolated web parts (using

domain isolation) run in a separate iframe with dedicated Azure AD app registration, providing security isolation for sensitive operations.

### Q30. How do you implement Microsoft Graph API calls in SPFx? [TOUGH]

**Answer:** Use MSGraphClient or MSGraphClientV3 from @microsoft/sp-http. Request permissions in the

package-solution.json webApiPermissionRequests. Admin approves in SharePoint Admin Center → Advanced → API access.

### Q31. Explain SharePoint Patterns and Practices (PnP) provisioning framework. [TOUGH]

**Answer:** PnP Provisioning uses XML templates (PnP schema) to define and deploy SharePoint artifacts (lists,

content types, pages, navigation). Apply-PnPProvisioningTemplate command deploys templates idempotently.

### Q32. What is Azure AD App-Only authentication for SharePoint? [TOUGH]

**Answer:** App-Only uses a certificate or client secret to authenticate without a user context. Used in background

services/daemons. Requires FullControl or Sites.Selected permissions granted in Azure AD and approved by global admin.

### Q33. How does SharePoint list indexing affect performance? [TOUGH]

**Answer:** Large lists (>5,000 items) hit the list view threshold. Indexed columns allow efficient filtering/sorting.

Create indexes on frequently filtered columns (e.g., Status, Created). Use filtered views with indexed columns to avoid threshold errors.

### Q34. Explain SharePoint Online External Sharing policies. [TOUGH]

**Answer:** External sharing controlled at tenant and site level. Levels: Anyone (anonymous links), New and

existing guests (Azure AD B2B), Existing guests only, Only people in your org. Guest access requires Azure AD B2B collaboration.

### Q35. What is SharePoint Tenant Administration via PowerShell? [TOUGH]

**Answer:** Using PnP.PowerShell or SPO Management Shell. Key cmdlets: Connect-SPOService,

Set-SPOTenant, Set-SPOSite, Get-SPOSite, Set-SPOUser, Revoke-SPOUserSession. Used for bulk configuration and automation.

### Q36. Explain SharePoint storage limits and management. [TOUGH]

**Answer:** Tenant pool of 1TB + 10GB per licensed user. Each site has a quota (default 25TB). Monitor with

Get-SPOSite | Select Url,StorageUsageCurrent,StorageQuota. Manage storage with Set-SPOSite -StorageQuota.

### Q37. What is the SharePoint Migration Tool (SPMT)? [TOUGH]

**Answer:** SPMT migrates content from file shares and on-premises SharePoint to SPO. Supports incremental

migration, JSON/CSV task files, and migration reports. Requires network access to both source and destination.

### Q38. How do you implement Custom Connectors for SharePoint in Power Platform? [TOUGH]

**Answer:** Custom Connectors define REST API interfaces using OpenAPI (Swagger) spec. Used in Power

Apps/Automate to call custom APIs or SharePoint REST endpoints not covered by standard connectors.

### Q39. Explain SharePoint column/site script and site design. [TOUGH]

**Answer:** Site Scripts are JSON-based instructions that create SharePoint artifacts (lists, columns, navigation).

Site Designs package one or more site scripts and are applied at site creation or via the API. Managed with PnP or SPO admin cmdlets.

### Q40. What are SharePoint Syntex document understanding models? [TOUGH]

**Answer:** Document Understanding uses AI Builder trained models to classify documents and extract key-value

pairs. Models are trained with positive/negative examples and applied to libraries for automatic metadata extraction and content type assignment.

### Q41. Explain SharePoint Online service health monitoring. [TOUGH]

**Answer:** Monitor via M365 Admin Center → Service Health. Use PowerShell: Get-SPOServiceInfo. Set up

email/webhook alerts. Check Microsoft 365 Service Health API via Graph for programmatic monitoring.

### Q42. What is Cross-Site Scripting (XSS) prevention in SharePoint SPFx? [TOUGH]

**Answer:** SPFx uses Content Security Policy (CSP) headers. Avoid innerHTML; use DOMParser or React's JSX

instead. Sanitize user input. Microsoft's trust fabric restricts script execution to approved domains.

### Q43. Explain the SharePoint People Search and expertise location. [TOUGH]

**Answer:** People Search indexes user profiles from Azure AD. Expertise, skills, and org chart data come from the

User Profile Service / Delve. Configure relevance using search schema, query rules, and result sources.

### Q44. How do you troubleshoot SharePoint search not returning results? [TOUGH]

**Answer:** Check: crawl status in admin center, search schema mappings, content source configuration, query

rules, result source scopes. Run Test-SPSite or use the Search Diagnostics page. Ensure content is crawled and indexed.

### Q45. What is Viva Connections and how does it use SharePoint? [TOUGH]

**Answer:** Viva Connections is a Teams app that surfaces a company intranet (SharePoint Communication Site)

inside Teams. It uses SharePoint's Home site, global navigation, and Dashboard (Adaptive Cards-based) for a personalized employee experience.

### Q46. Explain SharePoint audit logging and compliance. [TOUGH]

**Answer:** SharePoint audit logs track user activities (view, edit, share, delete). Configured via Microsoft Purview

Audit (unified audit log). Use Search-UnifiedAuditLog or the compliance portal. Retention up to 10 years with E5/add-on.

### Q47. What are SharePoint Retention Policies and Labels? [TOUGH]

**Answer:** Retention Policies apply auto-retention/deletion rules to SharePoint sites/OneDrive. Retention Labels

can be manually or auto-applied to items. They can trigger disposition review or auto-delete after specified periods.

### Q48. Explain SharePoint Framework Adaptive Card Extensions (ACE). [TOUGH]

**Answer:** ACEs are SPFx components that render Adaptive Cards in the Viva Connections Dashboard. Types:

BasicCard, ImageCard, PrimaryText. Defined in manifest with cardSize (Medium/Large). Support quick view and card view.

### Q49. How do you implement row-level security in SharePoint lists? [TOUGH]

**Answer:** Use item-level permissions (break inheritance per item) or audience targeting. For sensitive data, use

custom SPFx solutions with server-side filtering via Azure Function + Graph API using app-only permissions to filter data before returning to client.

### Q50. Explain SharePoint migration assessment and remediation. [TOUGH]

**Answer:** Use SPMT Assessment or SharePoint Migration Assessment Tool (SMAT) to scan source

environments for incompatibilities (InfoPath forms, classic workflows, large file sizes, special characters, path lengths >400 chars). Remediate before migration.

### Q51. A SharePoint document library shows 'Access Denied' to a user who has Edit permissions on

the parent site. What is the RCA? [TOUGH]

**Answer:** Root Cause: Item-level or library-level permission inheritance was broken and the user was not added

to the library's unique permission set. Resolution: Check library → Library Settings → Permissions → verify unique permissions. Re-add user or restore inheritance.

### Q52. Users report that SharePoint search returns no results for documents uploaded in the last 24

hours. RCA? [TOUGH]

**Answer:** Root Cause: Search indexing delay or crawl failure. Continuous crawl should run every 15 min; a stuck

crawl component causes lag. Resolution: Check admin center search diagnostics, reset crawl if stuck. Verify crawl log for errors.

### Q53. An SPFx web part works locally (gulp serve) but fails in production with a 401 error on Graph

API calls. RCA? [TOUGH]

**Answer:** Root Cause: Web API permissions not approved. In production, Graph permission requests defined in

package-solution.json must be approved by a Global Admin in SharePoint Admin Center → API access page. Local gulp serve uses mock auth.

### Q54. Power Automate flow on SharePoint list trigger stops running after 30 days. RCA? [TOUGH]

**Answer:** Root Cause: SharePoint webhooks (used by Power Automate) have a maximum subscription period of

6 months but flows pause if the connection owner's credentials expire or the owner loses access. Resolution: Renew connection, check owner permissions, consider a service account.

### Q55. SharePoint site collection storage shows 0 bytes used but the site has thousands of

documents. RCA? [TOUGH]

**Answer:** Root Cause: Storage metric cache refresh delay or a misconfigured storage quota showing incorrect

values. Also possible: documents exist only in Recycle Bin. Resolution: Run Update-SPOSite to force recalculation; empty Recycle Bin if needed.

### Q56. External users cannot access shared SharePoint files despite receiving invitation emails. RCA?

[TOUGH]

**Answer:** Root Cause: (a) External sharing disabled at tenant or site level, (b) B2B invitation not redeemed, (c)

Conditional Access policy blocking external users, (d) SPO external sharing limited to specific domains.

**Resolution:** Check tenant sharing settings, CA policies, and domain allowlists.

### Q57. A SharePoint list with 6,000 items throws 'List View Threshold exceeded' error. RCA? [TOUGH]

**Answer:** Root Cause: SPO enforces a 5,000-item threshold per view query. Non-indexed columns used in filters

cause full table scan. Resolution: Create an index on the filtered column, use filtered views based on indexed columns, or implement pagination.

### Q58. SPFx solution deployed to App Catalog is not visible on site pages. RCA? [TOUGH]

**Answer:** Root Cause: (a) App not installed on the site collection, (b) Missing site-scoped feature activation, (c)

Solution deployed with skipFeatureDeployment=false but not added to site. Resolution: Go to Site Contents → Add an App, install the app on the site.

### Q59. SharePoint Online site collection creation fails with 'URL already exists' even though the site

was deleted. RCA? [TOUGH]

**Answer:** Root Cause: Deleted sites go to the Deleted Sites pool and retain the URL for 93 days (or until

permanently deleted). Resolution: Use Remove-SPODeletedSite -Identity to permanently delete, then recreate.

### Q60. Users report that co-authoring in SharePoint breaks and a file shows 'Locked for editing'. RCA?

[TOUGH]

**Answer:** Root Cause: (a) User has the file checked out exclusively, (b) Legacy file lock from a crashed Office

session, (c) OneDrive sync client conflict. Resolution: Discard check-out via Library Settings, use Manage Checked Out Files, or use the SharePoint REST API to force check-in.

### Q61. What are SharePoint Communication Sites vs Team Sites? [EASY]

**Answer:** Communication Sites are for broad one-to-many publishing (announcements, news). Team Sites are

for collaboration among a group, linked to an M365 Group with shared mailbox, calendar, and Teams. Communication Sites have no M365 Group.

### Q62. How do you enable versioning in SharePoint libraries? [EASY]

**Answer:** Go to Library Settings → Versioning Settings. Enable major and/or minor versions. Set limits. Major

versions are published; minor versions are drafts visible only to editors.

### Q63. What is the SharePoint REST endpoint to get all list items? [EASY]

**Answer:** GET /_api/web/lists/getbytitle('ListName')/items with headers: Accept: application/json;odata=verbose

or odata=nometadata. Use $top, $skip for pagination and $filter, $select, $orderby for query options.

### Q64. What is the difference between SharePoint Groups and Azure AD Groups? [EASY]

**Answer:** SharePoint Groups are local to the site collection and manage site access. Azure AD Groups

(Security/M365) are tenant-wide and can be added to SharePoint groups. Azure AD groups support dynamic membership and conditional access.

### Q65. Explain SharePoint Online sensitivity labels. [EASY]

**Answer:** Sensitivity Labels (from Microsoft Purview) classify SharePoint sites by sensitivity (Public, Internal,

Confidential). They control external sharing, guest access, unmanaged device access, and apply encryption to downloaded content.

### Q66. How do you create a SharePoint list using REST API? [TOUGH]

**Answer:** POST to /_api/web/lists with body: {__metadata:{type:'SP.List'}, Title:'MyList', BaseTemplate:100}.

Header: Content-Type: application/json;odata=verbose. Include X-RequestDigest for write operations.

### Q67. What is the difference between SharePoint Add-ins and SPFx? [EASY]

**Answer:** SharePoint Add-ins (legacy) run in isolated app domains using an iFrame. SPFx runs in the same page

context, supports modern UI, uses TypeScript/React, and is the recommended approach for modern SharePoint development.

### Q68. Explain SharePoint Online conditional access integration. [TOUGH]

**Answer:** Azure AD Conditional Access can restrict SharePoint access based on device compliance, IP location,

sign-in risk, and app protection policies. 'Unmanaged device' policies restrict download/print but allow browser-only access.

### Q69. How do you implement SharePoint approval workflows using Power Automate? [EASY]

**Answer:** Use Power Automate's Approval connector (Start and wait for an approval). Trigger: When an item is

created/modified. Send approval to designated approvers, then update the SharePoint item status field based on outcome.

### Q70. What is Site Collection App Catalog vs Tenant App Catalog? [TOUGH]

**Answer:** Tenant App Catalog deploys solutions globally across all sites. Site Collection App Catalog (must be

enabled per site) allows developers to deploy solutions scoped to that site collection only, without tenant-wide impact.

### Q71. Explain SharePoint Managed Properties and Crawled Properties. [TOUGH]

**Answer:** Crawled Properties are automatically discovered by the search crawler from document metadata and

SharePoint columns. Managed Properties are explicitly defined search schema properties mapped to crawled properties, used in queries and refiners.

### Q72. How do you handle large file migrations to SharePoint? [TOUGH]

**Answer:** Use SPMT, SharePoint Migration API, or Mover for large-scale migrations. Pre-assess: file path length

<400 chars, filename special chars, file size <250GB. Use incremental passes, schedule during off-peak hours, monitor migration reports.

### Q73. What is SharePoint Framework Yeoman generator? [EASY]

**Answer:** The SPFx Yeoman generator (yo @microsoft/sharepoint) scaffolds SPFx projects. It creates the project

structure, configuration files, TypeScript source, and gulp tasks needed to develop, test, and package SPFx solutions.

### Q74. Explain OneDrive for Business sync client troubleshooting. [TOUGH]

**Answer:** Check sync client version (should be current), review sync errors in system tray, check storage quota,

verify file/folder name restrictions, check Conditional Access/CA policy blocking sync, use OneDrive Reset (odopen://reset).

### Q75. What is the SharePoint Spaces (Immersive Experience)? [EASY]

**Answer:** SharePoint Spaces is a mixed-reality/3D canvas for building immersive experiences inside SharePoint.

Supports 360° images, 3D models, and 2D web parts in a spatial environment. Used for virtual tours, product showcases.

### Q76. How do you implement search-driven rollups on a SharePoint intranet? [TOUGH]

**Answer:** Use the Highlighted Content Web Part (modern) configured with a content query or use a custom SPFx

web part calling SharePoint Search REST API (/_api/search/query?querytext=...) with result source and managed property filters.

### Q77. Explain SharePoint governance best practices. [EASY]

**Answer:** Governance includes: site provisioning policies, naming conventions, external sharing controls, lifecycle

management (inactive site reviews), sensitivity labeling, audit logging, retention policies, hub site architecture, and change management documentation.

### Q78. What are Power Pages and how do they differ from SharePoint? [EASY]

**Answer:** Power Pages (formerly Power Apps Portals) are external-facing websites built on Dataverse.

SharePoint is for internal collaboration. Power Pages is for public/customer portals with forms, authentication, and Dataverse integration.

### Q79. How do you automate SharePoint site provisioning? [TOUGH]

**Answer:** Use PnP PowerShell with provisioning templates, SharePoint REST API, Microsoft Graph API (POST

/sites), or Power Automate with HTTP connectors. For enterprise, use Azure Logic Apps or Azure Functions triggered by a request.

### Q80. Explain SharePoint site lifecycle management. [TOUGH]

**Answer:** Lifecycle management covers: site creation approval, activity monitoring (Microsoft 365 admin reports),

inactive site notifications (Microsoft 365 site lifecycle policies), archival, and deletion. Use Microsoft Viva Insights or custom scripts for reporting.

---

## Section 2 — M365 Administration & Development — Q81 to Q120

### Q81. What is Microsoft 365 and its core services? [EASY]

**Answer:** M365 is a subscription suite including Exchange Online, SharePoint Online, Teams, OneDrive, Office

apps, Power Platform, Azure AD, Intune, Microsoft Purview, and Defender services.

### Q82. What is Azure Active Directory (Azure AD / Entra ID)? [EASY]

**Answer:** Azure AD is Microsoft's cloud-based identity and access management service. It provides

authentication, SSO, MFA, Conditional Access, and user/group management for M365 and Azure resources.

### Q83. Explain Microsoft 365 licensing models. [EASY]

**Answer:** Licensing tiers: F1 (Frontline), M365 Business Basic/Standard/Premium, M365 E3, M365 E5. Higher

tiers add security (Defender), compliance (Purview), analytics (Power BI Pro), and advanced Teams features.

### Q84. What is Microsoft Intune? [EASY]

**Answer:** Intune is Microsoft's cloud-based MDM/MAM solution. It manages device enrollment, configuration

profiles, compliance policies, and app deployment for Windows, macOS, iOS, and Android devices.

### Q85. Explain Multi-Factor Authentication (MFA) in M365. [EASY]

**Answer:** MFA requires a second factor beyond password: authenticator app (push/TOTP), phone call, SMS,

FIDO2 key. Enforced via Azure AD Conditional Access, Per-User MFA, or Security Defaults. Protects against credential theft.

### Q86. What is Microsoft Purview? [EASY]

**Answer:** Microsoft Purview (formerly Compliance/Information Protection) provides data governance, compliance

management, eDiscovery, audit, retention, DLP, sensitivity labels, insider risk management, and communication compliance.

### Q87. Explain Conditional Access policies in Azure AD. [EASY]

**Answer:** CA policies are if-then rules: IF (user, location, device, app, sign-in risk) THEN (allow, block, require

MFA, require compliant device). They replace legacy per-user MFA and provide granular access control.

### Q88. What is Microsoft Defender for Office 365? [EASY]

**Answer:** MDO protects against phishing, malware, and business email compromise via Safe Links, Safe

Attachments, Anti-phishing policies, Attack Simulation Training, and Threat Explorer. Plan 1 adds protection; Plan 2 adds investigation.

### Q89. Explain Exchange Online mail flow and connectors. [EASY]

**Answer:** Mail flows through Exchange Online Protection (EOP), then MDO. Inbound/outbound connectors

handle mail routing to/from on-premises servers or third-party services. Transport rules apply compliance actions.

### Q90. What is Power Platform? [EASY]

**Answer:** Power Platform = Power Apps (low-code apps) + Power Automate (workflow automation) + Power BI

(analytics) + Power Virtual Agents (chatbots) + Power Pages (external portals). Connects to M365, Azure, and 400+ connectors.

### Q91. How do you troubleshoot M365 sign-in failures? [EASY]

**Answer:** Check: Azure AD sign-in logs (Entra ID → Monitoring → Sign-in logs), error codes (AADSTS codes),

CA policy blocking, MFA failures, account lock, password expiry, token cache issues. Use the Sign-in diagnostic tool.

### Q92. Explain Microsoft 365 Groups. [EASY]

**Answer:** M365 Groups are a cross-service membership concept. Creating a group provisions: a shared mailbox,

calendar, SharePoint Team Site, Teams channel (optionally), Planner board, and OneNote notebook — all under a single membership.

### Q93. What is Microsoft Viva? [EASY]

**Answer:** Microsoft Viva is an Employee Experience Platform with modules: Viva Connections (intranet in

Teams), Viva Insights (wellbeing analytics), Viva Learning (LMS in Teams), Viva Topics (AI knowledge management), Viva Engage (Yammer).

### Q94. Explain Microsoft 365 backup and recovery options. [TOUGH]

**Answer:** Native: deleted items retention (30 days), Recycle Bin (93 days for SharePoint), Exchange deleted item

recovery (14-30 days). For comprehensive backup: Microsoft 365 Backup (native, GA 2024), or third-party tools (Veeam, Acronis, AvePoint).

### Q95. What is Microsoft Entra ID (formerly Azure AD) Privileged Identity Management (PIM)? [TOUGH]

**Answer:** PIM provides just-in-time privileged access. Admins activate roles (Global Admin, etc.) on-demand with

time limits, requiring MFA and justification. Reduces standing privileged access risk. Provides access reviews and audit trails.

### Q96. Explain Microsoft 365 eDiscovery workflow. [TOUGH]

**Answer:** eDiscovery: Create case in Purview compliance portal → Add custodians (users) → Place holds → Run

content searches → Export results. Use Advanced eDiscovery for review sets, conversation threading, and predictive coding.

### Q97. What is DMARC/DKIM/SPF and how do you configure them in M365? [TOUGH]

**Answer:** SPF (DNS TXT): authorizes sending IPs. DKIM: signs emails with private key, DNS publishes public

key — enable in EAC/Defender portal. DMARC (DNS TXT): policy for handling failed auth (none/quarantine/reject). Together they prevent spoofing.

### Q98. Explain M365 tenant-to-tenant migration scenarios. [TOUGH]

**Answer:** T2T migration needed for mergers/acquisitions. Tools: Microsoft's Cross-Tenant Migration (mailboxes,

SharePoint GA 2023), BitTitan MigrationWiz, Quest On Demand. Steps: domain verification, source/target prep, batch migration, cutover.

### Q99. What is Microsoft Graph PowerShell SDK? [TOUGH]

**Answer:** Microsoft Graph PowerShell SDK replaces older MSOL and AzureAD PowerShell modules. Uses

modern Graph API endpoints. Install: Install-Module Microsoft.Graph. Connect: Connect-MgGraph -Scopes. Fully supports all M365 workloads.

### Q100. How do you implement zero-trust security in M365? [TOUGH]

**Answer:** Zero Trust = Verify explicitly + Least privilege + Assume breach. M365 components: Azure AD CA

(verify identity), Intune (verify device), MDA/MDO (verify apps), Purview (protect data), Defender XDR (detect/respond to breaches).

### Q101. What is Microsoft Copilot for M365? [EASY]

**Answer:** Copilot for M365 is an AI assistant embedded in Word, Excel, PowerPoint, Outlook, Teams, and other

M365 apps. It uses large language models grounded on Microsoft Graph data (emails, meetings, files) to assist with content creation and analysis.

### Q102. Explain M365 audit log retention periods. [TOUGH]

**Answer:** Standard audit: 90 days (E1/Business). Microsoft Purview Audit (Premium): up to 1 year (E3) or 10

years (E5 or add-on). Configured per-user or per-workload. Critical logs: AzureActiveDirectory, Exchange, SharePoint, OneDrive.

### Q103. What is Microsoft Secure Score? [EASY]

**Answer:** Secure Score measures an organization's security posture in M365. It scores actions across Identity,

Devices, Apps, and Data. Higher score = better security hygiene. Recommendations are actionable with implementation guidance.

### Q104. Explain M365 message encryption (OME). [TOUGH]

**Answer:** Office Message Encryption wraps emails with RMS protection. Recipients without M365 get a one-time

passcode via email to view the message in a secure portal. Advanced OME adds custom branding and revocation capabilities.

### Q105. How do you manage M365 with PowerShell? [TOUGH]

**Answer:** Connect to workloads: Connect-MgGraph (Graph), Connect-ExchangeOnline, Connect-SPOService,

Connect-MicrosoftTeams. Use Graph PowerShell SDK as the modern replacement for deprecated MSOL/AzureAD modules. Automate with Azure Automation or runbooks.

### Q106. What are M365 service health incidents and how do you respond? [EASY]

**Answer:** Monitor M365 Admin Center → Service Health. Set up email alerts for incidents. During incident: check

impacted services, communicate to users, apply workarounds from Microsoft, track resolution. Post-incident: review PIR (Post-Incident Review) from Microsoft.

### Q107. Explain Microsoft 365 compliance score. [TOUGH]

**Answer:** Compliance Score (in Purview) measures adherence to regulatory frameworks (GDPR, ISO 27001,

NIST, HIPAA). It provides improvement actions, tracks progress, and maps controls to regulatory requirements. Automated checks reduce manual assessment work.

### Q108. What is Microsoft Teams Phone (formerly Cloud Voice)? [EASY]

**Answer:** Teams Phone enables PSTN calling from Teams via Microsoft Calling Plans (direct from Microsoft) or

Direct Routing (connecting existing PBX/SBC). Features: voicemail, call queues, auto attendants, call recording, and E911.

### Q109. How do you implement Microsoft 365 DLP across workloads? [TOUGH]

**Answer:** In Purview → Data Loss Prevention → Create policy. Choose workloads (Exchange, SharePoint,

OneDrive, Teams, Endpoint). Define sensitive info types or trainable classifiers, set conditions and actions (block, notify, require justification).

### Q110. Explain Microsoft 365 cross-tenant sharing configuration. [TOUGH]

**Answer:** Configure via Entra ID External Identities → Cross-tenant access settings. Control inbound/outbound

B2B collaboration and Direct Connect (Teams shared channels). Trust MFA from partner tenants. Configure in SharePoint Admin for guest access.

### Q111. What is Microsoft Syntex content assembly? [TOUGH]

**Answer:** Syntex content assembly auto-generates documents from templates by mapping template placeholders

to SharePoint list columns or Power Automate variables, creating personalized documents at scale (contracts, letters, reports).

### Q112. Explain Microsoft 365 network connectivity best practices. [TOUGH]

**Answer:** Follow Microsoft 365 network principles: optimize (direct HTTPS to M365 endpoints), allow (bypass

proxy/inspection for known M365 IPs), default (route rest through proxy). Avoid SSL inspection on M365 traffic. Use ExpressRoute for critical workloads.

### Q113. What is Microsoft Defender for Cloud Apps (MDCA)? [TOUGH]

**Answer:** MDCA is a Cloud Access Security Broker (CASB). It discovers shadow IT, enforces data protection

policies, detects anomalous behavior, and controls access to cloud apps. Integrates with Azure AD CA for session/access controls.

### Q114. Explain Microsoft 365 message tracing. [EASY]

**Answer:** Message trace in EAC or Exchange Online PowerShell (Get-MessageTrace) shows email delivery

status: delivery status, expanded distribution groups, connector routing. Useful for diagnosing non-delivery, spam filtering, or routing issues.

### Q115. What is Autopilot and how does it integrate with M365? [EASY]

**Answer:** Windows Autopilot automates device enrollment and configuration. Devices come pre-registered with

hardware hash. On first boot, Autopilot joins Azure AD, enrolls in Intune, and applies configuration profiles — zero-touch provisioning.

### Q116. How do you configure M365 guest access policies? [TOUGH]

**Answer:** Azure AD: External Identities → External collaboration settings (allow/restrict guest invitations). M365

Groups: Allow guest access. Teams: Enable guest access in Teams Admin. SharePoint: Set sharing levels. CA: Apply guest-specific policies.

### Q117. What is Microsoft 365 Archive? [TOUGH]

**Answer:** M365 Archive (GA 2024) provides extended inactive site storage at reduced cost. Sites are archived

and restored on-demand. Archived content is not deleted but access is restricted until restored (takes ~24 hours for large sites).

### Q118. Explain Microsoft Search in M365. [EASY]

**Answer:** Microsoft Search is the unified search experience across M365 (SharePoint, Bing for Work, Office

apps, Teams). Powered by Microsoft Graph. Configure via Microsoft Search Admin (search.microsoft.com): bookmarks, Q&A;, floor plans, locations.

### Q119. What are M365 communication compliance policies? [TOUGH]

**Answer:** Communication compliance monitors Teams/email communications for policy violations (harassment,

profanity, sensitive data leakage). Reviewers receive flagged items in the compliance portal. Integrates with HR systems for supervised user populations.

### Q120. How do you perform an M365 Business Impact Analysis for outages? [TOUGH]

**Answer:** Map critical business processes to M365 services. Assign RTOs/RPOs per service. Document manual

fallback procedures. Test BCP regularly. Use M365 SLAs (99.9% uptime) in planning. Monitor via Service Health API for real-time status.

---

## Section 3 — Excel Troubleshooting — RCA Format — Q121 to Q180

### Q121. Excel is not responding or freezes when opening a large file. RCA? [TOUGH]

**Answer:** Symptom: Excel hangs on open. Root Cause: Large file with many formulas, conditional formatting

rules, or embedded objects causing memory exhaustion. Steps: Open in Safe Mode (excel /safe), disable add-ins (File→Options→Add-ins→Manage COM add-ins), check for circular references. Resolution: Remove unused styles/formatting, use xlsb format, increase VM RAM if on VDI.

### Q122. Excel formulas are showing as text instead of calculating. RCA? [EASY]

**Answer:** Symptom: Formula text visible in cell, not result. Root Cause: (a) Cell format set to 'Text' before formula

entry, (b) Show Formulas mode enabled (Ctrl+`). Steps: Change cell format to General/Number, re-enter formula, or press Ctrl+` to toggle. Resolution: Format cells as General, press F2 then Enter to recalculate.

### Q123. VLOOKUP returns #N/A error despite matching values appearing to exist. RCA? [EASY]

**Answer:** Symptom: #N/A on VLOOKUP. Root Cause: (a) Lookup value has trailing spaces or line breaks, (b)

Data type mismatch (text vs. number), (c) Exact match vs. approximate match parameter error. Steps: Use TRIM() and CLEAN() on lookup values, check column data types, verify 4th argument (0 for exact match).

**Resolution:** =VLOOKUP(TRIM(A2),B:C,2,0).

### Q124. Excel conditional formatting is not applying correctly to all rows in a table. RCA? [EASY]

**Answer:** Symptom: Formatting applies to some rows but not others. Root Cause: Conflicting rules or incorrect

relative/absolute cell references in formula-based rules. Steps: Manage Rules → inspect rule order and 'Stop If True' flags, check formula uses relative row reference. Resolution: Correct formula references and remove conflicting rules; ensure 'Applies to' range is correct.

### Q125. Excel file corrupted error on open. RCA? [TOUGH]

**Answer:** Symptom: 'Excel cannot open the file because the file format or extension is not valid.' Root Cause: File

corruption from abrupt shutdown, disk error, or antivirus quarantine. Steps: Try Open and Repair (File→Open→dropdown→Open and Repair), copy to new location, open with LibreOffice, extract XML from xlsx zip. Resolution: Restore from SharePoint version history or backup.

### Q126. Excel PivotTable shows '(blank)' entries unexpectedly. RCA? [EASY]

**Answer:** Symptom: Blank entries in PivotTable rows/columns. Root Cause: Source data has empty cells in the

field being pivoted. Steps: Filter source data to find empty cells, fill blanks using Go To Special → Blanks → enter value. Resolution: Clean source data or use PivotTable option 'For empty cells show: 0'.

### Q127. Excel slow calculation even with a small workbook. RCA? [TOUGH]

**Answer:** Symptom: Calculation takes many seconds. Root Cause: (a) Volatile functions (NOW, RAND,

OFFSET, INDIRECT) recalculate on every change, (b) VLOOKUP scanning large arrays, (c) Array formulas over large ranges. Steps: Switch to Manual calculation, profile with F9, replace volatile functions with INDEX/MATCH or static values. Resolution: Optimize formulas; use XLOOKUP or INDEX/MATCH.

### Q128. Excel 'Too many different cell formats' error. RCA? [TOUGH]

**Answer:** Symptom: Cannot apply formatting; error 'Too many different cell formats'. Root Cause: XLS format

limit = 4,000 unique cell format combinations. Often caused by copy-pasting from external sources. Steps: Save as XLSX (limit = 64,000), use XLStylesTool to remove duplicate styles, Inquire add-in for style analysis.

**Resolution:** Save as XLSX and clean styles programmatically.

### Q129. Excel shared workbook not saving changes for one user. RCA? [TOUGH]

**Answer:** Symptom: Co-author's changes not saving. Root Cause: Legacy shared workbook (Review→Share

Workbook) conflict; simultaneous edits cause merge conflicts. Steps: Check Share Workbook settings, switch to co-authoring (SharePoint/OneDrive) instead of legacy sharing. Resolution: Migrate to OneDrive/SharePoint co-authoring, disable legacy shared workbook feature.

### Q130. SUMIF returning 0 despite matching criteria. RCA? [EASY]

**Answer:** Symptom: SUMIF gives 0. Root Cause: (a) Criteria range and sum range sizes differ, (b) Numbers

stored as text in sum range, (c) Criteria text case sensitivity issue (SUMIF is not case-sensitive, but encoding differs). Steps: Check ranges are same size, convert text-numbers using Value(), verify no hidden spaces.

**Resolution:** Use =SUMIF(A:A,D1,B:B) with properly formatted numeric data.

### Q131. Excel macro not running on other users' machines. RCA? [TOUGH]

**Answer:** Symptom: Macro runs on developer PC but not others. Root Cause: (a) Macro security setting blocks

unsigned macros, (b) Macro references local file path, (c) Missing references (Tools→References). Steps: Check Trust Center → Macro Settings, sign macro with digital certificate, fix absolute paths, verify references.

**Resolution:** Deploy trusted certificate, use relative paths or network UNC paths.

### Q132. Excel crashes when copying a chart to PowerPoint. RCA? [TOUGH]

**Answer:** Symptom: Excel/PPT crashes on paste. Root Cause: Graphics memory issue, corrupted chart, or

mismatched Office version between source and destination. Steps: Try Paste Special → Picture, update Office, check for conflicting printer drivers (set default printer to Microsoft Print to PDF). Resolution: Update Office to same build; use Paste Special or export as PNG.

### Q133. DATE formula returning serial number instead of date. RCA? [EASY]

**Answer:** Symptom: Formula shows number like 45123. Root Cause: Cell formatted as General or Number

instead of Date. Steps: Select cell, Format Cells (Ctrl+1), choose Date category, select desired format.

**Resolution:** Apply Date format to result cell.

### Q134. Excel XLOOKUP not available in the workbook. RCA? [EASY]

**Answer:** Symptom: #NAME? error on XLOOKUP. Root Cause: XLOOKUP requires Microsoft 365 subscription

or Office 2021+. Earlier Office versions (2016/2019) don't support it. Steps: Check File→Account→Product Information for version. Resolution: Upgrade to M365 Apps, or use INDEX/MATCH as a backward-compatible alternative.

### Q135. Power Query connection refresh fails with 'Data source error'. RCA? [TOUGH]

**Answer:** Symptom: Refresh fails in Power Query. Root Cause: (a) Source file moved/renamed, (b) Credentials

expired, (c) Network access to data source blocked, (d) Privacy settings conflict. Steps: Data→Queries & Connections→right-click→Edit, fix source path, update credentials, check File→Options→Trust Center→Privacy→ignore privacy levels (caution: data exposure risk). Resolution: Fix source reference, re-authenticate.

### Q136. Excel named ranges showing REF# in formulas after deleting columns. RCA? [EASY]

**Answer:** Symptom: Named range formulas broken. Root Cause: Deleting columns that were part of a named

range definition causes REF errors. Steps: Formulas→Name Manager→inspect and fix broken references.

**Resolution:** Redefine named ranges or use structured table references instead of static named ranges.

### Q137. Excel online collaborative editing shows conflicts constantly. RCA? [TOUGH]

**Answer:** Symptom: Frequent 'Keep My Version / Keep Server Version' prompts. Root Cause: Multiple users

editing the same cells simultaneously; OneDrive sync conflicts or unstable internet. Steps: Identify hotspot cells, assign cell ownership, use structured data entry workflow, check OneDrive sync client health. Resolution: Use data validation + input workflow to prevent simultaneous edits to same cells.

### Q138. Pivot chart data not updating when source data changes. RCA? [EASY]

**Answer:** Symptom: Chart shows old data. Root Cause: PivotTable not refreshed after data change; charts use

PivotTable as source. Steps: Right-click PivotTable→Refresh, or Data→Refresh All. Enable automatic refresh on file open via PivotTable Options. Resolution: Enable 'Refresh data when opening the file' in PivotTable Options.

### Q139. Excel file size is abnormally large (100MB+) for simple data. RCA? [TOUGH]

**Answer:** Symptom: Unexpectedly large file. Root Cause: (a) Empty cells with lingering formatting extending

used range, (b) Embedded images/objects at full resolution, (c) Many defined names or styles from copy-pasting.

**Steps:** Check Ctrl+End to find last used cell, delete empty rows/columns, compress images, clean styles.

**Resolution:** Delete excess rows/columns, compress images (Picture Tools→Compress), save fresh copy.

### Q140. Excel Get & Transform (Power Query) duplicating rows on refresh. RCA? [TOUGH]

**Answer:** Symptom: Data doubled each refresh. Root Cause: Query appends new results without removing old

ones; usually a misconfigured Append Queries step. Steps: Open query in Power Editor, review all steps for Append operations, check Load Settings (Replace/Append). Resolution: Ensure Load to Table uses 'Replace data' not 'Append to existing data'.

### Q141. Excel formula returns wrong result after inserting a row. RCA? [EASY]

**Answer:** Symptom: Formula totals incorrect after row insertion. Root Cause: Static range references (e.g.,

SUM(A1:A10)) don't auto-expand when rows are inserted outside the range. Steps: Verify formula reference range, use Table-structured references or dynamic ranges with OFFSET. Resolution: Convert data to Excel Table (Ctrl+T); structured references auto-expand.

### Q142. Users cannot open Excel files from SharePoint in desktop app. RCA? [EASY]

**Answer:** Symptom: Files open only in Excel Online. Root Cause: (a) 'Open in app' preference not set, (b) M365

Apps not installed/activated, (c) Outdated Office version, (d) SharePoint library configured to open in browser.

**Steps:** Check Library settings → Advanced → Opening Documents in the Browser. Resolution: Set library to 'Use

the client application'; ensure M365 Apps desktop activated.

### Q143. Excel AutoFill not working correctly for custom lists. RCA? [EASY]

**Answer:** Symptom: AutoFill repeats same value instead of following custom sequence. Root Cause: Custom list

not defined in Excel options. Steps: File→Options→Advanced→Edit Custom Lists→import or type sequence.

**Resolution:** Add custom list; drag fill handle after defining.

### Q144. Excel crashes when using Solver add-in. RCA? [TOUGH]

**Answer:** Symptom: Crash when running Solver. Root Cause: (a) Solver model is too large for available memory,

(b) Conflicting add-ins, (c) Outdated Solver version. Steps: Disable other add-ins, reset Solver model, check Office updates. Resolution: Simplify model, update Office, run Excel as admin if needed.

### Q145. IFS function returning incorrect branch evaluation. RCA? [EASY]

**Answer:** Symptom: Wrong logical branch selected. Root Cause: Conditions evaluated left-to-right; first TRUE

condition wins. Overlapping conditions cause earlier condition to match unintentionally. Steps: Review condition order, add explicit boundaries (e.g., AND conditions). Resolution: Reorder conditions from most specific to most general; use AND() for compound conditions.

### Q146. Excel data validation dropdown not working for new rows in a table. RCA? [EASY]

**Answer:** Symptom: Dropdown missing in new rows. Root Cause: Data validation applied to fixed range, not the

full table column. Steps: Select entire column of table, reapply data validation to full column range (e.g., $B:$B).

**Resolution:** Apply validation to entire column so new table rows inherit it.

### Q147. Excel file protected with password cannot be opened after upgrading Office. RCA? [TOUGH]

**Answer:** Symptom: Password rejected after Office upgrade. Root Cause: Old AES-128 encryption (Office 2003

format) may not work in newer versions, or password contains special characters with encoding differences.

**Steps:** Try password with different capitalization, open in older Office, check file format (.xls vs .xlsx). Resolution:

If recoverable, remove protection in old version, save as XLSX, re-protect.

### Q148. Power BI Desktop can't import Excel file with Power Pivot model. RCA? [TOUGH]

**Answer:** Symptom: Import fails or model missing. Root Cause: Power Pivot in Excel uses Analysis Services

Tabular model; Power BI can import it but requires Excel with Power Pivot installed (Pro/M365 Apps). Steps: In Power BI: Get Data→Excel Workbook, select Tables and Data Model. Ensure Excel file saved in xlsx format.

**Resolution:** Use Get Data from Excel and select the Data Model option.

### Q149. Excel conditional formatting 'Manage Rules' shows many duplicate rules. RCA? [TOUGH]

**Answer:** Symptom: Hundreds of redundant CF rules causing slow performance. Root Cause: Copy-pasting cells

copies conditional formatting rules creating per-cell-range duplicates instead of shared rules. Steps: Manage Rules dialog→identify duplicates→consolidate manually or use VBA to clean. Resolution: Delete all CF rules, reapply one clean rule covering full range.

### Q150. TEXT function returning wrong date format across locales. RCA? [TOUGH]

**Answer:** Symptom: =TEXT(A1,'MM/DD/YYYY') works on US machine but not on UK machine. Root Cause:

TEXT function uses locale-specific format codes in some Excel versions. Steps: Check Windows regional settings on affected machine, use ISO format 'YYYY-MM-DD' which is locale-neutral. Resolution: Use ISO date format codes or ensure consistent regional settings across users.

### Q151. Excel Online doesn't support a macro needed for automation. RCA? [EASY]

**Answer:** Symptom: Macro buttons don't work in browser. Root Cause: Excel Online does not support VBA

macros. Office Scripts (JavaScript-based) replace VBA in the web environment. Steps: Convert VBA macro to Office Script (Automate tab in Excel Online). Resolution: Rewrite macro as Office Script; for complex automation, use Power Automate with Excel connector.

### Q152. INDIRECT function references not updating when sheets are renamed. RCA? [TOUGH]

**Answer:** Symptom: INDIRECT returns REF# after sheet rename. Root Cause: INDIRECT builds reference string

from text; if the text contains old sheet name as hardcoded string, rename breaks it. Steps: Find all INDIRECT formulas with hardcoded sheet names. Resolution: Avoid hardcoded names in INDIRECT; use a cell reference for sheet name or use defined names that update automatically.

### Q153. Excel 'Not enough memory' error when refreshing large Power Query. RCA? [TOUGH]

**Answer:** Symptom: Memory error on Power Query refresh. Root Cause: Query loads millions of rows into

memory; Excel's 32-bit memory limit (2GB) exceeded. Steps: Check if Office is 32-bit (File→Account→About Excel), enable query folding to push processing to source, filter early in query steps, use incremental refresh.

**Resolution:** Install 64-bit Office; filter data at source before loading.

### Q154. Excel file not saving to SharePoint — upload error. RCA? [EASY]

**Answer:** Symptom: 'Upload failed' when saving to SharePoint from Excel desktop. Root Cause: (a) File checked

out by another user, (b) File name has special characters, (c) SharePoint storage quota exceeded, (d) Network interruption. Steps: Check file checkout, rename without special chars, check site storage, test network.

**Resolution:** Check-in file, rename, free storage, ensure stable connection.

### Q155. GETPIVOTDATA function returns REF# after PivotTable structure change. RCA? [TOUGH]

**Answer:** Symptom: GETPIVOTDATA breaks after modifying PivotTable. Root Cause: GETPIVOTDATA

references specific field names and positions; changing PivotTable layout (moving/removing fields) breaks references. Steps: Regenerate GETPIVOTDATA formula by clicking PivotTable cell with Auto GETPIVOTDATA enabled. Resolution: Disable auto-GETPIVOTDATA (PivotTable Analyze→Options→Generate GetPivotData off) for flexible references.

### Q156. Excel chart axes labels overlap and cannot be fixed with format settings. RCA? [EASY]

**Answer:** Symptom: Overlapping axis labels. Root Cause: Too many data points, small chart size, or long label

text. Steps: Increase chart size, reduce font size (Format Axis→Labels→Font), rotate labels (Axis Options→Labels→Angle), reduce tick mark interval. Resolution: Combine labels, rotate 45°, or use a different chart type (bar instead of column).

### Q157. INDEX/MATCH returning first match when multiple matches exist but wrong match needed.

RCA? [TOUGH]

**Answer:** Symptom: INDEX/MATCH returns wrong row. Root Cause: INDEX/MATCH returns only the first match.

For multiple criteria, only one criterion specified. Steps: Add additional criteria using MATCH with multiplication: =INDEX(C:C,MATCH(1,(A:A=X)*(B:B=Y),0)) as array formula. Resolution: Use Ctrl+Shift+Enter for array formula or FILTER function (M365).

### Q158. Excel spin button/form control not working after worksheet protection. RCA? [EASY]

**Answer:** Symptom: Controls unresponsive. Root Cause: Sheet protected without enabling 'Edit Objects'

exception. Steps: Unprotect sheet (Review→Unprotect), re-protect with 'Edit Objects' checked. Resolution: Review→Protect Sheet→check 'Edit objects' and 'Use AutoFilter'.

### Q159. Excel is not printing gridlines despite option being checked. RCA? [EASY]

**Answer:** Symptom: Gridlines absent in print. Root Cause: (a) Page Layout→Sheet→Gridlines→Print not

checked, (b) White cell background overrides gridlines. Steps: Page Layout→Sheet Options→Gridlines→Print checkbox. Check cell fill color (should be 'No Fill'). Resolution: Enable Print Gridlines in Page Layout; clear white fill from cells.

### Q160. External data connection in Excel fails after network share path change. RCA? [EASY]

**Answer:** Symptom: Connection error on refresh. Root Cause: Hardcoded UNC path in connection string is no

longer valid. Steps: Data→Queries & Connections→Edit connection→update source path. Resolution: Update connection source to new UNC path or map to a stable network location; consider using SharePoint/OneDrive as data source for resilience.

### Q161. Excel for Mac file compatibility issue with Windows users. RCA? [EASY]

**Answer:** Symptom: Features missing or errors when file opened on Windows. Root Cause: Mac-specific

features (some fonts, AppleScript macros) not cross-platform; .numbers files vs .xlsx. Steps: Save as .xlsx on Mac (File→Save As), avoid Mac-only fonts, test on Windows. Resolution: Always save in .xlsx format; use cross-platform fonts (Calibri, Arial); replace AppleScript with VBA.

### Q162. FORECAST.ETS returning error for irregular time series. RCA? [TOUGH]

**Answer:** Symptom: Error or incorrect forecast. Root Cause: FORECAST.ETS requires regular intervals (daily,

monthly). Missing dates or duplicate dates cause model failure. Steps: Ensure time series has no gaps or duplicates, fill missing periods with appropriate values (0 or interpolated). Resolution: Regularize time series; use FORECAST.ETS.SEASONALITY to detect period.

### Q163. Excel hyperlink to another workbook breaks after moving files. RCA? [EASY]

**Answer:** Symptom: Hyperlink shows 'Cannot open specified file'. Root Cause: Absolute path hardcoded in

hyperlink. Moving files breaks the path. Steps: Right-click hyperlink→Edit Hyperlink→update path. Resolution: Use relative paths or store linked files in same SharePoint library; use SharePoint URLs instead of local paths.

### Q164. ARRAYFORMULA (legacy CSE) conflicts with dynamic array functions. RCA? [TOUGH]

**Answer:** Symptom: Unexpected spill errors or wrong results mixing old and new array syntax. Root Cause:

Legacy Ctrl+Shift+Enter arrays and new dynamic arrays (FILTER, SORT, UNIQUE) handle spill differently; mixing can conflict. Steps: Convert legacy arrays to dynamic equivalents where possible; avoid mixing in same formula. Resolution: Rewrite using modern dynamic array functions available in M365.

### Q165. Excel not recognizing dates from CSV import — stored as text. RCA? [EASY]

**Answer:** Symptom: Date column not recognized as dates; formulas fail. Root Cause: CSV date format (e.g.,

MM-DD-YYYY) doesn't match Windows regional settings; Excel imports as text. Steps: Select column→Data→Text to Columns→MDY date format matching CSV, or use Power Query→change type→Using Locale. Resolution: Use Power Query with correct locale for import; specify date format explicitly.

### Q166. Workbook sharing via email breaks Power Query parameters. RCA? [TOUGH]

**Answer:** Symptom: Recipient gets query errors. Root Cause: Parameters contain absolute local paths;

recipient's machine doesn't have same path structure. Steps: Replace local paths with SharePoint/OneDrive URLs in query source; use parameters with documented defaults. Resolution: Use cloud-based data sources; document and provide data setup instructions for recipients.

### Q167. Excel LAMBDA function not recognized. RCA? [EASY]

**Answer:** Symptom: #NAME? error on LAMBDA. Root Cause: LAMBDA requires Microsoft 365 (not Office 2021

standalone). Steps: Check subscription type (File→Account). Resolution: Upgrade to M365 subscription; for Office 2021, use VBA UDF as alternative.

### Q168. Excel file with macros saved as .xlsx loses all macros. RCA? [EASY]

**Answer:** Symptom: Macros gone after save. Root Cause: .xlsx format does not support macros (macro-free

format). Saving as .xlsx strips all VBA code. Steps: Save as .xlsm (Excel Macro-Enabled Workbook) to preserve macros. Resolution: Always save macro-containing workbooks as .xlsm; configure OneDrive/SharePoint to allow .xlsm files.

### Q169. LET function formula result differs from equivalent nested formula. RCA? [TOUGH]

**Answer:** Symptom: LET gives different result than equivalent without LET. Root Cause: Variable evaluation

order in LET is sequential; a variable referencing an earlier variable may cause precedence issue if logic is complex. Steps: Trace each LET variable value using helper cells. Resolution: Break complex LET into named ranges for debugging; validate each variable step.

### Q170. Excel XLOOKUP with approximate match returns unexpected row. RCA? [EASY]

**Answer:** Symptom: Wrong row returned. Root Cause: XLOOKUP approximate match (match_mode 1 or -1)

requires sorted data; unsorted data returns incorrect result. Steps: Sort lookup array in ascending/descending order matching the match_mode. Resolution: Sort source data or use XLOOKUP with exact match (match_mode=0) plus IFERROR.

### Q171. Excel filter dropdown not showing all unique values. RCA? [EASY]

**Answer:** Symptom: Filter list truncated. Root Cause: AutoFilter dropdown shows only 10,000 unique values in

older Excel; or Pivot Table cache out of date. Steps: Use search box within AutoFilter for more values; use PivotTable slicer for large datasets. Resolution: Use search within AutoFilter; for very large sets, use Power Query or Power BI.

### Q172. Excel macro runs fine locally but throws error 1004 on SharePoint. RCA? [TOUGH]

**Answer:** Symptom: Run-time error 1004 'Application-defined error' in SharePoint context. Root Cause: Macro

tries to open local file or use ActiveX control not supported in protected view / co-authoring mode. Steps: Check macro for ActiveX, local file references, or Protected View triggers. Resolution: Enable Editing on the document, or store macro workbook in trusted location.

### Q173. SUMPRODUCT giving inconsistent results with filtered data. RCA? [TOUGH]

**Answer:** Symptom: SUMPRODUCT doesn't reflect visible (filtered) rows only. Root Cause: SUMPRODUCT

does not respect AutoFilter visibility. Steps: Use SUBTOTAL(9,...) for filtered sums or AGGREGATE function.

**Resolution:** Replace SUMPRODUCT with SUMPRODUCT((SUBTOTAL(103,OFFSET(...))*criteria*values))

pattern for filter-aware calculation.

### Q174. Excel cannot connect to SQL Server via ODBC — 'Login failed'. RCA? [TOUGH]

**Answer:** Symptom: ODBC connection error on data refresh. Root Cause: (a) SQL Server credentials changed,

(b) Windows authentication user lacks SQL access, (c) Firewall blocking port 1433. Steps: Test ODBC DSN independently (odbcad32.exe), verify SQL login, check firewall. Resolution: Update credentials in connection string or DSN; ensure SQL user has db_datareader permission.

### Q175. Excel Advanced Filter extracting incorrect unique records. RCA? [TOUGH]

**Answer:** Symptom: Duplicate records in extract. Root Cause: 'Unique records only' requires exact match

including all columns; hidden whitespace in cells causes rows to appear different. Steps: TRIM all data, ensure font/format consistency, expand visible columns. Resolution: Clean data with TRIM/CLEAN before applying Advanced Filter.

### Q176. Embedded Excel object in Word document not updating. RCA? [EASY]

**Answer:** Symptom: Excel data in Word not current. Root Cause: Object is an embedded copy (not linked).

Changes to source Excel file not reflected. Steps: Double-click object to edit in-place; for live link: Insert→Object→Create from File→Link to file. Resolution: Use Link to file for live data; periodically refresh via Edit Links dialog.

### Q177. Excel crashes with 'Excel has stopped working' on startup. RCA? [TOUGH]

**Answer:** Symptom: Crash on open. Root Cause: (a) Corrupted XLSTART workbook, (b) Corrupt add-in, (c)

Damaged Office installation. Steps: Start in Safe Mode (excel /safe), delete files in %APPDATA%\Microsoft\Excel\XLSTART, disable add-ins. Resolution: Remove XLSTART files, repair Office (Apps & Features→Modify→Quick Repair).

### Q178. MATCH function with wildcard returns wrong position in large dataset. RCA? [EASY]

**Answer:** Symptom: Wildcard MATCH returns unexpected position. Root Cause: MATCH with wildcards

searches left-to-right and returns first match. If data unsorted or match_type not 0, returns approximate match.

**Steps:** Ensure match_type=0 for wildcard MATCH. Resolution: Always use match_type=0 (exact/wildcard) with

wildcards; MATCH('*text*',A:A,0).

### Q179. Excel's 'Protect Sheet' doesn't prevent macro from modifying cells. RCA? [TOUGH]

**Answer:** Symptom: Macro bypasses sheet protection. Root Cause: VBA can bypass sheet protection unless

code-level protection applied. Steps: In VBA, use ActiveSheet.Protect before sensitive operations and Unprotect with password for legitimate edits. Resolution: Add ws.Protect Password:='pwd' in VBA to re-lock after macro changes, or use worksheet_change event with password check.

### Q180. Excel formula audit (trace precedents/dependents) shows incorrect arrows after copy-paste.

RCA? [EASY]

**Answer:** Symptom: Audit arrows point to wrong cells. Root Cause: Copy-paste copies formula audit state too;

arrows may point to original source positions. Steps: Remove all arrows (Formulas→Auditing→Remove Arrows), re-run trace on current cells. Resolution: Clear and re-audit formulas after any significant restructuring.

---

## Section 4 — Word Troubleshooting — RCA Format — Q181 to Q220

### Q181. Word document shows 'file in use by another user' error when saving. RCA? [EASY]

**Answer:** Symptom: Cannot save; file locked. Root Cause: File open in two instances (desktop + browser),

another user has file open, or OneDrive sync conflict. Steps: Close browser version, check all open Word windows, wait for other user to close, check OneDrive sync status. Resolution: Use co-authoring on SharePoint/OneDrive instead of single-user locking; check for .lck or .tmp lock files.

### Q182. Word document formatting changes randomly after emailing. RCA? [EASY]

**Answer:** Symptom: Recipient sees different formatting. Root Cause: Recipient uses different font not installed,

different Word version interprets styles differently, or document uses local fonts. Steps: Embed fonts (File→Options→Save→Embed fonts), use standard fonts (Calibri, Times New Roman), save as PDF for final delivery. Resolution: Embed fonts or convert to PDF for distribution.

### Q183. Track Changes comments not visible for a reviewer. RCA? [EASY]

**Answer:** Symptom: Comments/track changes invisible. Root Cause: (a) Show Markup disabled for that reviewer,

(b) Show All Markup off, (c) Document in Final view. Steps: Review→Tracking→Show Markup→enable All Reviewers, check Display for Review dropdown = All Markup. Resolution: Enable All Markup and all reviewer markup visibility.

### Q184. Word 'Normal.dotm' template corrupted causing formatting issues. RCA? [TOUGH]

**Answer:** Symptom: All new documents have wrong fonts/styles. Root Cause: Normal.dotm (global template)

corrupted by add-in or macro. Steps: Close Word, rename Normal.dotm to Normal.old in %APPDATA%\Microsoft\Templates, restart Word (new Normal.dotm auto-created). Resolution: Delete/rename Normal.dotm; reconfigure custom default styles.

### Q185. Table of Contents not updating after adding new headings. RCA? [EASY]

**Answer:** Symptom: TOC missing new sections. Root Cause: TOC requires manual or automatic update;

Heading styles must be used (not manual bold text). Steps: Right-click TOC→Update Field→Update entire table; verify headings use Heading 1/2/3 styles. Resolution: Apply proper Heading styles; press F9 on TOC or use Update TOC button.

### Q186. Word mail merge producing wrong data in merged fields. RCA? [EASY]

**Answer:** Symptom: Wrong names/data in merged document. Root Cause: (a) Data source fields mapped

incorrectly, (b) Merge field names don't match data source headers, (c) Data source has extra spaces in headers. Steps: Mailings→Match Fields to re-map, verify Excel/CSV headers match field names exactly (case-insensitive but space-sensitive). Resolution: Clean data source headers; use Match Fields to remap.

### Q187. Word document extremely slow to scroll with many images. RCA? [TOUGH]

**Answer:** Symptom: Severe lag during scrolling. Root Cause: High-resolution images embedded at full size;

Word renders each image during scroll. Steps: Compress images (Picture Tools→Format→Compress Pictures→Email resolution), use Draft view (View→Draft) for editing. Resolution: Compress all images; consider linking images instead of embedding.

### Q188. Endnotes appearing in wrong location in Word document. RCA? [EASY]

**Answer:** Symptom: Endnotes at end of section not end of document. Root Cause: Section break with 'Endnotes

at end of section' option enabled. Steps: Double-click endnote→Note Options→change 'End of document' vs 'End of section' setting. Resolution: Set endnote position to 'End of document' in Note Options dialog.

### Q189. Word spell check not working for a specific language. RCA? [EASY]

**Answer:** Symptom: Spelling errors not flagged in French/Spanish/etc. Root Cause: (a) Language proofing tools

not installed for that language, (b) Text marked as 'Do not check spelling', (c) Wrong language set for paragraph.

**Steps:** Select text→Review→Language→Set Proofing Language (uncheck 'Do not check spelling/grammar'),

install language pack in M365 settings. Resolution: Install language proof pack; set correct language; remove 'Do not check' flag.

### Q190. Word document with linked Excel chart shows broken link on another machine. RCA? [EASY]

**Answer:** Symptom: Chart shows 'linked file unavailable'. Root Cause: Linked file path is absolute/local; recipient

doesn't have same path. Steps: Edit→Links→Update/Change source to new path, or break link (embed chart).

**Resolution:** Embed object instead of linking for distributed documents; use shared network paths for linked files.

### Q191. Word document opens in Protected View and cannot be edited. RCA? [EASY]

**Answer:** Symptom: Yellow bar 'Enable Editing' shown; editing blocked. Root Cause: File from internet/email or

shared network location triggers Protected View for security. Steps: Click 'Enable Editing', add file location to trusted locations (File→Options→Trust Center→Trusted Locations). Resolution: For organizational files, configure Group Policy or M365 admin to trust known SharePoint/network locations.

### Q192. Headers/footers showing inconsistently across sections in Word. RCA? [TOUGH]

**Answer:** Symptom: Header changes mid-document or disappears. Root Cause: 'Link to Previous'

broken/enabled between sections; different first page setting varies by section. Steps: Double-click header→verify 'Link to Previous' state per section, check 'Different First Page' settings per section. Resolution: Carefully manage 'Link to Previous' and section-specific header options.

### Q193. Word crashes when accepting all tracked changes in a large document. RCA? [TOUGH]

**Answer:** Symptom: Word freezes/crashes on Accept All. Root Cause: Extremely large number of tracked

changes or complex objects (tables, images) within tracked changes overloads Word memory. Steps: Accept changes in batches by section, use Word in 64-bit mode, split document. Resolution: Process sections separately; use Review→Accept→Accept All Changes in Document in 64-bit Word.

### Q194. Numbered list restarts numbering incorrectly after a paragraph break. RCA? [EASY]

**Answer:** Symptom: List restarts at 1 unexpectedly. Root Cause: List continuation breaks when intervening

paragraph uses a style not linked to the list, or list has 'restart' property set. Steps: Right-click first item of new list segment→Set Numbering Value→Continue Previous List. Resolution: Use 'Continue Numbering' option; link all list paragraphs to same list template.

### Q195. Word document collaboration in Teams shows 'Co-authoring not available'. RCA? [TOUGH]

**Answer:** Symptom: Cannot co-author in Teams tab. Root Cause: (a) File stored locally (not

SharePoint/OneDrive), (b) File format .doc not .docx, (c) Document has password protection, (d) IRM policy applied. Steps: Upload to SharePoint, convert to .docx, remove password protection and IRM for co-authoring.

**Resolution:** Store in SharePoint, use .docx format, remove conflicting protections.

### Q196. References/Bibliography not generating correctly in Word. RCA? [EASY]

**Answer:** Symptom: Citation shows placeholder or wrong format. Root Cause: (a) Source not fully filled in source

manager, (b) Wrong citation style selected, (c) Source corrupted in Sources.xml. Steps: References→Manage Sources→verify source details, select correct style (APA/MLA/Chicago). Resolution: Complete all required source fields; match citation style to requirement; refresh bibliography.

### Q197. Word Macro Security warning blocks all macros even from trusted sources. RCA? [TOUGH]

**Answer:** Symptom: All macros blocked despite trusted publisher. Root Cause: Trust Center macro setting set to

'Disable all macros without notification' overriding trusted publishers list. Steps: File→Options→Trust Center→Macro Settings→set to 'Disable all macros except digitally signed macros'. Resolution: Add publisher's certificate to Trusted Publishers; adjust macro security level appropriately.

### Q198. Autocorrect replacing specific technical terms incorrectly. RCA? [EASY]

**Answer:** Symptom: Technical abbreviations auto-corrected. Root Cause: AutoCorrect list contains the technical

term as a correction trigger. Steps: File→Options→Proofing→AutoCorrect Options→find and remove offending entries. Resolution: Remove incorrect AutoCorrect entries; add exceptions.

### Q199. Word font appears blurry on high-DPI displays. RCA? [TOUGH]

**Answer:** Symptom: ClearType fonts look fuzzy. Root Cause: ClearType disabled, Windows DPI scaling conflict

with Word, or wrong display scaling. Steps: Run ClearType Text Tuner (Start→ClearType), check Word display settings    (File→Options→Advanced→Display),         set    scaling     for    Word      app    (right-click exe→Properties→Compatibility→DPI override). Resolution: Enable ClearType; set DPI compatibility for Office apps.

### Q200. Word 'Compare Documents' showing too many trivial differences. RCA? [EASY]

**Answer:** Symptom: Compare generates thousands of changes for minor whitespace. Root Cause: Default

comparison includes whitespace, formatting, punctuation changes. Steps: Review→Compare→More→uncheck 'Formatting', 'Spaces/Punctuation' as needed. Resolution: Customize comparison settings; focus on text-level changes only.

### Q201. Word form fields not working after document protection. RCA? [EASY]

**Answer:** Symptom: Form fillable fields unresponsive. Root Cause: Document protected for 'Tracked Changes' or

'Comments' instead of 'Filling in forms'. Steps: Developer→Protect Document→Restrict Editing→Allow only 'Filling in forms'. Resolution: Set correct protection type; re-protect with 'Filling in forms' option.

### Q202. Word automatic hyphenation breaking technical URLs in document. RCA? [EASY]

**Answer:** Symptom: URLs hyphenated mid-word disrupting links. Root Cause: Automatic hyphenation applies to

all text including URLs. Steps: Select URL text→Language→Do Not Check (prevents hyphenation), or turn off hyphenation for document (Layout→Hyphenation→None). Resolution: Apply 'No proofing' language to URLs, or use character style with 'Do not hyphenate' property.

### Q203. Word document with embedded PDF object not displaying on recipient's machine. RCA?

[TOUGH]

**Answer:** Symptom: Embedded PDF shows blank/error. Root Cause: Recipient doesn't have Adobe

Acrobat/Reader installed as the OLE server for PDF objects; or the PDF is embedded as icon. Steps: Install Adobe Reader on recipient machine, or convert embedded PDF to images before sharing. Resolution: Embed PDF as image (Paste Special→Picture) for universal display.

### Q204. Styles panel not showing custom styles created in another template. RCA? [TOUGH]

**Answer:** Symptom: Custom styles missing from Styles pane. Root Cause: Custom styles defined in attached

template, but 'Automatically update document styles' or style copying not done. Steps: Developer→Document Template→attach correct template and check 'Automatically update document styles'. Resolution: Attach correct template, or copy styles via Organizer (Manage Styles→Import/Export).

### Q205. Word document printing different margins than shown on screen. RCA? [EASY]

**Answer:** Symptom: Printed margins don't match document settings. Root Cause: (a) Printer minimum margins

override document margins, (b) 'Scale to paper size' print option active, (c) Section-level margin overrides. Steps: File→Print→Preview confirms actual output; check printer properties for minimum margins; uncheck 'Scale to fit' in printer settings. Resolution: Adjust document margins to exceed printer minimum; disable scale to fit.

### Q206. Tracked changes from a reviewer appear as a different reviewer's name. RCA? [EASY]

**Answer:** Symptom: Changes attributed to wrong person. Root Cause: Document was edited while Office logged

in under a shared/service account, or author name not set correctly in Word options. Steps: File→Options→General→change username and initials. Resolution: Ensure each user opens Word with their own M365 credentials; avoid shared accounts.

### Q207. Word file saved as PDF has garbled characters for non-Latin scripts. RCA? [TOUGH]

**Answer:** Symptom: Arabic/Chinese/Hindi characters corrupted in PDF. Root Cause: Fonts not embedded in

PDF, or Word PDF export doesn't handle RTL/complex scripts correctly. Steps: File→Export→Create PDF/XPS→Options→'ISO 19005-1 compliant' and embed fonts. Resolution: Enable font embedding and use PDF/A compliance option; test with Save as PDF vs Adobe Acrobat PDF Maker.

### Q208. Word document section breaks causing unexpected page numbering. RCA? [TOUGH]

**Answer:** Symptom: Page numbers restart or skip in document. Root Cause: Section breaks with 'Start at'

numbering set incorrectly; continuous section breaks not intended to restart. Steps: Double-click footer→check 'Link to Previous', modify page number format per section (Insert→Header & Footer→Page Number→Format).

**Resolution:** Set page number format explicitly per section; link/unlink sections as needed.

### Q209. Word equation editor (Office Math) formulas not rendering on older Office. RCA? [TOUGH]

**Answer:** Symptom: Equations show as text or objects. Root Cause: OMML (Office MathML) format not

supported in Word 2007/2010; or equations created in new format don't downgrade gracefully. Steps: Save as compatibility mode, or use Equation as image. Resolution: For cross-version compatibility, convert equations to images; avoid OMML features not in target version.

### Q210. Word crashes when inserting a large table from clipboard. RCA? [TOUGH]

**Answer:** Symptom: Crash or 'not responding' on paste. Root Cause: Table with thousands of rows and merged

cells exceeds Word's clipboard paste buffer. Steps: Paste Special→Unformatted Text, then manually reformat; or split table into chunks. Resolution: Paste as plain text, or import table from Excel as linked object.

### Q211. Word document layout breaks when opening on Mac vs Windows. RCA? [EASY]

**Answer:** Symptom: Page breaks/tables misaligned between platforms. Root Cause: Different font rendering

metrics (Mac vs Windows); missing Windows fonts on Mac substitute differently. Steps: Embed fonts, use cross-platform fonts, test on both platforms. Resolution: Save as PDF for platform-sensitive layouts; use Calibri/Arial for cross-platform consistency.

### Q212. Word bibliography sort order changes unexpectedly. RCA? [EASY]

**Answer:** Symptom: References reorder on document update. Root Cause: Bibliography auto-sorts by citation

style rules (APA alphabetical); manual reordering is overwritten on update. Steps: To prevent reordering, convert bibliography to static text (right-click→Convert Bibliography to Static Text). Resolution: Finalize document, then convert bibliography to static text before submission.

### Q213. Word 'Find & Replace' with formatting options not finding all instances. RCA? [EASY]

**Answer:** Symptom: Some formatted instances missed. Root Cause: 'No Formatting' button in Find/Replace

removes format criteria; or formatting applied at character level not paragraph level. Steps: Use More→Format→Font in Find dialog to specify exact formatting. Resolution: Manually clear formatting criteria in Find dialog; run separate passes for different formatting levels.

### Q214. Word crashes specifically when printing to a network printer. RCA? [TOUGH]

**Answer:** Symptom: Crash only on print, not on screen. Root Cause: Corrupt printer driver interfering with Word's

GDI rendering. Steps: Set default printer to Microsoft Print to PDF → test print, update/reinstall network printer driver. Resolution: Update printer driver; set alternate default printer; repair Office installation.

### Q215. Word Merge fields showing field code syntax «MERGEFIELD» instead of data. RCA? [EASY]

**Answer:** Symptom: Field codes visible instead of merged data. Root Cause: Field code display toggled on

(Alt+F9), or mail merge preview not active. Steps: Press Alt+F9 to toggle field code display; use Preview Results button in Mailings tab. Resolution: Toggle Alt+F9 off; use Preview Results to verify merge output before completing merge.

### Q216. Word Online formatting toolbar shows different options than desktop. RCA? [EASY]

**Answer:** Symptom: Some formatting features unavailable in browser. Root Cause: Word Online has a subset of

desktop Word features; advanced formatting (ligatures, OpenType features, advanced paragraph spacing) not available. Steps: Download and open in desktop app for advanced formatting. Resolution: Use desktop Word for complex formatting; Word Online for basic editing and real-time collaboration.

### Q217. Word document protection password forgotten — cannot edit protected sections. RCA?

[TOUGH]

**Answer:** Symptom: Locked sections cannot be edited. Root Cause: Document protection password lost. Steps:

VBA method: Sub UnprotectDoc(): ActiveDocument.Unprotect Password:='': End Sub (works if protection stored in document XML). More reliably: Extract docx→edit settings.xml to remove w:documentProtection node.

**Resolution:** Use XML manipulation to remove protection; implement password management to prevent

recurrence.

### Q218. Word cross-references breaking after reorganizing document sections. RCA? [EASY]

**Answer:** Symptom: Cross-references show '0' or wrong heading. Root Cause: Headings referenced are

moved/deleted; field codes reference bookmarks that may have shifted. Steps: Select all (Ctrl+A)→F9 to update all fields; check broken cross-references manually. Resolution: Update all fields after restructuring; use Update Fields on document open setting.

### Q219. Word online version history not available for a document. RCA? [EASY]

**Answer:** Symptom: No version history in Word Online. Root Cause: Document stored on local drive or network

share, not SharePoint/OneDrive (version history requires SharePoint or OneDrive). Steps: Upload document to SharePoint/OneDrive library, enable versioning on library. Resolution: Migrate documents to SharePoint/OneDrive for version history; enable library versioning.

### Q220. Word AutoSave greyed out for a document. RCA? [EASY]

**Answer:** Symptom: AutoSave toggle disabled. Root Cause: Document not saved to OneDrive/SharePoint

(AutoSave requires cloud storage), or document in compatibility mode (.doc format). Steps: Save to OneDrive/SharePoint, convert to .docx format. Resolution: Upload to cloud storage and convert to modern format to enable AutoSave.

---

## Section 5 — PowerPoint Troubleshooting — RCA Format — Q221 to

### Q221. PowerPoint presentation plays incorrectly in Slide Show on different machine. RCA? [EASY]

**Answer:** Symptom: Animations/fonts wrong on another PC. Root Cause: Fonts not embedded, linked media files

missing, or PowerPoint version differences. Steps: File→Info→Compress Media and Embed fonts, use File→Save As→Tools→Save Options→Embed fonts, use 'Optimize for compatibility'. Resolution: Embed fonts, embed/compress media, use Optimize for Compatibility option.

### Q222. PowerPoint file size too large with many images. RCA? [EASY]

**Answer:** Symptom: File is 200MB+ for a 20-slide deck. Root Cause: High-resolution images inserted at full size;

each image stored at original resolution. Steps: Select all images→Picture Format→Compress Pictures→Email/Web resolution, delete cropped areas. Resolution: Compress all pictures; use 96-150 DPI for screen presentations; use linked images for print-quality source.

### Q223. Animations not playing in PowerPoint Online / Teams tab. RCA? [EASY]

**Answer:** Symptom: Animations play in desktop but not in browser/Teams. Root Cause: PowerPoint Online

supports a subset of animations; complex morph/3D/some entrance effects not fully supported. Steps: Test in Office Online, simplify animations for cross-platform use. Resolution: Use basic fade/appear animations for browser compatibility; download and present from desktop app.

### Q224. Slide master changes not applying to existing slides. RCA? [EASY]

**Answer:** Symptom: Modified master layout not reflected on slides. Root Cause: Slides use 'override' formatting

breaking master link; directly-formatted placeholders override master. Steps: Select slide→Reset Slide (Home→Reset) to reapply master formatting. Resolution: Click Reset on affected slides; train users to format via master, not directly on slides.

### Q225. PowerPoint Morph transition not working between two slides. RCA? [TOUGH]

**Answer:** Symptom: Morph shows as simple transition, not morphing objects. Root Cause: Objects to morph

must have identical names (!!name in Selection Pane) or same object type on both slides. Steps: View→Selection Pane→rename matching objects with !! prefix (e.g., !!circle). Resolution: Name objects consistently with !! prefix on both slides for Morph to detect match.

### Q226. PowerPoint Presenter View shows wrong screen order in dual-monitor setup. RCA? [EASY]

**Answer:** Symptom: Presentation shows on main screen, not projector. Root Cause: Display assignment

reversed; Slide Show tab monitor setting pointing to wrong display. Steps: Slide Show→Set Up Slide Show→choose correct monitor from 'Show presentation on' dropdown. Resolution: Swap monitor assignments in Slide Show settings; use Windows display settings to identify screen numbers.

### Q227. Embedded Excel chart in PowerPoint not updating with new data. RCA? [EASY]

**Answer:** Symptom: Chart shows old data. Root Cause: Chart is embedded (snapshot), not linked. Steps:

Double-click chart to edit embedded data, or right-click→Chart Object→Open to edit source. For linked chart: right-click→Update Link. Resolution: Use 'Paste Special→Paste Link' when inserting chart for live data; update links via Edit→Links.

### Q228. PowerPoint file corrupted after abrupt system shutdown. RCA? [TOUGH]

**Answer:** Symptom: Cannot open file; corruption error. Root Cause: AutoRecovery file may exist; main file

partially written. Steps: Check %APPDATA%\Microsoft\PowerPoint for .pptx recovery files, try Open and Repair, use online PowerPoint recovery tools. Resolution: Enable AutoSave to OneDrive to prevent data loss; restore from SharePoint version history.

### Q229. Slide numbers not displaying correctly in a multi-section presentation. RCA? [EASY]

**Answer:** Symptom: Slide numbers restart or skip. Root Cause: 'Start slide numbering at' set incorrectly; slide

number placeholder missing on some layouts. Steps: Design→Slide Size→Customize→set start number; Insert→Slide Number, apply to all. Resolution: Set start number in Design→Slide Size; add number placeholder to all Slide Master layouts.

### Q230. PowerPoint narration audio not playing on another machine. RCA? [EASY]

**Answer:** Symptom: Narration silent on recipient's PC. Root Cause: Audio saved as linked file (not embedded), or

codec mismatch. Steps: Use Optimize Media Compatibility (File→Info→Optimize Compatibility), ensure audio embedded not linked. Resolution: Record narration in PowerPoint (embeds as .m4a), use Optimize Compatibility before sharing.

### Q231. SmartArt graphic text becoming very small when adding too many items. RCA? [EASY]

**Answer:** Symptom: Text shrinks unreadably as items added. Root Cause: SmartArt auto-fits text to fit shape;

layout has a maximum item count before text becomes too small. Steps: Limit items (most SmartArt looks best with 3-7 items), convert to manual shapes, or split into two slides. Resolution: Keep SmartArt item count within layout's recommended range; convert to shapes if more items needed.

### Q232. PowerPoint video inserted from web URL doesn't play after sharing file. RCA? [TOUGH]

**Answer:** Symptom: Video shows placeholder, won't play offline. Root Cause: Online video linked to URL

requires internet connection; if URL changes or internet unavailable, video fails. Steps: Download video and insert as local file (Insert→Video→Video on My PC). Resolution: Embed video file directly; for SharePoint sharing, use Stream videos via embed code.

### Q233. Speaker notes formatting lost after exporting to PDF. RCA? [EASY]

**Answer:** Symptom: PDF handout shows garbled notes. Root Cause: PDF export of notes uses a basic layout;

complex note formatting (tables, bullets) may not render correctly. Steps: File→Export→Create PDF/XPS→Options→select 'Notes pages' for handout with notes. Resolution: Keep notes formatting simple; use Notes Pages view to verify before PDF export.

### Q234. PowerPoint collaboration conflict: two versions of same deck diverging. RCA? [EASY]

**Answer:** Symptom: Changes from co-author overwritten. Root Cause: File not stored on SharePoint/OneDrive;

each user working on local copy. Steps: Upload to SharePoint/OneDrive to enable co-authoring. Resolution: Always store shared presentations on SharePoint/OneDrive; use co-authoring, not email distribution.

### Q235. Action buttons/hyperlinks in presentation not working in Slide Show. RCA? [EASY]

**Answer:** Symptom: Clicking action button does nothing. Root Cause: (a) Action button linked to file that doesn't

exist on current machine, (b) Protected View blocks actions, (c) Wrong slide number in link. Steps: Right-click button→Edit Hyperlink→verify target, test in Slide Show mode (not Normal). Resolution: Verify link targets; ensure hyperlinks use relative paths or URLs; enable editing before presenting.

### Q236. PowerPoint design themes not applying consistently after upgrading Office. RCA? [TOUGH]

**Answer:** Symptom: Theme colors/fonts mismatch after upgrade. Root Cause: New Office version includes

updated theme definitions; old .thmx files may have different color/font assignments. Steps: Reapply theme from Design tab; check theme colors and fonts under Customize section. Resolution: Re-export and redistribute updated .thmx file; check with IT for standardized corporate template.

### Q237. Photo album feature in PowerPoint creating too many slides. RCA? [EASY]

**Answer:** Symptom: Hundreds of slides generated for large photo collection. Root Cause: Photo Album

(Insert→Photo Album) creates one slide per image by default. Steps: During album creation, select '2 pictures' or '4 pictures' per slide layout. Resolution: Choose appropriate images-per-slide layout in Photo Album dialog before creating.

### Q238. 3D model in PowerPoint not displaying on recipient's machine. RCA? [TOUGH]

**Answer:** Symptom: 3D object shows as placeholder. Root Cause: 3D model requires Windows 10+ and modern

Office (2019/M365); older OS or Office versions don't support .glb/.fbx 3D objects. Steps: Convert 3D to image (right-click→Save as Picture) for compatibility. Resolution: Flatten 3D to image for broad compatibility; note Office version requirements.

### Q239. Slide transition sound not playing during presentation. RCA? [EASY]

**Answer:** Symptom: Sound effects silent during Slide Show. Root Cause: System audio muted, wrong audio

device selected, or sound file was external WAV and not embedded. Steps: Check Windows volume/mute, verify audio device in Slide Show, check transition settings (Transitions→Sound). Resolution: Unmute system audio, embed sound files, verify audio output device.

### Q240. PowerPoint 'Reduce File Size' option permanently lowering image quality. RCA? [TOUGH]

**Answer:** Symptom: Images blurry after compress. Root Cause: Compress Pictures deletes cropped areas and

resamples to target resolution permanently. Undo (Ctrl+Z) is the only reversal. Steps: Use Ctrl+Z immediately to undo; work on a copy for compression. Resolution: Always work on a backup copy before compressing; set target resolution to match actual display need (150dpi for screen, 220+ for print).

### Q241. PowerPoint accessibility checker flagging many errors before executive presentation. RCA?

[TOUGH]

**Answer:** Symptom: Accessibility issues in Review→Check Accessibility. Root Cause: Missing alt text on images,

poor color contrast, reading order issues, no slide titles. Steps: Add alt text to all images, check contrast ratios, set reading order in Selection pane, add descriptive slide titles. Resolution: Systematically address each checker finding; use Accessibility Checker as part of slide creation process.

### Q242. Slide layout placeholders disappearing when switching to a different theme. RCA? [TOUGH]

**Answer:** Symptom: Content placeholders gone after theme change. Root Cause: New theme has different Slide

Master layouts; placeholders on slides linked to old layout names that don't exist in new theme. Steps: View→Slide Master→add required placeholders to matching layouts in new theme. Resolution: Design themes with same layout structure; map content to correct layout after theme change.

### Q243. PowerPoint runs slowly during Slide Show on modern laptop. RCA? [TOUGH]

**Answer:** Symptom: Lag and dropped frames in presentation. Root Cause: (a) Complex animations with many

objects, (b) Laptop running on battery power (performance throttling), (c) Software rendering instead of GPU.

**Steps:** Plug into power, disable hardware graphics acceleration (File→Options→Advanced→uncheck hardware

acceleration) then re-enable, simplify animations. Resolution: Connect to power; reduce animation complexity; ensure GPU drivers updated.

### Q244. Co-author in Teams loses access to edit a shared presentation. RCA? [EASY]

**Answer:** Symptom: 'You need permission' error for co-editor. Root Cause: Presenter changed sharing

permissions; file moved within SharePoint; guest access expired. Steps: Recheck sharing settings on SharePoint, reshare with Edit permission, verify guest access not expired. Resolution: Use 'Share' from within PowerPoint; grant Edit permission to specific users.

### Q245. Tables in PowerPoint have incorrect cell borders after copy from Word. RCA? [EASY]

**Answer:** Symptom: Cell borders misaligned or invisible after paste. Root Cause: Word table formatting uses

different border model; paste translates imperfectly. Steps: After paste, select table→Table Design→Borders→apply from scratch using PPT border tools. Resolution: Recreate table natively in PowerPoint; use Paste Special→Picture for visual fidelity.

### Q246. Speaker notes going missing after merging two presentations. RCA? [TOUGH]

**Answer:** Symptom: Notes blank in slides from second presentation. Root Cause: When using 'Reuse Slides',

notes are not imported. Steps: In source presentation, copy slides normally (not Reuse Slides); use Outline view to import content with notes. Resolution: Copy slides with Ctrl+C from source and Ctrl+V into destination to preserve notes.

### Q247. PowerPoint placeholder text not resizing to fit content. RCA? [EASY]

**Answer:** Symptom: Text overflows placeholder. Root Cause: AutoFit disabled for text box or placeholder. Steps:

Right-click placeholder→Format Shape→Text Options→Autofit→select 'Resize shape to fit text' or 'Shrink text on overflow'. Resolution: Enable Shrink text on overflow for fixed placeholders; Resize shape for flexible ones.

### Q248. Linked media file error when opening presentation on different OS. RCA? [EASY]

**Answer:** Symptom: 'Cannot find linked media file' error. Root Cause: Media files linked (not embedded) using

local path; path doesn't exist on new machine. Steps: File→Info→Optimize Compatibility (embeds media), or move media to same folder as PPTX and relink. Resolution: Always use 'Optimize Compatibility' before distributing; prefer embedding over linking for portability.

### Q249. PowerPoint chart with live data loses formatting when Excel source updated. RCA? [TOUGH]

**Answer:** Symptom: Chart formatting resets after data update. Root Cause: Unlinking the data or using 'Apply

Layout' resets chart format to default. Steps: Format chart elements and then use 'Set as Default Chart' for custom formats. Resolution: Lock chart formatting by not using 'Apply Chart Layout'; format elements individually and avoid Reset.

### Q250. Presentation exported to video has lower quality than on screen. RCA? [EASY]

**Answer:** Symptom: Video export blurry/pixelated. Root Cause: Default export resolution (720p) lower than

screen resolution. Steps: File→Export→Create a Video→choose 'Ultra HD (4K)' or 'Full HD (1080p)'. Resolution: Select higher resolution preset; note file size increases significantly at higher resolutions.

### Q251. PowerPoint add-in (COM) causing crash on specific slide. RCA? [TOUGH]

**Answer:** Symptom: Crash consistently on one slide with add-in active. Root Cause: Add-in hooks slide change

event and encounters an unsupported object type on that specific slide. Steps: Disable add-ins (File→Options→Add-ins→Manage COM Add-ins), test if crash persists. Resolution: Update or disable offending add-in; report to add-in vendor with crash dump.

### Q252. Text box with rounded corners reverts to sharp corners after save/reopen. RCA? [EASY]

**Answer:** Symptom: Shape format lost on reopen. Root Cause: Compatibility mode (.ppt format) doesn't support

rounded corner text boxes; saved as .pptx but Edit Compatibility dialog overrides. Steps: Save as .pptx (not .ppt), check File→Info→Check for Compatibility Issues. Resolution: Ensure file saved as .pptx; remove compatibility mode.

### Q253. Slide numbers shown in Slide Panel but not in Slide Show. RCA? [EASY]

**Answer:** Symptom: Numbers visible in edit, absent in presentation. Root Cause: 'Slide number' checkbox not

enabled in Insert→Header and Footer dialog, or placeholder removed from Slide Master. Steps: Insert→Header and Footer→Slide tab→check 'Slide number'→Apply to All. Resolution: Apply slide number from Header and Footer dialog; ensure number placeholder on Slide Master.

### Q254. Background image disappears when printing PowerPoint. RCA? [EASY]

**Answer:** Symptom: Background graphics absent in print output. Root Cause: 'Background graphics' option

disabled in Print dialog or Slide Master background settings. Steps: File→Print→Settings→check 'Print Background Colors and Images' (via Page Setup or print dialog). Resolution: Enable background graphics in print settings; for consistent print, use Design→Format Background with 'Apply to All'.

### Q255. PowerPoint Zoom feature (Summary Zoom) not available in older client. RCA? [TOUGH]

**Answer:** Symptom: 'Zoom' option greyed out or missing. Root Cause: Zoom/Summary Zoom requires Microsoft

365 or Office 2019+; Office 2016 and earlier don't support it. Steps: Check Insert menu for Zoom option.

**Resolution:** Upgrade to M365 Apps; for older clients, use traditional hyperlinks and navigation buttons instead of

Zoom.

### Q256. Presenter Coach feedback not appearing during practice. RCA? [TOUGH]

**Answer:** Symptom: Presenter Coach gives no real-time tips. Root Cause: Feature requires internet connection

and M365 subscription; firewall or proxy may block required endpoint. Steps: Check internet connection, verify M365 subscription, check if corporate firewall blocks speech API endpoints. Resolution: Whitelist Microsoft speech/cognitive service endpoints in firewall; use personal network to test.

### Q257. Inking annotations not saving after presentation ends. RCA? [EASY]

**Answer:** Symptom: Ink drawings from Slide Show discarded. Root Cause: At end of Slide Show, PowerPoint

prompts 'Keep Ink Annotations?' — user clicked Discard. Steps: At presentation end, click Keep when prompted.

**Resolution:** Train presenters to click 'Keep' at end; alternatively export as PDF with annotations before closing.

### Q258. PowerPoint SmartArt conversion to shapes losing colors. RCA? [EASY]

**Answer:** Symptom: After converting SmartArt to shapes, colors reset to default. Root Cause: SmartArt colors

defined by theme variant; converted shapes inherit base theme fill, not SmartArt variant. Steps: Before converting, note exact colors (eyedropper), reapply after conversion. Resolution: Document colors before conversion; use Format Painter or theme color pickers to restore.

### Q259. Custom show feature not working as expected in kiosk mode. RCA? [TOUGH]

**Answer:** Symptom: Kiosk presentation jumping to wrong custom show. Root Cause: Action button linked to

wrong custom show name, or custom show order is incorrect. Steps: Insert→Action→Hyperlink to→Custom Show→verify correct show selected, check 'Show and return'. Resolution: Verify all action button links in Normal mode; test custom show flow before deployment.

### Q260. PowerPoint translation feature produces incorrect translations. RCA? [EASY]

**Answer:** Symptom: Review→Translate gives wrong language output. Root Cause: Incorrect target language

selected, or service uses machine translation with domain-specific terminology errors. Steps: Verify source/target language selection; use Translate Selected Text and review before applying. Resolution: Use as draft translation only; have human reviewer verify technical/legal content translations.

### Q261. Embedded fonts in PowerPoint not appearing on Linux/Mac PDF viewer. RCA? [TOUGH]

**Answer:** Symptom: Fonts substituted in PDF on non-Windows platform. Root Cause: PowerPoint embeds

Windows TrueType fonts; some PDF viewers on Linux/Mac use different font rendering. Steps: Use PDF/A-1b export option (though PPT PDF export is basic); use Acrobat PDF Maker for full font embedding compliance.

**Resolution:** Install Adobe Acrobat for robust PDF export; verify on target platform before distribution.

### Q262. PowerPoint slide show rehearsal timings not saving. RCA? [EASY]

**Answer:** Symptom: Rehearsed timings not applied. Root Cause: At end of rehearsal, 'Keep timing' dialog

declined; or Slide Show→Use Timings not enabled. Steps: Slide Show→Rehearse Timings→accept save at end; enable 'Use Timings' checkbox. Resolution: Accept timings after rehearsal; verify Slide Show→Use Timings is enabled for auto-advance.

### Q263. PowerPoint 'Insert Online Pictures' fails to load images. RCA? [TOUGH]

**Answer:** Symptom: Bing image search shows no results or error. Root Cause: (a) Bing Creative Commons

search API rate-limited, (b) Firewall blocking Bing image endpoints, (c) Microsoft account not signed in. Steps: Sign in to Microsoft account, check proxy/firewall settings, use Insert→Pictures from device as alternative.

**Resolution:** Whitelist Bing endpoints; use internal image library or SharePoint images as alternative source.

### Q264. PowerPoint Shared Review feature not available for all users. RCA? [TOUGH]

**Answer:** Symptom: Review sharing option missing for some users. Root Cause: Shared Review requires M365

subscription; review workflow may use older email-based review in older Office. Steps: Upgrade to M365; use modern co-authoring via SharePoint link instead of Shared Review. Resolution: Use SharePoint link sharing for collaborative review; use Comments pane for feedback.

### Q265. Animation pane shows animations in wrong order for slide. RCA? [EASY]

**Answer:** Symptom: Elements animate out of intended sequence. Root Cause: Animation order set in Animation

Pane doesn't match trigger expectations; parallel vs. sequential timing misconfigured. Steps: Open Animation Pane, drag animations to correct order, set start triggers (On Click, With Previous, After Previous) correctly.

**Resolution:** Carefully sequence in Animation Pane; preview (Shift+F5 on slide) frequently.

### Q266. Header in PowerPoint handout view showing wrong date. RCA? [EASY]

**Answer:** Symptom: Incorrect date in printed handout. Root Cause: 'Update Automatically' date type selected; or

fixed date not updated. Steps: View→Notes and Handouts→Header and Footer→change date type; set fixed date or adjust automatic format. Resolution: Set fixed date for static handouts; configure auto-date format to match locale for dynamic dates.

### Q267. Screen recording inserted in PowerPoint has no audio in playback. RCA? [EASY]

**Answer:** Symptom: Screen recording plays without audio. Root Cause: During recording, wrong audio input

device selected; microphone muted; or 'Do not record audio' option chosen. Steps: Re-record screen capture (Insert→Screen Recording) with correct audio device selected, verify microphone in Windows Sound settings.

**Resolution:** Select correct microphone before recording; check recording settings.

### Q268. Slide Show terminates prematurely with a black screen. RCA? [TOUGH]

**Answer:** Symptom: Presentation ends before last slide. Root Cause: (a) Final slide has auto-advance timing set,

(b) Escape key accidentally pressed, (c) Action button on an earlier slide linked to 'End Show'. Steps: Check slide timings, remove accidental End Show actions, verify Escape hasn't been programmed. Resolution: Review all action buttons and timings; use Rehearse Timings to catch premature endings.

### Q269. Custom slide size results in distorted content when switching from standard. RCA? [EASY]

**Answer:** Symptom: Elements stretched/squished after size change. Root Cause: When changing slide size,

'Maximize' option stretches content; 'Ensure Fit' shrinks it, both potentially distorting. Steps: Design→Slide Size→Custom→choose 'Ensure Fit' to avoid cropping, then manually adjust elements. Resolution: Change slide size early in design process before adding content; manually reposition after change.

### Q270. PowerPoint spell check misses errors in text boxes added as 'objects'. RCA? [EASY]

**Answer:** Symptom: Errors in some text boxes not caught. Root Cause: Text boxes inserted as drawing objects

with 'Do not check spelling' property, or language set to 'No proofing'. Steps: Select text→Review→Language→clear 'Do not check spelling'; set correct language. Resolution: Ensure all text boxes have correct language with proofing enabled; check per-object language settings.

---

## Section 6 — Outlook Troubleshooting — RCA Format — Q271 to Q340

### Q271. Outlook not receiving emails but can send. RCA? [EASY]

**Answer:** Symptom: Incoming mail stopped. Root Cause: (a) Send/Receive group disabled or interval set to 0, (b)

Outlook offline mode active, (c) Exchange mailbox quota reached, (d) Mail flow rule in Exchange redirecting mail.

**Steps:** Check Send/Receive→Work Offline toggle, check Send/Receive Groups, verify mailbox quota (admin),

check transport rules in EAC. Resolution: Enable online mode, fix quota by cleanup or increase, remove blocking transport rules.

### Q272. Outlook profile corrupted — cannot start 'Cannot open your default email folders'. RCA?

[TOUGH]

**Answer:** Symptom: Outlook fails to open. Root Cause: OST file corrupted, or profile registry entries damaged.

**Steps:** Run scanpst.exe (Inbox Repair Tool) on OST, rebuild Outlook profile (Control Panel→Mail→Show

Profiles→Add), recreate OST. Resolution: Delete OST and let Outlook rebuild it; if profile corrupt, create new Outlook profile.

### Q273. Outlook Focused Inbox not filtering correctly. RCA? [EASY]

**Answer:** Symptom: Important emails in Other tab; clutter emails in Focused. Root Cause: Machine learning

model for Focused Inbox hasn't learned user preferences, or training signals not applied. Steps: Move misplaced emails manually (right-click→Move to Focused/Other) to train the model; allow 2-3 weeks for adaptation.

**Resolution:** Consistently move emails to correct tab; Focused Inbox improves over time with user feedback.

### Q274. Outlook Search returns no results or incomplete results. RCA? [TOUGH]

**Answer:** Symptom: Outlook search finds nothing. Root Cause: (a) Windows Search index not built or paused, (b)

Outlook data file excluded from index, (c) Search restricted to current mailbox subfolder. Steps: Control Panel→Indexing Options→check Outlook included in index, rebuild index; check Outlook search scope (All Mailboxes). Resolution: Rebuild Windows Search index including Outlook; expand search scope to All Mailboxes.

### Q275. Outlook calendar appointments showing wrong time zone for attendees. RCA? [EASY]

**Answer:** Symptom: Meeting time offset by hours for recipients. Root Cause: Calendar item created in wrong time

zone;    Outlook   time  zone     mismatch      with     Windows     timezone    setting.    Steps:    Check File→Options→Calendar→Time Zone setting; for existing appointments, open and verify time zone in scheduling tab. Resolution: Sync Outlook time zone with Windows; use 'Time Zones' feature when scheduling cross-timezone meetings.

### Q276. Outlook autodiscover failing for new user setup. RCA? [TOUGH]

**Answer:** Symptom: 'Cannot connect to server' during profile creation. Root Cause: Autodiscover DNS record

missing/wrong, SRV record not configured, certificate mismatch, or Exchange Online Autodiscover not responding. Steps: Test with https://testconnectivity.microsoft.com (Autodiscover test), check DNS: autodiscover.domain.com CNAME → autodiscover.outlook.com. Resolution: Fix DNS records; for hybrid, ensure Autodiscover points to Exchange Online.

### Q277. Outlook attachments not opening — 'Cannot create file' error. RCA? [TOUGH]

**Answer:** Symptom: Error when opening attachment from Outlook. Root Cause: Temp folder for attachments

(OLK folder) is full; Outlook saves temporary attachment copies and old ones accumulate. Steps: Navigate to %temp%\Outlook              Temp         (or        find        OLK         path         in        registry: HKCU\Software\Microsoft\Office\x.0\Outlook\Security\OutlookSecureTempFolder), delete all files. Resolution: Clear OLK temp folder; automate cleanup via startup script.

### Q278. Emails stuck in Outbox not sending. RCA? [EASY]

**Answer:** Symptom: Messages stay in Outbox. Root Cause: (a) Large attachment exceeds send limit, (b) Outlook

in offline mode, (c) SMTP auth failure, (d) Corrupt outgoing message. Steps: Toggle Work Offline, check attachment size vs. org limit (25MB default), delete stuck message and resend. Resolution: Reduce attachment size, disable offline mode, send via OneDrive link instead of attachment.

### Q279. Outlook meeting invites not showing in calendar after accepting. RCA? [EASY]

**Answer:** Symptom: Accepted meeting invisible in calendar. Root Cause: (a) Tracking option not updating

calendar, (b) Calendar permissions issue in Exchange, (c) Add meeting to calendar option not checked. Steps: Check Default Response Settings (File→Options→Calendar→Tracking→Auto-Accept Meeting Requests).

**Resolution:** Enable 'Automatically accept meeting requests' or manually click 'Accept and Add to Calendar'.

### Q280. Outlook new email notification not appearing for specific folders. RCA? [EASY]

**Answer:** Symptom: No desktop alert for emails in subfolder. Root Cause: Desktop alerts only trigger for Inbox by

default; subfolder email bypasses desktop notification. Steps: Create an Outlook rule: apply to messages in that folder→'Display a Desktop Alert'. Resolution: Add alert action to existing rules for subfolders; consider Power Automate for advanced notifications.

### Q281. Outlook OST file growing too large and consuming disk space. RCA? [TOUGH]

**Answer:** Symptom: OST file is 50GB+, disk space low. Root Cause: Large mailbox with no archiving; Outlook

synchronizes all Exchange mailbox content locally. Steps: Enable Online Mode (reduces OST size), configure auto-archive, use cached mode with mail to keep for 1-3 months only. Resolution: Limit cached mode sync period (File→Account Settings→Data Files→limit mail to keep offline); enable Exchange Online Archiving.

### Q282. Outlook calendar sharing permissions not working correctly. RCA? [EASY]

**Answer:** Symptom: Delegate cannot see or edit calendar despite permissions. Root Cause: (a) Wrong calendar

permission level assigned, (b) Delegate seeing wrong calendar (not shared one), (c) Mobile device cache out of date. Steps: Calendar→Share Calendar→Properties→verify permission level (Editor/Reviewer), remove and re-add delegate, check from delegate's perspective. Resolution: Reassign correct permissions; have delegate remove and re-add the shared calendar.

### Q283. Outlook S/MIME encrypted email cannot be read by recipient. RCA? [TOUGH]

**Answer:** Symptom: Recipient gets encryption error. Root Cause: Recipient doesn't have sender's public

certificate installed; or sender's certificate issued by untrusted CA. Steps: Exchange public certificates via unencrypted email first; import certificate to recipient's trusted store. Resolution: Use Microsoft Purview Message Encryption (simpler) instead of S/MIME for external recipients.

### Q284. Outlook rule moves emails but also leaves copy in Inbox. RCA? [EASY]

**Answer:** Symptom: Emails duplicated — in both Inbox and target folder. Root Cause: Rule missing 'stop

processing more rules' action, causing a later rule to also act on the same message; or rule condition matches 'move' + another 'copy' action. Steps: Review all rules in order (Home→Rules→Manage Rules), add 'Stop processing more rules' to first matching rule. Resolution: Add Stop Processing action; audit all rules for conflicts.

### Q285. Outlook crashes when opening emails with inline images. RCA? [TOUGH]

**Answer:** Symptom: Crash specifically on image-rich emails. Root Cause: Graphics rendering conflict, corrupted

graphics driver, or specific image format causing GDI failure. Steps: Disable hardware graphics acceleration (File→Options→Advanced→Display→disable HW accel), update graphics drivers. Resolution: Disable hardware acceleration; update or roll back graphics driver; repair Office.

### Q286. Out of Office reply sending to external senders incorrectly. RCA? [TOUGH]

**Answer:** Symptom: OOF sent to external senders when set to internal only. Root Cause: Exchange transport

rule or policy overriding OOF scope setting, or user configured 'Everyone' instead of 'My organization only'.

**Steps:** File→Automatic Replies→verify 'My Organization' vs 'Everyone' setting; check Exchange OOF transport

rules in EAC. Resolution: Set to 'My Organization'; if still leaking, check Exchange transport rules and OOF policies.

### Q287. Outlook 'The operation failed. An object could not be found' error. RCA? [TOUGH]

**Answer:** Symptom: Error when performing various Outlook operations. Root Cause: Corrupt Outlook profile,

damaged OST, or missing Exchange connection. Steps: Run scanpst.exe, create new Outlook profile, check Exchange connectivity. Resolution: Rebuild Outlook profile; delete and recreate OST file.

### Q288. Emails flagged as spam despite sender being in Safe Senders list. RCA? [TOUGH]

**Answer:** Symptom: Trusted emails going to Junk. Root Cause: (a) Server-side spam filter (EOP/MDO) overrides

client-side safe senders, (b) SCL (Spam Confidence Level) from transport rule, (c) DMARC failure causing marking. Steps: Check EOP quarantine in Defender portal, review transport rules, check message headers for SCL and X-Forefront-Antispam-Report. Resolution: Add domain to tenant-level Allow list in Defender; for persistent issue, submit false positive report.

### Q289. Outlook calendar free/busy information not showing for external contacts. RCA? [TOUGH]

**Answer:** Symptom: Cannot see external meeting attendee availability. Root Cause: Organization federation with

external Exchange org not configured; or user is in non-Exchange system (Google Workspace). Steps: Check Organization→Federation Trust in Exchange; for non-Exchange, use 'Suggest a Time' manually. Resolution: Configure Exchange federation for free/busy sharing with partner domains.

### Q290. Outlook for iOS not syncing calendar with Exchange. RCA? [TOUGH]

**Answer:** Symptom: Calendar empty or outdated on mobile. Root Cause: (a) Mobile device MDM compliance

failure blocking access, (b) Conditional Access policy requiring managed device, (c) Account not configured correctly. Steps: Check Intune compliance status, verify Conditional Access policies allow mobile Outlook, reconfigure account on device. Resolution: Enroll device in Intune, remediate compliance issues, or configure CA exception for approved apps.

### Q291. Outlook Group email not delivered to all members. RCA? [EASY]

**Answer:** Symptom: Some M365 Group members not receiving group emails. Root Cause: (a) Member opted out

of group email subscription, (b) Member's mailbox quota full, (c) Group delivery settings restricted. Steps: Check M365 Group subscription settings (group page→subscription toggle), verify all members' mailbox quotas.

**Resolution:** Re-subscribe affected members to group email; increase mailbox quota for members with full

mailboxes.

### Q292. Outlook 'Delegate Access' permissions not working after mailbox migration. RCA? [TOUGH]

**Answer:** Symptom: Delegate lost access after migration. Root Cause: Delegate permissions stored in mailbox

attributes; migration may not preserve all ACL settings correctly. Steps: Re-add delegate permissions post-migration; check for orphaned SIDs in permission ACLs. Resolution: Reconstruct delegate permissions after migration; verify with Get-MailboxPermission PowerShell.

### Q293. Meeting request timezone displays incorrectly for recipients in different regions. RCA?

[EASY]

**Answer:** Symptom: 3 PM meeting shows as 3 AM for recipient. Root Cause: Organizer's Outlook time zone not

set correctly; meeting created in wrong time zone context. Steps: File→Options→Calendar→set correct time zone; use 'Add Time Zones' in meeting scheduling to verify. Resolution: Correct Outlook time zone; use Teams meeting for international meetings (auto time zone conversion).

### Q294. Outlook cached mode causing email version conflicts. RCA? [EASY]

**Answer:** Symptom: Replies based on outdated email version. Root Cause: In cached mode, Outlook reads from

local OST cache; server email updated but cache not refreshed. Steps: Press F9 (Send/Receive all), or switch to Online Mode temporarily. Resolution: Reduce sync frequency issues by ensuring reliable internet; for critical items, verify server version via OWA.

### Q295. Outlook email signature not appearing on mobile (Outlook iOS/Android). RCA? [EASY]

**Answer:** Symptom: Signature set on desktop not on mobile. Root Cause: Outlook desktop and mobile maintain

separate signature settings; no sync between them. Steps: Manually configure signature in Outlook Mobile: Settings→Signature. Resolution: Set signature on each device separately; Exchange/Intune cannot push desktop signatures to mobile Outlook directly.

### Q296. Outlook conversation threading showing unrelated emails together. RCA? [EASY]

**Answer:** Symptom: Emails from different senders grouped together incorrectly. Root Cause: Conversation

threading matches on Subject line only; Reply/Forward chains with same subject merge. Steps: Ungroup (View→Messages→Show as Conversations uncheck), or sort by Date. Resolution: Disable conversation view if confusion persists; educate users to change subjects for new topics.

### Q297. Outlook calendar permissions via PowerShell not showing in UI. RCA? [TOUGH]

**Answer:** Symptom: Permissions set via Set-MailboxFolderPermission not visible. Root Cause: Permissions may

be set on localized calendar folder name rather than 'Calendar'; or permission cached in client. Steps: Use Get-MailboxFolderPermission to verify, set on default calendar (:\Calendar), restart Outlook. Resolution: Use the English folder name 'Calendar' in PowerShell; restart Outlook after changes.

### Q298. Outlook cannot connect to Exchange on-premises after certificate renewal. RCA? [TOUGH]

**Answer:** Symptom: Cannot connect after cert renewal. Root Cause: New certificate not assigned to Exchange

services (SMTP, IIS), or certificate chain incomplete, or Autodiscover returning old certificate. Steps: Run Get-ExchangeCertificate, Enable-ExchangeCertificate -Services IIS,SMTP,IMAP on new cert; test with testconnectivity.microsoft.com. Resolution: Assign new certificate to all required Exchange services; update DNS if SAN names changed.

### Q299. Outlook Add-in (COM) crashes specific to one user. RCA? [TOUGH]

**Answer:** Symptom: Add-in crashes only for one user; others unaffected. Root Cause: User-specific profile data

or add-in state corrupted; or user has different add-in version. Steps: Disable add-in for affected user (File→Options→Add-ins→COM Add-ins), rebuild profile, reinstall add-in. Resolution: Rebuild Outlook profile for affected user; clear add-in configuration registry keys.

### Q300. Outlook cannot open shared mailbox in new window. RCA? [EASY]

**Answer:** Symptom: 'Open in New Window' option not available or errors. Root Cause: Shared mailbox

auto-mapped but Full Access permission not granted; or Outlook not in Exchange Online mode. Steps: Grant Full Access via Add-MailboxPermission; allow auto-mapping; or add as secondary account manually. Resolution: Grant Full Access permission; wait 30 min for propagation; restart Outlook.

### Q301. Outlook for Mac not syncing with Exchange on-premises. RCA? [TOUGH]

**Answer:** Symptom: Mac Outlook stale or disconnected from on-prem Exchange. Root Cause: (a) Modern

authentication required but not enabled on Exchange, (b) Certificate not trusted on Mac, (c) EWS not enabled.

**Steps:** Verify Exchange EWS endpoint, trust SSL certificate on Mac, enable Modern Auth on Exchange 2016+

(Set-OrganizationConfig -OAuth2ClientProfileEnabled $true). Resolution: Enable Modern Auth on Exchange; add cert to Mac Keychain trust store.

### Q302. Distribution list not expanding correctly in Outlook. RCA? [EASY]

**Answer:** Symptom: Reply All to DL sends to wrong/incomplete set of recipients. Root Cause: (a) DL uses

cached membership from Outlook's offline GAL, (b) DL has nested DLs not expanded, (c) External members excluded by policy. Steps: Press F9 to update offline GAL, check DL membership in Exchange Admin Center.

**Resolution:** Force GAL update, verify DL membership in EAC, ensure external recipients included if allowed.

### Q303. Outlook email tracking (read receipts) not working. RCA? [EASY]

**Answer:** Symptom: Read receipts not returned. Root Cause: Recipient's Outlook configured to never send read

receipts; Exchange policy blocks read receipts; recipient uses web mail. Steps: Verify Request Read Receipt on sent email; advise recipient to configure Read Receipt response (Outlook→Options→Mail→Tracking).

**Resolution:** Understand that read receipts require recipient cooperation; consider alternative delivery

confirmation methods.

### Q304. Outlook categories not syncing across devices. RCA? [TOUGH]

**Answer:** Symptom: Categories set on desktop missing on mobile/OWA. Root Cause: Master category list stored

in registry and synchronized via Exchange only for some clients; not all clients support full category sync. Steps: For Exchange/M365, categories sync via server; mobile apps may have limited category display. Resolution: Use OWA to verify server categories; understand that mobile Outlook category support varies by version.

### Q305. Users cannot reply to emails in shared mailbox via Outlook. RCA? [TOUGH]

**Answer:** Symptom: Error or wrong 'From' address when replying. Root Cause: 'Send As' or 'Send on Behalf'

permission not granted; Outlook not configured to send from shared mailbox address. Steps: Grant Send As permission: Add-RecipientPermission, allow 30 min. In Outlook, add shared mailbox as account (not just open) for full Send As. Resolution: Grant Send As permission; configure Outlook to show shared mailbox as separate account.

### Q306. Outlook meeting room not auto-accepting bookings. RCA? [TOUGH]

**Answer:** Symptom: Room calendar doesn't auto-accept requests. Root Cause: Resource mailbox AutoAccept

not enabled, or booking delegate configured. Steps: Set-CalendarProcessing -Identity room@domain.com -AutomateProcessing AutoAccept. Resolution: Configure room mailbox with AutomateProcessing=AutoAccept via PowerShell.

### Q307. Outlook new email sound not playing despite being enabled. RCA? [EASY]

**Answer:** Symptom: No sound for new emails. Root Cause: (a) Windows sound scheme has no sound for 'New

Mail Notification', (b) Outlook notification sounds disabled in Windows settings, (c) Application volume muted.

**Steps:** Control Panel→Sound→Sounds tab→find 'New Mail Notification' assign sound, check Windows Volume

Mixer for Outlook. Resolution: Assign sound in Windows Sound scheme; unmute Outlook in volume mixer.

### Q308. Outlook email export to PST fails midway. RCA? [TOUGH]

**Answer:** Symptom: Export wizard stops with error. Root Cause: (a) Corrupted mailbox items in range, (b)

Insufficient disk space for PST, (c) PST file path has special characters. Steps: Export in smaller batches (by date range), check disk space, use simple path (C:\export.pst). Resolution: Export in date-range batches; ensure 2x mailbox size in free disk space; use simple file paths.

### Q309. Outlook Quick Steps not working after profile migration. RCA? [TOUGH]

**Answer:** Symptom: Quick Steps errors after moving to new machine. Root Cause: Quick Steps stored in registry

(HKCU\Software\Microsoft\Office\16.0\Outlook\) and not exported during profile migration. Steps: Export Quick Steps registry key from old machine, import on new machine. Resolution: Include Quick Steps registry export in migration checklist; recreate if registry unavailable.

### Q310. Recurring Outlook meeting series shows outdated information for some instances. RCA?

[EASY]

**Answer:** Symptom: One occurrence has old time/location. Root Cause: Single instance was individually edited

before master series update; individual exceptions created in calendar. Steps: Delete exception and open master series to update; or open specific occurrence and update manually. Resolution: For series-wide changes, always edit the master series; track exceptions in meeting notes.

### Q311. Outlook People/Contacts not syncing from Exchange Global Address List. RCA? [EASY]

**Answer:** Symptom: GAL contacts not appearing in People hub. Root Cause: GAL is directory service, not stored

in Personal Contacts; Outlook accesses GAL separately from local contacts. Steps: Type name in To: field for GAL lookup; use Ctrl+Shift+B to open Address Book. Resolution: Educate users: GAL ≠ local contacts; use Address Book for GAL, Contacts for personal entries.

### Q312. Outlook Task reminders not appearing at set time. RCA? [EASY]

**Answer:** Symptom: Task reminders silent. Root Cause: (a) Reminder dialog dismissed earlier and not reset, (b)

Outlook not running at reminder time, (c) Reminder set for wrong date/time zone. Steps: Check Task→Reminder checkbox, verify date/time, keep Outlook running in background or use mobile notifications. Resolution: Enable task reminders; use Teams task (Planner/To Do) for cross-platform reminder support.

### Q313. Emails with ZIP attachments blocked by Exchange. RCA? [TOUGH]

**Answer:** Symptom: Attachments stripped from emails. Root Cause: Exchange attachment filtering policy blocks

.zip files (default security configuration); anti-malware policy quarantines. Steps: Check EAC→Mail Flow→Rules for attachment blocking, check Defender for Office 365 anti-malware policies. Resolution: Whitelist specific ZIP attachments by sender, or use SharePoint link instead of email attachment.

### Q314. Outlook online archive not accessible in cached mode. RCA? [EASY]

**Answer:** Symptom: In-place archive not visible. Root Cause: Online Archive not cached locally (by design —

archive uses Online mode). When Outlook in cached mode, archive available but requires online connection.

**Steps:** Verify archive enabled in Exchange (Get-Mailbox -Archive), ensure internet connection, check archive

appears in Outlook navigation pane. Resolution: Ensure stable connection; the archive always operates in online mode — this is expected behavior.

### Q315. Email delayed delivery via 'Defer delivery' option arrived immediately. RCA? [EASY]

**Answer:** Symptom: Message sent immediately despite delay setting. Root Cause: Outlook must remain open for

deferred delivery to work; if Outlook closed before scheduled time, email sends immediately when Outlook next opens. Steps: Keep Outlook open until scheduled delivery time; verify with Outbox check. Resolution: Keep Outlook running; consider Power Automate for reliable scheduled email sending.

### Q316. Outlook Rules stopped working after mailbox moved to Exchange Online. RCA? [TOUGH]

**Answer:** Symptom: Rules created on-prem not executing in Exchange Online. Root Cause: On-premises

client-side rules not migrated to server-side rules in Exchange Online. Steps: In Exchange Online Outlook, go to File→Manage Rules & Alerts→review which rules are client-only vs server-side. Resolution: Recreate rules in Exchange Online; prefer server-side rules (marked without client icon) for reliability across devices.

### Q317. Outlook shows duplicate calendar events after migration. RCA? [TOUGH]

**Answer:** Symptom: Each calendar entry appears twice. Root Cause: Calendar synced from both Exchange

Online and old on-premises account still connected; or Outlook profile connected to both endpoints. Steps: Remove old Exchange on-premises account from Outlook profile; keep only Exchange Online account.

**Resolution:** Update Outlook profile to connect only to Exchange Online post-migration.

### Q318. Outlook IMAP account showing 'Disconnected' status intermittently. RCA? [EASY]

**Answer:** Symptom: IMAP connection drops repeatedly. Root Cause: (a) Server idle timeout, (b) Antivirus

scanning port 993, (c) Unstable internet connection, (d) ISP blocking IMAP. Steps: Update IMAP server settings, disable AV IMAP scan, check firewall port 993 (IMAPS), increase keep-alive interval. Resolution: Configure IMAP keep-alive, whitelist IMAP in AV, ensure port 993 open.

### Q319. Outlook cannot add room mailbox to recurring Teams meeting. RCA? [TOUGH]

**Answer:** Symptom: Error when adding room to Teams recurring meeting. Root Cause: Room booking policy

blocks recurring meetings beyond a certain number of days in advance or duration limit. Steps: Check room booking    policy:    Get-CalendarProcessing   -Identity   room;    adjust    MaximumDurationInMinutes, BookingWindowInDays. Resolution: Increase booking window: Set-CalendarProcessing -BookingWindowInDays 365.

### Q320. Outlook contacts autocomplete suggesting wrong email addresses. RCA? [EASY]

**Answer:** Symptom: Autocomplete selects old/invalid email. Root Cause: NK2/autocomplete cache (stored in

roaming profile or Exchange cache) has outdated entries. Steps: Delete specific entry by highlighting in autocomplete list and pressing Delete key, or clear all (File→Options→Mail→Clear Auto-Complete List).

**Resolution:** Clear autocomplete list; maintain accurate contacts in Exchange GAL.

### Q321. Outlook emails not loading images (only showing red X placeholders). RCA? [EASY]

**Answer:** Symptom: Inline images not displaying. Root Cause: (a) 'Don't download pictures' security option

enabled, (b) Images hosted on external server blocked by firewall, (c) Image URL contains tracking parameter blocked by policy. Steps: Right-click on red X → Download Pictures; File→Options→Trust Center→Automatic Download→uncheck 'Don't download'. Resolution: Adjust automatic download settings; add trusted senders to Safe Senders list.

### Q322. Outlook online (OWA) not loading in specific browser. RCA? [EASY]

**Answer:** Symptom: OWA blank or error in Chrome/Edge but works in another browser. Root Cause: Browser

extension interfering (ad blocker, uBlock, corporate extension), cache corruption, or cookie issue. Steps: Open in InPrivate/Incognito mode, disable extensions, clear browser cache/cookies. Resolution: Disable blocking extensions for OWA domain, clear cache, add OWA to trusted sites.

### Q323. Forwarding rule to external email not working in Exchange Online. RCA? [TOUGH]

**Answer:** Symptom: Auto-forward to Gmail/Yahoo fails. Root Cause: Exchange Online default anti-spam policy

blocks automatic forwarding to external domains (Anti-Spam Outbound Policy). Steps: Check anti-spam outbound policy in Defender portal→email policies→outbound→automatic forwarding=Off. Resolution: Enable per-user or per-domain forwarding exception in outbound policy; or use mailbox forwarding (Set-Mailbox -ForwardingAddress) which may be exempt.

### Q324. Outlook 'You don't have permission to create an entry in this folder' error in shared calendar.

RCA? [EASY]

**Answer:** Symptom: Cannot create appointments in shared calendar. Root Cause: Calendar permission level is

'Reviewer' (read-only) instead of 'Editor' or 'Author'. Steps: Calendar owner → right-click calendar → Sharing and Permissions → increase permission to Editor. Resolution: Grant Editor or higher permission to the user needing to create appointments.

### Q325. Outlook meeting invitation body text missing when opened by recipient. RCA? [EASY]

**Answer:** Symptom: Meeting invite arrives with empty body. Root Cause: Meeting body created in HTML with

inline CSS not supported by recipient's email client, or message size limit trimming the body. Steps: Resend with plain text body, check message size limits, test in OWA. Resolution: Use plain text or standard HTML formatting; check if message truncated by size limit.

### Q326. Outlook Search Folders showing incorrect unread count. RCA? [TOUGH]

**Answer:** Symptom: Search Folder shows 50 unread but folder appears empty. Root Cause: Search Folder

criteria include subfolders or hidden items; items marked read at item level but folder not refreshed. Steps: Right-click Search Folder→Update Count/Customize Search Folder to verify scope. Resolution: Verify search folder criteria, exclude deleted items folder; rebuild search index.

### Q327. Outlook 2019 prompts for credentials repeatedly despite saved password. RCA? [TOUGH]

**Answer:** Symptom: Password prompt every startup. Root Cause: (a) Credential Manager storing wrong

credentials, (b) Modern Auth not enabled for legacy Outlook, (c) Conditional Access blocking Basic Auth. Steps: Control Panel→Credential Manager→remove all Outlook entries, re-enter credentials; enable Modern Auth for Exchange Online. Resolution: Enable Modern Auth (Disable Basic Auth); update to M365 Apps which supports Modern Auth natively.

### Q328. Calendar overlay view showing incorrect appointments for shared calendar. RCA? [EASY]

**Answer:** Symptom: Overlaid calendar shows wrong events. Root Cause: Cached view showing stale shared

calendar data; shared calendar permissions changed recently. Steps: Close and reopen shared calendar in Outlook, press F9 to sync, verify permissions still valid. Resolution: Refresh shared calendar; remove and re-add shared calendar to view; verify permissions.

### Q329. Outlook email threading shows replies to different threads merged incorrectly. RCA? [EASY]

**Answer:** Symptom: Different threads merged into one conversation. Root Cause: Subject line identical; Outlook

groups by subject in conversation view. Steps: Disable Conversation View (View→Messages→uncheck Show as Conversations); or change subject slightly for new threads. Resolution: Use unique subjects per topic; disable conversation view if confusion persists.

### Q330. Outlook Sync Error folder accumulating errors. RCA? [TOUGH]

**Answer:** Symptom: Sync Errors folder growing with many error entries. Root Cause: Cached mode sync

conflicts between OST and Exchange; usually temporary network issues or item-level conflicts. Steps: Review errors (usually can be deleted), check for recurring patterns (specific items causing repeated errors), run Outlook Connectivity Test. Resolution: Delete sync error items, rebuild OST if errors persist, ensure stable network connection.

### Q331. Outlook emails from specific sender always landing in Junk despite whitelist. RCA? [TOUGH]

**Answer:** Symptom: Whitelisted sender still in Junk. Root Cause: Server-side EOP anti-spam policy overriding

client Safe Senders list; DMARC/DKIM failure on sender domain. Steps: Check message headers for X-Forefront-Antispam-Report SCL score, submit as Not Junk in Defender portal, check sender's email authentication. Resolution: Add to tenant Allow list in Defender portal (not just client Safe Senders); sender needs to fix email authentication.

### Q332. Email recall failing for message already read by recipient. RCA? [EASY]

**Answer:** Symptom: Recall notification says 'recall failed'. Root Cause: Recall only works if recipient hasn't

opened the email and both are on Exchange Online. If opened, read, or using non-Exchange client, recall fails.

**Steps:** Recall: Home→More Commands→Actions→Recall. Check if recipient on Exchange Online and if they've

read it. Resolution: Recall is unreliable; send a follow-up correction email; recall cannot be guaranteed.

### Q333. Outlook meeting polls (FindTime/Bookings with Me) not available. RCA? [EASY]

**Answer:** Symptom: Poll option missing from Outlook. Root Cause: FindTime add-in not installed; or 'Bookings

with Me' requires Microsoft Bookings license (M365 Business or E3+). Steps: Install FindTime from AppSource; verify Bookings license. Resolution: Install appropriate add-in; ensure correct licensing for Bookings with Me.

### Q334. Outlook desktop app not reflecting email read/unread status from mobile. RCA? [EASY]

**Answer:** Symptom: Emails marked read on mobile still show as unread on desktop. Root Cause: Cached mode

OST not synced; or Exchange sync delay between clients. Steps: Press F9 in Outlook, check internet connection, switch to Online Mode temporarily. Resolution: Press F9 to force sync; ensure both clients connected to Exchange; wait for sync propagation.

### Q335. Outlook for Android unable to add Exchange account — MDM enrollment required. RCA?

[TOUGH]

**Answer:** Symptom: 'Enrollment required' error on account add. Root Cause: Conditional Access policy requires

compliant/managed device; device not enrolled in Intune/MDM. Steps: Enroll device in Intune via Company Portal app, then retry account setup. Resolution: Complete Intune enrollment; if personal device, use MAM-only policy (no enrollment) if configured.

### Q336. Outlook data file .pst size limit causing 'The file is full' error. RCA? [TOUGH]

**Answer:** Symptom: Cannot receive/send email; PST full error. Root Cause: PST file reached default size limit

(50GB for ANSI PST = 2GB; Unicode PST = 50GB); or reached configured max. Steps: Compact PST (Account Settings→Data Files→Settings→Compact Now), archive older mail, increase PST limit via registry (MaxLargeFileSize). Resolution: Archive old emails, compact PST, switch to Exchange Online to eliminate PST dependency.

### Q337. OWA web app not displaying inline images in received email. RCA? [EASY]

**Answer:** Symptom: Red X or blank where images should be. Root Cause: External image blocked by OWA's

'Block external content' setting, or image referenced via HTTP (not HTTPS) blocked by browser. Steps: OWA Settings→Mail→Message Handling→uncheck block external images. Resolution: Adjust OWA image download setting; or use trusted sender override per email.

### Q338. Outlook voting buttons not appearing in received email. RCA? [EASY]

**Answer:** Symptom: No voting buttons visible for recipient. Root Cause: (a) Recipient using OWA or non-Outlook

client (voting buttons only work in full Outlook desktop), (b) Message forwarded (strips voting functionality).

**Steps:** Open email in desktop Outlook, not OWA; do not forward voting emails. Resolution: Voting buttons

require both sender and recipient using Outlook desktop with Exchange; use Microsoft Forms as a cross-platform alternative.

### Q339. Outlook PST password removal needed after password was forgotten. RCA? [TOUGH]

**Answer:** Symptom: PST password unknown; data inaccessible. Root Cause: PST password protection applied

and credentials lost. Steps: Use third-party PST password recovery tools (AOPR, PassFab for Outlook) — PST uses weak 32-bit hash easily cracked. Resolution: Recover password with dedicated tool; improve password management; consider PKI/enterprise solutions for PST security.

### Q340. Outlook meeting organizer changed after mailbox migration. RCA? [TOUGH]

**Answer:** Symptom: Meetings show different organizer after migration. Root Cause: During cross-tenant or

cross-forest migration, organizer attribution stored in calendar item may not update for existing meetings; new email address differs. Steps: Resend meeting invites from new account; instruct attendees to accept again.

**Resolution:** Post-migration, recreate recurring meetings from new address; communicate change to attendees.

---

## Section 7 — Microsoft Teams Troubleshooting — RCA Format — Q341

### Q341. Microsoft Teams cannot make or receive calls — status shows 'Unknown'. RCA? [TOUGH]

**Answer:** Symptom: Calls not working; status unknown. Root Cause: (a) Teams Phone license not assigned, (b)

SIP trunk failure in Direct Routing, (c) Network firewall blocking Teams media ports (UDP 3478-3481, 50000-59999). Steps: Verify Phone System license, check SBC connectivity for Direct Routing, run Teams Network Assessment Tool. Resolution: Assign Phone System license; fix SBC/SIP trunk; open required firewall ports.

### Q342. Teams meeting video freezing or poor quality for all participants. RCA? [TOUGH]

**Answer:** Symptom: Video choppy/frozen. Root Cause: Network bandwidth insufficient, packet loss, or Teams

media server congestion. Steps: Run Teams Network Assessment Tool, check bandwidth (Teams needs 1.5Mbps per HD stream), check for VPN bottleneck. Resolution: Upgrade bandwidth, use split-tunnel VPN for Teams, enable Teams QoS (DSCP marking), configure network for Teams media.

### Q343. Teams chat messages not loading — spinning loader. RCA? [EASY]

**Answer:** Symptom: Chat panel stuck loading. Root Cause: (a) Teams cache corrupted, (b) Azure AD token

expired, (c) M365 service degradation. Steps: Clear Teams cache (%appdata%\Microsoft\Teams\clear all except settings.json), sign out and back in, check M365 service health. Resolution: Clear cache, sign out/in; if service issue, wait for Microsoft resolution.

### Q344. Teams meeting recording not available after meeting ends. RCA? [TOUGH]

**Answer:** Symptom: Recording not in chat or Stream. Root Cause: (a) Recording went to SharePoint/OneDrive

but permissions missing, (b) Meeting policy doesn't allow recording, (c) Compliance hold delaying processing.

**Steps:** Check Teams Admin Center→Meeting Policies→Allow cloud recording; check SharePoint Recordings

folder permissions; wait up to 24 hours for processing. Resolution: Enable cloud recording in policy; grant access to Recordings folder in SharePoint.

### Q345. Users cannot join a Teams meeting from external (non-tenant) account. RCA? [EASY]

**Answer:** Symptom: External attendees get 'meeting not found' or lobby stuck. Root Cause: (a) External access

disabled for external domains, (b) Anonymous meeting join disabled, (c) Lobby policy requiring organizer admission. Steps: Teams Admin→External Access; allow external domains; Meetings→Meeting Policies→Allow anonymous users. Resolution: Enable external access and anonymous join; adjust lobby settings in meeting policy.

### Q346. Teams app crashing on Windows startup. RCA? [EASY]

**Answer:** Symptom: Teams crashes immediately after auto-start. Root Cause: Corrupted Teams installation,

incompatible GPU driver causing rendering crash, or user profile issue. Steps: Clear cache (%appdata%\Microsoft\Teams), reinstall Teams, check GPU driver. Resolution: Clear cache; if persists, uninstall/reinstall Teams; update GPU driver.

### Q347. Teams Channels not showing in left panel for some members. RCA? [EASY]

**Answer:** Symptom: Team channels invisible for certain users. Root Cause: (a) User is a guest (limited channel

visibility), (b) Private channel — user not added, (c) User left/hidden the channel. Steps: Check if channel is standard vs private; for private channels verify membership; user can restore hidden channels via 'Hidden channels'. Resolution: Add user to private channel; guide user to unhide channel.

### Q348. Teams status not updating from 'Away' despite user being active. RCA? [EASY]

**Answer:** Symptom: Status stuck on Away. Root Cause: (a) Computer locked/screensaver triggered causing

Away status, (b) Teams detects no keyboard/mouse activity, (c) App not detecting activity due to VDI/thin client issues. Steps: Move mouse periodically, check power settings (disable screensaver), set Teams status manually.

**Resolution:** Adjust Windows power/screensaver settings; set custom status in Teams; report to IT if VDI causes

persistent issue.

### Q349. Teams private channel cannot be created — option missing. RCA? [EASY]

**Answer:** Symptom: 'Private channel' option absent. Root Cause: Teams policy restricts private channel creation;

user doesn't have team owner or creator permission. Steps: Teams Admin→Teams Policies→check 'Allow private channel creation'; verify user's team role. Resolution: Enable private channel creation in Teams policy; ensure user is team member (owners can create private channels).

### Q350. Teams meeting transcription showing wrong names for speakers. RCA? [TOUGH]

**Answer:** Symptom: Transcription attributes speech to wrong person. Root Cause: Speaker identification requires

voice profile enrollment (Teams Intelligent Recap); noisy environment or similar voices cause misattribution.

**Steps:** Enroll voice profiles (Teams Admin→Voice recognition); improve meeting audio quality. Resolution: Enroll

voice profiles; use directional microphones; correct transcript manually post-meeting.

### Q351. Teams file sharing in chat showing 'You don't have access to this file'. RCA? [EASY]

**Answer:** Symptom: File link works for sender but not recipient. Root Cause: File shared from personal OneDrive

retains personal permissions; recipient not explicitly granted access. Steps: Sender should verify sharing link type (specific people vs anyone with link), reshare with 'Anyone with the link' or add recipient explicitly.

**Resolution:** Sender should check file permissions; use 'Share' with explicit recipients or 'Anyone with link' for

broader access.

### Q352. Teams Live Events reaching attendee limit. RCA? [TOUGH]

**Answer:** Symptom: Attendees cannot join live event at capacity. Root Cause: Live Events limit (10,000

attendees standard, 100,000 with extended limit). Exceeding capacity blocks new joins. Steps: Request increased capacity via M365 portal for qualifying events; consider Town Hall (Teams premium) instead.

**Resolution:** Use Teams Town Hall for up to 20,000 attendees; request event capacity increase for Live Events.

### Q353. Teams bot not responding in channel after installation. RCA? [TOUGH]

**Answer:** Symptom: @mentioning bot gets no response. Root Cause: (a) Bot service down or throttled, (b) Bot

not configured for channel scope (only personal/group), (c) Messaging endpoint unreachable. Steps: Check bot health in Azure Portal→Bot Service, verify scope in Teams app manifest, test bot in personal chat. Resolution: Fix bot service endpoint, ensure channel scope in manifest, update bot registration.

### Q354. Teams app not available in specific countries due to compliance. RCA? [TOUGH]

**Answer:** Symptom: Teams features restricted in certain regions. Root Cause: Data residency and compliance

requirements restrict certain Teams features in specific geographies (China, Russia). Steps: Check M365 International Availability page for Teams feature availability by region. Resolution: Configure data residency in M365 Admin if available; use feature alternatives; comply with local data regulations.

### Q355. Teams shared channels not syncing membership with external tenant. RCA? [TOUGH]

**Answer:** Symptom: External tenant members not visible in shared channel. Root Cause: B2B Direct Connect not

configured between tenants; cross-tenant access settings not aligned. Steps: Azure AD→External Identities→Cross-tenant access→configure Direct Connect for Teams shared channels with partner tenant.

**Resolution:** Configure Direct Connect in Entra ID cross-tenant access settings for both tenants.

### Q356. Teams auto-answer for calls not working on specific device. RCA? [TOUGH]

**Answer:** Symptom: Calls ring instead of auto-answering. Root Cause: Auto-answer requires Teams IP phone or

certified device; software Teams app doesn't support auto-answer the same way; Survivability mode affects behavior. Steps: Enable auto-answer in Teams Admin→Phones→Configuration Profile, or device-level settings.

**Resolution:** Configure auto-answer on Teams-certified IP phone via Teams Admin configuration profile.

### Q357. Teams meeting recording missing subtitles/captions. RCA? [TOUGH]

**Answer:** Symptom: No captions in recorded video. Root Cause: Live captions are generated in real-time but may

not be automatically embedded in recording; requires transcription policy. Steps: Teams Admin→Meeting Policies→enable Allow transcription; start transcription during meeting. Resolution: Enable transcription in policy; start transcription during meeting to generate recording with captions.

### Q358. Teams app shows outdated organization chart in People app. RCA? [EASY]

**Answer:** Symptom: Org chart missing recent hires or shows wrong reporting structure. Root Cause: Azure AD

user profiles (Manager attribute) not updated for new employees; sync delay from HR to Azure AD. Steps: Update Manager attribute in Azure AD/Entra ID for affected users; verify HR system→AD sync (via Azure AD Connect or cloud sync). Resolution: Update user manager attribute in Azure AD; sync from HR system.

### Q359. Teams Calling Plan calls failing with 'User not enabled for Enterprise Voice'. RCA? [TOUGH]

**Answer:** Symptom: Cannot make PSTN calls. Root Cause: User missing Phone System license, missing Calling

Plan assignment, or phone number not assigned. Steps: Verify in Teams Admin→Users: Phone System license, Calling Plan, assigned phone number (Get-CsOnlineUser check). Resolution: Assign Phone System + Calling Plan licenses; assign phone number via Teams Admin Center.

### Q360. Teams notification badges not clearing after reading messages. RCA? [EASY]

**Answer:** Symptom: Red badge persists after viewing messages. Root Cause: (a) Notification from a channel tab

(not chat) not marked read, (b) @mention not explicitly viewed, (c) Mobile app badge not synced. Steps: Go to Activity feed→mark all as read; check each notification type. Resolution: Use 'Mark all as read' in Activity; disable badge for specific notification types in Teams settings.

### Q361. Teams meeting lobby holding all external attendees despite policy. RCA? [EASY]

**Answer:** Symptom: All external users stuck in lobby even for trusted organization. Root Cause: Meeting-level

settings override admin policy; organizer didn't set lobby bypass; per-meeting 'Who can bypass the lobby' overrides tenant default. Steps: Organizer → meeting options → 'Who can bypass the lobby?' → set to appropriate level. Resolution: Change per-meeting lobby settings; update Teams Admin meeting policy to set appropriate tenant-level default.

### Q362. Teams tenant move affecting availability during migration window. RCA? [TOUGH]

**Answer:** Symptom: Teams unavailable for hours during M365 tenant region move. Root Cause: M365 geo

migration for Teams includes data move that requires maintenance window. Steps: Inform users of scheduled maintenance window; plan migration during off-hours. Resolution: Communicate migration schedule; plan for 2-6 hour Teams unavailability; ensure business continuity plan in place.

### Q363. Teams channel tab (SharePoint page) shows 'Something went wrong'. RCA? [EASY]

**Answer:** Symptom: SharePoint tab in Teams channel errors. Root Cause: (a) SharePoint site deleted or

permissions changed, (b) Tab configured for a different SharePoint environment, (c) Token refresh failure. Steps: Verify SharePoint site exists and user has access, remove and re-add tab, sign out/in to Teams. Resolution: Fix SharePoint permissions; remove and reconfigure tab; clear Teams cache.

### Q364. Teams meeting poll (Forms) results not showing for attendees. RCA? [EASY]

**Answer:** Symptom: Poll created but participants can't see it. Root Cause: Poll added to meeting but not

launched; or Forms poll in Meeting Chat not sent properly. Steps: During meeting, open Forms tab → click Launch for participants to see; check if Forms permissions allow responses. Resolution: Launch poll explicitly during meeting; ensure all attendees have Forms access.

### Q365. Teams Rooms device not joining meeting automatically. RCA? [TOUGH]

**Answer:** Symptom: Room device misses auto-join for scheduled meeting. Root Cause: (a) Teams Rooms app

not updated, (b) Account credentials expired, (c) MTR (Microsoft Teams Room) account not licensed properly.

**Steps:** Check Teams Rooms app version (should be current), verify MTR account password not expired, verify

Teams Rooms license (Teams Rooms Basic/Pro). Resolution: Update Teams Rooms app; reset MTR account password; assign Teams Rooms license.

### Q366. Teams Viva Insights (personal insights) not loading. RCA? [EASY]

**Answer:** Symptom: My Analytics/Viva Insights tab blank. Root Cause: (a) Viva Insights license not assigned, (b)

User opted out of insights, (c) Privacy policy not accepted. Steps: Verify Viva Insights license in M365 Admin; check user settings in Insights (Settings→Opt out). Resolution: Assign Viva Insights license; ensure user hasn't opted out; accept privacy terms.

### Q367. Teams app switching between accounts drops ongoing meeting. RCA? [TOUGH]

**Answer:** Symptom: Meeting disconnects when switching accounts in Teams. Root Cause: Teams desktop app

supports multi-account but switching context while in meeting drops the active call due to audio device reallocation. Steps: Use Teams on browser for second account during meeting while keeping desktop for primary meeting. Resolution: Use different Teams clients (desktop + browser) for simultaneous meetings on different accounts.

### Q368. Teams search not finding messages from more than 30 days ago. RCA? [TOUGH]

**Answer:** Symptom: Old messages not appearing in search. Root Cause: Teams search indexes messages up to

30-90 days in standard; Compliance search via Purview required for older records. Steps: Use Microsoft Purview Content Search for older Teams messages (requires E3/E5 compliance). Resolution: Use Purview eDiscovery for historical message search; Teams search is limited to recent messages by design.

### Q369. Teams meeting recording upload to OneDrive failing for guest organizers. RCA? [TOUGH]

**Answer:** Symptom: Guest organizer's meeting recordings not saving. Root Cause: Guest accounts don't have

OneDrive license; recording destination requires organizer to have OneDrive storage. Steps: Set recording policy to save to organizer's designated internal storage, or change meeting organizer to an internal user with OneDrive. Resolution: Assign internal co-organizer; recordings save to internal user's OneDrive/SharePoint.

### Q370. Teams cannot play video in meetings from screen share (black screen). RCA? [TOUGH]

**Answer:** Symptom: Screen shared video appears black to participants. Root Cause: Hardware acceleration

DRM prevents screen capture of protected content (Netflix, etc.); standard screen share captures display but DRM blocks. Steps: Use 'Share window' instead of 'Share screen'; disable GPU hardware acceleration in Teams settings. Resolution: Disable hardware acceleration in Teams (Settings→General→Disable GPU acceleration); use video sharing within Teams if available.

### Q371. Teams App policies blocking users from installing personal apps. RCA? [EASY]

**Answer:** Symptom: Users cannot add apps to Teams. Root Cause: Teams App Setup Policy or App Permission

Policy restricts app installation for user group. Steps: Teams Admin→Apps→Permission policies→check user's assigned policy for allowed apps. Resolution: Update app permission policy to allow required apps; assign correct policy to users.

### Q372. Teams guest users cannot access Files tab in Teams channel. RCA? [EASY]

**Answer:** Symptom: File tab blank or error for guest. Root Cause: Guest access to SharePoint underlying the

Teams   channel   restricted;  SharePoint      site  external   sharing  disabled.   Steps:   SharePoint Admin→site→Sharing→set to 'Existing guests' or higher; verify Teams guest settings in Azure AD. Resolution: Enable external sharing on SharePoint site; ensure Teams guest access enabled in Teams Admin.

### Q373. Teams PSTN call quality degraded for remote workers on VPN. RCA? [TOUGH]

**Answer:** Symptom: Poor audio quality on calls via VPN. Root Cause: VPN hairpinning forces Teams media

through corporate network; introduces latency, jitter, and packet loss. Steps: Implement VPN split tunneling for Teams media endpoints (Office 365 IPs). Resolution: Configure split tunnel VPN: Teams Optimize-marked IP ranges bypass VPN. Follow Microsoft's VPN split tunnel guidance.

### Q374. Teams external access blocked for specific partner domain. RCA? [EASY]

**Answer:** Symptom: Cannot chat/call users from partner company. Root Cause: External access configured to

block specific domains, or partner's tenant has blocked your domain. Steps: Teams Admin→External Access→verify domain not in blocked list; contact partner to verify their settings. Resolution: Remove domain from block list; coordinate with partner to allow your domain.

### Q375. Teams background effects not loading for some users. RCA? [TOUGH]

**Answer:** Symptom: Background blur/images not available. Root Cause: (a) GPU not meeting minimum

requirements for background effects, (b) Teams running in restricted mode (VDI without GPU passthrough), (c) Admin policy disabled effects. Steps: Check GPU requirements (Intel HD 4000+, AMD/NVIDIA equivalent), check Teams Meeting Policy→Video filters, verify VDI GPU passthrough. Resolution: Enable GPU passthrough in VDI, assign meeting policy with video filters enabled.

### Q376. Teams Queues app not routing calls correctly. RCA? [TOUGH]

**Answer:** Symptom: Calls going to wrong agents in call queue. Root Cause: Call queue routing method

misconfigured (Attendant/Round Robin/Longest Idle), overflow/timeout settings incorrect, or agents not set to accept queue calls. Steps: Teams Admin→Voice→Call queues→verify routing method and agents; check agent opt-in status. Resolution: Correct routing configuration; ensure agents are opted in and available status active.

### Q377. Teams room system (MTR) shows 'Offline' in Teams Admin Center despite being powered on.

RCA? [TOUGH]

**Answer:** Symptom: MTR shows offline in portal. Root Cause: (a) MTR app crashed or hung, (b) Network

connectivity issue, (c) Account signed out, (d) Teams Rooms Pro Management agent not reporting. Steps: Restart MTR device, check network, verify MTR account credentials valid, check Teams Rooms license.

**Resolution:** Restart device; verify network; re-sign into MTR app if needed.

### Q378. Teams whiteboard not loading in meeting. RCA? [EASY]

**Answer:** Symptom: Whiteboard tab shows error or blank. Root Cause: Microsoft Whiteboard service disruption,

or whiteboard creation policy disabled, or user not licensed. Steps: Check M365 Service Health for Whiteboard service, check Teams Meeting Policy→Allow whiteboard. Resolution: Enable whiteboard in meeting policy; check service health and wait if service issue.

### Q379. Teams Together Mode not available for some participants. RCA? [EASY]

**Answer:** Symptom: Some attendees can't see Together Mode. Root Cause: Together Mode requires all

participants to have M365 Apps license with updated Teams; older clients or mobile may not support all Together Mode scenes. Steps: Ensure all participants have current Teams client; Together Mode initiated by organizer/presenter. Resolution: Update all clients to latest Teams version; switch to gallery view for mixed client meetings.

### Q380. Teams data loss prevention (DLP) policy blocking file sharing in chat. RCA? [TOUGH]

**Answer:** Symptom: Files blocked in Teams chat with DLP warning. Root Cause: Sensitive information detected

in shared file triggering M365 DLP policy applied to Teams. Steps: Review DLP policy in Purview (Teams DLP policy), verify if overly broad match, add exception if legitimate business use. Resolution: Tune DLP policy sensitivity; add business justification override; review match conditions.

### Q381. Teams cannot create new team — quota limit reached. RCA? [TOUGH]

**Answer:** Symptom: 'Team limit reached' error. Root Cause: M365 Group limit (max 500,000 groups) or per-user

team creation limit reached. Steps: Review M365 Group usage; archive inactive teams; adjust team creation policy. Resolution: Archive stale teams; increase limits via support ticket; implement team lifecycle management.

### Q382. Teams Breakout Rooms assignments resetting between meetings. RCA? [TOUGH]

**Answer:** Symptom: Room assignments not saved for recurring meetings. Root Cause: Breakout Room

assignments not preserved across recurring meeting instances. Steps: Reassign rooms at meeting start; use pre-assignment feature (requires organizer to re-confirm). Resolution: Save room configuration before meeting ends; Teams is improving cross-session persistence — check latest release notes.

### Q383. Teams translator feature not appearing in meeting toolbar. RCA? [TOUGH]

**Answer:** Symptom: Language interpreter option missing. Root Cause: Language Interpretation requires Teams

Premium license; not available in standard M365. Steps: Verify Teams Premium license assignment; enable interpreter in meeting options before meeting. Resolution: Assign Teams Premium license; pre-configure interpreters in meeting invite options.

### Q384. Teams third-party app data not appearing in Teams tab. RCA? [TOUGH]

**Answer:** Symptom: Integrated app tab shows empty data. Root Cause: (a) OAuth token expired for app

integration, (b) App backend service down, (c) Firewall blocking app's API endpoint. Steps: Remove and re-add app tab to re-authenticate, check app health status page, check firewall for app endpoints. Resolution: Re-authenticate app; check app vendor status; whitelist app endpoints in firewall.

### Q385. Teams channel meeting chat not synced with pre-meeting chat. RCA? [EASY]

**Answer:** Symptom: Messages in channel meeting thread not visible in Teams chat. Root Cause: Channel

meetings have chat in the channel post thread, not in separate chat; users looking in wrong location. Steps: Check channel post where meeting was created for meeting chat thread. Resolution: Educate users: channel meeting chats are in the channel post thread, not in Meetings→Chat.

### Q386. Teams GCC (Government Cloud) feature missing compared to commercial. RCA? [TOUGH]

**Answer:** Symptom: Feature available in commercial Teams not in GCC. Root Cause: GCC and GCC-High have

a subset of commercial Teams features due to compliance requirements (FedRAMP). Steps: Check Microsoft 365 Government feature availability matrix. Resolution: Refer to Microsoft's GCC feature list; request commercial-equivalent features via Microsoft feedback portal.

### Q387. Teams is consuming too much RAM/CPU on user machine. RCA? [EASY]

**Answer:** Symptom: Teams using 4GB+ RAM causing other apps to slow down. Root Cause: Teams Electron

app historically memory-intensive; multiple open chats and channels, browser tabs, and meeting rendering add up. Steps: Use 'New Teams' client (lighter WebView2-based), close unused chats, disable GPU hardware acceleration. Resolution: Upgrade to New Teams (Microsoft's modern reimplemented client); reduce open channels; close Teams when not in use.

### Q388. Teams channel notifications not alerting despite being enabled. RCA? [EASY]

**Answer:** Symptom: No notification for channel messages despite settings. Root Cause: (a) Focus Assist/Do Not

Disturb active on Windows, (b) Per-channel notification override set to Off, (c) Quiet hours in Teams mobile.

**Steps:** Check Windows Focus Assist settings, Teams→channel→notification settings (bell icon), check Teams

notification settings globally. Resolution: Disable Focus Assist, reset per-channel notifications, adjust quiet hours settings.

### Q389. Teams app failing SSO (Single Sign-On) in SharePoint Framework app. RCA? [TOUGH]

**Answer:** Symptom: SPFx app in Teams tab can't authenticate via SSO. Root Cause: Azure AD app registration

missing Teams scope (access_as_user), or SPFx solution missing Teams context configuration. Steps: Check Azure AD app registration for 'access_as_user' API permission in Teams scope, verify TeamsJS SDK initialization in SPFx. Resolution: Add access_as_user permission, configure SPFx TeamsJS context, approve API permissions in SharePoint Admin.

### Q390. Teams meeting invite link not working for users from a different forest. RCA? [TOUGH]

**Answer:** Symptom: Users from federated forest cannot join with Teams link. Root Cause: Cross-forest

federation not configured; users have no Azure AD identity recognizable by the meeting tenant. Steps: Configure Azure AD B2B federation with partner forest's Azure AD, or allow anonymous join for the meeting. Resolution: Set up cross-tenant access (Entra ID B2B); or allow anonymous join for external participants.

### Q391. Teams Planner tasks not visible in Teams Tasks app. RCA? [EASY]

**Answer:** Symptom: Planner boards created externally not appearing in Teams Tasks by Planner. Root Cause:

Planner plans created outside of a Teams channel may not auto-appear; must be connected to a Team. Steps: Open Teams→Tasks by Planner→check if plan is listed; manually pin Planner tab to Teams channel for the relevant plan. Resolution: Pin Planner plan as tab in Teams channel; or create plan directly from Teams for automatic integration.

### Q392. Teams Emergency Calling not sending correct location. RCA? [TOUGH]

**Answer:** Symptom: E911 location wrong or empty. Root Cause: Emergency address not assigned to user, or

network site not configured for dynamic location; user working remotely (location unknown). Steps: Teams Admin→Locations→verify Emergency Addresses; assign emergency location to user; configure network sites for dynamic routing. Resolution: Assign emergency location; configure dynamic E911 for network locations; inform remote workers of manual location requirement.

### Q393. Teams app message delivery confirmation not available. RCA? [EASY]

**Answer:** Symptom: Cannot confirm if Teams message was read. Root Cause: Teams does not display message

read receipts in group chats (only in 1:1 chat if read receipts enabled by admin). Steps: Check if 1:1 chat shows read indicator. Resolution: Read receipts available in 1:1 chats only; for confirmation in channels/group chats, use @ mention or require explicit reply.

### Q394. Teams meeting organizer changed after scheduled meeting — attendees not notified. RCA?

[EASY]

**Answer:** Symptom: Organizer changed but invite not updated. Root Cause: Teams meetings are tied to

organizer's identity; changing organizer requires creating a new meeting. Steps: Cancel original meeting (send cancellation), create new meeting from new organizer's account, re-invite all attendees. Resolution: Always send cancellation when changing organizer; new meeting required with new organizer.

### Q395. Teams app crashing on macOS after OS update. RCA? [EASY]

**Answer:** Symptom: Teams crashes on launch on updated macOS. Root Cause: macOS system update changed

security permissions or Teams app incompatible with new macOS APIs. Steps: Clear Teams cache (~/Library/Application Support/Microsoft/Teams), reinstall Teams, check System Preferences→Privacy→allow Teams permissions. Resolution: Clear cache, reinstall, grant required macOS permissions (microphone, camera, screen recording).

### Q396. Teams meeting bot not joining scheduled meeting for recording. RCA? [TOUGH]

**Answer:** Symptom: Third-party recording bot misses meeting join. Root Cause: Bot invitation revoked, bot not

given proper Graph permissions (OnlineMeetings.ReadWrite), or bot service outage. Steps: Re-invite bot to meeting, verify Graph API permissions, check bot service health. Resolution: Verify bot Graph permissions; re-invite; check vendor service status; use Microsoft native recording as backup.

### Q397. Teams knowledge base (Viva Topics) not surfacing in channels. RCA? [TOUGH]

**Answer:** Symptom: Topic cards not appearing in Teams. Root Cause: (a) Viva Topics license not assigned to

users, (b) Topics AI processing not complete, (c) SharePoint Viva Topics site not configured. Steps: Verify Viva Topics license, check Knowledge Center SharePoint site status, allow 2-3 weeks for AI topic mining. Resolution: Assign Viva Topics license; configure Knowledge Center; allow initial processing to complete.

### Q398. Teams meeting capacity exceeded for Teams webinar. RCA? [TOUGH]

**Answer:** Symptom: Attendees cannot register or join webinar — at capacity. Root Cause: Teams Webinar limit

(1,000 interactive attendees; 10,000 view-only). Steps: Switch to Teams Town Hall for larger audiences (20,000+); or use Teams Live Events. Resolution: Use Teams Town Hall (M365/Teams Premium) for large audiences; plan capacity before promotion.

### Q399. Teams new features not appearing for users despite admin enabling. RCA? [EASY]

**Answer:** Symptom: Feature enabled in admin but not visible to users. Root Cause: (a) Feature rollout not

reached user's ring (Teams rings: internal, TAP, general production), (b) Teams client requires update, (c) Policy propagation delay (up to 48 hours). Steps: Check Teams Admin policy propagation, force client update, verify feature rollout status via M365 Roadmap. Resolution: Wait for policy propagation (up to 48 hours); update Teams client; check M365 Roadmap for feature availability.

### Q400. Teams Operator Connect PSTN calling failing after number transfer. RCA? [TOUGH]

**Answer:** Symptom: Transferred numbers not making/receiving calls. Root Cause: Number porting process

incomplete; carrier not fully completed transfer; Teams user object not updated with new number. Steps: Verify porting order completion with carrier, check Teams Admin→Users→Phone Number assigned, run Test-CsOnlineLisCivicAddress. Resolution: Coordinate with carrier to complete port; reassign number in Teams Admin after confirmation; allow DNS propagation period. ■ End of Document L2 M365 & SharePoint Developer Interview Preparation 400 Questions • 7 Sections • Easy + Tough • Full RCA Coverage Good Luck with Your Interview!

---
