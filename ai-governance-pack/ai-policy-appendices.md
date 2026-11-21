**AI Policy \-- Appendices**

**Recommended Governance Templates**

**Companion to:** Artificial Intelligence (AI) Policy

**Version:** 0.3 (draft)

**Last updated:** 2026-06-14

**Prepared by:** Laura Rowe

***Advisory only** \-- per SOW SS2.2 and SS5, the advisory firm does not create or enforce policy. Organization owns adoption, review, and enforcement.*

These appendices hold the recommended templates and outlines referenced from the AI Policy body. They are starting points for the Organization to adopt and complete \-- not finished, enforceable instruments. They were separated from the policy so the policy itself stays concise.

**[APPENDIX A: AI FACTSHEET (RECOMMENDED VENDOR QUESTIONNAIRE)]{.underline}**

A questionnaire the Organization (Finance + IT Manager) can require a vendor to complete before an AI tool is procured or deployed, supporting the AI Review in Policy Section 5.2. Capture one FactSheet per AI system.

**A.1 System and vendor identification**

- AI system / product name and version

- Vendor / developer name and primary contact

- Hosting model (vendor SaaS, Organization tenant, on-premises, hybrid)

- Is the system, or any sub-processor, inside the Organization\'s Microsoft 365 GCC compliance boundary?

**A.2 Purpose and intended use**

- Business purpose and the Organization department(s) that will use it

- Categories of users (staff, contractors, public, the affiliated Foundation personnel)

- Is this generative AI, predictive/decision AI, or an embedded AI feature? (See Policy Section 1 three-category framework.)

- Does the system inform or make decisions that affect individuals (employment, benefits, permits, access to services)?

**A.3 Data handling**

- Categories of Organization data the system will process (note any PII, PHI, financial, donor/prospect, legal, personnel, or minors\' data per Policy Section 6.1)

- Are Organization inputs/outputs used to train or improve the vendor\'s models? Can this be disabled?

- Data retention period and deletion process

- Data residency / storage location(s) and any sub-processors

- Encryption at rest and in transit

- Does the tool ingest or rely on third-party data that may originate from data brokers? (See Policy Section 6.1.)

**A.4 Security and access**

- Authentication and access-control model (SSO/SAML, MFA, role-based access)

- Independent security attestations (SOC 2 Type II, ISO 27001, FedRAMP, StateRAMP, etc.)

- Breach notification commitments and timelines

- Logging and audit capabilities available to the Organization

**A.5 Model, transparency and limitations**

- Model type / underlying foundation model(s)

- Known limitations, error modes, and documented bias/fairness testing

- Explainability: can the system\'s outputs be explained or sourced?

**A.6 Human oversight**

- Where in the workflow does a human review or approve outputs before action?

- Can fully automated decision-making be disabled (per the Policy Section 6 prohibition)?

**A.7 Compliance and contractual**

- Data Processing Agreement (DPA) available? CPRA / California public-agency terms?

- Compliance with the California Public Records Act for records the system generates or stores (see Policy Section 8, including AI artifacts)

- Contractual commitment to Organization policy standards (Policy Section 4)

- California data-broker registration status of the vendor and its material data suppliers (see Policy Section 6.1)

- Contracting entity: Organization or the affiliated Foundation? (See Policy Section 2 Foundation coverage.)

**A.8 AI Review outcome (IT Manager use)**

- Risk tier assigned (per Policy Section 1 three-category framework)

- Reviewed by / date

- Decision (approve / approve with conditions / deny)

- Conditions

- Re-review date

- Legal Counsel routing: was this tool flagged as high-risk and routed to Legal under Policy Section 5.2? If yes, record Legal determination.

**[APPENDIX B: AI INCIDENT RESPONSE PLAN (RECOMMENDED OUTLINE)]{.underline}**

The Organization does not currently have a dedicated AI Incident Response Plan; in the interim, AI-related incidents are handled through existing IT incident response under the Cyber Security Policy, using the AI Incident Reporting Template to capture the report. The outline below is recommended when the Organization formalizes an AI-specific plan.

- **Purpose & scope** \-- what qualifies as an "AI incident" (data exposure to an unsanctioned tool, harmful or biased output acted upon, automated decision without oversight, model/vendor breach, use of a prohibited consumer AI tool per Policy Section 6.3).

- **Roles & responsibilities** \-- IT Manager (lead), affected department, Department Director, Legal Counsel, General Manager Office, the affiliated Foundation Director of Strategic Partnerships and Philanthropy (for Foundation-related incidents); tie to the roles in Policy Section 4.

- **Detection & reporting** \-- how staff report (supervisor + IT Manager, per Policy Section 6.2), intake via the AI Incident Reporting Template, monitoring signals from the cloud security environment.

- **Triage & classification** \-- severity tiers, data-sensitivity assessment, whether PII/PHI was involved, whether the incident involves a consumer AI tool or an unsanctioned tool.

- **Containment** \-- revoke access, block the tool, isolate affected data/accounts.

- **Investigation** \-- scope of data exposed, root cause, vendor engagement.

- **Notification** \-- internal escalation, Legal Counsel review, statutory/breach notification obligations (CPRA, affected individuals).

- **Remediation & recovery** \-- corrective actions, policy/control updates, tool re-review.

- **Post-incident review** \-- lessons learned, FactSheet/sanctioned-list updates, documentation for the annual policy review (Policy Section 9.2).

**[APPENDIX C: AI GOVERNANCE MANUAL (RECOMMENDED OUTLINE)]{.underline}**

The Organization does not currently have a separate AI Governance Manual; until one is adopted, the AI Policy serves as the primary governance document. The outline below is recommended when the Organization formalizes a manual.

- **Governance structure** \-- roles from Policy Section 4; optional AI Governance Committee charter and membership.

- **AI Review process** \-- intake via AI Tool Approval Workflow (Policy Section 5.1), FactSheet (Appendix A), risk tiering, approval/denial workflow, Legal Counsel routing for high-risk tools (Policy Section 5.2), documentation.

- **Risk classification** \-- how standalone generative AI vs. embedded AI vs. high-risk decision-support AI are tiered (aligns with the Policy Section 1 three-category framework).

- **Approved-tools register** \-- the sanctioned-tools list in Policy Section 11; change process (see the Change Request \-- Sanctioned AI Tool Addition template).

- **Monitoring & enforcement** \-- what the Organization monitors and how; operational detail held in the internal Technical Controls Appendix.

- **Procurement** \-- Finance Department purchasing process, contractual standards, vendor obligations coordinated with the IT Manager.

- **Training & awareness** \-- onboarding and recurring staff training.

- **Exceptions & emergency use** \-- documentation and review windows (Policy Section 10).

- **Audit & annual review** \-- evidence collection and the annual policy review cadence (Policy Section 9.2).

**[DEFERRED CONSIDERATIONS]{.underline}**

Items raised during drafting that the Organization may revisit later. These are not open decisions for the current leadership review (those are in the cover letter).

- **Section 3.4 Transparency \-- AI-use disclosure on public-facing materials.** Whether to require a statement indicating when AI tools contributed to public-facing documents, reports, or communications. Disposition: not now \-- revisit as the governance program matures. (Related to the staff-side disclosure decision in the cover letter.)
