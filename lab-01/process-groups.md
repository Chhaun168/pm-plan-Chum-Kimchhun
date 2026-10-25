# Process Groups and Semester Mapping: Realtime Quiz Platform

## 1. Process Groups across the Semester
| Process group | Weeks active | Main activities | Outputs | Lab that produces them |
|---------------|--------------|-----------------|---------|------------------------|
| Initiating | 1 | Defining project purpose, securing sponsor approval, drafting charter | Project charter, stakeholder list | Lab-01 |
| Planning | 1 - 3 (continuing re-planning) | Scope definition, business case formulation, scheduling, risk analysis | Business case, WBS, risk register | Labs-01, 04, 05, 09 |
| Executing | 2 - 14 | Software development, frontend/backend integration, documentation | Working code increments, MVP release | Labs-02 to 08 |
| Monitoring and controlling | 1 - 14 | Weekly status reviews, tracking schedule and cost variances, managing changes | Weekly status reports, change logs, variance analyses | Every lab (practice) & Labs-05, 06, 09 |
| Closing | 14 | Conducting student pilot, final handover to operations, lessons learned | Pilot report, operations runbook, project closure document | Labs-01, 12 |

## 2. Process groups over the semester (Gantt chart)
```mermaid
gantt
  title Process groups over the 14-week semester (Realtime Quiz)
  dateFormat YYYY-MM-DD
  axisFormat %d %b
  section Initiating
  Charter, stakeholders, business case   :i1, 2026-09-29, 7d
  section Planning
  PM plan and subsidiary plans           :p1, 2026-09-29, 21d
  Re-planning after each status review   :p2, 2026-10-20, 77d
  section Executing
  Build to MVP (Must features)           :e1, 2026-10-13, 35d
  MVP demo                               :milestone, m1, 2026-11-13, 0d
  Should and Could features, hardening   :e2, 2026-11-17, 42d
  section Monitoring and controlling
  Weekly status, variance, change log    :m2, 2026-09-29, 98d
  section Closing
  Pilot with 50 students, lessons learned :c1, 2026-12-29, 7d