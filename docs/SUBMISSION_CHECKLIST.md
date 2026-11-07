# Submission checklist

- [x] README and Mermaid architecture diagram
- [x] Q1 ideation document (three use cases)
- [x] Q2 design/build/cost/evaluation write-up
- [x] Q3 program charter
- [x] Q4 reflection and next steps
- [x] Six exported Langflow workflows included
- [x] Official T1–T12 baseline test inputs included
- [ ] **Review all exported workflows for secrets and private paths before publishing**
- [ ] Add screenshots: full canvas, example agent outputs, Langfuse traces
- [ ] Attach verified result evidence for all 12 baseline prompts; mark only supported PASS/FAIL
- [ ] Add actual model token/cost evidence or explicitly state not measured
- [ ] Test imports/flow-ID references in the final environment
- [ ] Create GitHub repository and upload package contents (not the outer ZIP alone)
- [ ] Submit GitHub repository URL plus required documents

## Suggested screenshots
`evidence/01_main_orchestrator.png`, `02_planner_output.png`, `03_risk_output.png`, `04_status_output.png`, `05_milestone_output.png`, `06_langfuse_trace.png`.

## Final statement for reviewer
Mira is a Langflow-based, source-grounded, router-orchestrated PM/TPM assistant with planning, risk, status and milestone specialist workflows. It uses structured validation and Langfuse observability. Interactive tests were conducted; automated export evidence is incomplete and must be distinguished from successful agent runs.
