**AI Policy \-- Technical Controls Appendix**

**Companion to:** Artificial Intelligence (AI) Policy

**Audience:** the Organization's IT staff \-- internal reference; not intended for public posting.

**Version:** 0.3 (draft)

**Last updated:** 2026-06-14

**Prepared by:** Laura Rowe

This attachment captures the technical control detail, licensing dependencies, and Microsoft 365 GCC platform constraints that sit behind the AI Policy. It was separated from the main policy body so the policy stays concise and client-facing while the implementation specifics are preserved for IT reference. Section numbers below map to the corresponding sections of the AI Policy.

**[1. AI Policy to Technical Controls Cross-Reference]{.underline}**

 --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Policy Section** **Technical Control** **Status**
 ------------------------------- -------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 3.2 Security and Safety MDA unsanctioned app tagging (1,218 Generative AI apps tagged Unsanctioned; 13 Sanctioned) Complete \-- monitoring-only; endpoint enforcement blocked by SentinelOne coexistence

 3.2 Security and Safety Microsoft Purview browser extensions \-- Edge, Chrome, Firefox (Windows-only via Intune) Deployed to all managed Windows devices; mobile-only devices not covered

 3.3 Privacy Purview DLP policy \-- detect sensitive info shared with AI sites (audit mode, all users) Deployed \-- detects sensitive data sharing with AI sites; does not detect bare site visits

 3.4 Transparency AI meeting note-taking disclosure requirement Policy-level requirement \-- staff responsibility per Sections 3.4 and 6.2

 5.1 AI Tool Approval Workflow Director to IT Manager two-gate process Policy-level process \-- implemented via Change Request template

 5.2 AI Review IT Manager risk assessment + Legal Counsel routing for high-risk tools Policy-level process \-- AI FactSheet (Appendix A); Legal Memo routed for Wealth Engine and ChatGPT

 6.3 Consumer AI Tool Ban Prohibition on free/personal/consumer-tier generative AI tools Enforcement via MDA unsanctioned app tagging (monitoring-only). Endpoint blocking requires MDE active mode. Cloud Discovery provides supplementary on-network visibility.

 7 Monitoring Purview DSPM for AI dashboard Accessible \-- covers 2 Purview Suite users only. Viva Insights / Copilot Dashboard not available in GCC.

 8 Public Records AI artifacts as Organization records (prompts, chat histories, meeting summaries) Policy-level classification. Zoom AI Companion retention settings and Copilot audit logging are the tool-level controls.

 11 Restricted Platforms MDA Cloud App Catalog \-- sanctioned/unsanctioned app list Complete (1,218 Unsanctioned, 13 Sanctioned)

 11 Restricted Platforms Cloud Discovery log collector (Cisco FTD syslog to MDA) Connected \-- data flows in bursts; continuous forwarding depends on firewall-side configuration
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**[2. Security and Safety Controls (Policy Section 3.2)]{.underline}**

- **MDA unsanctioned app tagging** \-- Microsoft Defender for Cloud Apps tags Generative AI category apps as sanctioned/unsanctioned in the Cloud App Catalog. 1,218 apps tagged Unsanctioned; 6 Microsoft AI apps + 7 core M365 infrastructure apps tagged Sanctioned (13 total). Configured as a scoped deployment for the 2 Purview Suite licensed users.

- **Microsoft Purview browser extensions** \-- three separate artifacts that monitor AI tool usage on Windows endpoints: Edge (manual Intune force-install profile required in GCC; auto-provisioning via DLP policy does not work), Chrome (CRX, via Intune), Firefox (XPI, via Intune ADMX import). Requires Windows 10/11 x64 1809+. Not supported on macOS, iOS, Android, Linux, or non-Edge/Chrome/Firefox browsers.

- **DSPM for AI dashboard** \-- surfaces Copilot interaction telemetry and sensitive-data detection. Browser-extension signals require per-user Endpoint DLP licensing (E5/A5/G5 or Purview Suite) to flow to Activity Explorer and the dashboard \-- currently 2 users at Organization.

