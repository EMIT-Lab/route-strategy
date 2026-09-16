# ROUTE Strategy — v1.0

**Strategy-first AI collaboration for research, writing, presentations, grants, decisions, and other high-value work.**

> **Do not confuse the requested deliverable with the real objective.**
>
> The goal is not to make AI do more work.  
> **The goal is to make sure the work is worth doing.**

ROUTE is a reusable problem-solving protocol for working with AI before premature execution:

- **R — Reframe the task**
- **O — Define the Outcome**
- **U — Understand the game**
- **T — Test the strategy**
- **E — Execute by gates**

It is designed for situations where a polished answer to the wrong problem would still be a failure.

---

## Why ROUTE exists

A default AI assistant is often optimized to be helpful by executing the stated request:

> "Write the speech."  
> "Polish the response to the reviewer."  
> "Improve this research plan."  
> "Make the slides."

For low-stakes tasks, that is exactly what we want.

For consequential tasks, however, the requested output is often only a **means**. The real task may be to change a reviewer's judgment, position a paper, choose a research direction, win institutional support, persuade a stakeholder, avoid an irreversible strategic mistake, or decide not to do the requested work at all.

ROUTE inserts a strategy layer before execution.

---

## Repository structure

```text
route-strategy/
├── README.md
├── SKILL.md
├── VERSION
├── agents/
│   └── openai.yaml
├── examples/
│   ├── 01-paper-reviewer-novelty.md
│   ├── 02-research-project-reframing.md
│   └── 03-high-stakes-presentation.md
└── integrations/
    ├── chatgpt/
    │   └── PROJECT_INSTRUCTIONS.md
    └── codex/
        └── AGENTS.md
```

---

# 1. Use in ChatGPT on the web

For teaching and personal use, the simplest deployment is a dedicated ChatGPT Project.

1. Create a Project, e.g. **Strategy-First Research**.
2. Open **Project settings → Project instructions**.
3. Copy the contents of:
   `integrations/chatgpt/PROJECT_INSTRUCTIONS.md`
4. Use this Project for research planning, paper strategy, grants, major presentations, career decisions, and other high-value work.
5. Keep routine editing/calculation tasks outside this Project if you want to avoid unnecessary strategic overhead.

### Teaching recommendation

Ask students to maintain two workspaces for comparison:

- **Normal Research** — no ROUTE instructions
- **ROUTE Research** — ROUTE Project Instructions enabled

Run the same real task in both and compare **problem definition**, not prose quality.

---

# 2. Install as a Codex skill

Current OpenAI Codex documentation (verified 2026-09-03) loads user skills from:

```text
$HOME/.agents/skills/
```

and repository skills from:

```text
$REPO_ROOT/.agents/skills/
```

### Personal installation

Copy this entire folder so that the final path is:

```text
$HOME/.agents/skills/route-strategy/SKILL.md
```

For example:

```bash
mkdir -p "$HOME/.agents/skills"
cp -R route-strategy "$HOME/.agents/skills/route-strategy"
```

Then invoke it explicitly in Codex with:

```text
$route-strategy
```

Codex can also discover a skill implicitly from the `description` in `SKILL.md`.

### Repository-level installation

For a shared research/code repository:

```text
your-project/
└── .agents/
    └── skills/
        └── route-strategy/
            └── SKILL.md
```

This makes the skill available in that repository context.

### GitHub installation

Once this folder is hosted on GitHub, Codex's built-in `$skill-installer` can install a skill from a GitHub directory URL. After installation, if it does not appear immediately, restart Codex.

---

# 3. Add the ROUTE trigger to Codex AGENTS.md

`SKILL.md` contains the full workflow. `AGENTS.md` should contain only the **triggering habit**.

Copy or merge:

```text
integrations/codex/AGENTS.md
```

into either:

```text
~/.codex/AGENTS.md
```

for global personal guidance, or:

```text
<repository-root>/AGENTS.md
```

for project-specific guidance.

This creates a two-layer system:

```text
AGENTS.md
    ↓
"When should I stop and think strategically?"
    ↓
$route-strategy
    ↓
"How exactly should I perform the strategic analysis?"
```

