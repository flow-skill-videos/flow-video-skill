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
- Flow safety false-positive recovery
- hands-only rescue inserts
- U.S.-audience creative signaling
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

**0.4.0 — Safety recovery + U.S. targeting + kiwi workflow**

Version 0.4 adds the newest validated production lessons from the kiwi + baking-soda smoothie remodel and repeated Flow safety false-positive tests.

Major improvements include:

- additive `SKILL_PATCH_0_4.md`
- U.S.-audience semantic / visual signaling rules
- one authentic flag in wider scenes without forcing it into every insert
- stronger First Frame `locked photographic plate` logic
- instruction to avoid re-describing a correct environment during animation
- diagnosis of prompt-level vs asset-level Flow safety errors
- escalation from identity-light prompt → crop face → hands-only insert → fresh session
- off-camera voice support for object-focused microtakes
- stop-the-loop rule for repeated identical safety warnings
- validated kiwi → baking soda → lemon → water → blend sequence
- one-glass finished-drink payoff
- U.S.-targeted GUIDE CTA

## Start here

### 1. General reusable production rules
Read [`SKILL.md`](./SKILL.md).

### 2. New v0.4 patch
Read [`SKILL_PATCH_0_4.md`](./SKILL_PATCH_0_4.md) **immediately after `SKILL.md`**.

This patch contains the newest Flow safety recovery, asset-diagnosis, U.S.-targeting and kiwi-workflow rules.

### 3. Current Josh project handoff
Read [`PROJECT_PROFILE.md`](./PROJECT_PROFILE.md).

This file contains the current recurring-character, environment, voice, CTA, funnel, U.S.-audience and workflow settings needed to continue the active project in a new chat/profile.

### 4. Recent validated patterns
Read [`docs/RECENT_VALIDATED_PATTERNS.md`](./docs/RECENT_VALIDATED_PATTERNS.md).

This records practical lessons from hydrogen-peroxide, potato-water, baking-soda foot, five-food-tests, cheesecake, lung-demonstration, digestive-tea and kiwi-smoothie productions.

### 5. Change history
Read [`CHANGELOG.md`](./CHANGELOG.md).

## Repository structure

```text
flow-video-skill/
├── README.md
├── SKILL.md
├── SKILL_PATCH_0_4.md
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
│   ├── video-004-digestive-tea-remodel/
│   └── video-005-kiwi-baking-soda-remodel/
├── docs/
│   └── RECENT_VALIDATED_PATTERNS.md
└── ...
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

When Flow repeatedly returns the same safety warning after meaningful prompt simplification, switch from **prompt rewriting** to **asset strategy**:

1. reduce identity language
2. remove nonessential flag / national symbols from the insert
3. reduce / crop the face
4. use hands + object only
5. use off-camera voice if needed
6. start a fresh Flow project / clean insert if the classification persists

## Current validated project pattern

For the active outdoor natural-remedy project:

**Bizarre Hook → Recipe / Demonstration → Finished Payoff → Natural Explanation → GUIDE CTA**

U.S.-targeted CTA:

> If you're in the U.S. and want more natural recipes like this, comment GUIDE and I'll send you the full guide.

The guide itself is normally not shown physically in the generated footage.

## Quick load order for a Custom GPT / new chat

Use this read order:

1. `SKILL.md`
2. `SKILL_PATCH_0_4.md`
3. `PROJECT_PROFILE.md`
4. `docs/RECENT_VALIDATED_PATTERNS.md`
5. relevant example README for the current video style

If two rules conflict, the newer specific rule in `SKILL_PATCH_0_4.md` or `PROJECT_PROFILE.md` wins over an older generic rule.