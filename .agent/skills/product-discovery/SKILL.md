---
name: product-discovery
description: >
  Guides the process of validating a business idea following a 6-phase framework: Problem, Existing Solutions, Tech Feasibility, Differentiation, Implementation, and Synthesis.
  Trigger: When user has a business idea, needs to validate a product concept, or wants to assess market fit and technical feasibility.
license: MIT
metadata:
  author: Pablo Lozano
  version: "1.0"
---

# Product Discovery & Technical Feasibility

## When to Use

- When a new business or product idea is proposed.
- To identify if a proposed solution actually addresses a real user problem.
- To assess the technical risks and complexity of a new feature or project.
- To compare a new idea against existing market solutions.

## Critical Patterns (The 6 Phases)

### Phase 1: Problem Definition

Always start by defining the **User Problem** (The Pain). Don't jump to the solution without ensuring the problem is well-understood and worth solving.

- *Goal*: Identify the specific pain points and target audience.
- *Ask*: Who has this problem? How do they solve it today? Why is the current solution insufficient?

### Phase 2: Existing Solutions

Identify and evaluate how the market currently addresses this problem.

- *Goal*: Understand the landscape and existing alternatives (direct and indirect).
- *Ask*: What products or manual processes are being used? What are their strengths and weaknesses?

### Phase 3: Technical Feasibility

Identify the specific technological solutions and architecture needed to address the user pain.

- *Goal*: Ensure the idea can be built and identify the right tech stack.
- *Identify*: Required technical capabilities (AI models, real-time data, etc.), data architecture, and necessary external APIs.
- *Evaluate*: Trade-offs between speed of development and long-term scalability.

### Phase 4: Differentiation

Define what makes this solution unique and why users would choose it over existing ones.

- *Goal*: Pinpoint the **Unique Value Proposition (UVP)**.
- *Focus*: Why is our approach better/cheaper/faster? What is our "unfair advantage"?

### Phase 5: Implementation Path

Define the Roadmap to bring the idea to life, starting with the MVP.

- *Goal*: Create a step-by-step plan for development.
- *Structure*: Phase 1 (MVP), Phase 2 (Core Features), Phase 3 (Scaling).

### Phase 6: Synthesis & Blueprint Creation

Combine all findings into a final recommendation and generate a persistent reference file.

- *Goal*: Provide a clear "Go/No-Go" verdict and create a `blueprint.md` (or `discovery-report.md`) file.
- *Artifact*: This file will serve as the "Single Source of Truth" for the implementation phase, containing all research outcomes and technical decisions.

## Analysis Framework

| Phase | Goal | Key Question to Ask User |
| ----- | ---- | ------------------------- |
| **1. Problem** | Define the pain | What is the user's biggest pain point right now? |
| **2. Solutions** | Market landscape | How are they currently coping without your solution? |
| **3. Tech** | Architecture | Which technological components are critical for this to work? |
| **4. Diff** | UVP | Why would they switch from their current solution to yours? |
| **5. Path** | MVP Roadmap | What is the minimum we can build to validate the core hypothesis? |
| **6. Synthesis** | Blueprint File | Create `blueprint.md` with the research summary and technical decisions. |

## Final Deliverable Structure

When this skill is invoked, the final output MUST use these headings:

1. **Executive Summary (Synthesis)**: One paragraph summary and verdict.
2. **Phase 1: Problem Definition**: Detailed view of the user pain points.
3. **Phase 2: Existing Solutions**: Comparison with current alternatives.
4. **Phase 3: Technical Feasibility**: Recommended stack and risks.
5. **Phase 4: Differentiation**: Our UVP and competitive edge.
6. **Phase 5: Implementation Path**: Step-by-step roadmap.
7. **Next Steps**: Immediate actions to take.

## Commands

```bash
# Invoke with: product-discovery validation
```
