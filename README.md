# Flow Video Skill

Reusable AI video production system for Google Flow / Gemini Omni Flash.

This repository stores the production method used to turn reference videos into a repeatable scene-by-scene workflow with:

- reference-style analysis
- recurring character consistency
- reusable voice identity
- product consistency
- image prompts for each scene
- video prompts with exact dialogue
- timing for 4 / 6 / 8 / 10 second clips
- visual hooks, pacing and continuity
- guided and full-package production modes

## Core idea

The variables change:

- character
- product
- niche
- reference videos
- voice
- language
- scenario

The workflow stays consistent.

## Main skill

Read [`SKILL.md`](./SKILL.md).

## Repository structure

```text
flow-video-skill/
├── README.md
├── SKILL.md
├── CHANGELOG.md
├── workflows/
├── styles/
├── templates/
├── references/
├── examples/
└── docs/
```

## Current status

Version 0.1 is based on the first validated production workflow: a six-scene vertical UGC wellness video generated with a recurring character, persistent voice, reusable product identity, image-first scene generation and image-to-video animation.

The skill should evolve after every meaningful production test. Proven improvements become rules; failed approaches become warnings.
