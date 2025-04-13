---
weight: 200
title: "Our Architectural Process"
description: ""
icon: "article"
date: "2025-04-12T11:38:27-06:00"
lastmod: "2025-04-12T11:38:27-06:00"
draft: true
toc: true
---

## Our Architecture Process (The Real-World Version)

Welcome to the way we do software architecture: grounded in reality, driven by business needs, and shaped by our domain. This isn’t ivory-tower modeling—it’s a working process that grows alongside the system and the team.

---

### 1. Understand the Drivers (Before Writing Diagrams)

**What we’re doing here:** We figure out what really matters before diving into tech. That means:

- What do users want?
- What makes the business tick?
- What can’t we break (regulations, data models, expectations)?

**How we do it:**

- Run **event-storming** and **domain storytelling** sessions with stakeholders.
- Use **Wardley Maps** to understand where change is coming from.
- Capture not just the requirements but also change axes and trade-offs.

**Artifacts:**

- Raw sticky notes (or Miro boards)
- Context map sketches
- Notes on risks and constraints

---

### 2. Sketch the System (Just Enough)

**What we’re doing here:** Define the backbone of the system—don’t over-engineer.

**How we do it:**

- Use **bounded contexts** to find natural seams.
- Model the system using the **C4 model** (plus connectors—let’s call it C5).
- Write **Architectural Decision Records (ADRs)** for the big choices.

**Artifacts:**

- Context/container/component diagrams (PlantUML or diagrams.net)
- C5 models for inter-service comms
- Initial repo + deployment layout

---

### 3. Test the Ideas (Before They Break)

**What we’re doing here:** Make sure this thing will work *before* it gets expensive to fix.

**How we do it:**

- Define **fitness functions** for the qualities we care about (performance, modifiability, etc.).
- Walk through a few "worst-case" scenarios.

**Artifacts:**

- Fitness function definitions (e.g. latency budget, retry logic, API contracts)
- List of architectural risks and how we’re addressing them

---

### 4. Communicate It (So Everyone Gets It)

**What we’re doing here:** Make sure devs, ops, and leadership are aligned.

**How we do it:**

- Share C4/C5 visuals
- Publish documentation that matches our domain (use the same language)
- Put it all in a wiki—update it often

**Artifacts:**

- ADRs
- Architecture as code (PlantUML, markdown, etc.)
- System overview slides (for onboarding)

---

### 5. Build It (Without Losing the Plot)

**What we’re doing here:** Start coding, but stay aligned with the architecture.

**How we do it:**

- Define workflows (BPMN or similar) for Temporal or service orchestration
- Use **Tactical DDD** to keep code clean
- Integrate fitness checks into CI/CD

**Artifacts:**

- Working service skeletons
- CI pipelines with architecture checks
- Code that reflects our bounded contexts

---

### 6. Change it (Without Wrecking It)

**What we’re doing here:** Embrace change, but don’t let entropy creep in.

**How we do it:**

- Re-run event-storming when things shift
- Keep fitness functions up to date
- Monitor drift and run architectural reviews periodically

**Artifacts:**

- Updated domain models and diagrams
- New or revised ADRs
- Notes from architecture syncs

---

### Tools & Practices We Actually Use

- **Event Storming**: Start here. Always.
- **Domain Storytelling**: Use when people prefer talking in use cases.
- **C4 + C5 Diagrams**: For everything from context to deployment views.
- **Fitness Functions**: Validate what matters (latency, availability, coupling, etc.)
- **PlantUML & diagrams.net**: Architecture as code (or near enough).
- **ADR templates**: Track the decisions, trade-offs, and when we change our minds.
- **Wardley Maps**: To align architecture with business shifts.

---

### References That Shaped This

- *Fundamentals of Software Architecture* — Mark Richards, Neal Ford  
- *Building Evolutionary Architectures* — Ford, Parsons, Kua, Sadalage  
- *Software Architecture for Developers* — Simon Brown  
- *EventStorming* — Alberto Brandolini  
- *DDD by Example* — Michael Plöd  
- *Architecture Modernization* — Nick Tune  
- *Software Architecture Visual Notes* — Cesare Pautasso  

---

This document evolves like our architecture. If it’s out of date, that’s a bug; file an issue or drop it in Slack. We build things that change, and our process reflects that.

