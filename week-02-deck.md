---
marp: true
theme: default
paginate: true
header: "CSC 394 — Week 2"
footer: "Project Management and Roles"
style: |
  section {
    font-size: 28px;
  }
  section.lead h1 {
    font-size: 48px;
  }
  section.lead h3 {
    font-size: 24px;
    color: #666;
  }
  table {
    font-size: 22px;
  }
  blockquote {
    border-left: 4px solid #0366d6;
    padding-left: 16px;
    color: #444;
    font-style: italic;
  }
---

<!-- _class: lead -->
<!-- _paginate: false -->

# Week 2: Project Management and Roles

### CSC 394 · DePaul University

---

# Last Week → This Week

**Week 1:** Requirements, AI-assisted development

**Today:** Roles · Agile · Scoping · Risks · Workflow

<!-- Moving from WHAT to build → HOW to build it together. -->

---

# Projects Fail from **Organization**, Not Code

🔴 Poor communication
🔴 No clear ownership
🔴 Scope creep

> "We all assumed someone else was doing it."

---

# Communication Lines Grow Fast

**Brooks's Law:** Communication channels = **n(n−1) / 2**

| Team Size | Communication Lines |
|:---------:|:-------------------:|
| 2 | 1 |
| 4 | 6 |
| 6 | 15 |

Structure (roles, boards, meetings) tames this complexity.

---

# Visibility Is Everything

❌ "I think Alex is working on login..."
❌ "The backend is... mostly done?"

✅ Your task board = **single source of truth**

Every team member should be able to answer:
*What are we building? What's done? What's blocked?*

---

# "We'll Just Figure It Out"

Sounds agile — but means nobody is responsible.

Agile does **NOT** mean no plan.
It means: plan, execute in short cycles, inspect, adapt.

That requires **more discipline** than waterfall, not less.

---

<!-- _class: lead -->

# Team Roles

---

# Six Core Roles

| Role | Owns |
|------|------|
| **Project Manager** | Schedule, communication, blockers |
| **Tech Lead** | Architecture, tech decisions |
| **Frontend Lead** | UI/UX implementation |
| **Backend Lead** | API, database, server |
| **QA Lead** | Testing, quality gates |
| **DevOps Lead** | CI/CD, deployment, repo |

Everyone codes. Roles = **decision ownership**.

---

# The "One Name" Rule

> Every task has **exactly one owner**.

❌ "The team will handle deployment"
✅ "**Maria** owns deployment by Friday"

Shared responsibility = no responsibility.

---

# Combining Roles for Small Teams

| Team of 4 | Team of 5 | Team of 6 |
|-----------|-----------|-----------|
| PM + QA | PM | PM |
| Tech Lead + DevOps | Tech Lead + DevOps | Tech Lead |
| Frontend Lead | Frontend Lead | Frontend Lead |
| Backend Lead | Backend Lead + QA | Backend Lead |
| | | QA + DevOps |

- PM + QA pairs well (both track progress and issues)
- Tech Lead + DevOps pairs well (architecture aligns with build/deploy)
- **Never** combine Frontend + Backend — they need healthy tension

---

# TaskBoard Team Example (5 people)

| Person | Role(s) | Week 1 Task |
|--------|---------|-------------|
| Priya | PM | Set up project board |
| James | Tech Lead + DevOps | Create repo & CI |
| Sofia | Frontend Lead | Wireframe board view |
| Malik | Backend Lead | Design DB schema |
| Chen | QA Lead | Write Definition of Done |

Consider rotating PM each sprint.

---

# 💬 Discussion

> Your team of 4 has PM also serving as QA. This week: 8 bugs to triage AND sprint planning to run.

**How do you handle it while keeping accountability clear?**

---

<!-- _class: lead -->

# Agile Basics

---

# What Is Agile?

The Agile Manifesto (2001) prioritizes:

- **Individuals** over process
- **Working software** over documentation
- **Collaboration** over contracts
- **Responding to change** over following a plan

🔄 **Iterative** — repeated cycles, not big-bang
📦 **Incremental** — working pieces each cycle
🔀 **Adaptive** — change the plan as you learn

---

# The Sprint Cycle

```
PLAN  →  BUILD  →  REVIEW  →  RETRO  →  REPEAT
```

- **Plan:** What to build this sprint?
- **Build:** Heads-down development
- **Review:** Demo working software
- **Retro:** What went well / didn't?

**Your sprints = 1 week** (Weeks 3–10)

---

# Sprint Ceremonies

| Ceremony | When | Purpose |
|----------|------|---------|
| **Sprint Planning** | Start of sprint | Pick & assign tasks |
| **Standup** | 2–3×/week | Done, doing, blocked |
| **Sprint Review** | End of sprint | Demo working software |
| **Retrospective** | End of sprint | Improve process |

Standups can be async (Slack/Discord).
3 questions: *What did I do? What will I do? Blockers?*

---

# The Task Board

```
BACKLOG → TO DO → IN PROGRESS → IN REVIEW → DONE
```

- Cards move **left to right**
- **WIP limit:** max 1–2 "In Progress" per person
- If it's not on the board, it doesn't exist
- Moving to "Done" requires meeting the **Definition of Done**

