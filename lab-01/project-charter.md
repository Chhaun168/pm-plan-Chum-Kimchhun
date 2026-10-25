# Project charter: Realtime Quiz platform

| Field    | Value                              |
|----------|------------------------------------|
| Version  | 1.0 (draft for sponsor approval)   |
| Date     | 2026-09-29                         |
| Sponsor  | Head of the IT department[cite: 1]          |
| PM       | Supervising lecturer[cite: 1]               |

## 1. Purpose and justification
The IT department currently faces a heavy manual marking load and lacks a unified tool for conducting live, interactive classroom quizzes with immediate feedback. This project builds a web-based Realtime Quiz platform allowing instructors to author multiple-choice quizzes and host live timed sessions with instant WebSocket leaderboards. This automates assessment collection, reduces instructor grading workload by at least 30%, and increases student engagement. For a complete financial breakdown, refer to `business-case.md`.

## 2. Objectives and success criteria
| #  | Objective (what will be true)      | Success criterion (number + week) |
|----|------------------------------------|-----------------------------------|
| O1 | Deploy MVP Must features live      | All Must features operational by week 7[cite: 1] |
| O2 | Conduct successful student pilot   | 50 pilot participants with 0 blocking defects, week 14[cite: 1] |
| O3 | Maintain low broadcast latency     | <= 500 ms at the 95th percentile, measured week 14[cite: 1] |
| O4 | Handle target concurrency server load | 20 sessions of 100 participants on 2 vCPU and 2 GB RAM, tested week 12 |
| O5 | Ensure high code quality standards | Line coverage >= 80% with green CI on every merge by week 13[cite: 1] |

## 3. High-level scope
In scope:
- Multiple-choice quiz authoring and question management interface
- Real-time session hosting using WebSockets and 6-character join codes
- Instant feedback, scoring, and dynamic leaderboards
- User authentication, role management (Instructor, Student, Guest)
- Result exports to CSV and PDF formats

Out of scope:
- Native mobile applications (iOS/Android)[cite: 1]
- Alternative question types (no free text or essay questions)[cite: 1]
- Built-in video conferencing integration[cite: 1]
- LMS platform integrations (e.g., Moodle/Canvas)[cite: 1]
- Multi-node scaling (single server instance only)[cite: 1]

## 4. Milestones
| Week | Milestone                          | Ends process group |
|------|------------------------------------|--------------------|
| 1    | Charter approved, team formed[cite: 1]      | Initiating[cite: 1]         |
| 3    | Accounts, security, and setup done | Planning[cite: 1]         |
| 5    | Quiz authoring module complete     | Executing[cite: 1]        |
| 7    | MVP demo (Must features live)[cite: 1]      | Executing[cite: 1]        |
| 10   | Analytics and export modules done  | Executing[cite: 1]        |
| 12   | Hardening and 100-student load test| Monitoring and controlling[cite: 1] |
| 14   | Pilot with 50 students, closure[cite: 1]    | Closing[cite: 1]          |

## 5. Budget summary
Effort:  students 4 x 14 x 8 h = 448 h; PM 14 x 3 h = 42 h; total 490 h[cite: 1]
Cash:    hosting 4 x 25 USD = 100 USD; domain 15 USD; tools 60 USD; reserve 25 USD (14%)[cite: 1]
         total 200 USD cap[cite: 1]

## 6. Assumptions
- The four student team members will consistently dedicate 8 hours per week to development[cite: 1].
- Campus network infrastructure supports stable WebSocket and Caddy reverse-proxy connections.
- The 200 USD cash budget cap will completely cover cloud hosting and domain fees for the semester[cite: 1].

## 7. Constraints
- The project must be fully completed and piloted within the strict 14-week semester timeline[cite: 1].
- Cash expenditure must not exceed the 200 USD project cap[cite: 1].
- Student user data compliance requires storage configurations managed securely on campus or approved cloud instances.

## 8. High-level risks
- Campus network firewalls or proxies may block standard WebSocket traffic (fallback: SockJS configured)[cite: 1].
- Late client submissions may race with question timers closing, requiring strict server-authoritative time synchronization[cite: 1].
- Feature creep from "Could" features into the core MVP timeline[cite: 1].

## 9. Project manager authority
The project manager (supervising lecturer) has the authority to re-plan tasks within the approved 490 person-hours and 200 USD budget. However, adding significant new scope, altering pilot timelines, or spending beyond the cash reserve requires formal written approval from the sponsor within 5 working days.

## 10. Approval
Sponsor: _________________________  Date: ________[cite: 1]
PM:      _________________________  Date: ________[cite: 1]