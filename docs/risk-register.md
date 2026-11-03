# MediLink risk register

Things that could go wrong in the next release. Each one is based on something we saw last release or during this cycle. A warning signal means "go check", not that something already went wrong. When we see one, we ask why before changing anything.

We update this list when we see a signal, after an incident, and at the end of the cycle. Developer A and Developer B get real names once we pick roles.

**Rating:** likelihood and impact go from 1 (low) to 3 (high). We multiply them. Anything at 6 or more, we deal with now.

| ID | Risk | Type | Likelihood | Impact | Score | Owner |
|----|------|------|------------|--------|-------|-------|
| R1 | Bugs get through because we skip checks | Quality / workflow | 3 | 3 | 9 | Developer B |
| R2 | Reviews take days while people start new work | Teamwork / workflow | 3 | 2 | 6 | Engineering Manager |
| R3 | Support requests pull people off planned work | Maintenance / production support | 3 | 2 | 6 | Milos |
| R4 | We rely on one person for hard problems | Teamwork | 2 | 2 | 4 | Engineering Manager |
| R5 | Changes to booking or cancelling break reminders | Technical dependency | 2 | 3 | 6 | Developer A |

## R1. Bugs get through because we skip checks
- **Evidence:** two bugs got to clinics last release because we skipped checks. Incident #2 got through because we only tested the main thing.
- **Warning signal:** a card skips Verification, or a bug fix has no test.
- **Potential consequence:** patients see errors, and we lose time fixing them.
- **Likelihood:** 3, it has already happened three times.
- **Impact:** 3, patients notice.
- **Preventive action:** someone other than the author tests it, and nothing goes to Done until the Definition of Done is met (#4).
- **Owner:** Developer B

## R2. Reviews take days while people start new work
- **Evidence:** last release, reviews took days and people started new tasks while they waited.
- **Warning signal:** a change waits a full day for review, or Code Review goes over its WIP limit.
- **Potential consequence:** work is late, and rushed reviews miss bugs.
- **Likelihood:** 3, same team, same habits.
- **Impact:** 2, it slows us down but patients don't feel it.
- **Preventive action:** review other people's work before starting something new, pick a reviewer for every change, and say in your daily update which reviews you owe.
- **Owner:** Engineering Manager

## R3. Support requests pull people off planned work
- **Evidence:** support kept interrupting developers last release, and incident #2 did it again this cycle.
- **Warning signal:** more than 2 support requests in a week, or daily updates say support got in the way.
- **Potential consequence:** planned work gets late, and switching between tasks causes mistakes.
- **Likelihood:** 3, several clinics use MediLink every day.
- **Impact:** 2, the release slows down but support still gets done.
- **Preventive action:** one person handles support each week (#7), and requests get sorted into "now" or "next planning".
- **Owner:** Milos

## R4. We rely on one person for hard problems
- **Evidence:** last release, one developer solved most of the hard problems, and in incident #2 only one person knew how reminders work.
- **Warning signal:** daily updates keep saying "waiting for" the same person.
- **Potential consequence:** work stops when that person is busy or away, and nobody else learns those parts.
- **Likelihood:** 2, it only hurts when that person isn't around.
- **Impact:** 2, a few tasks get stuck but patients don't feel it.
- **Preventive action:** work in pairs on hard tasks (#5), share reviews, and help people with questions instead of giving the problem to the expert.
- **Owner:** Engineering Manager

## R5. Changes to booking or cancelling break reminders
- **Evidence:** incident #2. Reminders depend on booking. They're made when an appointment is booked, so anything that changes an appointment has to update its reminder too. The admin page didn't.
- **Warning signal:** a booking or cancelling change that says nothing about reminders, or a report of a wrong reminder.
- **Potential consequence:** patients get reminders for cancelled visits or miss real ones. Clinics get no-shows and extra calls.
- **Likelihood:** 2, it happened once and the fix isn't tested yet.
- **Impact:** 3, it affects patients at several clinics.
- **Preventive action:** make every way of cancelling delete the reminder, check before sending (#3), and write a short page on how reminders work (#5).
- **Owner:** Developer A

## History
- Nov 3: started with R1 to R4.
- Nov 3: added R5 after incident #2, and used the incident as evidence for R1, R3 and R4.
