**AI FactSheet \-- Placer AI**

**Document status:** DRAFT \-- for IT Manager review and intake completion

**Version:** 0.1

**Date:** June 2026

**Prepared by:** Laura Rowe

**Companion to:** AI Policy Section 5 AI Review \-- Appendix A, AI FactSheet template

**Tool tier:** Placer Basic Plan (confirmed by IT Manager, June 2026)

*Advisory only. Per SOW SS2.2 and SS5, the advisory firm provides this FactSheet as a draft intake artifact. Vendor postures below are based on Placer public documentation as of mid-2026 and must be confirmed against the executed contract/DPA before sanctioning. The IT Manager owns the final AI Review determination (A.8).*

**[A.1 System and Vendor Identification]{.underline}**

 ---------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **AI system / product name** Placer.ai \-- location-analytics platform (foot-traffic and audience estimates derived from aggregated mobile-device signals)

 **Vendor / developer name** Placer Labs Inc.

 **Primary contact** TBD \-- Placer account manager assigned to Organization

 **Hosting model** Vendor SaaS (Placer-hosted, AWS US per public documentation)

 **Inside Organization M365 GCC boundary?** No. Placer is a separate SaaS platform outside the M365 GCC tenant. Note, however, that Organization does not upload Organization data to Placer (see A.3) \-- the data flow is one-directional, from Placer\'s aggregated panel to Organization.
 ---------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**[A.2 Purpose and Intended Use]{.underline}**

 ----------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Business purpose** Location analytics \-- foot-traffic and audience estimates supporting park planning, program siting, capital planning, and marketing/communications.

 **Organization departments using it** TBD \-- confirm during intake. Likely: Park Operations, Recreation Program Planning, Capital Planning, Communications/Marketing.

 **Categories of users** Designated analysts (staff), per-named-user access.

 **AI type** Decision-support analytics AI. Aggregates third-party mobile-location signals into estimates that inform planning decisions. Does not profile or decide about identifiable individuals.

 **Decision-influencing?** Informs planning decisions (siting, capital, programming). Does not make or materially inform decisions about identifiable individuals \-- outputs are aggregated estimates, not individual profiles.
 ----------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**[A.3 Data Handling]{.underline}**

**Critical data-direction note.** Organization does not purchase location data and does not upload its own visitor or resident lists to Placer. Organization pays for algorithm access only; Placer converts third-party cell-phone signal data into aggregated estimates. There is no back-and-forth transfer of Organization-held personal data. This materially limits Organization\'s data-handling exposure for this tool.

 ------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Categories of Organization data processed** None uploaded. Organization does not send Organization PII, resident lists, or visitor lists to Placer. Organization defines geofences (place boundaries) to scope queries; these are location definitions, not personal data.

 **Inputs/outputs used to train vendor models?** Organization supplies no training data. Placer\'s panel data is its own; Organization queries it. Confirm contractually that Organization-defined geofences and queries are not used to enrich Placer\'s commercial dataset.

 **Can training-on-data be disabled?** Not applicable \-- Organization supplies no data to train on.

 **Data retention** Limited to query logs and audit metadata per Placer\'s standard policy. No Organization PII is entered, so retention exposure is confined to query metadata, not personal data.

 **Data residency / storage location** AWS US per published documentation; specific region not separately confirmed. Acceptable given no Organization PII is transferred.

 **Subprocessors** Mobile-location data suppliers / SDK aggregators that form Placer\'s panel, per Placer\'s published documentation. Relevant to the data-broker-proximity review in A.7.

 **Encryption** TLS in transit, AES-256 at rest per Placer published docs. Standard posture accepted.
 ------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**[A.4 Security and Access]{.underline}**

 --------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------
 **Authentication / access control** Per-named-user access; restrict to designated analysts. SSO (SAML) supported. Confirm SSO integration with Organization M365 / Entra ID.

 **Independent security attestations** Placer publishes SOC 2 Type II. Request current attestation report. ISO 27001 / FedRAMP / StateRAMP: confirm if relevant.

 **Breach notification** Governed by Placer\'s standard DPA breach-notification terms. Confirm the timeline in the executed agreement.

 **Logging / audit capabilities** Query and usage logs available. Confirm export and retention of audit logs for Organization records.
 --------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------

