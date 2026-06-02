# Systems Built Index

**Relevant for:** AI startup leadership, forward-deployed AI, AI operations, customer success transformation, security/compliance platforms, agent systems.

Most of my current work cannot be open-sourced. The code touches active products, customer workflows, auth, infrastructure, and security assumptions.

This is the public-safe version: what the systems prove without exposing private source code, customer data, credentials, prompts, logs, hostnames, IPs, or active infrastructure detail.

## The Pattern

Across the projects I have been building, the same pattern keeps showing up:

1. Start with the operating workflow.
2. Make the system of record explicit.
3. Give agents narrow jobs and schemas.
4. Route risky work through approval gates before it touches customers, money, security, or production state.
5. Preserve artifacts, state, and evidence.
6. Make the workflow observable enough for an operator, customer, or executive to trust it.

## High-Signal Systems

| System Area | What It Demonstrates |
| --- | --- |
| EU compliance scanner | Rails control plane, queue-backed orchestration, specialized agent phases, dispatch/callback contracts, persisted findings, audit evidence, and a Firecracker-backed isolated compute path for heavier scan workloads. |
| Operational SaaS for field service | Tenant-scoped operations, message intake, reviewable agent actions, approval requests, change-event history, customer portal, billing foundation, inventory, knowledge, and generated reports. |
| Risk-gated agent runtime | Safe-by-default execution, deterministic inputs, proposal-card evidence, scheduler/dashboard/gateway surfaces, kill switch, capital floor, and testable risk boundaries. |
| Document automation SaaS | Real-world PDF automation with coordinate-based filling, form-field fallbacks, validation scripts, multi-format workflow planning, authentication, and end-to-end testing. |
| AI agent monitoring app | macOS menu bar control surface for monitoring local and remote agent instances, including SSH trust and instance configuration. |
| Operator governance runtimes | Independent worker identities, gateway boundaries, backup/readback checks, callback paths, approval rules, and evidence-first operating docs for internal agents. |
| LLM build/debug CLI | Local developer workflow for review, build, and debug loops that loads project instructions, keeps task state, and turns AI work into repeatable commands. |
| Grant and storage SaaS builds | Multi-tenant product surfaces with auth, payments, queues, dashboards, collaboration, organization scoping, and AI-assisted workflow features. |

Some of these systems are active product work. Some are internal tools. Some are build/spec work that shaped later implementation. I am careful not to turn every folder into a production claim.

## What I Deliberately Do Not Publish

- private product source code;
- customer records, screenshots, logs, prompts, or payloads;
- credentials, account claims, hostnames, IPs, or infrastructure paths;
- vendor repos or third-party code as personal proof;
- draft/spec-only claims as production proof.

## What This Proves

I am not only experimenting with agents. I am building the surrounding operating system: state, queues, contracts, approvals, observability, evidence, supportability, and deployment posture.

That is the part a customer or operator actually has to trust.