Do not duplicate the whole ROUTE protocol inside `AGENTS.md`.

---

# 4. Recommended training progression

ROUTE should train the **human**, not merely make the AI more autonomous.

### Stage 1 — Explicit invocation

Students must decide when to type:

```text
$route-strategy
```

Goal: develop the metacognitive question:

> **Is this a task I should execute, or a task I should first reframe?**

Do not add automatic ROUTE triggering yet.

### Stage 2 — Assisted invocation

Add the supplied `AGENTS.md` trigger.

Codex should notice strategically consequential tasks and suggest or use ROUTE when appropriate.

### Stage 3 — Natural collaboration

Students should become able to move fluidly among:

```text
Strategy → Structure → Artifact → Polish
```

without mechanically running a long framework every time.

The final goal is not ritual compliance with ROUTE.  
The final goal is **better judgment**.

---

# 5. When ROUTE SHOULD trigger

Strong candidates include:

- deciding what a paper is really about;
- responding to a reviewer whose criticism may reveal a deeper manuscript problem;
- selecting or redefining a research project;
- choosing experiments when the scientific claim is uncertain;
- designing a grant strategy;
- preparing a high-stakes speech, interview, defense, pitch, or presentation;
- making a career or collaboration decision;
- planning a multi-stage project where an early choice constrains later work;
- tasks with important stakeholders, incentives, power, reputation, or resource allocation;
- requests where the user has specified an output, but not why that output matters.

---

# 6. When ROUTE SHOULD NOT trigger

Do not turn ROUTE into "strategic theater."

Usually execute directly for:

- unit conversion;
- simple factual lookup;
- routine translation;
- spelling or grammar correction;
- reformatting a citation;
- changing a figure label;
- straightforward code edits with clear acceptance criteria;
- reversible, low-cost tasks where reframing would not change the approach.

A key competence is knowing **when not to use the framework**.

---

# 7. The Strategy Contract

For strategically important tasks, ROUTE tries to establish six things:

```text
Surface task:
Real objective:
Key stakeholder:
Success criterion:
Strategic risk:
Recommended first move:
```

If these are materially different from the user's literal request, the AI should surface the mismatch before doing substantial downstream work.

---

# 8. A 20-minute classroom exercise

For a new-student training session:

### Round 1 — 3 minutes
Give everyone the same consequential prompt and ask normal ChatGPT/Codex to answer it.

### Round 2 — 5 minutes
Run the same prompt with ROUTE.

### Round 3 — 5 minutes
Compare the two answers using only four questions:

1. Did either answer redefine the problem?
2. Did it identify who actually determines success?
3. Did it identify a way the task could be executed well and still fail?
4. Did the strategy change what should be done first?

### Round 4 — 7 minutes
Give four mini-tasks and ask students **whether ROUTE should be invoked at all**.

The most important learning outcome is not "students can use a skill." It is:

> **Students can recognize when execution itself is premature.**

---

# 9. Design principles

ROUTE deliberately avoids several failure modes.

### No endless questioning
Ask only questions whose answers could materially change the strategy. Otherwise make reasonable assumptions and proceed.

### No invented hidden motives
Infer underlying objectives only when context supports them. Distinguish fact, inference, and hypothesis.

### No compulsory disagreement
"Challenge the user" does not mean disagree for performance. Falsification is useful only after the right problem has been identified.

### No analysis paralysis
ROUTE must eventually choose a route and execute. Strategy is a gate, not a permanent waiting room.

### No generic stakeholder lists
Identify the actor or criterion that actually determines success.

### No polished wrong answers
A beautiful artifact built on a bad framing is still a failed interaction.

---

# 10. Version

**v1.0 — 2026-09-03**

This first public-ready version is instruction-only. Future versions can add:

- domain skills built on top of ROUTE (`paper-strategy`, `grant-strategy`, etc.);
- eval cases for trigger/no-trigger classification;
- student reflection rubrics;
- structured adversarial review ("grill") as a child skill;
- plugin packaging for one-click distribution.

Before public release, choose and add the license that matches how you want others to reuse the material.
