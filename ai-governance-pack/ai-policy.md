**Artificial Intelligence (AI) Policy**

**Document status:** DRAFT \-- for review and input

**Version:** 0.4 (draft \-- expanded scope; reconciled to June 2026 client direction)

**Last updated:** 2026-06-25

**Prepared by:** Laura Rowe

**Companion documents:** AI Policy Appendices \-- recommended governance templates (AI FactSheet, Incident Response Plan, Governance Manual); Technical Controls Appendix \-- internal IT reference (not for public posting).

**Sources:** This policy is adapted from the GovAI Coalition AI Policy Template provided to the advisory firm by the Organization. Sections 11 (Restricted Platform Alternatives) and 12 (Terms and Definitions) have been customized to reflect the Organization\'s current Microsoft 365 environment. The v0.3 expansion incorporates direction from the IT Manager and PM following the 2026-06 leadership review to broaden coverage to all Organization AI tools, integrate the affiliated Foundation, add a procurement approval workflow, and prohibit unsanctioned consumer AI tools.

**Changes in this revision (v0.4).** Reconciled to confirmed June 2026 client direction: the affiliated Foundation contracting clarified \-- the Foundation signs its own contracts and DPAs, the IT Manager reviews use (Sections 2, 4, 12); Foundation point-of-contact title updated (Section 4); AI-decision responsibilities (FactSheet, vendor AI compliance) assigned to the IT Manager, with Finance retaining purchasing (Sections 4, 5); FreshService AI marked available-not-active and Canva AI scoped to Canva for Teams, staff use only (Section 11); Placer AI removed from the Section 1 high-risk example, as no Organization PII flows; and the Organization's Microsoft AI tools (Copilot Studio, Security Copilot, Designer, Image Creator) added to the Section 11 sanctioned list.

**[IN PLAIN TERMS]{.underline}**

Artificial intelligence (AI) tools are now part of everyday work across the Organization. Used well, they help staff work faster, write more clearly, and serve the community better. Used carelessly, they can expose private information, produce inaccurate or biased results, or create legal and privacy problems for the Organization and the affiliated Foundation.

This policy explains, in clear terms, how the Organization \-- and the affiliated Foundation operating on Organization infrastructure \-- uses AI responsibly: what is allowed, what is not, who is responsible, and how to protect the personal and confidential information the Organization handles. It applies to all AI tools across the Organization, not just Microsoft Copilot, and covers both standalone AI services (like chatbots) and AI features built into business applications staff already use (like meeting note-taking, document Q&A, or marketing-design tools).

It works alongside the Organization\'s existing Cyber Security Policy and the Employee Handbook. The goal is simple \-- let staff enjoy the benefits of AI while keeping the public\'s information safe and keeping the Organization\'s decisions accountable to people, not machines.

**[1. PURPOSE]{.underline}**

This policy establishes a flexible governance structure for AI systems used by, or on behalf of, a mid-sized California public-sector agency ("the Organization") and the affiliated Foundation operating on Organization infrastructure. This policy enables the Organization to use AI systems for the benefit of the community while safeguarding against potential harms.

The key objectives of the AI Policy are to:

- Provide guidance that is clear, easy to follow, and supports decision-making for the staff (full-time, part-time), interns, consultants, contractors, partners, volunteers, and the affiliated Foundation personnel operating on Organization infrastructure who may be purchasing, configuring, developing, operating, or maintaining the Organization\'s AI systems or leveraging AI systems to provide services to the Organization.

- Ensure that when using AI systems, the Organization or those operating on its behalf adhere to the Guiding Principles that represent values with regards to how AI systems are purchased, configured, developed, operated, or maintained.

- Define roles and responsibilities related to the Organization\'s usage of AI systems.

- Establish and maintain processes to assess and manage risks and values presented by AI systems used by the Organization.

- Align the governance of AI systems with existing data governance, security, and privacy measures in accordance with the Organization Employee Handbook.

- Define prohibited uses of AI systems, including the use of unsanctioned consumer AI tools.

- Establish a documented procurement and approval workflow for new AI tools.

- Establish "sunset" procedures to safely retire AI systems that no longer meet the needs of the Organization.

- Define how AI systems may be used for legitimate Organization purposes in accordance with applicable local, state, and federal laws, and existing agency policies.

The Organization defines "artificial intelligence" or "AI" to be a machine-based system that can, for a given set of human-defined objectives, make predictions, recommendations, or decisions influencing real or virtual environments. AI systems use machine- and human-based inputs to perceive real and virtual environments; abstract such perceptions into models through analysis in an automated manner; and use model inference to formulate options for information or action.

The Organization defines an "AI system" to be any data system, software, hardware, application, tool, or utility that operates in whole or in part using AI. This definition covers three categories of AI the Organization encounters:

