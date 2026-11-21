**Vendor AI Evaluation Cheat Sheet**

**Purpose:** A structured reference for evaluating any vendor\'s AI features or AI-enabled products before purchase, trial, or contract renewal.

**Audience:** Department directors, purchasing staff, anyone meeting with a vendor whose product may use AI.

**How to use:** Work through the questions with the vendor. Score their answers against the guidance below. Anything in the red-flag column triggers an IT consultation before moving forward.

**Grounding:** NIST AI Risk Management Framework, GovAI Coalition vendor evaluation guidance, California CCPA / CPRA / data-broker requirements.

**Prepared by:** Laura Rowe

**Version:** 1.0

A vendor who cannot answer these questions clearly is not a vendor Organization should onboard for AI use. Before the meeting, scan the question categories. During the meeting, ask the questions \-- don\'t accept "we\'re committed to privacy" as an answer. After the meeting, compare what they said against the red-flag column and forward the vendor\'s written responses (or your notes) to the IT Manager with a change request if you want to move forward.

**[PAGE 1 \-- THE QUESTIONS]{.underline}**

**1. AI Disclosure and Function**

- Is AI used anywhere in your product? If yes, where and for what?

- Is the AI feature on by default, or opt-in? Can it be disabled?

- Did this product have AI features before, or were they added in a recent update?

- Who builds the underlying AI model \-- your company, or a third-party provider (OpenAI, Anthropic, Google, Microsoft, etc.)?

- Will adding new AI capabilities in the future trigger notification to Organization, or does the existing contract cover it automatically?

**2. Data Handling**

- What Organization data flows into the AI feature?

- Is Organization\'s data used to train your AI models \-- now or in the future?

- Is Organization\'s data used to train your AI provider\'s models (e.g., OpenAI\'s models)?

- Where is the AI processing physically happening \-- your servers, a sub-processor\'s servers, US-only, or international?

- How long is Organization\'s data retained by the AI system? Prompts, outputs, logs?

- Is Organization\'s data segregated from other customers\' data, or commingled in shared training/inference pipelines?

**3. Contractual and Compliance Posture**

- Do you have a Data Processing Agreement (DPA), and does it specifically address AI features?

- Will you sign a DPA addendum confirming no training on Organization\'s data?

- Are you SOC 2 Type II audited? Most recent report date?

- Do you comply with CCPA / CPRA? Are you a registered California data broker?

- Do you have a designated subprocessor list, and will you notify Organization of changes?

- What is your incident notification commitment if your AI system or training data is breached?

**4. California and Public Sector Specifics**

- Are you registered with the California data broker registry? (Required if you sell or share personal information about California residents.)

- Have other California special districts, cities, counties, or state agencies deployed your AI features? References?

- Can Organization-generated AI artifacts (prompts, outputs, logs) be produced in response to a California Public Records Act request?

- Are your AI features compliant with California\'s automated decision-making transparency rules (CPRA regulations)?

- If Organization terminates the contract, what happens to data in your AI system \-- deleted, retained, used to train models going forward?

**5. Human Oversight and Control**

- Can an Organization administrator see what prompts users submitted and what outputs they received?

- Can Organization set policies (block certain data types, restrict certain users, audit access)?

- Does the AI make any automated decisions that affect Organization operations, staff, or constituents without human review?

- What\'s the escalation path when the AI produces an incorrect or harmful result?

- Can outputs be flagged, corrected, or removed from the system?

**6. Operational Boundaries**

- What\'s the published accuracy rate of the AI feature? How is it measured?

- What are the documented failure modes \-- situations where the AI is known to perform poorly?

- Is the AI feature classified as "high-risk" under any regulatory framework (EU AI Act, NIST AI RMF, sectoral US rules)?

- How do you handle bias testing? Can you share results?

- What\'s your roadmap for the AI features over the next 12 months?

**[PAGE 2 \-- SCORING GUIDANCE]{.underline}**

For each category above, compare the vendor\'s answers against the columns below. Anything in the right-hand column means stop and consult IT.