> 5 tasks in-progress = 0 tasks done. Focus.

---

# GitHub Projects Setup

1. Repo → **Projects** → **New** → **Board** view
2. Columns: Backlog | To Do | In Progress | In Review | Done
3. Fields: Assignee, Priority, Size, Sprint
4. Every task = a **GitHub Issue**
5. Labels: Priority (`P0`–`P3`), Type (`feature`/`bug`/`chore`), Size (`XS`–`XL`)
6. Enable automation (auto-move on PR merge)

PM owns this — set up before next class.

---

# Writing Good Issues

Each issue needs:
- **Title** — short and clear
- **User story** — "As a ___, I want ___, so that ___"
- **Acceptance criteria** — checkboxes

> **User can create a new task**
> As a team member, I want to create a task so I can track work.
> - [ ] "New Task" button on board
> - [ ] Form with title (required), description, assignee, priority
> - [ ] Submitting creates task in "To Do" column
> - [ ] Persists across refresh

---

# T-Shirt Sizing

| Size | Effort | Example |
|:----:|--------|---------|
| **XS** | Trivial | Update README |
| **S** | Small | One API endpoint |
| **M** | Medium | Login page + validation |
| **L** | Large | Drag-and-drop board |
| **XL** | Too big | ⚠️ **Break it down!** |

Sprint target ≈ 2–3 **M** tasks per person.
Relative sizing beats exact hours.

---

# 💬 Discussion

> Your teammate estimates "user registration and login" as a **Small**.
> You think it's a **Large**.

**How do you resolve this?**

---

# Definition of Done ✅

An **agreed checklist** every task must pass:

- [ ] Code compiles/runs without errors
- [ ] Feature matches acceptance criteria
- [ ] At least one test covers the feature
- [ ] Code reviewed by one teammate (PR)
- [ ] No known bugs introduced
- [ ] Docs updated if needed

**"Works on my machine" ≠ Done**
Prevents the "90% done" trap. QA Lead enforces.

---

# Sample Sprint Plan — TaskBoard Sprint 1

**Sprint Goal:** *Users can sign up, log in, and create tasks on a board.*

| # | User Story | Size | Assignee | Status |
|---|-----------|:----:|----------|--------|
| 1 | Repo + README setup | S | Alice | Done |
| 2 | DB schema (tasks/users) | M | David | Done |
| 3 | User registration API | M | David | In Review |
| 4 | User login API | M | David | In Progress |
| 5 | Task creation API | M | David | To Do |
| 6 | Registration/login UI | M | Carol | In Review |
| 7 | Task creation form UI | M | Carol | To Do |
| 8 | CI/CD (GitHub Actions) | S | Bob | Done |
| 9 | Registration tests | S | Eve | In Progress |
| 10 | Task creation tests | S | Eve | To Do |

---

# 💬 Discussion

> David has 4 tasks while others have 1–2.

**Is this a problem? What would you do?**

---

<!-- _class: lead -->

# Scoping Your Project

---

# MVP = Minimum Viable Product

> The **smallest version** that delivers **real value**.

Not a mockup. A **working** app with fewer features.

**TaskBoard MVP:**
*A user can create an account, log in, create tasks, and see them on a board.*

No due dates. No notifications. No drag-and-drop.

🎯 **Working MVP by Week 6**

---

# Realistic Timeline

| Phase | Weeks | Activity |
|-------|:-----:|----------|
| Setup & Organizing | 1–3 | Roles, repo, planning |
| Feature Building | 4–8 | Core development |
| Integration & Polish | 9–10 | Bug fixes, final features |
| Presentation | 11 | Demo day |

**~5 weeks of peak productivity.** Scope accordingly.

---

# MoSCoW Prioritization — TaskBoard

| Priority | Features |
|----------|----------|
| **Must** | CRUD tasks, board view, auth, assignment |
| **Should** | Due dates, labels, search |
| **Could** | Drag-and-drop, dark mode, activity log |
| **Won't** | Real-time collab, mobile, AI suggestions |

**Must Have = your MVP.** Ship this first.
**Won't Have** protects against scope creep.

---

# Cut Scope, Not Quality

| ✅ Do | ❌ Don't |
|-------|---------|
| Remove a feature | Skip testing |
| Simplify UI | Skip code review |
| Postpone nice-to-haves | Deploy broken code |

> **5 polished features beats 10 broken ones.**

When behind: (1) ground in data, (2) refer to MoSCoW, (3) defer don't delete, (4) team decision.

---

# Common Scoping Mistakes

🚫 **Too Ambitious** — "Spotify but better"
🚫 **Goldplating** — Perfect login, nothing else done
🚫 **No Priorities** — Everything is "must have"
🚫 **Feature Creep** — "One more thing..." weekly
🚫 **Technology Tourism** — Proven tech; one new thing max
🚫 **All Plan, No Build** — Still designing in Week 5

**Fix:** Prioritize. Ship. Iterate.

---

# 💬 Discussion

> Two days to Sprint 2 demo. In progress:
> - Task assignment (**Must**, 80% done)
> - Due dates (**Should**, 50% done)
> - Notifications (**Could**, 20% done)