- **Standalone generative AI tools** \-- chatbots, image generators, code assistants, and similar services accessed directly by users (e.g., Microsoft 365 Copilot Chat, ChatGPT, Google Gemini).

- **Embedded AI features in approved business applications** \-- AI capabilities built into platforms the Organization already uses (e.g., Microsoft 365 Copilot in Word and Excel, Zoom AI Companion for meeting notes, Adobe Acrobat AI Assistant, Canva AI for design, FreshService AI for helpdesk tickets, Bonterra "Que" for CRM analysis).

- **High-risk decision-support AI** \-- systems that make or materially inform decisions about identifiable individuals (e.g., wealth-screening tools such as Wealth Engine, volunteer-matching or background-check-integrated systems such as Civic Champs).

**Operational scope.** For the next two to three years, the Organization\'s operational monitoring and enforcement focus is narrowed to generative AI tools and high-risk AI systems \-- those that process Organization PII or sensitive data, or that materially affect public services. The broad definition above is retained for governance coverage; this narrowed operational focus determines which tools are actively monitored and which activities are flagged.

Embedded AI features in approved business applications remain in scope for governance and for the sanctioned-tools list (Section 11), but are not the primary target of active endpoint monitoring. Each embedded-AI feature is reviewed and recorded on the sanctioned-tools list with any conditions that apply to its use.

**[2. SCOPE]{.underline}**

This policy applies to:

- All AI systems deployed by the Organization or on the Organization\'s behalf;

- Staff (full-time, part-time), interns, consultants, contractors, partners, and volunteers who may be purchasing, configuring, developing, operating, or maintaining the Organization\'s AI systems or who may be leveraging AI systems to provide services to the Organization; and

- **the affiliated Foundation personnel** operating on Organization payroll and using the Organization\'s Microsoft 365 tenant. The Foundation is a separate California 501(c)(3); this policy reaches Foundation personnel\'s use of AI tools on Organization infrastructure. The Foundation signs its own contracts and Data Processing Agreements for Foundation-procured AI tools and bears the associated statutory data-protection obligations as a separate legal entity. The IT Manager reviews any Foundation-procured tool used on Organization infrastructure or with Organization data under the AI Review (Section 5) before use.

**[3. GUIDING PRINCIPLES FOR RESPONSIBLE AI SYSTEMS]{.underline}**

These principles describe the Organization\'s values with regards to how AI systems are purchased, configured, developed, operated, or maintained.

**3.1 Human-Centered Design**

AI systems are developed and deployed with a human-centered approach that evaluates AI-powered services for their impact on the public.

**3.2 Security and Safety**

AI systems maintain confidentiality, integrity, and availability through safeguards that prevent unauthorized access and use. Implementation of AI systems is reliable and safe, and minimizes risks to individuals, society, and the environment.

**3.3 Privacy**

Privacy is preserved in all AI systems by safeguarding personally identifiable information (PII) and other sensitive data from unauthorized access, disclosure, and manipulation.

The Organization classifies data as **Internal** or **Confidential** under the Cyber Security Policy, and AI systems must handle data according to that classification. **Confidential data** \-- information that could create legal, financial, or security risk if disclosed \-- includes, but is not limited to:

- Names, addresses, phone numbers, email addresses, and Social Security numbers

- Financial data such as bank account numbers, credit card information, and payroll records

- Donor and prospect financial profiles, giving histories, and any data derived from third-party wealth-screening or data-broker services

- Protected health information (PHI) including medical records and health plan data

- Legal records, attorney-client privileged communications, and litigation materials

- Employee personnel records and performance evaluations

- Minors\' personal information subject to COPPA or state equivalent protections, including any volunteer records, waivers, or background-check status involving minors

**3.4 Transparency**

The purpose and use of AI systems is proactively communicated and disclosed to the public. An AI system, its data sources, operational model, and policies that govern its use are understandable and documented.

**Transparency in practice \-- AI meeting note-taking.** Where an AI tool records, transcribes, or summarizes a meeting (for example, Zoom AI Companion or equivalent), all participants must be informed at the start of the meeting that AI note-taking is in use. AI note-taking must not be enabled for personnel-action meetings, closed-session discussions, attorney-client privileged conversations, or donor-strategy meetings. Retention of AI-generated meeting summaries must align with the Organization\'s records-retention schedule (see Section 8).

**3.5 Equity**

AI systems support equitable outcomes for everyone. Bias in AI systems is effectively managed with the intention of reducing harm for anyone impacted by its use.

**3.6 Accountability**

Roles and responsibilities govern the deployment and maintenance of AI systems, and human oversight ensures adherence to relevant laws and regulations.

**3.7 Effectiveness**