**AI Disclosure and Function**

 --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Acceptable** **Caution** **Red Flag**
 ----------------------------------------------------------- -------------------------------------------------------- -----------------------------------------------------------
 Clear, specific list of where AI is used and what it does Vague phrases like "AI-powered" without specifics Vendor cannot or will not confirm whether AI is used

 AI feature is opt-in or can be disabled per organization AI is on by default but can be disabled per user AI cannot be disabled, or vendor "doesn\'t know"

 Vendor names their underlying AI provider "We use industry-standard AI" without naming providers Vendor refuses to disclose the underlying model

 Notification commitment for future AI additions "We\'ll let you know" with no contractual basis Contract gives vendor unilateral right to add AI features
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Data Handling**

 -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Acceptable** **Caution** **Red Flag**
 ----------------------------------------------------------------- -------------------------------------------------- ----------------------------------------------------------
 Contractual commitment: no training on customer data Default no-training but no contractual guarantee Training on customer data is the default, opt-out only

 Processing location specified (US-only, named regions) "Globally distributed" without specifics International processing with no jurisdiction commitment

 Specific retention periods stated (e.g., 30 days, configurable) "As long as needed" or "per business purposes" Indefinite or undisclosed retention

 Customer data segregated and tagged Logical separation in shared systems Commingled in training pipelines
 -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Contractual and Compliance**

 ------------------------------------------------------------------------------------------------------------------------------------------------
 **Acceptable** **Caution** **Red Flag**
 --------------------------------------------- ---------------------------------------------------- ---------------------------------------------
 DPA with AI-specific addendum or section Generic DPA, willing to negotiate AI addendum No DPA, or refuses to amend

 Current SOC 2 Type II within last 12 months SOC 2 Type II older than 12 months, or Type I only No SOC 2, or "in progress" with no timeline

 Explicit CCPA / CPRA compliance statement "We follow industry standards" Cannot speak to California requirements

 Subprocessor list and change notification Subprocessor list available on request No subprocessor disclosure

 24-72 hour incident notification "As soon as practical" with no defined window No incident notification commitment
 ------------------------------------------------------------------------------------------------------------------------------------------------

**California and Public Sector Specifics**

 -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Acceptable** **Caution** **Red Flag**
 -------------------------------------------------------------------------- ------------------------------------------------------- ------------------------------------------------------------
 Confirmed not a data broker, OR registered and transparent about it Unclear data broker status, will research and confirm Operates as data broker without disclosure or registration

 Working with multiple California public agencies, can provide references Limited California public-sector experience No public-sector deployments, especially in California

 Confirms AI artifacts are exportable for CPRA requests "We\'d have to work with you on that" AI artifacts not retrievable or not exportable

 Termination triggers full data deletion within contractual window Deletion possible but requires manual request Data retained or used for training after termination
 -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Human Oversight and Control**

 --------------------------------------------------------------------------------------------------------------------------------------------------------
 **Acceptable** **Caution** **Red Flag**
 ----------------------------------------------------------- ----------------------------------------------- --------------------------------------------
 Admin visibility into prompts, outputs, and user activity Aggregated reporting only, no per-user detail No admin visibility

 Policy controls available (data types, users, audit) Some controls available, others on roadmap No administrative policy controls

 Human-in-the-loop for any consequential decisions Optional human review with default automation Fully automated decisions without override

 Defined escalation and remediation path Informal escalation through support No defined process for AI errors
 --------------------------------------------------------------------------------------------------------------------------------------------------------

**Operational Boundaries**

 ---------------------------------------------------------------------------------------------------------------------------------------------------------------
 **Acceptable** **Caution** **Red Flag**
 -------------------------------------------------------- --------------------------------------------------- --------------------------------------------------
 Published accuracy metrics and measurement methodology Internal metrics only, willing to share under NDA No accuracy metrics, or "it\'s industry-leading"

 Documented failure modes and limitations General disclaimers about AI limitations Vendor claims the AI doesn\'t fail

 Bias testing results available Bias testing in progress No bias testing, or refuses to discuss

 Clear 12-month roadmap Roadmap shared under NDA No visibility into future AI changes
 ---------------------------------------------------------------------------------------------------------------------------------------------------------------

**[WHEN TO STOP AND CONSULT IT]{.underline}**

Trigger an IT consultation immediately if any of the following surface:

- Vendor cannot confirm whether AI is used in their product

- AI uses customer data for training and won\'t contractually opt out

- Vendor is a data broker or sells/shares personal information about California residents

- No SOC 2 Type II audit, or audit older than two years

- Product makes automated decisions affecting Organization operations, staff, or constituents without human review

- Vendor cannot produce AI artifacts (prompts, outputs, logs) for a Public Records Act request

- AI processing happens outside the US with no jurisdiction commitment

- Contract gives the vendor unilateral right to add AI features without notification

- Any answer involves the phrase "we\'ll have to get back to you" on a fundamental data-handling question

**[WHAT HAPPENS AFTER EVALUATION]{.underline}**

- If the vendor answered cleanly: submit the change request through your Director, attaching this completed cheat sheet and the vendor\'s written responses.

- If answers fell in the Caution column: discuss with IT before moving forward \-- IT may negotiate contract terms or request additional vendor documentation.

- If anything fell in the Red Flag column: do not move forward. IT will determine whether the product can be safely onboarded with mitigations, or whether Organization should decline.

The IT Manager will use this information to complete a formal AI FactSheet for the tool, route any legal questions to the Organization's Legal Counsel, and issue a sanctioning decision.

**[REFERENCE FRAMEWORKS]{.underline}**

- NIST AI Risk Management Framework (AI RMF 1.0)

- GovAI Coalition vendor evaluation guidance

- California Consumer Privacy Act (CCPA) / California Privacy Rights Act (CPRA)

- California Data Broker Registration requirements (Cal. Civ. Code Section 1798.99.80 et seq.)

- California Public Records Act (CPRA \-- public records, distinct from the privacy law of the same acronym)
