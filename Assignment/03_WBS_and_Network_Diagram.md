# Assignment 3: WBS Decomposition, Network Diagramming & Critical Path Analysis

## Assignment Overview & Objectives

In Assignment 1, your team established the organizational authority and macro boundaries for your IT project via the Project Charter. In Assignment 2, you established the initial baseline by defining the Project Scope Statement, drafting a high-level Work Breakdown Structure (WBS) (Levels 1–3), and building a Stakeholder Register.

In Assignment 3, your team will transition from scope definition to schedule network logic. You will expand your WBS into detailed work packages and activity-level tasks. Using these tasks, you will model the project’s execution path by building a Project Schedule Network Diagram, identifying all path durations, and calculating the Critical Path.

This deliverable must be completed by configuring, prompting, and iterating with your team's Custom Copilot Agent (or custom LLM equivalent). Your agent must be updated to process your prior deliverables (Charter and Scope Statement) as its knowledge base.

---

## Phase 1: Configure & Ground Your Copilot Agent

Your team must create a Microsoft Copilot Custom Agent (or platform equivalent: Gemini Gem, ChatGPT Custom GPT, or Claude Project).

### Agent Configuration Updates

1. **Updated Persona & Role:** Configure your agent to act as an *Expert IT Project Systems Architect & PMP-Certified Schedule Analyst*.
2. **Knowledge Base / Grounding:** Attach your team's Assignment 1 Project Charter and Assignment 2 Scope Statement & WBS. Ensure the agent checks every new activity against the scope baseline to prevent scope creep.
3. **Execution Instructions - WBS Expansion:** Require the agent to break down WBS Level 3 elements into Level 4 Work Packages and discrete activity tasks.
4. **Execution Instructions - Scheduling Logic:** Instruct the agent to assign realistic duration estimates (in days) and define task dependencies (predecessors) using standard Precedence Diagramming Method (PDM) relationships.
5. **Execution Instructions - Critical Path:** Direct the agent to evaluate all network paths and calculate total float/slack to isolate the Critical Path.

---

## Phase 2: Required Deliverable Sections

Your final PDF submission must contain the following sections, formatted strictly to professional publishing standards:

### 1. Multi-Level Work Breakdown Structure (Expanded to Level 4)

* **Graphical or Structured Tree Decomposition:** Expand your Level 1–3 WBS from Assignment 2 down to Level 4 (discrete work packages and executable tasks).
* **Hierarchical WBS Coding:** Apply standard numbering (e.g., 1.0 → 1.2 → 1.2.3 → 1.2.3.1).
* **Task Dictionary Attributes:** For every Level 4 work package/task, include Work Package / Activity Title, Estimated Effort / Duration (in business days), and Assigned Primary Role / Ownership.

---

### 2. Activity Dependency & Predecessor Table

Before constructing the network diagram, present a structured table defining the logical sequencing between activities:

| Activity ID | Task / Work Package Name | WBS Ref | Duration (Days) | Predecessor ID(s) | Dependency Type | Dependency Rationale |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| A | API Gateway Config | 1.2.1.1 | 5 | None | — | Initial task |
| B | Database Schema Build | 1.3.1.2 | 8 | A | FS | DB cannot build until API endpoints are set |

*\*Note: Ensure dependencies reflect valid hard (mandatory) or soft (discretionary) logic.*

---

### 3. Project Schedule Network Diagram

* **Diagram Format:** Render a clear Precedence Diagramming Method (PDM / Activity-on-Node) schematic diagram showing node boxes connected by directional arrows.
* **Node Content:** Each node box must explicitly display:
  * Activity ID & Title
  * Duration (D)
  * Early Start (ES) & Early Finish (EF)
  * Late Start (LS) & Late Finish (LF)
  * Total Float / Slack ($\text{Slack} = \text{LS} - \text{ES} \text{ or } \text{LF} - \text{EF}$)
* **Visual Formatting:** The diagram must be clean and legible. No overlapping arrows or fragmented node boxes across page breaks.

---

### 4. Network Path & Critical Path Analysis

List every unique path through the network diagram from Start to Finish, summarizing the total duration for each path:

| Path ID | Sequence of Activity IDs | Calculation (Sum of Durations) | Total Duration (Days) | Path Status |
| :--- | :--- | :--- | :--- | :--- |
| Path 1 | A → B → E → H | 5 + 8 + 12 + 4 | 29 Days | Non-Critical |
| Path 2 | A → C → F → H | 5 + 14 + 10 + 4 | 33 Days | CRITICAL PATH |

* **Critical Path Identification:** Explicitly state which path is the Critical Path (the longest duration path through the network with zero total float).
* **Impact Analysis:** Explain what happens to the overall project completion date if any task on the critical path slips by even one day.

---

### 5. Copilot Agent Configuration & Reflection Report

* **System Prompt & Configuration:** Provide the system prompt, instructions, and file grounding configuration used in your Copilot Agent.
* **Prompt Iteration Log:** Include examples of at least two prompt refinements where your team corrected or guided the agent (e.g., correcting invalid task dependencies, adjusting duration logic, or fixing a network path error).

> **Reflection Questions to be included at the end of your submission:**
> 1. How effective was the AI Agent at logic-checking dependencies and identifying the critical path compared to manual calculation?
> 2. What risks arise if a project manager relies entirely on an LLM for schedule sequencing without validating PDM network logic?

---

## 🎨 Professional Formatting Requirements

To enforce corporate PMO publication standards, submissions failing to adhere to layout rules will incur point deductions:

1. **Document Flow & Page Breaks:** No orphan headers, split tables, or node diagrams split awkwardly across page breaks.
2. **Visual Consistency:** Maintain uniform typography, table styles, and color palettes matching your prior assignment submissions.
3. **Diagram Legibility:** Network diagrams and WBS tree diagrams must be high-resolution and fully readable when viewed on screen or printed to PDF.

---

## Final Submission Deliverables

Submit via Canvas by the posted deadline:

1. **Assignment 3 Master PDF Document:** Containing the Expanded WBS (Level 4), Dependency Table, PDM Network Diagram, Critical Path Analysis Table, and Reflection Report.
2. **Agent Configuration Screenshot / Link:** Verification showing your Copilot Agent setup and knowledge file attachments.

---

## Evaluation Rubric

| Criterion | Weight | Exemplary Performance (100%) |
| :--- | :---: | :--- |
| **WBS Decomposition (Level 4)** | 20% | Comprehensive breakdown to Level 4; clear WBS coding, effort estimates, and role assignments fully consistent with Assignment 2 scope. |
| **Dependency Logic & Table** | 20% | Logical activity sequencing using valid PDM relationships (FS, SS, FF, SF); technical rationale provided for every dependency. |
| **Network Diagram (PDM)** | 20% | High-quality AON/PDM schematic; nodes display ES, EF, LS, LF, Duration, and Float accurately without visual clutter or broken rendering. |
| **Critical Path Analysis** | 20% | All paths correctly identified and summed; Critical Path accurately designated with zero total float explained thoroughly. |
| **Agent Engineering & Reflection** | 15% | Clear evidence of agent grounding, prompt iteration log, and deep critical evaluation of AI capabilities and risks in project scheduling. |
| **Professional Formatting** | 5% | Flawless document styling, clean layout, no split headers/tables, and consistent visual branding throughout. |

