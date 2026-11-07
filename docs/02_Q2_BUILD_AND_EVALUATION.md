# Q2 — Build Mira: design, implementation, cost and evaluation

## Design and orchestration
A router/dispatcher pattern selects one specialist based on request intent. The Main Orchestrator passes the request to the Router, then dispatches to Planner, Risk Assessor, Status Reporter or Milestone Tracker. Specialists use grounding data, prompts, structured outputs and validation. Langflow Desktop 1.11.0 supports visual workflow construction; Langfuse is used for trace observability. This design reduces unnecessary model calls relative to a fixed sequential pipeline.

## Implemented scope
The exported repository includes six workflows: Main Orchestrator, Router, Planner, Risk Assessor, Status Reporter and Milestone Tracker. Core capabilities address grounded plans, categorized risk matrices and task-board-based status reports. Milestone tracking is the chosen extended capability. Reviewer approval remains necessary before external communication.

## Data grounding and quality
Project context is supplied through project description, risk register, timeline and task board. Source facts must be distinguished from model judgments. Task counts and date comparisons should be computed deterministically. Missing-data prompts should seek clarification rather than inventing scope or progress.

## Evaluation
The official T1–T12 baseline tests include detailed and vague prompts, source-risk relevance, blocked task T024, task counts, milestone accuracy and sprint-specific stakeholder communication. Prior interactive testing was reported as 12/12 passed; however, raw successful Playground responses were not preserved in this package. A subsequent API export run failed with HTTP 400 and did not exercise the agents. This is a **documentation/evidence gap**, not proof of agent failure or success. See evaluation report.

**Metrics to report after verified runs:** HTTP execution success; intent-routing accuracy; structured-output/validator pass rate; grounded factual accuracy; task-count accuracy; latency and token/cost per request. The earlier 20-case evaluation reported 100% HTTP success, 80% valid JSON, and 75% validation pass **before subsequent fixes**; it must not be presented as the final T1–T12 result.

## Cost methodology
For each successful run, capture input tokens, output tokens, number of LLM calls and model name from traces. Compute **cost per request = (input tokens / 1,000,000 × model input price) + (output tokens / 1,000,000 × model output price)**, summed over all calls in that request. Calculate average and p95 cost across runs; compare router overhead against specialist cost. No verified token-level measurements or pricing snapshot is included here, so a dollar estimate is intentionally omitted.

## Known limitations and next actions
Re-importing flows may require re-linking IDs and paths. API-based automated export returned 400, so use verified Playground evidence for submission. Add three screenshots: canvas, representative output and Langfuse trace. Recheck baseline outputs against each criterion before labeling cases PASS. Do not claim production deployment or automatic Slack/Gmail sending.
