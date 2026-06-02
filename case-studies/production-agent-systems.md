# Production Agent Systems

**Relevant for:** AI startup leadership, Head of Engineering - AI Stack, CTO/co-founder, forward-deployed AI, agent systems, AI compliance/security platforms.

## Context

Paput.ai / EUCompli.ai started from a recurring problem I had seen across operations and customer success: teams want automation, but the implementation burden often becomes the product.

For compliance and security-adjacent workflows, a simple chat interface is not enough. The system has to remember what happened, explain why it happened, preserve evidence, and give a human a clean place to intervene.

## What I Built

I built the product around a Rails 8 control plane rather than treating the LLM as the application.

The useful pieces are the boring ones:

- persistent tasks and phase state;
- queue-backed execution with Solid Queue;
- structured findings and artifacts;
- auth, authorization, and subscription gates;
- traceable tool calls;
- audit logs and evidence bundles;
- watchdog and recovery paths;
- human review gates for risky or customer-visible work;
- observability for cost, queues, runtime behavior, and stale jobs.

## Key Decisions

**Use narrow agents instead of broad assistants.**  
Each agent should have a job, a schema, and a boundary. That makes outputs easier to validate and handoffs easier to debug.

**Keep state outside the prompt.**  
The database and queue should know what phase the workflow is in. The model should not be the source of truth.

**Treat evidence as a first-class output.**  
For compliance work, an answer without supporting evidence is not enough. The system needs artifacts, records, and a path back to how a finding was produced.

**Design for isolated compute before it becomes urgent.**  
The current orchestration can run through Rails and Solid Queue, but heavier scan workloads need a path into Firecracker-backed isolated compute without breaking contracts, state, gates, monitoring, or reporting.

## Constraints

- Product code and infrastructure details are private.
- Some workflows touch compliance and security-sensitive assumptions.
- The public proof has to describe the architecture without exposing implementation details that should stay private.

## Evidence I Can Talk About Publicly

- Rails 8 control plane with PostgreSQL, Solid Queue, auth, authorization, API surfaces, and deployment posture.
- Structured scan and workflow phases with persisted findings, artifacts, and audit evidence.
- Agent patterns built around roles, schemas, tool use, review gates, and traceability.
- Firecracker path for heavier workloads, higher scan volume, and concurrent agent execution.
- Monitoring patterns around queues, runtime behavior, cost, stale work, and reporting.

## Related Systems I Have Built

The same pattern shows up across several private systems I have been building:

- compliance scanner work with dispatch records, signed callbacks, checksum-backed artifacts, and audit evidence;
- operational SaaS work with reviewable agent actions, approval requests, change-event history, message intake, customer portal, billing, inventory, knowledge, and reports;
- risk-gated agent runtime work with paper-mode defaults, proposal-card evidence, deterministic inputs, scheduler/dashboard surfaces, capital-floor controls, and kill switches;
- agent monitoring work for local and remote AI instances;
- developer workflow tooling that loads project instructions and turns LLM review/build/debug loops into repeatable commands.

## What I Would Improve Next

- Add more fake-data examples from intake to final evidence bundle.
- Add screenshots from a demo environment rather than an active product environment.

## What This Proves

I know how to make AI work inside an operating system: state, contracts, tooling, review, evidence, and deployment constraints. That is the part most demos skip.
