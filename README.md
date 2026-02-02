Project Kickoff Operator

A deterministic planning operator for turning vague ideas into runnable, local-first projects — designed for Claude Code.

This repository contains a single, opinionated Claude skill system prompt that behaves like a planning compiler. The skill definition lives in project-kickoff-operator.skill.md.
	•	conversational when shaping ideas
	•	deterministic and non-interactive when generating execution plans

No application code. No MCP servers. No network access.
Just a clean operator that turns intent into action.

⸻

What This Is

The Project Kickoff Operator is a planning-layer operator, not a coding agent.

Its purpose is to:
	1.	Help users refine a project idea in plain language
	2.	Convert that idea into a runnable, version-controlled project plan suitable for execution with Claude Code

It enforces:
	•	local-first workflows
	•	git from minute zero
	•	deterministic outputs
	•	explicit assumptions
	•	safety and security baselines

This mirrors how serious projects actually get built.

⸻

Why This Exists

Most “AI planning” tools fail because they:
	•	ask too many questions forever, or
	•	jump to implementation without locking interfaces, or
	•	produce plans that look detailed but are not runnable

This operator solves that by splitting planning into two strict modes:
	•	Idea Workshop → human-friendly, exploratory
	•	Project Kickoff → compiler-like, no questions, no prose, fixed structure

Once the idea is complete, the operator switches modes automatically and produces a deterministic kickoff plan.

⸻

Skill Design Principles
	•	Skills-first: reasoning only, no MCP unless strictly required
	•	Deterministic output: same input → same plan
	•	Action over tracking: every plan leads to a runnable vertical slice
	•	Local-first: no cloud dependency assumptions
	•	Honest scope: explicit tradeoffs, no magical thinking

Designed explicitly for Claude Code–style execution workflows.

⸻

How To Use (As a Claude Skill)
	1.	Create a new Claude skill (or system prompt)
	2.	Paste the contents of project-kickoff-operator.skill.md verbatim into Claude’s system prompt
	3.	Start chatting normally

You do not need to reference files, schemas, or modes.
The operator manages all internal structure implicitly.

Typical Flow
	1.	Describe an idea casually
	2.	Answer a small number of high-impact clarification questions
	3.	Say:
“Kick this off” / “Create the plan” / “I’m ready to build”
	4.	Receive a fully structured project kickoff plan, ready for execution

⸻

Output Contract (When Kicking Off)

When generating a project, the operator always outputs:
	1.	Assumptions
	2.	Stack, platform, users, scale, constraints
	3.	Repo & workspace layout
	4.	Dev environment
	5.	Run commands (install / run / test)
	6.	Minimum viable architecture
	7.	Security & safety baseline
	8.	Milestones (Day 0 / Day 1 / Day 2)
	9.	Git plan (3–7 atomic commits)
	10.	Claude Code prompt pack (6–10 prompts)

No filler. No explanations. No emojis. No questions.

⸻

What This Is Not
	•	Not a code generator
	•	Not a startup template
	•	Not a SaaS
	•	Not a generic prompt collection

It is a reference operator for disciplined project execution.

⸻

Who This Is For
	•	Developers using Claude Code
	•	Product-minded builders
	•	Research engineers
	•	Anyone who wants plans that actually run

⸻

License

MIT — use freely, adapt thoughtfully.
