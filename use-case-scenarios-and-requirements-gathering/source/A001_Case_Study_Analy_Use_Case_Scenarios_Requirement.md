# Use Case Scenarios & Requirements Specification
## Semester Group Project — Assignment 2 of the Series

---

> **Module:** Use Case Scenarios
> **Assignment Type:** Semester Group Project (Series Assignment)
> **Estimated Student Effort:** 2–4 hours of coordinated group work
> **AI Use Policy:** Generative AI tools are permitted on this assignment. If you use AI assistance, document how it was used in your submission (e.g., "We used AI to draft initial step sequences, which we then reviewed and revised against our stakeholder notes"). AI-generated content must be reviewed, verified, and owned by your team.

---

## Learning Outcomes

By the end of this assignment, you will be able to:

1. **Identify** all relevant stakeholders and user roles for your software project, distinguishing between direct users and broader stakeholders.
2. **Construct** complete, well-structured Use Case Scenarios for every action your software supports, including main success scenarios, alternative flows, exception flows, preconditions, and postconditions.
3. **Produce** a Hierarchical Task Analysis (HTA) for each core and unique action in your software, mapping user tasks to the steps documented in your use cases.
4. **Evaluate** your use case set for completeness by verifying that every identified actor and stakeholder goal is traceable to at least one documented scenario.

---

## TILT Framework

### Purpose — Why This Assignment Matters

In real software development, teams that skip structured requirements gathering build systems that miss what users actually need. This assignment puts you in the role of a requirements analyst responsible for capturing *exactly* what your software must do — from every relevant user's perspective — before any design or coding begins.

The documents you create here will be the authoritative reference for your team for the rest of the semester. Every interface design decision, every feature built, and every test written will trace back to the use cases and task analyses you produce now. Getting this right saves your team significant rework later and reflects genuine industry practice in software engineering.

This assignment directly builds on the project context, stakeholder identification, and initial problem framing established in your previous assignment.

### Task — What You Are Doing

You are producing a **Requirements Specification Package** for your semester software project. This package contains:

- A complete **Stakeholder & Actor Registry**
- A complete set of **Use Case Scenarios** covering every action your software supports
- A **Hierarchical Task Analysis (HTA)** for each core and unique action
- A **Coverage Matrix** confirming completeness