AI systems are reliable, meet their objectives, and deliver precise and dependable outcomes for the utility and contexts in which they are deployed.

**3.8 Workforce Empowerment**

Staff are empowered to use AI in their roles through education, training, and collaborations that promote participation and opportunity.

**[4. ROLES AND RESPONSIBILITIES]{.underline}**

Several roles are responsible for enforcing this policy, outlined below.

- **IT Manager:** The IT Manager is responsible for directing Organization technology resources, policies, projects, services, and coordinating the same with other Organization departments. The IT Manager shall actively ensure AI systems are used in accordance with the Organization\'s Cyber Security Policy.

 - The IT Manager also oversees the Organization\'s cybersecurity operations, security policy updates, and policy compliance monitoring. The IT Manager coordinates the review of AI systems used by the Organization and oversees the security practices of AI systems used by or on behalf of Organization departments.

 - The IT Manager serves as the primary point of contact for AI governance decisions, including functions that may be designated as CISO or Chief AI Officer in other organizations.

 - **The IT Manager holds final approval authority** for all AI tool procurement, trials, and deployments under the workflow in Section 5.

- **Department Directors:** Department Directors are responsible for the first-gate departmental review of AI tool requests originating in their department. A Director\'s approval indicates the proposed AI tool aligns with the department\'s business need and that the Director has confirmed the request belongs in the AI Review process. Director approval does not by itself authorize use; the IT Manager\'s final approval is required.

- **Organization departments:** Organization departments are responsible for following this policy and following updates to this policy and the Organization Employee Handbook and shall check compliance with these documents at least annually.

- **Policy updates:** The IT Manager shall notify Organization departments when an update to this policy is released.

- **Organization\'s Legal Counsel:** Organization\'s Legal Counsel is responsible for advising of any legal issues or risks associated with AI systems usage by or on behalf of Organization departments. Legal Counsel determinations are documented on the AI FactSheet (Appendix A.8) for tools flagged as high-risk during AI Review.

- **General Manager Office:** The General Manager Office may, at its discretion, inspect the usage of AI systems and require a department to alter or cease its usage of AI systems or a partner\'s usage of AI systems on behalf of the department.

- **Finance Department:** The Finance Department oversees purchasing and procurement execution for AI systems (purchase orders and contract execution) in alignment with existing Organization procurement processes. AI-specific vendor requirements \-- completion of the AI FactSheet and compliance with Organization AI policy standards \-- are coordinated by the IT Manager under the AI Review (Section 5). All AI tool procurement requires IT Manager approval prior to purchase under the workflow in Section 5.

- **the affiliated Foundation Director of Strategic Partnerships and Philanthropy:** The Foundation\'s Director of Strategic Partnerships and Philanthropy is the point of contact for AI tools procured by the Foundation as a separate legal entity. The Foundation signs its own contracts and Data Processing Agreements for Foundation-procured tools and bears the associated data-protection obligations as a separate legal entity. Where such a tool is used on Organization infrastructure or with Organization data, the IT Manager reviews it under the AI Review process before use.

**[5. POLICY]{.underline}**

When purchasing, configuring, developing, operating, or maintaining AI systems, the Organization will:

1. Uphold the Guiding Principles for Responsible AI Systems (Section 3).

2. Conduct an AI Review to assess the potential risk of AI systems. The IT Manager is responsible for coordinating review of AI systems used by the Organization.

3. Obtain technical documentation about AI systems using the AI FactSheet \-- a recommended vendor-questionnaire template is provided in Appendix A \-- or create equivalent documentation if internally developing the AI system. The IT Manager is responsible for requiring vendors to complete the AI FactSheet.

4. Require contractors to comply with applicable Organization policies and contractual requirements governing AI systems, overseen by the IT Manager.

5. In the event of an incident involving the use of an AI system, the Organization will follow established incident response procedures. A recommended AI Incident Response Plan outline is provided in Appendix B; in the interim, AI-related incidents are handled through existing IT incident response procedures under the Cyber Security Policy. The IT Manager is responsible for overseeing the security practices of AI systems used by or on behalf of Organization departments.

6. Require IT Manager approval for all AI tool procurement and deployment. No AI tool, service, or subscription may be purchased, trialed (including free trials, free tiers, or personal-account use for Organization business), or deployed without completing the AI Tool Approval Workflow below and receiving documented IT Manager approval.

**5.1 AI Tool Approval Workflow (Director to IT Manager)**

All new AI tool requests follow a two-gate approval process before any procurement, trial, free-tier sign-up, or deployment may occur.

**Gate 1 \-- Department Director approval.** The requesting staff member submits an AI Tool Change Request (see the Change Request \-- Sanctioned AI Tool Addition template) to their Department Director. The Director confirms the proposed tool aligns with a department business need and approves the request to proceed to AI Review. Director approval is required for both paid procurement and any free-tier or trial use.