**What do you do?**

---

<!-- _class: lead -->

# Risk Management

---

# What Is a Risk?

Something that **might** happen that would **hurt your project**.

- If it already happened → it's a **problem**
- Risk management = identifying potential problems early

These risks happen **every quarter:**

| Risk | Likelihood |
|------|:----------:|
| Team member drops or goes silent | Med |
| Tech harder than expected | Med |
| Frontend/backend integration fails | High |
| Team can't agree on decisions | Med |
| Scope too large for timeline | High |

---

# Risk Register (TaskBoard)

| Risk | Impact | Mitigation | Owner |
|------|:------:|------------|-------|
| Member drops | High | Cross-train, no SPOF | PM |
| Tech too hard | High | Prototype risky parts early | Tech Lead |
| Integration fail | High | API contracts early | Backend |
| Disagreements | Med | Vote; TL breaks ties | PM |
| Scope too large | High | MoSCoW + MVP check Wk 6 | PM |
| Auth harder than est. | Med | Use proven library; spike early | Backend |
| Deploy fails late | High | Deploy Sprint 1; every sprint | DevOps |

---

# Mitigation Strategies

| Strategy | Example |
|----------|---------|
| **Avoid** | Use familiar stack |
| **Reduce** | Prototype risky parts early |
| **Transfer** | Use managed DB (no self-host) |
| **Accept** | "Might skip dark mode — that's OK" |

---

# The Pre-Mortem

> *Imagine it's Week 11. Your project failed. What went wrong?*

Each member writes 2–3 reasons independently.
Team builds the risk register from those answers.

Teams doing pre-mortems identify **~30% more risks**.

---

# 💬 Discussion

> Pre-mortem: It's Week 11. Your project is broken.

**What's the most likely reason? What could you do in Week 2 to prevent it?**

---

<!-- _class: lead -->

# Setting Up Your Workflow

---

# Repository Setup

**README.md** — Project name, team + roles, tech stack, setup instructions, board link

**.gitignore** — `node_modules/`, `.env`, `.DS_Store`, `dist/`, `*.log`

```
taskboard/
├── README.md
├── CONTRIBUTING.md
├── .gitignore
├── frontend/
│   ├── src/
│   └── package.json
├── backend/
│   ├── src/
│   ├── tests/
│   └── package.json
└── docs/
    └── api-spec.md
```

Set this up **now**. Not organically.

---

# Branching Strategy

```
main ────────────────────────────
  ├── feature/login ──── PR ──→ main
  ├── feature/task-crud ─ PR ──→ main
  └── feature/board-view (WIP)
```

1. **`main`** — always deployable, never commit directly
2. **Feature branches** — `feature/task-creation-form`, `fix/login-bug`, `chore/setup-eslint`
3. All changes via **Pull Request**
4. **1 reviewer** minimum before merge

---

# Working Agreements → CONTRIBUTING.md

```markdown
## Our Agreements
- Respond within 24 hours
- No direct pushes to main
- PRs need 1 approval
- Update task cards daily
- Ask for help if stuck 30+ minutes
- Commits: feat:, fix:, docs:
```

Written rules prevent 90% of conflict.

---

<!-- _class: lead -->

# Project Pitches

---

# Pitch Format

**Cover these five points:**

| | Example (TaskBoard) |
|-|---------------------|
| **Problem** | Teams lose track of tasks |
| **Users** | Dev teams of 3–8 |
| **Core Features** | Board, assignment, tracking (3–5 items) |
| **Tech Stack** | React + Node + PostgreSQL |
| **Unique Aspect** | AI task estimation |

Be specific. Show enthusiasm. Know your MVP cold. Acknowledge one risk.

---

# Giving Pitch Feedback

💚 **"I like..."** — a specific strength
💛 **"I wonder..."** — a question or concern
💙 **"What if..."** — a suggestion to consider

> "I like the small-team focus. I wonder about offline use.
> What if you added mobile views?"

Specific feedback > generic praise.

---

<!-- _class: lead -->

# Key Takeaways

---

# Seven Principles

1. **Organization > talent** — process prevents chaos
2. **One owner per task** — shared responsibility = none
3. **Sprint weekly** — plan, build, review, retro, repeat
4. **Scope ruthlessly** — MVP first, cut scope not quality
5. **Board = source of truth** — if it's not there, it doesn't exist
6. **Estimate with T-shirts** — XL means split it
7. **Plan for risks early** — pre-mortem in Week 2

---

# This Week's Deliverables

| Task | Owner |
|------|-------|
| Assign team roles | PM |
| Set up GitHub repo + README + .gitignore | Tech Lead |
| Create GitHub Projects board (5 columns) | PM |
| Write CONTRIBUTING.md | Team |
| Write 10+ user stories as Issues | Team |
| Create Definition of Done | QA Lead |
| Build risk register (5+ risks) | Team |
| Prepare 2-minute project pitch | Team |

---

# Next Week

### Week 3 — Version Control and Collaboration

Git workflows, merge conflicts, PR reviews, and GitHub Actions CI

