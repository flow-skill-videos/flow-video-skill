# Flow Video Skill — Update Process

This document defines how to evolve the production system without losing stable behavior.

## Source of truth

The GitHub repository is the canonical source of truth.

The custom GPT Knowledge file is a deployed snapshot of the repository knowledge at a given point in time.

Do not treat the Knowledge upload as the master copy.

## Update categories

### 1. Prompt tweak
Use for a local improvement that affects one generation or one scene.
Examples:
- stronger negative constraint
- shorter dialogue
- more specific hand action

Action:
- test first
- only promote to the skill if it repeatedly improves output

### 2. Reusable rule
Use when a finding generalizes across productions.
Examples:
- preserve production language from references instead of chat language
- always embed full dialogue in video prompts
- use previous still as environment continuity reference

Action:
- update SKILL.md or the relevant workflow/template
- add a CHANGELOG entry
- include in next Knowledge snapshot

### 3. Style-specific rule
Use when the lesson belongs to one visual style rather than all videos.

Action:
- add/update a style profile under styles/
- avoid polluting global rules

### 4. Example-specific lesson
Use for a lesson learned from one finished production.

Action:
- document under examples/<video-id>/
- promote to a global rule only if validated more broadly

## Validation loop

For each meaningful test, collect:

WORKED:
- what clearly improved output

FAILED:
- what broke or underperformed

KEEP:
- what should remain unchanged

CHANGE:
- what should be modified next

NEW RULE:
- any reusable production rule discovered

## Versioning

Use semantic-style internal versions for the skill snapshots:

- v1.0 = first stable usable system
- v1.1 = backwards-compatible improvement
- v1.2 = another compatible improvement
- v2.0 = major workflow change

Do not create a new major version for small prompt tuning.

## Safe deployment workflow

1. Test a change in a real production.
2. Decide whether it is local, reusable, style-specific or example-specific.
3. Update GitHub.
4. Update CHANGELOG.md for meaningful reusable changes.
5. Build a new consolidated Knowledge snapshot file.
6. Open the custom GPT editor.
7. Replace the old Knowledge snapshot with the new one.
8. Keep the compact core behavior rules in Instructions.
9. Test in Preview with at least:
   - new project entry
   - reference-analysis flow
   - character step
   - voice/language routing
   - one image prompt
   - one video prompt with embedded dialogue
10. Select Update to deploy the draft changes to the live GPT.
11. Start a new chat for validation when testing new instructions/knowledge.

## Important language rule

Never infer production language from chat language alone.

Priority:
1. explicit user request
2. reference-video spoken language
3. ask one clarification if mixed/unclear

Keep separate:
- chat language
- production language
- voice accent

## Knowledge snapshot rule

The Knowledge file should contain:
- stable skill rules
- workflows
- prompt templates
- style-analysis framework
- validated examples
- version notes

Avoid loading every experimental note into Knowledge.
Keep experiments in GitHub until validated.

## Sharing

The public/share link points to the currently deployed GPT configuration.
When the GPT is edited, changes remain in draft until Update is selected.

After major updates, run a new-chat smoke test before treating the release as stable.

## Recommended release checklist

Before deploying a new version:
- instructions under limit
- no contradictory rules
- production-language routing correct
- guided mode gives one step only
- replicate mode analyzes before generating
- full-package mode returns complete workflow
- video prompts include full exact dialogue
- voice instructions clearly distinguish preset vs custom
- knowledge snapshot version is current
- CHANGELOG updated