**Gate 2 \-- IT Manager final approval.** The approved Change Request is forwarded to the IT Manager, who coordinates the AI Review (Section 5.2), routes high-risk tools to Legal Counsel where required, and issues the final approval decision: **approve**, **approve with conditions**, or **deny**. The decision and any conditions are recorded on the AI FactSheet (Appendix A.8) and the tool is added to the sanctioned-tools list in Section 11.

**No purchase, trial, sign-up, or deployment of any AI tool may occur before Gate 2 is complete.** This includes free-tier and personal-account use of AI services for Organization business; see Section 6.3.

**5.2 AI Review**

The AI Review is the IT Manager\'s risk assessment of the proposed tool against this policy, the AI FactSheet questions (Appendix A), the Cyber Security Policy data classification, and any tool-specific concerns (e.g., data-broker status, location-data collection, COPPA implications for tools touching minors\' data, CCPA "sharing/sale" exposure for tools that ingest Organization PII). High-risk tools \-- defined as tools touching Confidential data, profiling identifiable individuals, operating as a third-party data broker, or making or materially informing decisions about individuals \-- are routed to Legal Counsel for determination before sanctioning.

**[6. PROHIBITED USES]{.underline}**

The use of certain AI systems is prohibited due to the sensitive nature of the information processed and the severe potential for harm. The prohibited uses below reflect standard government AI policy best practices recommended by the GovAI Coalition; they are included to establish comprehensive governance guardrails regardless of the Organization\'s current operations. Prohibited purposes include:

- Real-time and covert biometric identification.

- Classification of human facial or body movements into certain emotions or sentiment with the use of computer vision techniques or emotion analysis (e.g., positive, negative, neutral, happy, angry, nervous).

 - This prohibition applies to systems that use emotion or sentiment classification to make or inform decisions about individuals. Incidental features embedded in approved platforms (such as gesture-based emoji reactions in Microsoft Teams) that do not store, report, or act on behavioral data are not within its scope.

- Fully automated decisions that do not require any meaningful human oversight but substantially impact individuals. This includes automated decisions affecting employment, benefits eligibility, permit approvals, or access to Organization services where no human review occurs before the decision takes effect.

- Social scoring, or the use of AI systems to track and classify individuals based on their behaviors, socioeconomic status, or personal characteristics.

- Cognitive behavioral manipulation of people or specific vulnerable groups.

- Autonomous weapons systems.

**6.1 Confidential Information in AI Systems**

Organization staff and the affiliated Foundation personnel operating on Organization infrastructure must not input, upload, paste, or otherwise provide **Confidential data** (as classified under the Cyber Security Policy, ) to any AI system that has not been explicitly sanctioned by the Organization and configured to handle such data. Confidential data includes, but is not limited to:

- **Personally Identifiable Information (PII):** Information that can be used to identify an individual, including names, Social Security numbers, driver\'s license numbers, addresses, phone numbers, email addresses, dates of birth, and biometric data.

- **Protected Health Information (PHI):** Health-related information subject to HIPAA or state health privacy laws, including medical records, health plan enrollment data, and disability or accommodation records.

- **Financial Data:** Bank account numbers, credit card numbers, payroll data, tax records, vendor payment information, and budget documents marked as confidential.

- **Donor and Prospect Financial Profiles:** Donor giving histories, prospect financial profiles, and any data derived from third-party wealth-screening or data-broker services.

- **Legal Records:** Attorney-client privileged communications, litigation materials, personnel investigations, and records subject to legal hold.

- **Personnel Records:** Employee evaluations, disciplinary records, salary information, and other confidential HR data.

- **Minors\' Records:** Volunteer records, waivers, background-check status, or any other records identifying minors, subject to COPPA or state equivalent protections.

**External sharing of PII to AI tools.** Uploading Organization or Foundation lists of identifiable individuals (donor lists, prospect lists, volunteer rosters, customer lists, employee rosters, etc.) to any AI tool may constitute "sharing" or "sale" of personal information under the California Consumer Privacy Act / California Privacy Rights Act (CCPA/CPRA). Before such uploads, the receiving tool must be sanctioned under Section 5, the vendor\'s data-broker status and CCPA terms must be reviewed by Legal Counsel, and the data-handling terms must be confirmed on the AI FactSheet (Appendix A).

If staff are uncertain whether information is Internal or Confidential, they should treat it as Confidential and consult with their supervisor or the IT Manager before using it in any AI system.

**6.2 Staff Responsibilities for AI-Generated Content**

Organization staff and Foundation personnel who use AI tools to assist in creating work products are responsible for the quality, accuracy, and appropriateness of the final output. Staff must:

