**AI Monitoring and Administration Guide**

**Audience:** Organization IT staff

**Purpose:** Reference guide for monitoring AI usage and maintaining the configuration after the advisory firm engagement

**Prepared by:** Laura Rowe, Technical Lead, the advisory firm

**Last updated:** 2026-05-29

**Environment:** Microsoft 365 GCC (Government Community Cloud - moderate)

**[WHAT WAS CONFIGURED]{.underline}**

During this engagement, the advisory firm configured the following:

- Microsoft Defender for Cloud Apps (MDA) - Cloud App Catalog with sanctioned and unsanctioned AI app tags

- MDA Cloud Discovery - Docker log collector on an Organization host receiving syslog from the Cisco Firepower 1120 FTD. Surfaces third-party AI site visits and unsanctioned-app usage at the network level (no user attribution)

- Microsoft Purview browser extensions - Chrome, Edge, and Firefox extensions deployed via Intune to monitor AI tool usage on managed Windows devices

- Microsoft Purview Endpoint DLP policies - Activates Edge native browser integration, enables Activity Explorer data collection, and detects sensitive data shared with AI sites

- Microsoft Purview DSPM for AI - Dashboard showing AI usage patterns and sensitive data exposure

- Microsoft 365 Copilot - Enabled for pilot users with license assignments

- Insider Risk Management analytics - Enabled for baseline risk assessment

**[WHERE TO FIND THINGS]{.underline}**

**Defender for Cloud Apps (MDA) - App Catalog**

**What it shows:** Which AI apps are approved (Sanctioned) and which are not (Unsanctioned).

**How to access:**

- Go to security.microsoft.com

- Left nav: Cloud apps \> Cloud app catalog

- Filter by Category: Generative AI (left sidebar) to see all AI apps

- Filter by Tag: Sanctioned or Unsanctioned

**Current state:**

- 13 apps tagged Sanctioned (6 Microsoft AI apps + 7 core M365 infrastructure apps)

- Approximately 1,218 Generative AI apps tagged Unsanctioned

- Discovery policy ("Generative AI - Unsanctioned Category") automatically tags newly discovered AI apps as Unsanctioned if Cloud Discovery receives traffic data

**Common tasks**

 -------------------------------------------------------------------------------------------------------------------------
 **Task** **How**
 ------------------------------------------- -----------------------------------------------------------------------------
 See which apps are approved Cloud app catalog \> filter by Tag: Sanctioned

 See which apps are unsanctioned Cloud app catalog \> filter by Tag: Unsanctioned

 Approve a new AI app Cloud app catalog \> search for the app \> click it \> mark as Sanctioned

 Mark a new AI app as unsanctioned Cloud app catalog \> search for the app \> click it \> mark as Unsanctioned

 See if users accessed an unsanctioned app Cloud apps \> Activity log \> filter by app or user
 -------------------------------------------------------------------------------------------------------------------------

**Important:** Changing an app from Unsanctioned to Sanctioned (or the reverse) updates the catalog tag only. Endpoint enforcement requires Microsoft Defender for Endpoint (MDE) with Network Protection enabled and Microsoft Defender Antivirus running in active mode. MDE P1 is licensed and assigned to both pilot users but is not currently enforcing - the existing endpoint protection agent keeps MDAV in passive mode, which disables Network Protection. Without active-mode MDAV, the catalog tags serve as a monitoring and classification tool, not an enforcement mechanism.

**Cloud Discovery:** Connected to the Organization\'s Cisco Firepower 1120 FTD via a Docker log collector on an Organization host. As of 5/28: 311 apps discovered, 293 IP addresses, 5.4 GB traffic; unsanctioned Generative AI apps detected: ChatGPT, Google Gemini, Superhuman Grammarly, OpenAI. Full details and how-tos in the Cloud Discovery section below.

**Cloud Discovery - Third-Party AI Site Visibility**

**What it shows:** Network-level visibility into third-party AI site visits (ChatGPT, Gemini, etc.) and other cloud apps used by people on the Organization network, based on firewall log data.

**How to access:**

- Go to security.microsoft.com

- Left nav: Cloud apps \> Cloud Discovery

- Top tabs: Dashboard, Discovered apps, IP addresses, Users

**Current state (as of 5/28):**

- Log collector connected to Cisco Firepower 1120 FTD via syslog

- 311 apps discovered, 293 IP addresses observed, 5.4 GB total traffic

- Unsanctioned Generative AI apps detected: ChatGPT (Consumer & Enterprise), Google Gemini, Superhuman Grammarly, OpenAI

**Common tasks**

 ----------------------------------------------------------------------------------------------
 **Task** **How**
 ------------------------------------------ ---------------------------------------------------
 See which AI sites have been visited Discovered apps \> filter Category: Generative AI

 See which IPs visited a specific AI site Discovered apps \> click app \> IP addresses tab

 Filter to unsanctioned apps only Discovered apps \> filter Tag: Unsanctioned

 Adjust risk threshold Discovered apps \> top filter bar
 ----------------------------------------------------------------------------------------------

