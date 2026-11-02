# Power BI Translytical AI Benchmark

This project compares how far AI coding agents can go when working with **Power BI and Microsoft Fabric**.

The benchmark compares:

- **OpenAI Codex**
- **GitHub Copilot**

Both agents received the same semantic model, business scenario and frozen prompts.

The experiment was divided into two stages.

## Stage 1 — Power BI report authoring

The first benchmark tested whether each agent could independently create an executive Power BI report using an existing semantic model.

The business focus was:

- Store performance
- Inventory availability
- Inventory risk
- Sales and margin context

OpenAI produced the version I preferred because it created a clearer analytical journey and connected store performance with inventory availability more naturally.

## Stage 2 — Translytical write-back

The second benchmark tested whether the agents could turn the analytical report into an operational experience using:

- Power BI Translytical Task Flows
- Fabric User Data Functions
- Fabric SQL Database
- Direct Lake
- DirectQuery

The goal was to allow a store manager to:

**Identify inventory risk → create an action → assign an owner → set a due date → track it → update it**

without leaving Power BI.

## Results

### OpenAI Codex

OpenAI reached a working Translytical architecture including:

- Fabric SQL write-back layer
- User Data Functions
- Authentication logic
- Optimistic concurrency
- DirectQuery read-back
- Direct Lake analytical data
- Power BI operational UX

The final semantic model combined:

**Direct Lake for analytics + DirectQuery for operational actions**

The native Data Function buttons still required final manual configuration in Power BI.

### GitHub Copilot

Copilot also made meaningful progress.

It created the Fabric SQL Database, validated the operational tables, constraints and indexes, and produced a local UDF implementation with four passing tests.

However, the UDF was not successfully published to Fabric and the Power BI Translytical report was not completed end-to-end.

## Agent-built vs human-refined

The repository also includes:

- the original OpenAI agent-built report
- the human-refined version
- architecture diagrams
- benchmark screenshots
- frozen prompts
- implementation evidence

The human refinement focused on UX and storytelling rather than changing the underlying business logic.

The final journey became:

**Store performance → Inventory risk → Action → Tracking**

## Runtime requirement

This solution was built and validated using a **Microsoft Fabric Trial capacity**.

The repository preserves the report design, architecture and implementation artifacts, but the live Direct Lake, Fabric SQL Database and Translytical write-back experience requires an active Microsoft Fabric capacity.

## Repository structure

```text
powerbi-translytical-ai-benchmark/
│
├── README.md
├── prompts/
├── screenshots/
│   ├── first-benchmark/
│   ├── openai-agent-built/
│   ├── openai-human-refined/
│   └── copilot/
├── architecture/
├── openai/
├── copilot/
└── docs/
```

## Notes

This repository documents an AI-assisted BI engineering experiment.

I designed and supervised the benchmark, reviewed the agents’ technical decisions and results, intervened where necessary, and performed the final BI validation and UX refinements.