**[A.5 Model, Transparency, and Limitations]{.underline}**

 ----------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Model type** Proprietary estimation models that convert aggregated mobile-device location signals into foot-traffic and audience estimates.

 **Known limitations** Estimates carry sample-size and margin-of-error; they are modeled approximations, not a census. Panel composition may under- or over-represent demographic groups, which matters for equity-sensitive siting. Staff must apply AI Policy Section 6.2 \-- treat estimates as decision support, not ground truth.

 **Bias / fairness testing** Request Placer\'s methodology on demographic-representation bias in panel data and audience-segmentation outputs. The operative control is human review of any estimate that informs a high-stakes decision.

 **Explainability** Outputs are aggregated estimates; vendor documents methodology at a high level. Individual-level tracing is neither available nor relevant (no individuals are identified).
 ----------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**[A.6 Human Oversight]{.underline}**

 ------------------------------------------------------ --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Where does a human review/approve outputs?** Analysts interpret Placer estimates; estimates inform but do not by themselves make planning, siting, or capital decisions. Per AI Policy Section 6.2, staff are responsible for the appropriate use of these estimates.

 **Can fully automated decision-making be disabled?** Not applicable \-- Placer does not make decisions about individuals. Confirm the vendor does not add automated-decisioning features without customer opt-in.
 ------------------------------------------------------ --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**[A.7 Compliance and Contractual]{.underline}**

 --------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Data Processing Agreement (DPA)** Confirm executed copy on file with the Organization. Given the location-data domain, a Legal Counsel pass on the DPA is recommended before sanction is finalized.

 **CPRA / California terms** Precise geolocation is sensitive personal information under CPRA. Note that Organization handles no individual geolocation \-- Placer\'s outputs are aggregated estimates \-- but Legal should confirm CCPA/CPRA terms and that no individual SPI flows to Organization.

 **California data-broker status** Confirm Placer\'s and its material data suppliers\' California data-broker registration status (Delete Act / CCPA registry). This is the principal reason for the recommended Legal pass.

 **California Public Records Act** Placer reports and outputs used in Organization planning may constitute Organization records under the CPRA (see AI Policy Section 8). Retention should align with the Organization\'s records-retention schedule.

 **Contractual commitment to Organization policy standards** Confirm the contract prohibits use of Organization-defined geofences or queries to enrich Placer\'s commercial dataset, and addresses CCPA/CPRA service-provider terms.

 **Contracting entity** Organization.
 --------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**[A.8 AI Review Outcome (IT Manager Use)]{.underline}**

+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Risk tier assigned** | **Moderate.** Higher-touch than Canva or FreshService due to the location-data domain and data-broker proximity, but materially contained because Organization purchases algorithm access only \-- no Organization PII is purchased, uploaded, or combined with Placer data. Risk concentrates in estimate reliability and the vendor\'s upstream data sourcing, not in Organization-data exposure. |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Reviewed by** | the IT Manager, IT Manager |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Review date** | TBD \-- pending intake completion and DPA verification |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Decision** | Recommended: Approve with conditions (see below) |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Conditions** | 1\. No upload of Organization PII, resident lists, or visitor lists to Placer. Use limited to aggregated location-analytics outputs. |
| | |
| | 2\. Geofences limited to Organization facility boundaries (from shapefiles) and Organization-sponsored event areas. No geofence is configured to target individuals, and geofencing is not extended to locations where minors are the primary population beyond Organization programming. (Forward-looking rule \-- no static geofence list is maintained in policy.) |
| | |
| | 3\. Analysts apply AI Policy Section 6.2 human review: estimates inform but do not solely determine high-stakes decisions, with awareness of sample-size and margin-of-error limitations. |
| | |
| | 4\. Legal Counsel review of the Placer DPA recommended before sanction is finalized \-- CCPA/CPRA terms, data-broker disclosure, and a contractual prohibition on using Organization geofences or queries to enrich Placer\'s commercial dataset. |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Re-review date** | At the annual policy review (Section 9.2), or immediately on any material change in use \-- in particular, any attempt to combine Placer data with Organization-held PII would trigger re-review. |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Legal Counsel routing** | Yes \-- DPA review recommended (Open Items L-3, L-4) given the location-data domain. This is a moderate-touch Legal pass on the DPA, not a full high-risk hold like Wealth Engine; the tool may be used for aggregated analytics under the conditions above while the DPA review proceeds, at the IT Manager\'s discretion. |
+---------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