***Important coverage notes:***

***No user attribution.** Firewall logs contain source/destination IP addresses only, not user identity. The Users column will show 0 for all apps. To identify who visited an AI site, cross-reference the source IP with DHCP lease records or static IP assignments.*

***On-network only.** Cloud Discovery only sees traffic that traverses the Organization firewall. Users on home networks or other off-network locations are not covered by this signal.*

***Subnet coverage (confirmed 5/29 by Organization firewall admin):** staff wifi (10.15.180.x) and guest wifi (10.15.185.x) are flowing. Other segments (e.g., guest LAN 10.15.110.x) are absent because they are currently unused, not because of a forwarding gap.*

**What you will NOT see:**

- Visits from off-network devices (home wifi, cellular, etc.)

- User identity (firewall logs are IP-only)

- Sensitive data shared with AI sites (that signal is in Activity Explorer / DSPM for AI for the 2 Purview-licensed users)

**Activity Explorer - AI Usage Events**

**What it shows:** Individual AI usage events captured by the Purview browser extensions and DLP policies. Shows which users interacted with Copilot, what files were involved, and when it happened.

**How to access:**

- Go to purview.microsoft.com

- Left nav: Data Loss Prevention \> Explorers \> Activity explorer

**What you will see:**

- AI Interaction - A user used Copilot or Copilot Chat

- Sensitive info types - Sensitive data (names, financial data, medical terms, etc.) was detected in content Copilot accessed

**What you will NOT see:**

AI Visit - This activity type does not exist in GCC environments. Visits to third-party AI sites (ChatGPT, Gemini, etc.) are not captured in Activity Explorer. This is a GCC platform limitation, not a configuration issue. See the Cloud Discovery section above for the alternative path.

**Filtering:**

- Use the date filter to set your timeframe

- Use the User filter to see a specific person\'s activity

- Use the Activity filter to isolate AI Interaction vs. Sensitive info types events

***Coverage limitation:** Full signal data (AI Interaction events with file details) flows only from users with Microsoft Purview Suite licenses. Currently 2 users have Purview Suite licenses. The browser extensions are installed on all pilot devices, but users without Purview Suite licenses generate limited or no Activity Explorer data. Expanding Purview Suite licensing would expand monitoring coverage.*

**DSPM for AI Dashboard**

**What it shows:** A summary view of AI usage across the organization, including sensitive data categories detected in AI interactions, documents accessed by Copilot without sensitivity labels, and potential risky AI usage patterns.

**How to access:**

- Go to purview.microsoft.com

- Left nav: Data Security Posture Management (or search for "DSPM")

- Select the AI overview or Reports tab

**Key panels:**

- AI interactions - Total volume of AI usage over time

- Sensitive interactions - Interactions that involved sensitive data (PII, financial data, medical terms, etc.)

- Microsoft 365 Copilot tab - Documents accessed by Copilot, broken down by whether they have sensitivity labels applied

- Sensitive data categories - Breakdown by type (Full Names, Medical Terms, Financial data, etc.)

**What to watch for:**

- A high number of sensitive interactions relative to total interactions may indicate users are sharing sensitive data with AI tools

- Documents accessed by Copilot with no sensitivity labels applied represent a data classification gap - these documents should be reviewed and labeled

- The "Potential risky AI usage" panel flags interactions that may warrant investigation

***Coverage limitation:** Same as Activity Explorer - DSPM for AI data covers Purview Suite licensed users only.*

**Intune - Browser Extension Deployment Status**

**What it shows:** Whether the browser extensions are successfully installed on managed devices.

**How to access:**

- Go to intune.microsoft.com

- Left nav: Devices \> Configuration

- Search for "Purview" to find the three profiles

**Three profiles to monitor**

 -----------------------------------------------------------------------------------------------
 **Profile** **Browser** **Type**
 ------------------------------------------- ------------- -------------------------------------
 Purview Chrome Extension - Force Install Chrome Settings catalog

 Purview Edge Extension - Force Install Edge Settings catalog

 Purview Firefox Extension - Force Install Firefox Administrative Templates (Imported)
 -----------------------------------------------------------------------------------------------

**What "success" looks like:**

- All three profiles show device check-in counts matching the number of managed Windows devices in the assigned group

- Each profile\'s Device status page shows individual devices with "Success" status

**GCC note:** Edge browser extension deployment in GCC requires a manual Intune force-install profile. The auto-provisioning mechanism described in Microsoft documentation (where creating a Purview DLP policy automatically generates an Edge configuration profile) does not function in GCC environments. The manual profile uses the Settings catalog setting "Control which extensions are installed silently."

**Common issues:**

