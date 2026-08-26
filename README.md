# Flow Video Skill

Reusable AI-video production system for Google Flow / Gemini / Veo-style workflows.

This repository stores the production method used to turn reference videos into repeatable scene-by-scene UGC workflows with:

- frame-by-frame reference analysis
- close reference remodelling
- recurring character consistency
- reusable voice identity
- exact environment continuity
- still-image-first scene generation
- image-to-video animation
- 4 / 6 / 8 / 10 second scene planning
- exact dialogue inside every animation prompt
- bizarre visual hooks
- object-count constraints
- physical-action continuity
- scene-lock / First Frame locking
- micro-action decomposition
- CTA adaptation
- guided and full-package production modes

## Core idea

The variables can change:

- character
- product
- niche
- reference videos
- voice
- language
- environment
- CTA destination

The workflow stays consistent.

## Current version

**0.3.0 — Exact-remodel + scene-lock + micro-action workflow**

Version 0.3 incorporates the latest validated production lessons from multiple outdoor wellness / natural-remedy reference remodels.

Major improvements include:

- `same hook / same copy / same recipe` remodel mode
- exact First Frame scene locking
- no-cut continuous physical-action prompts
- fixed-object vs moving-object rules
- ingredient-by-ingredient micro-actions
- anti-floating-prop constraints
- transformation timing such as `CONTACT = IMMEDIATE CHANGE`
- ground-level crouched bizarre hooks
- natural camera-distance outdoor voice
- GUIDE-based CTA replacement

## Start here

### General reusable production rules
Read [`SKILL.md`](./SKILL.md).

### Current Josh project handoff
Read [`PROJECT_PROFILE.md`](./PROJECT_PROFILE.md).

This file contains the current recurring-character, environment, voice, CTA, funnel and workflow settings needed to continue the active project in a new chat/profile.

### Change history
Read [`CHANGELOG.md`](./CHANGELOG.md).

## Repository structure

```text
flow-video-skill/
├── README.md
├── SKILL.md
├── PROJECT_PROFILE.md
├── CHANGELOG.md
├── workflows/
├── styles/
├── templates/
├── references/
├── examples/
│   ├── video-001-morning-greens/
│   ├── video-002-pep-tonic-bizarre-hook/
│   ├── video-003-cheesecake-remodel/
│   └── video-004-digestive-tea-remodel/
└── docs/
```

## Production philosophy

For fragile generative-video tasks, physical simplicity wins.

Prefer:

1. analyze the reference closely
2. establish the exact first frame
3. animate one clear physical action
4. lock stationary objects
5. preserve the same scene
6. confirm the result
7. move to the next step

A complex 10-second prompt containing many independent object transfers is usually less reliable than several simple 4–6 second clips.

## Current validated project pattern

For the active outdoor natural-remedy project:

**Bizarre Hook → Recipe / Demonstration → Finished Payoff → Natural Explanation → GUIDE CTA**

Typical CTA:

> If you want more natural remedies like this, comment GUIDE and I’ll send you the full guide.

The guide itself is normally not shown physically in the generated footage.
