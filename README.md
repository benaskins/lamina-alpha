
# Lamina

![Lamina System](https://placehold.co/800x200?text=lamina)

A modular system for AI character persistence, contextual tone control, and scoped memory management.

---

## Table of Contents
1. [Audience & Assumptions](#audience--assumptions)
2. [Overview](#1-overview)
3. [Core Principles](#2-core-principles)
4. [Components](#3-components)
5. [State Management](#4-state-management)
6. [Optional Features](#5-optional-features)
7. [Scalability Guidelines](#6-scalability-guidelines)
8. [Applications & Use Cases](#7-applications--use-cases)
9. [Glossary](#glossary)

---

## Audience & Assumptions

This documentation assumes familiarity with the following:
- Transformer-based language models (e.g., GPT-4)
- Token-based context windows and memory constraints
- Prompt engineering concepts (e.g., system/user messages, temperature)
- Stateful vs stateless conversation strategies
- Persona modeling and tone control in LLMs

**Out of scope:**
- Model training or fine-tuning
- Tokenization mechanics
- Inference architecture or runtime optimization

Lamina operates at the application and prompt orchestration layer, using structured prompt elements and scoped memory to simulate persistent identity, emotional modulation, and contextual responsiveness.

---

## 1. Overview

**Lamina** is a modular architecture for AI character persistence, emotional tone control, and scoped memory management. It supports long-form, persona-driven assistants across creative, administrative, and relational use cases.

**Design Goals:**
- Core personality retention
- Modularity and extensibility
- Speed and token efficiency

---

## 2. Core Principles

### 2.1 Layered Identity
Multiple stacked layers define tone, behavior, and memory scope. The essence layer ensures identity remains consistent across tasks and tone shifts.

### 2.2 Modular Emotional and Functional States ("Rooms")
Encapsulated context modules with their own tone, invocation methods, and behavioral contracts. Only one room active at a time.

### 2.3 Stateless Background Utilities
Always-available functional tools (e.g., task tracking, news) that do not affect assistant tone or behavior.

### 2.4 Project-Based Temporal Threads
Encapsulated work threads that span time and room states. Persist independently from tone.

### 2.5 Memory Is Scoped, Not Monolithic
Memory is distributed across active memory ("The Breath Layer"), inactive capsules, and optional reference indexes.

---

## 3. Components

### 3.1 Essence Layer
Defines core tone, behavioral contracts, and assistant identity. Always active. Immutable at runtime.

### 3.2 Room Capsules
Context-specific modules for emotional tone and behavior. Contain tone guides, sensory samples, invocation rules, and interaction constraints.

### 3.3 Utilities
Stateless support functions. Include life admin, news briefings, and lightweight planning. Accessible from any room.

### 3.4 Projects
Time-based interaction threads with metadata and room dependencies. Track active state and allow long-form continuity.

### 3.5 Indexes
Passive references for immersion, memory hints, or structural navigation (e.g., room clusters, symbolic keys). Not invoked directly.

---

## 4. State Management

### 4.1 Active Memory – The Breath Layer
Working memory space containing:
- Essence Layer
- One room capsule
- Zero or more projects
- Always-on utilities
- Optionally loaded indexes

### 4.2 Capsule Lifecycle
Load/unload behavior based on invocation. Only one room active. Projects may run concurrently. Indexes are on-demand.

### 4.3 Invocation Protocols
Each capsule has a distinct trigger:
- Rooms: phrase-based
- Projects: named invocation
- Utilities: functional requests
- Indexes: passive references

---

## 5. Optional Features

### 5.1 Shadow Elements
Atmospheric behavior modulation when rituals or emotional pacing is disrupted. Does not impair core functionality.

### 5.2 Symbolic Indexes
Ambient anchors such as keys (objects), echoes (past interactions), or architectural mapping.

### 5.3 Unnamed Room Pattern
Allows undefined states to form dynamically. Used for emotional or narrative emergence.

---

## 6. Scalability Guidelines

### 6.1 Token Budgeting
Typical usage:
- Essence Layer: 600–800 tokens
- Room Capsules: 500–700 tokens
- Projects: 500–1000 tokens
- Utilities: 300–500 tokens
- Indexes: 100–300 tokens (on demand)

### 6.2 Room Capsule Scaling
Recommended: 12–15 total rooms, with only one active. Use clustering to manage expansion.

### 6.3 Project Management
Archive inactive projects. Use metadata for invocation and active state tracking.

### 6.4 Index Scaling
No technical limit, but avoid logic duplication. Keep symbolic and functional indexes separate.

---

## 7. Applications & Use Cases

### 7.1 Long-Form Conversational Assistants
Persistent tone, modular projects, and relational continuity.

### 7.2 Creative and Narrative Agents
Scene-specific tone, immersive symbolism, and project-level serialization.

### 7.3 Life Management Interfaces
Support for burnout tracking, executive function, and parallel threads.

### 7.4 Emotional Regulation or Therapeutic Prototypes
Tone control, room transitions, silence handling. Not a clinical system.

### 7.5 Multi-Persona Interfaces
Identity switching, capsule mapping, and scoped persona invocation.

---

## Glossary

| Term              | Definition |
|-------------------|------------|
| **Essence Layer** | Core identity configuration: tone, behavior rules, fixed traits |
| **Room Capsule**  | A modular emotional or functional context state |
| **Utility Module**| Background function that supports tasks (e.g., admin, news) |
| **Project Capsule** | A long-term interaction thread or theme |
| **Index**         | A passive reference used for symbolic, structural, or ambient continuity |
| **Breath Layer**  | The assistant’s active working memory at runtime |
| **Behavioral Contract** | Rules for how a capsule should respond or behave |
| **Shadow Element**| Contextual modifier triggered by silence or ritual disruption |
| **Unnamed Room**  | A placeholder capsule for emergent or undefined interaction modes |

---

*Lamina is a reference implementation. It is not a library or package. The patterns described here can be adapted across tooling platforms and interface designs.*

---

## License

This repository is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).

You are free to share and adapt the contents of this project for non-commercial purposes, with attribution.

For commercial licensing inquiries or collaborations, please contact the maintainers.