- **Endpoint enforcement** \-- blocking unsanctioned apps at the endpoint requires Microsoft Defender for Endpoint (MDE) Network Protection. MDE P1 is licensed and assigned to both pilot users but SentinelOne coexistence blocks enforcement (see Section 5).

- **Cloud Discovery** \-- log collector connected to the Cisco Firepower 1120 via a Docker container on an Organization host. Cisco ASA FirePOWER parser. Provides org-wide IP-level visibility into third-party app usage regardless of per-user Purview licensing.

**[3. Privacy Controls (Policy Section 3.3)]{.underline}**

- DLP policy "Detect sensitive info pasted or uploaded to AI sites" deployed in audit mode, scoped to all users. Fires when sensitive data matching SIT patterns is shared with AI sites. Does not detect bare AI site visits.

- IRM browsing indicator ("Browsed to generative AI websites") does not exist in GCC \-- permanent platform gap. Bare AI site visit detection is not possible through Purview IRM in this environment.

- PII blocking in AI prompts was identified as a candidate Purview compliance policy for the 2 pilot users. Not deployed \-- additional sensitive information types TBD during future policy scoping.

**[4. Microsoft 365 GCC Feature Parity (Policy Section 3.8, Training)]{.underline}**

Training materials and demos must exclude features unavailable in GCC. The following are not currently available in GCC:

- Teams Meeting Copilot

- Copilot in Loop

- Copilot in Whiteboard

- Microsoft Viva Insights / Copilot Dashboard

- Copilot Chat Edge sidebar

Web grounding is OFF by default in GCC. As of April 15, 2026, the in-app Copilot experience in Word, Excel, PowerPoint, and OneNote is restricted to users with a paid Microsoft 365 Copilot license.

**Copilot Licensing and Plan Eligibility**

- Microsoft 365 Copilot is a licensed add-on to a qualifying base plan. In GCC, qualifying base plans are Office 365 G1, G3, G5, F3 and Microsoft 365 G3, G5, F1. It operates within the Organization\'s M365 GCC tenant compliance boundary.

- Microsoft 365 Copilot Chat is the chat interface at copilot.microsoft.com with enterprise data protection, available to all users with an eligible M365 base subscription at no additional cost; it does not require a Copilot add-on license. The full in-app experience requires a paid Copilot license (April 15, 2026 change).

- Full Copilot functionality favors the G3 cohort; pilot users should be selected accordingly.

**[5. Enforcement and Monitoring Constraints (Policy Section 11)]{.underline}**

- **MDE Network Protection requirement** \-- endpoint enforcement of unsanctioned-app blocking requires MDE Network Protection, which does not function in passive mode. MDE P1 is licensed and assigned to both pilot users.

- **SentinelOne coexistence** \-- Organization runs SentinelOne as its primary EDR, which registers as the primary AV and forces Microsoft Defender Antivirus (MDAV) into passive mode, disabling Network Protection. Options: (a) the Organization's IT removes SentinelOne from the pilot devices so MDAV runs in active mode (recommended), or (b) reconfigure SentinelOne not to register with Windows Security Center. Simple agent removal is NOT sufficient \-- stale WSC registration keeps MDAV passive. Deferred at client direction; revisit at SentinelOne contract renewal (November 2026).

- **Cloud Discovery traffic-source dependency** \-- MDA Cloud Discovery requires a traffic source. The Docker-based log collector is connected to Organization\'s Cisco Firepower 1120 via syslog. Data flows intermittently; continuous forwarding depends on firewall-side configuration. Running the collector on a user-closable desktop app makes the feed operationally fragile \-- harden by auto-starting the service or moving to an always-on host.

- **Third-party AI site monitoring \-- permanent GCC platform gap** \-- the IRM browsing indicator that would detect AI site visits does not exist in GCC. Browser extensions capture Copilot telemetry natively; third-party AI site visibility depends on Cloud Discovery.
