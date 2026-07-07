# Homework Module 3: AI Orchestration with Kestra

This homework was completed directly in the Kestra UI, including running flows, inspecting logs, and modifying a flow prompt. These changes were not made in local code files.

## Setup

GitHub Codespaces is used with Docker Compose to run Kestra locally.

From the 03-orchestration directory, Kestra is started with:

```bash
cd 03-orchestration
docker compose up -d
```

Environment variables were stored in a local .env file in the project root.

```bash
GEMINI_API_KEY=...
OPENAI_API_KEY=...
TAVILY_API_KEY=...
KESTRA_USERNAME=...
KESTRA_PASSWORD=...
POSTGRES_USER=...
POSTGRES_PASSWORD=...
```

Before running Docker Compose, the environment variables were loaded:

```bash
source ../.env
```

Then the base64-encoded secrets were exported:

```bash
export SECRET_GEMINI_API_KEY=$(echo -n "$GEMINI_API_KEY" | base64)
export SECRET_OPENAI_API_KEY=$(echo -n "$OPENAI_API_KEY" | base64)
export SECRET_TAVILY_API_KEY=$(echo -n "$TAVILY_API_KEY" | base64)
```

The example flows from the 03-orchestration/flows directory were imported into Kestra.

Questions were answered based on the videos, instructions, Kestra UI runs, and execution logs.
