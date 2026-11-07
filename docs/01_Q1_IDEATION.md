# Q1 — Ideation: PM/TPM productivity use cases

## 1. Grounded project planning
**Pain point:** Manual synthesis of descriptions and timelines into structured plans.
**Agentic solution:** Planner reads the provided project context and creates phases, activities, milestones, deliverables and estimates; requests clarification for vague scope.
**Inputs:** project description, timeline, request. **Outputs:** structured draft plan with references.
**Success metrics (proposed):** (1) grounded milestone accuracy, (2) completeness against required fields, (3) PM review time saved.
**Knowledge base:** project_description.txt and project_timeline.csv.

## 2. Risk identification and mitigation
**Pain point:** Inconsistent risk assessment coverage and delayed escalation.
**Agentic solution:** Risk Assessor produces categorized risk/impact/mitigation output grounded in the supplied risk register; flags assumptions.
**Inputs:** project description and risks. **Outputs:** risk matrix and recommended mitigations.
**Success metrics (proposed):** (1) source-risk coverage, (2) unsupported-risk rate, (3) reviewer acceptance rate.
**Knowledge base:** project_risks.csv and project description.

## 3. Status reporting and milestone oversight
**Pain point:** Time-consuming weekly reporting and missed blocked work.
**Agentic solution:** Status Reporter calculates task status and blocker summaries; Milestone Tracker relates the schedule to progress.
**Inputs:** task board, timeline, sprint/time request. **Outputs:** status report and milestone alerts.
**Success metrics (proposed):** (1) exact task-count accuracy, (2) blocker detection recall, (3) status-report preparation time saved.
**Knowledge base:** sample_task_board.csv and project_timeline.csv.

**Note:** Metrics above are proposed evaluation metrics, not achieved business outcomes.