Full step-by-step instructions are provided in the [Task Description](#task-description) section below.

### Criteria — How You Will Be Graded

See the [Grading Rubric](#grading-rubric) section at the end of this document.

---

## Background & Context

This assignment is **Part 2** of your semester-long group project series. In your previous assignment, you defined your software project concept and identified the problem your system will solve. You should have that work available as a reference.

In this assignment, you are moving from *what problem we are solving* to *how every type of user will interact with the system*. You will document every action the software supports — not just the interesting or unique ones — and you will do so using the structured Use Case Scenario format and Task Analysis methods covered in this module.

**Key terms used throughout this assignment:**

| Term | Definition |
|---|---|
| **Stakeholder** | Any individual, group, or organization with an interest in or affected by the software system — not limited to direct users |
| **Actor** | A role that interacts directly with the system interface; represented in use cases as a named role, not a specific person |
| **Use Case Scenario** | A narrative description of how an actor interacts with the system to achieve a specific goal, including all possible paths |
| **Main Success Scenario** | The ideal interaction path where everything goes as expected and the actor achieves their goal |
| **Alternative Flow** | A valid variation from the main path that still results in a defined outcome |
| **Exception Flow** | What happens when an error, invalid input, or system failure interrupts the interaction |
| **Precondition** | The state the system and actor must be in *before* the use case begins |
| **Postcondition** | The guaranteed state of the system *after* the scenario completes |
| **HTA (Hierarchical Task Analysis)** | A structured breakdown of a user goal into sub-tasks and individual actions, arranged as a hierarchy |
| **Edge Case** | A valid but infrequent scenario occurring at the boundary of normal operating conditions |
| **Coverage Matrix** | A table mapping actors to use cases to verify that no actor or goal is left without a scenario |

---

## Task Description

Work through the following steps in order. Each step builds on the previous one.

---

### Step 1 — Audit and Finalize Your Action Inventory

Before writing use cases, you need a complete list of every action a user can perform in your system.

**What to do:**

1. As a group, brainstorm every action your software will support. Think about every screen, every button, every workflow.
2. Organize actions into two categories:
   - **Standard/Common Actions:** Actions that virtually every application includes (e.g., log in, log out, register an account, reset a password, update profile). These behaviors are widely understood.
   - **Core/Unique Actions:** Actions that are specific to your application's purpose — the things that make your software distinct.
3. Write a numbered master list of all actions separated into these two categories. This list will drive everything else in this assignment.

> **Tip:** Think about your software from multiple users' perspectives. An action available to an administrator is still an action that needs to be documented, even if a regular user never sees it.

---

### Step 2 — Build Your Stakeholder & Actor Registry

**What to do:**

1. List every **stakeholder** — everyone who has an interest in your software, including those who will never touch the interface (e.g., a business owner, a compliance officer, a third-party integration partner).
2. For each stakeholder, write one or two sentences describing their **primary interest or concern** regarding the system.
3. From your stakeholder list, identify every **actor** — the roles that will directly interact with the system interface.
4. For each actor, document:
   - **Role name** (e.g., "Registered User," "Administrator," "Guest")
   - **Brief description** of who fills this role
   - **Permissions/capabilities** — a short summary of what this role can and cannot do
   - **Which actions from your Step 1 inventory this actor can perform**

Format this as a registry (a structured list or table).

---

### Step 3 — Write Use Case Scenarios for Standard/Common Actions

For **standard/common actions** (e.g., login, logout, registration, password reset), your team does **not** need to write out the full standard interaction in detail. Instead, for each standard action:

**What to do:**

1. Write the **title** and identify the **actor(s)**.
2. Document only what is **distinct or different** about how this action works in your specific application compared to a typical application. Focus on:
   - Any **unique preconditions** specific to your system
   - Any **non-standard steps** or requirements in your version of this flow
   - Any **constraints or rules** particular to your system (e.g., password complexity rules unique to your context, multi-factor authentication requirements, account approval workflows)
   - Any **edge cases or exceptions** specific to your application
3. If a standard action is completely typical with no distinctions, you may note it as "Standard implementation — no unique requirements" and move on.

> **Example:** If your application requires admin approval before a new account is activated, that approval step is a distinct requirement and must be documented.

---

### Step 4 — Write Full Use Case Scenarios for Core/Unique Actions

For every **core or unique action** in your inventory, write a complete Use Case Scenario using the template below. Every field is required.

**Use the following template for each use case:**

---

**USE CASE: [UC-###]**

| Field | Content |
|---|---|
| **Title** | A short, active-verb phrase describing the goal (e.g., "Submit Project Proposal") |
| **Actor(s)** | List all roles involved |
| **Priority** | High / Medium / Low |
| **Frequency** | Estimated how often this occurs (e.g., daily, occasionally, rarely) |
| **Preconditions** | What must be true before this use case begins |
| **Trigger** | What event or action initiates this use case |

**Main Success Scenario:**
Write a numbered sequence of steps. Each step is either an *actor action* or a *system response*. Steps should alternate. Do not describe technical implementation — describe *what* happens, not *how* the system achieves it internally.

```
1. Actor does X.
2. System responds with Y.
3. Actor does Z.
4. System confirms W.
...
```

**Alternative Flows:**
For each valid variation from the main path, document:
- *At step [#]:* Description of the variation and what happens instead.

**Exception Flows:**
For each error, invalid input, or failure condition, document:
- *Trigger:* What causes this exception.
- *System Response:* What the system does.
- *Recovery:* How the user can continue (if applicable).

**Postconditions:**
- *Main flow:* State of the system after successful completion.
- *Alternative flows:* Any differing end states for alternatives.

**Edge Cases to Consider:**
List any boundary or infrequent but valid scenarios the team identified for this use case.

---

**Writing quality expectations for use case steps:**
- Use specific, concrete verbs — not vague words like "handles," "processes," or "manages."
- Name the actor explicitly in each step (e.g., "The Registered User selects…" not "The user does…").
- Each step should describe one action or one system response — do not combine multiple actions into one step.
- Steps must be understandable to both a developer and a non-technical stakeholder.

---

### Step 5 — Perform Hierarchical Task Analysis (HTA) for Core/Unique Actions

For each **core or unique action**, produce a Hierarchical Task Analysis alongside its use case. Standard/common actions do not require an HTA unless your team identified something non-standard about them.

**What to do:**

1. State the **top-level goal** of the task (this should match the use case title).
2. Break that goal into **sub-tasks** — the major phases of the task.
3. Break each sub-task into **individual actions** — the specific steps the user takes.
4. For each sub-task level, write a **plan** — a note describing the order and any conditions under which sub-tasks are performed (e.g., "Do 1, then 2. If error occurs, do 3 before continuing.").
5. Note any **decision points** where the user must choose between paths.

**HTA can be represented as an indented outline or a table — your choice:**

*Indented outline format example:*
```
0. Goal: [Top-Level Goal Name]
   Plan 0: Do 1, then 2, then 3.
   1. Sub-task 1
      Plan 1: Do 1.1 then 1.2.
      1.1 Individual action
      1.2 Individual action
   2. Sub-task 2
      Plan 2: Do 2.1. If condition, do 2.2.
      2.1 Individual action
      2.2 Individual action (conditional)
   3. Sub-task 3
      ...
```

**After each HTA**, write 2–3 sentences explaining how the HTA output informed your use case — specifically how the sub-task steps map to steps in the main success scenario and where decision points became alternative or exception flows.

---

### Step 6 — Build the Coverage Matrix

Create a table that maps every actor to every use case to confirm that:
- Every actor appears in at least one use case.
- Every use case has at least one actor assigned.
- Every stakeholder goal identified in your Stakeholder & Actor Registry is traceable to at least one use case.

**Format:**

| Use Case | Actor 1 | Actor 2 | Actor 3 | Actor N |
|---|---|---|---|---|
| UC-001: [Title] | ✓ | | ✓ | |
| UC-002: [Title] | | ✓ | | ✓ |
| ... | | | | |

Below the matrix, add a short **Coverage Confirmation** paragraph (3–5 sentences) stating:
- Whether all actors are covered
- Whether any stakeholder goals remain without a use case (and if so, explain why)
- Any gaps your team identified and how you resolved them

---

### Step 7 — Group Reflection

As a group, write a short reflection (approximately one paragraph per question, 3–5 sentences each) responding to the following:

1. Which requirements elicitation technique(s) did your team use to identify user actions and stakeholder needs for this assignment (e.g., group discussion, document review, interviewing potential users, etc.)? How effective were they?
2. Describe one edge case or exception flow your team almost missed. How did you discover it, and why does it matter?
3. How did performing task analysis change or improve the use cases you wrote? Give a specific example.

---

## Parameters & Constraints

- **Scope:** All actions your software supports must be accounted for — no action should be undocumented.
- **Use Case Numbering:** Number use cases sequentially using the format UC-001, UC-002, etc.
- **Writing Style:** Plain language. Write for an audience that includes both technical developers and non-technical stakeholders.
- **Step Granularity:** Each numbered step in a use case should represent one action or one system response — no compound steps.
- **HTA Depth:** HTA outlines must have at least two levels of decomposition (sub-task → individual action) for each core use case.
- **Coverage Matrix:** Must include every actor and every use case — no omissions.
- **Reflection:** Responses must be specific to your project — generic or hypothetical answers will not receive credit.
- **Citations:** No formal citation style is required for this assignment. If you reference external sources or frameworks, note them informally.
- **File Format:** Submit in the format specified by your instructor or your learning management system.

---

## Accessibility Notes

- If your team uses tables in your submission, ensure they are formatted so that each column has a clear header row.
- If you use diagrams for your HTA, provide a text-based outline equivalent in the same document.
- All abbreviations should be spelled out on first use (e.g., Hierarchical Task Analysis (HTA)).
- Write use case steps as complete sentences — avoid shorthand or notation-only formats that may be unclear to all readers.

---

---

# ✅ SUBMISSION CHECKLIST & REQUIRED DELIVERABLES

*The items below are what your team must submit. Review this checklist before submitting.*

---

> ### 📋 Required Submission Item 1: Action Inventory
> A complete numbered list of all actions your software supports, organized into:
> - Standard/Common Actions
> - Core/Unique Actions

---

> ### 📋 Required Submission Item 2: Stakeholder & Actor Registry
> A structured registry including:
> - All stakeholders with their interest/concern described
> - All actors with role name, description, permissions summary, and list of actions they can perform

---

> ### 📋 Required Submission Item 3: Use Case Scenarios — Standard/Common Actions
> For each standard/common action:
> - Title and actor(s)
> - Documentation of any distinctions, unique requirements, or constraints specific to your application
> - "Standard implementation — no unique requirements" notation where applicable

---

> ### 📋 Required Submission Item 4: Use Case Scenarios — Core/Unique Actions
> For each core/unique action, a **complete Use Case Scenario** including:
> - UC number, title, actor(s), priority, frequency
> - Preconditions and trigger
> - Numbered main success scenario
> - Alternative flows
> - Exception flows
> - Postconditions
> - Edge cases

---

> ### 📋 Required Submission Item 5: Hierarchical Task Analysis (HTA)
> For each core/unique action:
> - Full HTA in outline or table format (minimum two levels of decomposition)
> - Plan statements at each sub-task level
> - A 2–3 sentence explanation of how the HTA informed the use case

---

> ### 📋 Required Submission Item 6: Coverage Matrix
> - Table mapping all actors to all use cases
> - Coverage Confirmation paragraph (3–5 sentences)

---

> ### 📋 Required Submission Item 7: Group Reflection
> Three reflection responses, one paragraph each (3–5 sentences per question), addressing