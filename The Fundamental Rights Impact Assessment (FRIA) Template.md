# High-Risk-Deployer-FRIA-Governance-Toolkit.
Under Article 27 of the EU AI Act (Regulation 2024/1689), bodies governed by public law or private entities deploying high-risk AI systems (such as HR resume screeners, credit scoring models, or automated performance evaluators) must conduct a Fundamental Rights Impact Assessment (FRIA) prior to putting the system into service.
Markdown
# Fundamental Rights Impact Assessment (FRIA) Template

> **Mandatory Compliance Assessment under Article 27 of Regulation (EU) 2024/1689 (EU AI Act)**

---

## 1. System & Deployment Information

| Field | Details |
| :--- | :--- |
| **AI System Name** | *[e.g., TalentScout CV Screener]* |
| **System Identifier** | *[e.g., AI-2026-001]* |
| **Deployer Entity / Department** | *[e.g., Human Resources / Global Recruitment]* |
| **AI System Provider** | *[e.g., Third-Party Vendor / Internal AI Engineering]* |
| **Intended Purpose** | *[e.g., Automated scoring and shortlisting of job applicant resumes]* |
| **EU AI Act Risk Classification** | **Tier 3: High Risk** (Annex III, Section 4a - Employment & HR) |
| **Target Population Affected** | *[e.g., Job applicants, internal employees applying for promotions]* |
| **Assessment Date & Version** | YYYY-MM-DD | v1.0 |
| **Lead Assessor Name & Title** | Senior GRC Specialist / Data Protection Officer (DPO) |

---

## 2. Assessment of Impact on Fundamental Rights

Evaluate the potential adverse impacts on rights protected under the **EU Charter of Fundamental Rights**:

### A. Non-Discrimination & Equal Treatment (Article 21)
* **Risk Identified:** Demographic bias in training data leading to adverse impact against protected groups (age, gender, ethnicity, disability).
* **Likelihood:** Medium | **Impact:** High | **Pre-Mitigation Risk Level:** High
* **Mitigation Controls:** Mandatory pre-deployment bias testing using historical resume samples; removal of proxy variables (zip codes, graduation dates); regular audit logs of selection ratios.
* **Residual Risk Level:** Low

### B. Protection of Personal Data & Privacy (Article 8)
* **Risk Identified:** Unlawful processing of sensitive data or unauthorized retention of applicant CVs beyond statutory limits.
* **Likelihood:** Medium | **Impact:** Medium | **Pre-Mitigation Risk Level:** Medium
* **Mitigation Controls:** Integration with Enterprise Data Retention Policy (deletion after 180 days); strict Role-Based Access Control (RBAC); AES-256 data encryption at rest and in transit.
* **Residual Risk Level:** Low

### C. Human Dignity & Right to Fair Working Conditions (Articles 1 & 31)
* **Risk Identified:** Fully automated rejection of candidates without human review or clear explainability.
* **Likelihood:** High | **Impact:** Medium | **Pre-Mitigation Risk Level:** High
* **Mitigation Controls:** Enforcement of Article 26 Human-in-the-Loop policy—no candidate can be rejected without secondary human review by a trained HR recruiter.
* **Residual Risk Level:** Low

---

## 3. Human Oversight & Operational Safeguards (Article 26)

1. **Designated Oversight Personnel:**
   * Primary: Lead Technical Recruiter
   * Secondary: HR Compliance Manager
2. **Oversight Mechanism:** Human-in-the-Loop (HITL) setup where the AI provides a confidence score, but final hiring decisions remain strictly human-driven.
3. **Override & Stop Authority:** Designated operators hold full operational authority to override AI rankings or disable the system upon detecting anomalous scoring behaviors or bias drift.

---

## 4. Post-Deployment Monitoring Plan (Article 27(1)(e))

* **Metrics Monitored:** Disparate Impact Ratio (Four-Fifths Rule compliance), false positive/negative rates, manual override frequency.
* **Monitoring Frequency:** Monthly operational review; Quarterly audit report to the AI Governance Committee.
* **Incident Escalation:** Immediate halt of automated scoring if selection ratio for any protected demographic drops below 0.80 compared to the highest-scoring group.

---

## 5. Formal Approval & Sign-Off

| Role | Name | Signature | Date |
| :--- | :--- | :--- | :--- |
| **Lead GRC Assessor** | _______________________ | _______________________ | YYYY-MM-DD |
| **Data Protection Officer (DPO)** | _______________________ | _______________________ | YYYY-MM-DD |
| **Business Unit Head (Deployer)** | _______________________ | _______________________ | YYYY-MM-DD |
