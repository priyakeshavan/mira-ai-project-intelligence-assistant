# Mira baseline evaluation and evidence status

## Test suite
The official baseline includes T1–T12 (see CSV). Required dimensions include intent routing, grounded plan/risk/status content, handling vague inputs, exact task counts, T024 blocker identification, timeline accuracy, sprint-specific communication and overall output quality.

## What has and has not been verified
- **Earlier interactive test:** project owner reported 12/12 PASS after iterations; full raw responses for those successful cases were not supplied for this submission bundle.
- **Earlier separate 20-case test:** reported HTTP 100%, valid JSON 80%, validation pass 75% *at that time*, before later fixes. Not equivalent to final 12-case baseline.
- **Automated capture retry:** 12/12 HTTP 400 (`Invalid HTTP request received.`), `NOT_RUN`; therefore it provides no basis for an agent-quality pass rate.

## Final evidence to add before submitting
| Case | Scenario | Final result | Evidence |
|---|---|---|---|
| T1 | Grounded detailed plan | Needs saved evidence | Playground screenshot/output |
| T2 | Vague plan clarification | Needs saved evidence | Playground screenshot/output |
| T3 | Grounded risk assessment | Needs saved evidence | Playground screenshot/output |
| T4 | Vague risk clarification | Needs saved evidence | Playground screenshot/output |
| T5 | Sprint 3 task status | Needs saved evidence | Playground screenshot/output |
| T6 | No-data status handling | Needs saved evidence | Playground screenshot/output |
| T7 | Top 3 source risks | Needs saved evidence | Playground screenshot/output |
| T8 | Blocked/at-risk tasks, T024 | Needs saved evidence | Playground screenshot/output |
| T9 | Two-week vague plan | Needs saved evidence | Playground screenshot/output |
| T10 | Task status counts | Needs saved evidence | Playground screenshot/output |
| T11 | Upcoming milestones | Needs saved evidence | Playground screenshot/output |
| T12 | Sprint 2 stakeholder update | Needs saved evidence | Playground screenshot/output |

## Evaluation methodology
For each case: capture exact input, full output, selected route, validator result, source-grounding check, latency and trace link/ID. Judge against the official case-specific criteria. Track: routing accuracy, schema/validation pass rate, factual accuracy, blocker recall, count accuracy, clarification quality, latency and token cost.

**Do not label a case PASS solely because HTTP=200 or `validation_status=PASS`; review the expected criteria and source facts.**
