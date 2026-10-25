# Business case: live quizzes for the IT department

## 1. Problem
The IT department currently spends excessive manual hours marking paper or basic form-based quizzes, leading to delayed feedback for students and a high administrative load for lecturers. 
**Assumptions:**
- Lecturers running quizzes: 10
- Marking time per lecturer per week: 1 h
- Teaching weeks per year: 30
- Notional value of one hour: 10 USD (students are unpaid; used for comparison)

## 2. Options
| Option | Description | One-off cost | Annual cost | Annual benefit |
|--------|-------------|--------------|-------------|----------------|
| A      | Do nothing  | 0            | 0           | 0              |
| B      | Buy SaaS (commercial quiz platform at 15 USD/month per lecturer, cited from standard ed-tech pricing assumption) | 0 | 1,800 USD | 3,000 USD (marking time saved) |
| C      | Build Realtime Quiz (charter team effort and hosting) | 4,900 USD | 300 USD (hosting) | 4,800 USD (marking time saved + SaaS fee avoided) |

## 3. Comparison
| Option | Net annual benefit | Payback (years) | Sensitivity (6 lecturers instead of 10) |
|--------|--------------------|-----------------|-----------------------------------------|
| B      | 1,200 USD          | 0 (no one-off)  | 720 USD                                 |
| C      | 4,500 USD          | 1.09 years      | Net benefit: 2,880 USD / Payback: 1.7 years |

## 4. Benefits not priced
- Enhanced learning outcomes through immediate classroom engagement and real-time leaderboards.
- Full data ownership and privacy compliance (keeping student assessment data stored locally on campus).
- No per-seat limits or sudden subscription price hikes from third-party vendors.

## 5. Risks per option
- **Option A (Do nothing):** Continued high staff burnout from manual grading; declining student engagement.
- **Option B (Buy SaaS):** Vendor lock-in; potential data privacy concerns regarding student data stored on external servers; recurring subscription cost inflation.
- **Option C (Build):** Scope creep or student team burnout; campus network firewalls blocking WebSocket connections (mitigated by fallback configurations).

## 6. Recommendation and review gate
**Recommendation:** Select **Option C (Build)**. Although it requires a higher upfront effort investment (4,900 USD equivalent), it achieves payback within slightly over one academic year, eliminates recurring SaaS licensing fees, and provides students with valuable capstone software engineering experience.
**Review gate:** If the week-7 MVP demo fails to meet core requirements, the department will immediately switch to **Option B (Buy SaaS)** for the following semester.