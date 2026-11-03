
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

The supplied GitHub screenshots show an active MediLink repository containing issues related to appointment reminders, incident handling, documentation, support rotation, and daily coordination.

The pull-request screenshot shows three open pull requests:

- Add risk register for the next release
- Add incident template
- Add support rotation

These records establish that management-related work has been created in the repository.

However, the screenshots do not establish completed reviews, verified work items, checklist compliance, or First-Time-Right outcomes.

Therefore, numerical performance results cannot yet be calculated reliably from the supplied screenshots alone.

## 5. Interpretation and Limitations

Engineering performance indicators should be interpreted in context.

For example, a delayed pull request may reflect unclear requirements, competing priorities, technical complexity, or limited reviewer availability.

Similarly, a blocked issue may indicate an external dependency rather than an individual performance problem.

The dashboard should therefore support investigation, discussion, and improvement rather than serve as a ranking system for developers.

## 6. Conclusion

A balanced engineering dashboard combines delivery, quality, and workflow indicators.

By examining these measures together, the MediLink team can identify potential bottlenecks, investigate their causes, and evaluate improvements without relying on misleading activity-based productivity measures.
