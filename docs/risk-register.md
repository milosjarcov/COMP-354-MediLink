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

## R1. Bugs get through because we skip checks
- **Evidence:** two bugs got to clinics last release because we skipped checks.
- **Warning signal:** a card skips Verification, or a bug fix has no test.
- **Potential consequence:** patients see errors, and we lose time fixing them.
- **Likelihood:** 3, it happened twice last release.
- **Impact:** 3, patients notice.
- **Preventive action:** someone other than the author tests it, and nothing goes to Done until the Definition of Done is met.
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
- **Evidence:** support kept interrupting developers last release.
- **Warning signal:** more than 2 support requests in a week, or daily updates say support got in the way.
- **Potential consequence:** planned work gets late, and switching between tasks causes mistakes.
- **Likelihood:** 3, several clinics use MediLink every day.
- **Impact:** 2, the release slows down but support still gets done.
- **Preventive action:** one person handles support each week, and requests get sorted into "now" or "next planning".
- **Owner:** Milos

## R4. We rely on one person for hard problems
- **Evidence:** last release, one developer solved most of the hard problems.
- **Warning signal:** daily updates keep saying "waiting for" the same person.
- **Potential consequence:** work stops when that person is busy or away, and nobody else learns those parts.
- **Likelihood:** 2, it only hurts when that person isn't around.
- **Impact:** 2, a few tasks get stuck but patients don't feel it.
- **Preventive action:** work in pairs on hard tasks, share reviews, and help people with questions instead of giving the problem to the expert.
- **Owner:** Engineering Manager

## History
- Nov 3: started with R1 to R4.