- Fact-check AI-generated content against reliable sources before publishing, distributing, or acting on it.

- Review and edit all AI-generated text, analysis, or recommendations for accuracy, completeness, and tone appropriate to Organization communications.

- Verify that AI-generated content does not infringe on copyright or intellectual property rights.

- Ensure that AI-assisted work products meet the same quality standards as work produced without AI assistance.

If Organization staff or Foundation personnel become aware of an instance where an AI system has caused harm, they must report the instance to their supervisor and the IT Manager.

**6.3 Use of Unsanctioned Consumer AI Tools**

The use of unsanctioned consumer AI tools for any Organization or Foundation business is prohibited. This prohibition specifically covers:

- Free, personal, or consumer tiers of generative AI chatbots and assistants (including, but not limited to, the free, personal, or Plus tiers of ChatGPT, Google Gemini, Claude.ai, Microsoft Copilot consumer, Perplexity, and equivalent generative AI services not on the Organization\'s sanctioned-tools list).

- Any AI tool, service, or subscription that has not completed the AI Tool Approval Workflow (Section 5.1) and been added to the sanctioned-tools list.

- Personal-account access (using a staff member\'s personal credentials or personal email address) to any AI service used for Organization or Foundation business, regardless of the service\'s commercial tier.

This prohibition is in addition to, and reinforces, the Confidential-data prohibition in Section 6.1: even non-Confidential Organization business may not be conducted through an unsanctioned consumer AI tool.

**This prohibition does not apply to** AI tools on the sanctioned-tools list (see Section 11), including Microsoft 365 Copilot, Microsoft 365 Copilot Chat, and other tools that have been approved through the AI Review process. Where a vendor offers both a consumer tier and an enterprise tier, only the specific sanctioned tier is permitted \-- generic vendor names ("ChatGPT," "Gemini") do not authorize use; the specific tier sanctioned on the approved-tools list does.

Violations of this section are subject to the disciplinary provisions in Section 9.1.

**[7. SUNSET PROCEDURES]{.underline}**

If an AI system operated by the Organization or on its behalf ceases to provide a positive utility to the Organization\'s employees as determined by the IT Manager, then the use of that AI system must be halted unless express exception is provided by the General Manager. If the abrupt cessation of the use of that AI system would significantly disrupt the delivery of Organization services, usage of the AI system shall be gradually phased out over time.

**[8. PUBLIC RECORDS]{.underline}**

The Organization is subject to the California Public Records Act (CPRA). Organization staff must follow all current procedures for records retention and disclosure.

**AI artifacts as Organization records.** Records generated by, submitted to, or derived from AI systems used by the Organization \-- including but not limited to:

- Prompts and queries submitted by staff to AI tools;

- Chat histories with AI assistants;

- AI-generated meeting summaries, transcriptions, and notes (including Zoom AI Companion outputs, Microsoft 365 Copilot meeting recaps, and equivalent);

- AI-generated drafts, analyses, recommendations, and decision-support outputs incorporated into Organization work products;

- AI tool audit logs maintained by sanctioned tools

\-- may constitute Organization records subject to disclosure under the CPRA. Staff must follow current procedures for records retention and disclosure as applied to these AI artifacts. Where a sanctioned AI tool offers configurable retention settings (for example, Zoom AI Companion meeting-summary retention periods), the IT Manager will set the retention period to align with the Organization\'s records-retention schedule. The retention configuration for each sanctioned tool is documented on its AI FactSheet (Appendix A).

**[9. POLICY ENFORCEMENT]{.underline}**

All employees and agents of the Organization, whether permanent or temporary, interns, volunteers, contractors, consultants, vendors, and other third parties operating AI systems on behalf of the Organization, as well as the affiliated Foundation personnel operating on Organization infrastructure, are required to abide by this Policy and the Organization Employee Handbook. The Organization does not currently have a separate AI Governance Manual; until one is adopted, this policy serves as the primary governance document. A recommended AI Governance Manual outline is provided in Appendix C.

**9.1 Violations of the AI Policy**

Violations of any section of the AI Policy, including failure to comply with the Organization Employee Handbook as it relates to AI usage, may be subject to disciplinary action, up to and including termination. Violations by a third party operating an AI system on behalf of the Organization constitute a breach of contract and may result in pursuit of damages, termination, or both, at the Organization\'s sole discretion. Infractions that violate local, state, federal or international law may be referred to the proper authorities.

**9.2 Annual Policy Review**

This policy shall be reviewed at least annually by the IT Manager to ensure it remains current with evolving AI technologies, regulatory requirements, and Organization operations. The annual review date and any changes made shall be documented.

**[10. EXCEPTIONS]{.underline}**

Staff, as described in the scope of this policy, must adhere to all controls outlined in this policy document unless a specific documented exception is explicitly granted by the IT Manager. Policy violations that have not been formally documented as an exception will be treated as a security incident in accordance with Organization policy.

Organization staff or departments may encounter emergency situations that necessitate the immediate use of AI tools or technologies. In these circumstances, each incident use case must obtain documented approval via the Department Director or IT Manager prior to use. In such situations, the department must submit the approved use case to the IT Manager for review within 30 days of the incident.

**[11. RESTRICTED PLATFORM ALTERNATIVES]{.underline}**

Any AI tool not explicitly listed as sanctioned below is considered unsanctioned and requires approval from the IT Manager (and the Department Director as the first gate) before use, per the AI Tool Approval Workflow in Section 5.1. **Consumer / free / personal tiers of generative AI tools are prohibited under Section 6.3** \-- the unsanctioned status reflected here for those tiers is reinforced by that prohibition. No employee or Foundation staff member may use an AI tool for Organization or Foundation business until it has been reviewed and approved through the process described in Sections 5 and 5.1.

In the event that the Organization restricts access to certain AI platforms, whenever practicable, the Organization will provide employees with information about approved alternative platforms. A remote-accessible redirect page for blocked AI platforms is a planned future IT initiative; in the interim, employees should consult the sanctioned-tools list in this section or contact the IT Manager for approved alternatives.

**Sanctioned AI Tools**

The sanctioned-tools list below is the authoritative list at the time of this policy\'s publication. Updates to the sanctioned-tools list between policy revisions will be communicated by the IT Manager per Section 4.

 -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Tool** **Tier / access** **Conditions** **Notes**
 ------------------------------------------- -------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------
 **Microsoft 365 Copilot** Licensed add-on (paid Copilot license on qualifying Organization M365 plan) Use within the Organization\'s M365 GCC tenant. Confidential data permitted per the Organization\'s GCC compliance boundary. The full Copilot assistant inside Word, Excel, PowerPoint, Outlook, and Teams.

 **Microsoft 365 Copilot Chat** Included for eligible staff (no Copilot add-on required for chat; in-app experience requires paid Copilot license) Use within the Organization\'s M365 GCC tenant. A secure chat assistant (at copilot.microsoft.com) with Organization data protection, at no extra cost to eligible staff.

 **Microsoft Copilot Studio** Authorized staff (IT-managed) Use within the Organization\'s M365 GCC tenant. IT approval required for each custom agent or workflow. No Confidential data in agents that call external services. Low-code tool for building custom AI agents and workflows.

 **Microsoft Security Copilot** IT staff (IT-managed) Use within the Organization\'s M365 GCC tenant. Security operations use only. AI assistant for security operations.

 **Microsoft Designer** Staff with an eligible Organization M365 account Use within the Organization\'s M365 GCC tenant. No Confidential data in prompts (Section 6.1); review outputs before use (Section 6.2). AI image and design generation.

 **Microsoft Image Creator (in Designer)** Staff with an eligible Organization M365 account Use within the Organization\'s M365 GCC tenant. No Confidential data in prompts (Section 6.1); review outputs before use (Section 6.2). AI image generation within Designer.

 **Canva AI** Organization subscription (Canva for Teams) Canva for Teams; staff use only (not contractors or volunteers). Standard sanction. AI FactSheet on file. AI design and generation features inside the Organization\'s Canva subscription.

 **Placer AI** Organization subscription **Sanctioned with conditions.** Location-data and aggregation-data handling reviewed; no upload of Organization PII; use limited to publicly available and aggregated location-analytics data. Location-analytics platform. Closer scrutiny than other embedded-AI tools due to location-data sensitivity.

 **Adobe Acrobat AI Assistant** Organization Adobe Acrobat subscription **Sanctioned with conditions.** Do not use the AI Assistant prompt on PDFs containing Confidential data; dismiss the prompt where it appears on such documents. AI document Q&A and summary feature in Adobe Acrobat.

 **Zoom AI Companion** Organization Zoom enterprise tier **Sanctioned with conditions.** Enterprise-tier privacy settings and zero-retention configuration required. **Participant notification of AI note-taking is required at the start of each meeting** (see Section 3.4). Do not enable for personnel-action meetings, closed-session discussions, attorney-client privileged conversations, or donor-strategy meetings. Summary retention configured to align with the Organization\'s records-retention schedule (Section 8). Meeting transcription and summarization.

 **FreshService AI** Organization FreshService subscription **Available, not active.** Freddy AI features are available in the Organization\'s FreshService subscription but are not currently enabled; IT review required before enabling. Employee PII in helpdesk tickets handled per Section 6.1. AI features in the IT helpdesk ticketing system.

 **Bonterra "Que" (Network for Good)** Foundation subscription Standard sanction with DPA confirmation. AI FactSheet on file. Contracting entity: the affiliated Foundation. CRM reports / forecasts for Foundation donor and constituent records.

 **Civic Champs** Foundation subscription **Sanctioned with conditions.** Volunteer PII, background-check status, and any records involving minors (COPPA / state-equivalent) handled per Section 3.3 and 6.1. Human oversight of any AI-driven volunteer matching or automated messaging. Contracting entity: the affiliated Foundation. Volunteer management with AI-driven matching and messaging.
 -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Tools in AI Review \-- Pending Legal Counsel Determination**

The following tools have been flagged as high-risk during AI Review and routed to Legal Counsel under Section 5.2. They are neither sanctioned nor outright prohibited and must not be used for new Organization or Foundation business until Legal Counsel returns a determination, recorded on the AI FactSheet (Appendix A.8).

 -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Tool** **Reason for Legal review** **Interim status**
 --------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Wealth Engine (Altrata)** Operates as a third-party data broker (registered under California\'s data-broker statute / Delete Act); profiles identifiable individuals using aggregated personal and financial data; CCPA / CPRA "sharing/sale" implications when uploading donor or prospect lists. **In AI Review \-- Pending Legal.** Foundation use paused pending determination.

 **ChatGPT (specific tier TBD)** Consumer / free / Plus tiers prohibited under Section 6.3. A business, Team, or Enterprise tier with executed Data Processing Agreement, training opt-out, and Organization-approved data-handling terms may be sanctionable \-- pending Legal Counsel review of the specific tier, DPA, and contracting entity (Organization or Foundation). **In AI Review \-- Pending Legal.** No Organization or Foundation business may be conducted via any ChatGPT tier until a specific tier is sanctioned. Consumer-tier use prohibited under Section 6.3.
 -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Unsanctioned AI Tools**

All AI tools not explicitly listed above as sanctioned are considered unsanctioned. **Consumer / free / personal tiers of generative AI tools are prohibited under Section 6.3.** Other unsanctioned AI tools (including non-consumer tools the Organization has not yet reviewed) require the AI Tool Approval Workflow in Section 5.1 before use. Generative AI applications, including consumer versions of tools such as ChatGPT, Google Gemini, Claude.ai, and other third-party AI services, have been identified and tagged in the Organization\'s cloud security environment.

Current enforcement status:

- **Monitoring:** AI usage monitoring is active via browser extensions deployed to managed Windows devices. The Organization\'s cloud security environment provides additional visibility into application access patterns.

- **Endpoint enforcement:** Endpoint-level enforcement capabilities are being evaluated. Enforcement status will be updated as the Organization\'s security configuration is finalized.

The purpose of these controls is to help prevent Organization data from being shared with unauthorized platforms, in keeping with the Organization\'s Electronic Media Policy, the Information Access Policy, and the Cyber Security Policy. This approach allows employees to choose amongst various platforms which meet applicable privacy and security standards established by the Organization to facilitate productivity.

The IT Manager will designate a department to perform regular assessments of AI platforms and to regularly monitor such platforms so that the Organization can restrict and remove access in the event of a security or privacy incident.

The specific technical controls, licensing dependencies, and platform constraints behind this monitoring and enforcement are maintained as a separate technical reference for the Organization's IT.

**[12. TERMS AND DEFINITIONS]{.underline}**

**Artificial Intelligence:** "Artificial intelligence" or "AI" is a machine-based system that can, for a given set of human-defined objectives, make predictions, recommendations, or decisions influencing real or virtual environments. Artificial intelligence systems use machine- and human-based inputs to perceive real and virtual environments; abstract such perceptions into models through analysis in an automated manner; and use model inference to formulate options for information or action.

**AI system:** Any data system, software, hardware, application, tool, or utility that operates in whole or in part using AI. (See Section 1 for the full definition and the three operational categories: standalone generative AI, embedded AI features, and high-risk decision-support AI.)

**Embedded AI:** AI capabilities built into platforms the Organization already uses, where the AI is one feature of a broader business application rather than the application\'s primary function (e.g., AI summary in Adobe Acrobat, AI note-taking in Zoom, AI design assistance in Canva, AI prediction in Bonterra). Embedded-AI features are in scope of this policy and recorded on the sanctioned-tools list in Section 11.

**Generative AI:** A category of AI systems that create new content such as text, images, code, audio, or video in response to user prompts. Examples include chatbots, text generators, image generators, and code assistants.

**High-risk AI:** An AI system that processes Confidential data, profiles identifiable individuals, operates as a third-party data broker, or makes or materially informs decisions about individuals. High-risk AI systems are routed to Legal Counsel during AI Review (Section 5.2) before sanctioning.

**AI artifact / AI-generated record:** Any record generated by, submitted to, or derived from an AI system in the course of Organization or Foundation business, including prompts, chat histories, AI-generated meeting summaries, AI-generated drafts and analyses, and AI tool audit logs. AI artifacts may constitute Organization records subject to disclosure under the California Public Records Act (see Section 8).

**Consumer AI tool / consumer-tier AI:** A free, personal, or consumer-tier AI service offered by a vendor that does not include enterprise-grade data-protection terms (Data Processing Agreement, training opt-out, admin controls, audit logging, retention configuration). Examples include the free, personal, and Plus tiers of ChatGPT, Google Gemini, Claude.ai, and Microsoft Copilot consumer. Consumer AI tools are prohibited for Organization and Foundation business under Section 6.3.

**the affiliated Foundation:** The Organization\'s Foundation, a separate California 501(c)(3) public-benefit corporation that supports the Organization. Foundation personnel operating on Organization payroll and using the Organization\'s Microsoft 365 tenant are in scope of this policy; the Foundation signs its own contracts and DPAs for Foundation-procured AI tools as a separate legal entity, and the IT Manager reviews any such tool used on Organization infrastructure or with Organization data under the AI Review (Section 5).

**Internal data:** Information intended for Organization employees, contractors, and authorized personnel only. Unauthorized disclosure may cause operational disruption but does not pose a critical risk. (Per the Cyber Security Policy.)

**Confidential data:** Sensitive information that, if disclosed, could result in legal, financial, or security risk; access is restricted to authorized personnel. Includes PII, PHI, financial, donor/prospect financial, legal, personnel, and minors\' records. (Per the Cyber Security Policy.)

**Personally Identifiable Information (PII):** Information that can be used to identify an individual, including but not limited to names, Social Security numbers, addresses, phone numbers, email addresses, dates of birth, driver\'s license numbers, and biometric data.

**Protected Health Information (PHI):** Health-related information protected under HIPAA or state health privacy laws, including medical records, health plan data, and disability or accommodation records.

**Microsoft 365 Copilot:** Microsoft\'s AI assistant built into Word, Excel, Teams, Outlook, and other Microsoft 365 applications, available as a licensed add-on. It operates within the Organization\'s protected Microsoft 365 environment.

**Microsoft 365 Copilot Chat:** A secure AI chat tool available at no additional cost to eligible Organization staff, with Organization data protection. It does not require a paid Copilot add-on license; the full in-app experience does.

**Sanctioned AI tool:** A specific AI tool, at a specific tier, that has been reviewed, approved, and authorized for use by Organization staff or Foundation personnel in accordance with this policy. Generic vendor names ("ChatGPT," "Gemini") do not constitute sanction; sanction applies to the specific tier and configuration approved through the AI Tool Approval Workflow (Section 5.1).

**Unsanctioned AI tool:** An AI tool that has not been approved for use under this policy. Access may be monitored and/or blocked via the Organization\'s cloud security and endpoint protection systems. Use of consumer / free / personal tiers of generative AI tools for Organization or Foundation business is specifically prohibited under Section 6.3.

**AI Review:** The IT Manager\'s risk assessment of a proposed AI tool against this policy, conducted as Gate 2 of the AI Tool Approval Workflow (Section 5.1). High-risk tools are routed to Legal Counsel under Section 5.2 before sanctioning.

**AI Tool Approval Workflow:** The two-gate Director to IT Manager approval process required before any AI tool may be procured, trialed, or deployed for Organization or Foundation business (Section 5.1).

**[13. ACKNOWLEDGEMENT]{.underline}**

This policy was adapted from a publicly available AI policy template developed by the GovAI Coalition and customized for a mid-sized California public-sector agency by the advisory firm. Version 0.4 reflects the CO-1 expansion to cover all Organization AI tools, integrate the affiliated Foundation, add a procurement approval workflow, and prohibit unsanctioned consumer AI tools.

**Approved:**

IT Manager Date: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Approved for posting:**

Director of Employee Relations / HR Date: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**[RECOMMENDED FUTURE GOVERNANCE DOCUMENTS]{.underline}**

Documents referenced in this policy that do not yet exist are recommended as the Organization\'s AI governance program matures. Recommended templates and outlines are provided in the AI Policy Appendices:

- **AI FactSheet** \-- vendor questionnaire template for AI procurement evaluations (Appendix A)

- **AI Incident Response Plan** \-- procedures for responding to AI-related security or operational incidents (Appendix B)

- **AI Governance Manual** \-- comprehensive procedures for AI review, approval, and ongoing oversight (Appendix C)

- **AI Governance Committee charter** \-- if leadership elects to establish a formal review body

- **AI Governance Handbook for Leadership** \-- the non-technical leadership-facing companion to this policy (CO-1 D4)
