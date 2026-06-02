# Gary Dobkin - Proof of Work

Most of my current product work cannot be open-sourced. It includes active product code, auth flows, infrastructure assumptions, customer workflow detail, and security-sensitive implementation choices.

This repo is the version I can make public: short, sanitized notes on what I built, what decisions mattered, and what the work proves.

- Website: [paput.ai](https://paput.ai)
- LinkedIn: [linkedin.com/in/gvbd](https://www.linkedin.com/in/gvbd)
- GitHub: [github.com/illmethinks0](https://github.com/illmethinks0)
- Email: [gary@paput.ai](mailto:gary@paput.ai)

## If You Are Scanning Quickly

I build and operate systems where AI has to do real work, not just produce a demo. The pattern I keep coming back to is simple:

1. Make the workflow explicit.
2. Give agents narrow jobs.
3. Preserve state, evidence, and ownership.
4. Add gates where automation can create risk.
5. Make the system observable enough that a customer, operator, or executive can trust it.

## Case Studies

| Case Study | What To Look For |
| --- | --- |
| [Production Agent Systems](case-studies/production-agent-systems.md) | How I think about agent platforms: state, queues, contracts, traceability, validation, approval gates, and isolated compute paths. |
| [Customer Success + AI Operations](case-studies/customer-success-ai-operations.md) | How my customer success background changes the way I build AI workflows: adoption, handoffs, health signals, and time-to-value. |
| [Global Security Deployment](case-studies/global-security-deployment.md) | What I learned leading security deployments at scale: readiness, SLAs, escalation, regional teams, reporting, and operational trust. |

## Recent Proof Notes

- 2026-06-02: [Production Agent Systems](case-studies/production-agent-systems.md)
- 2026-06-02: [Customer Success + AI Operations](case-studies/customer-success-ai-operations.md)
- 2026-06-02: [Global Security Deployment](case-studies/global-security-deployment.md)

## Artifacts

- [Sanitized production agent workflow diagram](assets/architecture-diagrams/production-agent-workflow.md)
- [Fake-data AI compliance workflow example](examples/fake-data-ai-compliance-workflow.md)
- [AI Systems Proof Brief](proof-briefs/ai-systems-proof-brief-gary-dobkin.pdf)
- [Customer Success + AI Operations Proof Brief](proof-briefs/customer-success-ai-operations-proof-brief-gary-dobkin.pdf)
- [Simple proof page](https://illmethinks0.github.io/gary-dobkin-proof-of-work/)

## What This Proves

- I have built beyond the resume bullet. The work includes product definition, implementation, deployment posture, support workflows, and operating cadence.
- I understand why AI projects fail in production: vague ownership, weak handoffs, no durable state, no evidence, no review gates, no monitoring.
- I can connect technical systems to customer outcomes because I have run customer success, onboarding, support, security deployment, and founder-led product work.

## Current Technical Scope

Rails 8, Ruby, PostgreSQL, Solid Queue, Rodauth, Pundit, MCP, TypeScript, Python, FastAPI, Next.js, React, OpenAPI, Playwright, Docker, Render, Firecracker, Tailscale, Langfuse, GitHub Actions.

## Sanitization Rules

This repo does not include:

- private source code;
- customer names or customer data;
- secrets, logs, tokens, or infrastructure identifiers;
- screenshots from active product or customer systems;
- proprietary product detail that should remain private.

The goal is to show judgment and execution pattern without exposing private material.
