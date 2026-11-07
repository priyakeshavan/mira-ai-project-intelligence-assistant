# Mira workflow exports — GitHub review copies

These are the six user-supplied Langflow JSON exports. Local absolute CSV paths have been replaced with relative `data/...` references for portability. LLM components reference the `OPENAI_API_KEY` environment variable.

## Important before importing or running
- Set credentials in your own Langflow environment; never commit actual secrets.
- Reconfigure the Status Reporter and Milestone Tracker CSV file paths to actual files on your computer.
- Reconfigure the Main Orchestrator Run Flow selection and specialist flow IDs for your own Langflow instance.
- Recheck any custom Python components for environment-specific assumptions.
- These are static export checks, **not** a runtime security audit or a verified successful import.
- No source CSV files are bundled in this folder.