- Devices that have not synced with Intune recently will not receive updated profiles. Check the device\'s last check-in date.

- Non-compliant devices may not receive policies depending on Conditional Access configuration.

- Firefox uses an Administrative Templates (Imported) profile type, not Settings catalog. Look under the correct profile type if searching.

**Copilot Licensing**

**How to check license assignments:**

- Go to admin.microsoft.com

- Left nav: Users \> Active users

- Click on a user \> Licenses and apps

**Licensed Copilot users vs. Copilot Chat users:**

- Users with a Microsoft 365 Copilot license get in-app AI features in Word, Excel, Outlook, PowerPoint, and Teams.

- All other users can access Microsoft Copilot Chat at copilot.microsoft.com - a free web-based AI chat with enterprise data protection. Copilot Chat does not access organizational data, individual files, or Graph connector data.

- As of April 15, 2026, Microsoft removed in-app Copilot features for unlicensed users. Unlicensed users are limited to the Copilot Chat web interface only.

**To assign Copilot to a new user:**

- The user must be on an Office 365 G3 base license for the full Copilot experience (G1 users have limited functionality)

- In the user\'s Licenses and apps page, check the Microsoft 365 Copilot checkbox

- Save. License propagation may take up to 24 hours.

- Available Copilot licenses can be checked at Billing \> Licenses

**[ROUTINE MONITORING CHECKLIST]{.underline}**

A suggested weekly or biweekly review:

- **Activity Explorer** - Check for new AI Interaction events. Are users actively using Copilot? Are there any unexpected patterns?

- **DSPM for AI** - Review the sensitive interactions panel. Are sensitive data categories increasing? Are new categories appearing?

- **MDA Activity Log** - Check for sign-in or app activity for sanctioned cloud apps (security.microsoft.com \> Cloud apps \> Activity log). For third-party AI site visits, use Cloud Discovery - the Activity Log surfaces app activity for sanctioned apps, not bare network visits.

- **Cloud Discovery dashboard** - Review newly discovered cloud apps, especially in the Generative AI category. Watch for new third-party AI sites with traffic or risk-score changes (security.microsoft.com \> Cloud apps \> Cloud Discovery \> Dashboard).

- **Intune profile status** - Spot-check that browser extension profiles are still deployed and devices are checking in

- **Cloud App Catalog** - Review if any new Generative AI apps have been discovered and auto-tagged by the discovery policy

**[WHAT IS NOT CONFIGURED (OUT OF SCOPE)]{.underline}**

The following were not part of the advisory firm engagement and would require additional work should the Organization elect to implement them:

**Endpoint enforcement of app blocking -** Requires Microsoft Defender for Endpoint (MDE) with MDAV in active mode. MDE P1 is licensed and assigned to both pilot users but is not enforcing - SentinelOne (the Organization\'s primary EDR) keeps MDAV in passive mode, which disables Network Protection. Status: Deferred at client direction. IT Director acknowledged the constraint in the 5/27 weekly sync and chose to keep SentinelOne in place for now. Revisit at the SentinelOne contract renewal (November 2026) if the Organization decides to consolidate to MDE.

**DLP policies with enforcement actions -** DLP policies are currently in audit mode (detect and log, no block or warn). Creating enforcement DLP policies is a separate effort.

**Sensitivity labels and data classification -** No sensitivity labels are currently applied to Organization content. Labeling would improve Copilot data protection and DSPM reporting.

**Insider Risk Management policies -** IRM analytics are enabled but no policies are configured. The IRM browsing indicator for detecting visits to generative AI websites is not available in GCC. IRM policies for other risk signals (data exfiltration patterns) could be configured separately.

**Conditional Access policies -** Not configured. Would complement browser extensions by controlling access based on device, location, and risk level.

**[KEY CONTACTS]{.underline}**

 ---------------------------------------------------------------------------------------------------
 **Role** **Contact** **For**
 -------------------------- ---------------- -------------------------------------------------------
 Organization IT Director the IT Manager Day-to-day monitoring, user issues, license changes

 the advisory firm To be filled Questions about configuration or follow-on engagement
 ---------------------------------------------------------------------------------------------------

**[REFERENCE LINKS]{.underline}**

- Microsoft Defender for Cloud Apps documentation - learn.microsoft.com/en-us/defender-cloud-apps/

- Microsoft Purview Data Loss Prevention - learn.microsoft.com/en-us/purview/dlp-learn-about-dlp

- DSPM for AI overview - learn.microsoft.com/en-us/purview/ai-microsoft-purview

- Intune device management - learn.microsoft.com/en-us/mem/intune/

- Microsoft 365 Copilot administration - learn.microsoft.com/en-us/copilot/microsoft-365/microsoft-365-copilot-overview

- Cloud Discovery setup - learn.microsoft.com/en-us/defender-cloud-apps/set-up-cloud-discovery
