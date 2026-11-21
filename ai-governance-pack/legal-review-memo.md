**AI GOVERNANCE ADVISORY**

Microsoft Cloud & AI Governance Advisory

**AI Tool Legal Review \-- Wealth Engine & ChatGPT**

**To:** the Organization's Legal Counsel (via the IT Manager, per AI Policy Section 4)

**From:** Laura Rowe

**Date:** June 11, 2026

**Re:** AI Tool Legal Review \-- Wealth Engine & ChatGPT (Version 0.1, DRAFT for Legal Counsel review)

**Companion to:** AI Policy; Foundation AI Tools Evaluation; Systems & AI Inventory

***Advisory only.** Per SOW SS2.2 and SS5, the advisory firm does not create or enforce policy and does not provide legal advice. This memo poses focused questions for the Organization's Legal Counsel so the AI Review (Policy Section 5 / Appendix A AI FactSheet) can conclude with a documented decision. Organization owns the sanction decision and any enforcement.*

**Purpose**

Two AI tools surfaced during the AI Policy expansion are high-risk and should not be sanctioned until the Organization's Legal Counsel has reviewed them. Both should carry the interim status "In AI Review \-- pending Legal" in the policy\'s sanctioned/unsanctioned lists \-- neither sanctioned nor outright prohibited \-- until Legal returns a per-tool determination (approve / approve-with-conditions / deny), recorded on the AI FactSheet (Appendix A.8).

**Entity-scoping question (applies to both tools)**

The affiliated Foundation is a separate California 501(c)(3), but Foundation staff are on Organization\'s payroll and operate on Organization\'s M365 tenant \-- so the AI Policy reaches their tool use. As a matter of general direction, the Foundation signs its own contracts and DPAs as a separate legal entity. The remaining question for these two high-risk tools is confirmation of the contract / liability boundary per tool: which entity signs the DPA, and which bears the statutory data-protection / data-broker exposure.

**Tool 1 \-- Wealth Engine (Altrata)**

**What it is:** Donor wealth-screening / prospect research \-- AI-driven financial and personal profiling of identifiable individuals (donors) using aggregated third-party data. Used by the Foundation. Currently unsanctioned.

**Why it needs Legal:** It appears to operate as a third-party data broker selling personal/financial data, and profiling identifiable individuals raises CCPA/CPRA and California public-agency considerations that exceed an IT risk review.

**Questions for Legal:**

1. **Data-broker status** \-- Is Altrata / Wealth Engine a registered data broker under California\'s Delete Act / CCPA data-broker registry? Does Organization\'s or the Foundation\'s use as a "business" / "third party" trigger obligations?

2. **Source-data lawfulness** \-- What is the provenance of the personal/financial data Wealth Engine aggregates, and are there consent or notice obligations to the individuals being profiled?

3. **CPRA data-subject rights** \-- How are access, deletion, opt-out of sale/sharing, and limit-use-of-sensitive-PI rights handled for the individuals profiled, and does Organization/the Foundation inherit any obligation to honor them?

4. **Public-agency / CPRA exposure** \-- As a public agency subject to the California Public Records Act, are Wealth Engine outputs (donor profiles) public records, and what are the privacy implications of retaining them?

5. **Contract / DPA** \-- Does the current Foundation agreement include a DPA, CPRA-compliant terms, data-use/retention limits, and breach-notification commitments? Which entity is the contracting party?

6. **Decisioning / human oversight** \-- Are outputs used to make or inform decisions about individuals? (Ties to AI Policy Section 6 prohibited uses and the human-oversight requirement.)

**Recommended interim disposition:** Unsanctioned \-- do not use for new donor screening pending Legal. Resolve to approve-with-conditions or deny on Legal\'s read of the data-broker, public-records, and contract items.

**Tool 2 \-- ChatGPT (OpenAI)**

**What it is:** General-purpose generative AI; the Foundation\'s heavy-use primary AI tool (grant research, proposal writing, newsletter editing, etc.). The free / consumer tier is prohibited under the consumer-AI ban. Sanctionability turns entirely on subscription tier and data terms.

**The crux:** Consumer / Plus trains on inputs and has no enterprise DPA, so it is not sanctionable for any non-public Organization or Foundation data. ChatGPT Team / Enterprise provides a DPA, training-off-by-default, and admin controls, so it is potentially sanctionable with conditions. "ChatGPT" must not be sanctioned generically \-- only a specific tier under specific conditions.

**Questions to resolve before sanctioning (IT + Legal):**

7. **Tier** \-- What exact ChatGPT subscription does the Foundation use today (Free / Plus / Team / Enterprise)?

8. **DPA / terms** \-- Is there an executed OpenAI DPA / enterprise agreement, and which entity signed it?

9. **Training opt-out** \-- Is "do not train on our data" in effect (default on Team/Enterprise; unavailable on consumer)?

10. **Data handling** \-- Retention, data residency, and sub-processors, mapped to the Organization's Cyber Security Policy data classes (Internal / Confidential).

11. **Use boundaries** \-- Even if sanctioned, confirm restriction to non-Confidential data per AI Policy Section 6.1.

**Recommended interim disposition:** Free / consumer ChatGPT \-- prohibited (consumer-AI ban). A specific Team / Enterprise tier may be sanctioned with conditions once the DPA and training-opt-out are confirmed; unsanctioned until then.

**What we need from Legal**

- A per-tool determination \-- approve / approve-with-conditions (specify the conditions) / deny \-- recorded on the AI FactSheet (Appendix A.8).

- Confirmation of the contracting entity (Organization vs Foundation) for each tool.

- Target: before 6/30 to align with the FY AI-Policy-expansion window. Interim policy status for both: "In AI Review \-- pending Legal."
