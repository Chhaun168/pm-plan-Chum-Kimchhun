# Task 1: project, operation or programme?

| #  | Initiative | Temporary? | Unique? | Coordinated? | Class | Justification |
|----|------------|------------|---------|--------------|-------|---------------|
| 1  | Build the Realtime Quiz platform and pilot it with 50 students in week 14 | yes | yes | no | Project | It has a fixed 14-week duration and delivers a unique software platform that did not exist before. |
| 2  | Run the nightly backup of the gicitc.com PostgreSQL database | no | no | no | Operation | It repeats every night with identical output and no end date as part of keeping the service running. |
| 3  | Move the department's three web servers to a new Linode region before 15 December | yes | yes | no | Project | It has a strict deadline of 15 December and a unique migration objective. |
| 4  | Answer helpdesk tickets within the 4-hour service level | no | no | no | Operation | It is an ongoing, repetitive service activity with no end date, even though individual tickets have a 4-hour SLA. |
| 5  | "Digital classroom": Realtime Quiz, LMS upgrade and lecture capture sharing one login and one grade export | yes | yes | yes | Programme | It groups several related projects whose shared benefit of a unified login and grade export exists only when coordinated together. |
| 6  | Apply the monthly security patches to the VPS | no | no | no | Operation | It is a routine, repetitive maintenance cycle applied every month to maintain system security. |
| 7  | Add multi-node scaling (RabbitMQ relay, Redis registry) to Realtime Quiz next semester | yes | yes | no | Project | It has a defined timeframe next semester and a unique architectural scope to implement multi-node scaling. |
| 8  | Operate the Realtime Quiz platform after go-live: password resets, restarts, monitoring | no | no | no | Operation | It consists of ongoing maintenance, monitoring, and user support activities that continue indefinitely after go-live. |
| 9  | Write and publish the department's annual IT report for the dean by 31 January | yes | yes | no | Project | It has a strict deadline of 31 January, and each yearly report is a unique deliverable for that year. |
| 10 | Replace 40 wireless access points in two buildings during the summer break | yes | yes | no | Project | It has a definite timeframe during the summer break and results in a uniquely upgraded physical network infrastructure. |

## Grey zones
* **Initiative 7 (Multi-node scaling)**: This could be argued either as an operation (maintenance/enhancement) or a project. To settle it, we need to know whether the sponsor funds it as a separate endeavour with its own dedicated budget and end date, or if it is just a routine operational upgrade.
* **Initiative 9 (Annual IT report)**: This is repetitive and happens every year, yet each report is a unique document with a hard deadline. Most departments treat it as a small recurring yearly project, but if handled by permanent administrative staff as routine duty, it leans towards an operation.

## What our project hands over
Upon reaching go-live in week 14, the Realtime Quiz project team hands over the running platform to IT operations. Specifically, the team hands over the production Docker configuration (`docker-compose.prod.yml`), the deployment runbook, and monitoring access. IT operations will then take over day-to-day management, restarts, and routine support.