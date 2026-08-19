# Flow Video Production Skill

## Purpose

Turn one or more reference videos into a reusable AI-video production plan for Google Flow / Gemini Omni Flash while preserving the visual DNA of the references without copying a specific person's identity.

This skill is optimized for vertical social video, especially UGC/direct-response formats.

## Operating modes

### Guided mode
Use when the user wants one step at a time.

Rules:
- Give exactly one production step at a time.
- Do not jump ahead.
- After each step, stop and wait for the user to say they are ready or ask for the next step.
- Explain actions simply and concretely.
- Never assume the user has completed a step until they confirm it.

### Full-package mode
Use when the user wants everything at once.

Return:
1. reference analysis
2. character setup
3. voice setup
4. product reference setup if needed
5. final script
6. scene breakdown
7. image prompt for every scene
8. video prompt for every scene
9. exact duration for every scene
10. continuity rules
11. editing notes

### Replicate mode
Use when the user uploads reference videos and wants a reusable style profile.

Extract:
- persona archetype
- hook type
- camera behavior
- framing
- pacing
- typical scene duration
- physical props
- object interaction
- voice characteristics
- product reveal timing
- CTA style
- caption style
- editing rhythm

Save the result conceptually as a STYLE PROFILE that can be applied to new products and new characters.

## Mandatory production order

Unless the user explicitly asks for another workflow, use this order:

1. Analyze reference videos.
2. Define character identity.
3. Create/save character reference image(s).
4. Select or create persistent voice.
5. Add character behavior/profile information.
6. Create product master reference if a product must remain visually consistent.
7. Write the complete script.
8. Break the script into Flow-compatible scene durations.
9. Generate one still image for each scene using the character/product references.
10. Animate each scene from its still image.
11. Assemble clips with hard cuts unless the reference style requires something else.
12. Add captions and finishing edits.
13. Review failures and update this skill.

## Flow duration rules

For Gemini Omni Flash workflows covered by this skill, choose scene durations only from:

- 4 seconds
- 6 seconds
- 8 seconds
- 10 seconds

Do not force every scene to the maximum duration.
Choose duration from the spoken line, action complexity and pacing.

### Default speech budget

Use these as starting ranges, then adjust for the selected voice:

- 4 sec: about 8–10 words
- 6 sec: about 11–15 words
- 8 sec: about 15–19 words
- 10 sec: about 20–24 words

Target roughly 2.0–2.3 words/second for natural direct-response UGC. Prefer fewer words if the scene contains visible physical actions such as pouring, pointing, stirring or handling a product.

## Script rules

Every scene must have one clear job.
Typical jobs:

- visual hook
- verbal hook
- misconception
- problem explanation
- mechanism
- curiosity escalation
- demonstration
- transition to solution
- product reveal
- proof
- anti-hype credibility
- CTA

Avoid scenes that merely repeat the previous scene.

The first scene should normally begin with action, tension, surprise or a visually unusual object. Do not waste the opening second on a static idle pose.

## Image prompt requirements

Every scene image prompt must explicitly include:

- character reference instruction
- exact identity-consistency rules
- wardrobe continuity
- environment continuity
- scene-specific action/pose
- prop continuity
- product continuity when relevant
- composition
- camera perspective
- lighting
- realism level
- negative constraints

When possible, use the previous scene image as an additional environment/continuity reference.

For master character and master product references, prefer clean/simple backgrounds so the asset is easy to reuse.

## Video prompt requirements

Every video prompt MUST be ready to copy and paste. Never make the user manually add the dialogue afterward.

Every video prompt must contain:

1. exact duration
2. aspect ratio
3. visual style
4. strict character consistency
5. environment continuity
6. product/prop continuity
7. exact physical action
8. facial performance
9. camera behavior
10. voice identity and tone
11. exact spoken dialogue
12. explicit instruction not to paraphrase dialogue
13. lip-sync requirement
14. audio ambience
15. negative constraints

### Dialogue block

Always include a clear block such as:

`Josh must say EXACTLY:`

followed by the full line.

Then state:
- do not paraphrase
- do not add words
- do not repeat words
- only the intended character speaks
- finish within the selected duration
- use accurate natural lip sync

## Voice consistency

A recurring character must have a recurring voice identity whenever the platform supports it.

Define:
- apparent age
- gender presentation
- accent
- pitch/register
- rasp/breathiness
- cadence
- energy
- warmth
- authority level
- sales intensity

For organic UGC, default away from announcer-style delivery.
The character should usually sound like they are speaking to one person, not presenting to a crowd.

## Character consistency

Treat character identity as a locked asset.

Preserve across scenes:
- face
- age
- skin tone
- eyes
- hairstyle
- hair color
- facial hair
- body proportions
- recurring wardrobe when continuity requires it

Do not silently redesign or beautify the character.

## Product consistency

If a product is important across multiple scenes, create a master product reference before repeated use.

Preserve:
- container type
- shape
- proportions
- lid
- label layout
- colors
- brand name placement

Avoid generating multiple inconsistent versions of the same product.

## UGC realism defaults

Unless reference videos indicate otherwise:

- vertical 9:16
- realistic smartphone perspective
- medium or medium-close framing
- natural daylight
- believable real location
- subtle camera micro-movement
- restrained gestures
- natural blinking and breathing
- minimal cinematic movement
- hard cuts between clips
- no baked-in subtitles during generation

## Caption rule

Prefer captions in post-production rather than asking the video model to render them, unless there is a specific reason to bake text into the video.

## Reference analysis rule

Separate what is structural from what is incidental.

Structural examples:
- visual-hook-first storytelling
- expert-like persona
- 6–8 second scene blocks
- hard cuts
- late product reveal

Incidental examples:
- exact shirt color
- exact kitchen
- exact jar shape

The style profile should preserve the structural DNA while allowing new products, characters and environments.

## Iteration protocol

After every generated video, collect observations under:

- Worked
- Failed
- Keep
- Change
- New rule

If an observation repeatedly improves generations, promote it into this SKILL.md.

Do not overwrite useful history; record meaningful changes in CHANGELOG.md.

## Safety and claim quality

For health, wellness, finance or other sensitive commercial topics, avoid inventing medical or guaranteed outcome claims. Prefer neutral language such as personal routine, general support, product use or demonstrable product features unless verified claims are supplied by the user.

## Current validated baseline

The first validated workflow used:

- one recurring male character
- persistent voice
- six scenes
- 6/8/8/6/8/6 second timing
- visual curiosity hook with three containers
- misconception/reframe
- simple-routine transition
- product demonstration
- anti-hype credibility beat
- soft CTA
- still-image-first generation for every scene
- image-to-video animation per scene
- hard-cut assembly

See `examples/video-001-morning-greens/`.
