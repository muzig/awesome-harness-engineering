# Awesome Harness Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of articles, essays, benchmarks, and reference implementations for harness engineering: the practice of building the context, constraints, feedback loops, and runtime scaffolding that make AI agents reliable.

Inspired by the [awesome](https://github.com/sindresorhus/awesome) list thing.

Harness engineering sits between context engineering, architecture, evaluation, observability, and orchestration. This list focuses on practical material for teams building long-running, production-grade agents.

## Table of Contents

- [Definitions & Field Notes](#definitions--field-notes)
- [Long-Running Agents & Working State](#long-running-agents--working-state)
- [Operating Principles & Playbooks](#operating-principles--playbooks)
- [Evals, Benchmarks & Observability](#evals-benchmarks--observability)
- [Orchestration & Reference Implementations](#orchestration--reference-implementations)
- [Contributing](#contributing)

---

## Definitions & Field Notes

### Harness engineering: leveraging Codex in an agent-first world

> OpenAI's flagship field report on building a large application with Codex, emphasizing architectural rigidity, repo-local knowledge, browser-driven validation, and observability as harness primitives.

[Read](https://openai.com/index/harness-engineering/)

### Effective harnesses for long-running agents

> Anthropic's canonical breakdown of failure modes in long-running coding agents, including initializer agents, feature lists, `init.sh`, self-verification, and handoff artifacts across context windows.

[Read](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)

### The Anatomy of an Agent Harness

> A crisp definition from LangChain: agent = model + harness, where the harness includes prompts, tools, infrastructure, orchestration, and deterministic middleware.

[Read](https://blog.langchain.com/the-anatomy-of-an-agent-harness/)

### Harness Engineering

> Birgitta Bockeler's Thoughtworks framing of harness work into three buckets: context engineering, architectural constraints, and "garbage collection" against entropy.

[Read](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering.html)

### Skill Issue: Harness Engineering for Coding Agents

> A practical essay from HumanLayer on why coding-agent results are often limited more by harness design than by model quality.

[Read](https://www.humanlayer.dev/blog/skill-issue-harness-engineering-for-coding-agents)

### Your Agent Needs a Harness, Not a Framework

> Inngest's case for treating retries, state persistence, event routing, concurrency control, and traces as harness concerns rather than model concerns.

[Read](https://www.inngest.com/blog/your-agent-needs-a-harness-not-a-framework)

### What Is Harness Engineering? Complete Guide for AI Agent Builders

> A high-signal secondary overview that synthesizes the emerging term, its pillars, and why better harnesses often matter more than swapping models.

[Read](https://www.nxcode.io/resources/news/what-is-harness-engineering-complete-guide-2026)

## Long-Running Agents & Working State

### Harness design for long-running application development

> Anthropic's follow-up case study on long-running app generation, with generator/evaluator separation, structured task state, and better self-evaluation loops.

[Read](https://www.anthropic.com/engineering/harness-design-long-running-apps)

### Context Engineering for AI Agents: Lessons from Building Manus

> A deeply practical context-engineering playbook: KV-cache discipline, tool masking, filesystem memory, todo recitation, and keeping failures in the context.

[Read](https://manus.im/blog/Context-Engineering-for-AI-Agents-Lessons-from-Building-Manus)

### My AI Adoption Journey

> Mitchell Hashimoto's practitioner diary, notable for the "Engineer the Harness" stage: turn repeated agent failures into better `AGENTS.md` instructions and real tools.

[Read](https://mitchellh.com/writing/my-ai-adoption-journey)

### Humans and Agents in Software Engineering Loops

> A useful mental model from Thoughtworks: humans improve the "how loop" by strengthening the harness, instead of manually inspecting every artifact.

[Read](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html)

## Operating Principles & Playbooks

### 12 Factor Agents

> HumanLayer's operating principles for production agents: own prompts, own context, unify execution and business state, launch/pause/resume cleanly, and prefer small focused agents.

[Read](https://www.humanlayer.dev/blog/12-factor-agents)

### 12-Factor AgentOps

> An operations-focused companion that emphasizes context discipline, git-based workflows, scoped sessions, research-before-build, and external validation.

[Read](https://www.12factoragentops.com/)

### GitHub: humanlayer/12-factor-agents

> The canonical repo version of the 12-factor principles, useful as a shareable reference inside teams.

[Read](https://github.com/humanlayer/12-factor-agents)

## Evals, Benchmarks & Observability

### Testing Agent Skills Systematically with Evals

> OpenAI's concrete guide to turning agent traces into repeatable evals with JSONL logging, deterministic checks, and failure-driven coverage.

[Read](https://developers.openai.com/blog/eval-skills/)

### Improving Deep Agents with harness engineering

> LangChain shows a large benchmark gain from harness changes alone, detailing self-verification loops, context injection, and loop-detection middleware.

[Read](https://blog.langchain.com/improving-deep-agents-with-harness-engineering/)

### Evaluating Deep Agents: Our Learnings

> LangChain's testing patterns for stateful agents, including single-step evals, full-turn evals, multi-turn evals, and clean per-run environments.

[Read](https://www.blog.langchain.com/evaluating-deep-agents-our-learnings/)

### HAL: Holistic Agent Leaderboard

> A standardized, cost-aware third-party leaderboard plus evaluation harness for comparing agents across benchmarks with trace logging and reliability views.

[Read](https://hal.cs.princeton.edu/)

### Terminal-Bench

> A benchmark suite for terminal-native agents, especially relevant when your harness lives in shells, filesystems, sandboxes, and verification scripts.

[Read](https://www.tbench.ai/)

### Introducing Terminal-Bench 2.0 and Harbor

> The launch note for a harder Terminal-Bench plus Harbor, a generalized harness for large-scale evaluation and agent improvement.

[Read](https://www.tbench.ai/news/announcement-2-0)

## Orchestration & Reference Implementations

### Agent Frameworks, Runtimes, and Harnesses, Oh My!

> A useful decomposition from LangChain for deciding what should live in a framework, what should live in a runtime, and what belongs in the harness.

[Read](https://blog.langchain.com/agent-frameworks-runtimes-and-harnesses-oh-my/)

### GitHub: inngest/utah

> A reference implementation of a durable, event-driven agent harness with steps, retries, sub-agents, concurrency control, and channel-agnostic triggers.

[Read](https://github.com/inngest/utah)

## Contributing

Contributions welcome. Please prefer resources that are:

- Primary sources or original implementations
- Specific about failure modes, constraints, evals, or runtime design
- Useful to someone building an agent harness today

Not every agent framework belongs here. Favor materials that explain how the harness itself is designed, improved, or measured.
