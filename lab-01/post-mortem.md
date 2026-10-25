# Post-mortem: CampusPay Wallet Project (2025)

## 1. Timeline and sources
| # | When | Event | Source |
|---|------|-------|--------|
| 1 | Month 1 | University requests a cashless payment app for canteen purchases and library fines within one semester. | Fictional case from Lab-01 |
| 2 | Month 2 | Head of finance agrees to "sponsor" by email but never attends review meetings. | Fictional case from Lab-01[cite: 1] |
| 3 | Month 3 | Lead developer acts as both informal project manager and sole coder without a formal project charter. | Fictional case from Lab-01[cite: 1] |
| 4 | Month 4 | Scope expands via survey feedback from canteen purchases to include bus tickets and parking fees. | Fictional case from Lab-01[cite: 1] |
| 5 | Month 5 | Launch date is strictly set for September; no end-to-end integration tests are run with real card terminals. | Fictional case from Lab-01[cite: 1] |
| 6 | Launch Day | App goes live; physical card terminals reject 40% of payments, and canteen queues double in length. | Fictional case from Lab-01[cite: 1] |
| 7 | Day 3 Post-Launch | Due to severe operational failure and user backlash, the application is officially withdrawn. | Fictional case from Lab-01[cite: 1] |
| 8 | 5 Months Later | App is successfully re-launched, scaled down strictly to the original canteen payment scope. | Fictional case from Lab-01[cite: 1] |

## 2. Classification and organisation
- **Project or Programme:** Treated as a single high-risk IT project with an aggressive, unvalidated deadline.
- **Structure and PM Authority:** The lead developer functioned without formal project management authority, making it impossible to reject unauthorized scope additions.
- **Sponsor, Charter, PMO:** There was no signed project charter. The head of finance acted merely as a nominal email sponsor with zero active engagement, and no PMO oversight existed.

## 3. Success criteria
- **Stated Criteria:** "Launch in September" (a pure, unvalidated schedule milestone).
- **Missing Measurable Criteria:** Transaction error rates, payment latency, system concurrency limits, and physical hardware integration success rates.
- **Ignored Wider Dimensions:** User satisfaction, operational support readiness, financial security verification, and team sustainability.

## 4. Process groups and knowledge areas
| Process group | What went wrong or was skipped |
|---------------|--------------------------------|
| Initiating | Skipped completely; no formal charter was established or signed. |
| Planning | Inadequate; requirements grew uncontrollably without a formal change control process. |
| Executing | Focused strictly on rapid code generation while neglecting critical hardware integrations. |
| Monitoring and controlling | Completely ignored; project status was blindly reported as "on schedule" without testing failure rates (the invisibility trap). |
| Closing | Abrupt withdrawal and emergency shutdown instead of a structured project closure review. |

**Knowledge areas most responsible:**
1. **Scope Management:** Uncontrolled scope growth (adding bus tickets and parking late in the cycle).
2. **Quality Management:** Total omission of end-to-end testing with real card terminals prior to launch.
3. **Risk Management:** Failure to identify and mitigate hardware rejection risks or plan contingency fallback lines.

## 5. Ethics
- **Decision Examined:** Launching a financial transaction app into production knowing that hardware integration testing had not been completed.
- **Core Values Assessment:** This decision violates **responsibility** (failing to ensure system safety and reliability before releasing it to users) and **honesty** (reporting the project as "on schedule" while ignoring fundamental technical defects).

## 6. What our project will do differently
| # | Commitment (We will ...) | Measured by | By week | Charter line |
|---|--------------------------|-------------|---------|--------------|
| 1 | We will run a live session with 100 simulated students and the campus network before the pilot | Load test report with 0 critical errors | Week 12 | Objective O4 / Milestone week 12[cite: 1] |
| 2 | We will hold a signed project charter with a named sponsor who attends scheduled gate reviews | Signed charter document and gate meeting minutes | Week 1 | Section 10 Approval / PM Authority clause[cite: 1] |
| 3 | We will enforce strict scope boundaries, requiring formal change requests for any additions | Change log tracking with sponsor sign-off | Ongoing (Weeks 1–14) | High-level Scope (In-scope / Out-of-scope)[cite: 1] |
| 4 | We will maintain rigorous code quality standards with automated testing suites | Line coverage >= 80% with green CI builds on every merge | Week 13 | Objective O5[cite: 1] |
| 5 | We will conduct formal phase gate reviews to verify readiness before advancing | Gate checklist review sign-offs | Weeks 1, 7, 13 | Section 3 Phase Gates[cite: 1] |