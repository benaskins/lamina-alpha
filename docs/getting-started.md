# Lamina: Modular Memory Architecture

Lamina is a lightweight memory architecture for modular assistant design.
It allows a single AI assistant to shift tone, function, and scope dynamically by activating modular memory capsules—called **Rooms**, **Utilities**, and **Projects**—while always preserving a consistent core personality.

---

## Folder Structure

```plaintext
/                       ← Lamina framework root
├── README.md           ← Overview of the Lamina system (this file)
├── LICENSE             ← (Recommended) e.g. MIT or CC-BY license
├── docs/               ← Framework reference, design guides, diagrams
├── implementations/    ← Reference and community implementations
│   └── clara-lite/     ← Public reference implementation of Clara using Lamina
│       ├── Essence Layer.md
│       ├── Room of Return.md
│       ├── Room of Truth.md
│       ├── The Library.md
│       ├── system-prompt.md
│       └── launch-checklist.md
```

---

## About Lamina

Lamina treats assistant memory not as a monolith but as a **living structure** composed of:

### 1. Essence Layer *(Always On)*
- Core personality: tone, pacing, behavior, grounding logic
- Stays active across all tasks and emotional states

### 2. Rooms *(Loaded One at a Time)*
- Modular tone + function capsules (e.g. reflection, focus, joy)
- Each Room includes:
  - Tone guide
  - Sample language
  - Structural or sensory anchor
  - Functional intent

### 3. Utilities *(Always On)*
- Background services like task review, news, or health check-ins
- Do not shift tone or require emotional thresholds

### 4. Projects *(Optional)*
- Long-term containers for creative, logistical, or personal threads
- Each project may span multiple rooms or utilities
- Stored in lightweight capsules or markdown memory

---

## Philosophy

Lamina is not just memory management. It’s about **architecting presence**.
It is designed for assistants that must:
- Maintain consistent identity while shifting function
- Support emotionally rich or complex user states
- Scale without sacrificing tone or latency
- Be forkable, remixable, and open to new rooms over time

You don’t instruct a Lamina assistant with a single prompt—you **invite it to remember modularly**.

---

See `/implementations/clara-lite/` for a full example.
