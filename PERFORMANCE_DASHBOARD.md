
# MediLink Engineering Performance Dashboard

## 1. Purpose

This dashboard illustrates how MediLink can evaluate the effectiveness of its software development workflow using meaningful engineering performance indicators.

The objective is to identify potential bottlenecks, monitor quality, and support continuous improvement rather than judge individual developers based on activity counts.

## 2. Performance Indicators

| Metric | Measurement | Why It Is Useful | What It Does NOT Prove |
|---|---|---|---|
| Review Turnaround Time | Average time between opening a pull request and receiving its first review | Identifies potential delays in the code review process | A long review time does not necessarily mean a reviewer is unproductive |
| Delivery Reliability | Percentage of planned work items completed during the development cycle | Helps evaluate planning accuracy and delivery consistency | A low completion rate does not prove poor individual performance |
| Blocked Work | Number of work items experiencing documented blockers | Identifies dependencies and workflow interruptions | A blocked task does not necessarily indicate a developer's mistake |
| Checklist Compliance | Percentage of reviewed work items completing all required verification checks | Helps assess whether quality procedures are followed consistently | Completing a checklist does not guarantee defect-free software |
| First-Time-Right (FTR) | Percentage of reviewed work items accepted without avoidable corrective rework | Helps identify opportunities to improve preparation and quality | A lower FTR rate does not automatically indicate poor developer performance |

## 3. Measurement Methods

### Review Turnaround Time

Formula:

Total time to first review / Number of reviewed pull requests

Measurement source: GitHub pull-request timestamps and submitted review records.

### Delivery Reliability

Formula:

(Completed planned work items / Total planned work items) × 100

Measurement source: GitHub project board and issue history.

### Blocked Work

Formula:

Number of distinct work items experiencing documented blockers during the cycle.

Measurement source: GitHub issue comments, blocker labels, and project board history.

### Checklist Compliance

Formula:

(Reviewed items completing all required checks / Total reviewed items) × 100

Measurement source: Definition of Done and verification records.

### First-Time-Right

Formula:

(Reviewed items accepted without avoidable corrective rework / Total reviewed items) × 100

Measurement source: Pull-request reviews and rework records.

## 4. Initial Repository Observations

The following observations were obtained from the MediLink GitHub repository during the simulated development cycle.

| Indicator | Observed Result | Interpretation |
|---|---|---|
| Open issues | 7 | The repository contains documented work items requiring attention. |
| Initially open pull requests | 3 | Three changes were awaiting integration at the time of the initial screenshot. |
| Dashboard and coaching pull requests | 2 merged (PR #11 and PR #12) | Both documentation changes were successfully integrated into the main branch. |
| Formal reviews on PR #11 and PR #12 | 0 shown | Both were merged without a formal GitHub review recorded. |
| Linked GitHub Project board | None | The repository does not currently have a linked project board. |

These observations describe repository activity and workflow visibility. They do not independently establish developer productivity, delivery reliability, checklist compliance, or First-Time-Right quality.

### Measurement Availability

Review turnaround time cannot currently be calculated for PR #11 and PR #12 because no formal review is recorded.

Delivery reliability requires a defined set of planned work items and their completion status.

Blocked work requires documented blockers, while checklist compliance and FTR require verification and review evidence.

Missing measurements should be reported as unavailable rather than treated as zero.

### Current Performance Dashboard

| Performance Metric | Current Result | Evidence Status |
|---|---|---|
| Review Turnaround Time | N/A | No formal reviews recorded for PR #11 or PR #12 |
| Delivery Reliability | N/A | No confirmed baseline of planned versus completed work |
| Blocked Work | Not yet verified | No documented blocker count established |
| Checklist Compliance | N/A | Verification checklist results not available |
| First-Time-Right (FTR) | N/A | No confirmed acceptance-without-rework records |

N/A indicates insufficient evidence, not zero performance. These results are preliminary and should be updated when the team completes and documents its workflow activities.

## 5. Interpretation and Limitations

Engineering performance indicators should be interpreted in context.

For example, a delayed pull request may reflect unclear requirements, competing priorities, technical complexity, or limited reviewer availability.

Similarly, a blocked issue may indicate an external dependency rather than an individual performance problem.

The dashboard should therefore support investigation, discussion, and improvement rather than serve as a ranking system for developers.

## 6. Conclusion

A balanced engineering dashboard combines delivery, quality, and workflow indicators.

By examining these measures together, the MediLink team can identify potential bottlenecks, investigate their causes, and evaluate improvements without relying on misleading activity-based productivity measures.
