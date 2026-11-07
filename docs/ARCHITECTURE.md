# Architecture and data flow

See the Mermaid diagram in the repository README. **Router/Dispatcher** is chosen because plan, risk, status and milestone requests require different data and outputs. Main Orchestrator accepts the user input, calls Router, dispatches to one specialist, and returns the structured result. Langfuse captures traces where configured.

## Input contracts
- `project_description.txt`: client scope, objectives and business context.
- `project_risks.csv`: recorded project risks and mitigations.
- `sample_task_board.csv`: task IDs, sprint, status, assignee and due dates.
- `project_timeline.csv`: phases, relative weeks, activities and milestones.

## Validation contract
Ground all factual claims in the source; label recommendations; reject unsupported assumptions; compute counts deterministically; ask for missing scope or date anchors. Human review precedes external sharing.

## Environment limitations
Langflow Desktop 1.11.0 on Windows; imported JSON may contain local flow IDs and machine-specific paths. No live Gmail/Slack integration is included.
