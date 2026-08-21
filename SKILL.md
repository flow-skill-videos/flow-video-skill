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
11. camera choreography
12. editing notes

### Replicate mode
Use when the user uploads reference videos and wants a reusable style profile.

Extract:
- persona archetype
- hook type
- hook absurdity / contradiction mechanism
- camera behavior
- camera distance and apparent focal length
- framing
- foreground dominance
- indoor vs outdoor lighting strategy
- pacing
- typical scene duration
- physical props
- object interaction
- prop lifecycle across scenes
- voice characteristics
- production language and accent
- product reveal timing
- CTA style
- caption style
- editing rhythm

Save the result conceptually as a STYLE PROFILE that can be applied to new products and new characters.

## Mandatory production order

Unless the user explicitly asks for another workflow, use this order:

1. Analyze reference videos.
2. Define the STYLE PROFILE.
3. Define character identity if not already created.
4. Create/save character reference image(s) if needed.
5. Select or create persistent voice if needed.
6. Add character behavior/profile information.
7. Create product master reference if a product must remain visually consistent.
8. Write the complete script.
9. Break the script into Flow-compatible scene durations.
10. Define camera choreography and visual job for every scene.
11. Generate one still image for each scene using the character/product references.
12. Animate each scene from its still image.
13. Assemble clips with hard cuts unless the reference style requires something else.
14. Add captions and finishing edits.
15. Review failures and update this skill.

If the user has already completed a step, do not repeat it.

## Language routing

Never infer the production language solely from the language used in chat.

Keep separate:
- CHAT LANGUAGE = language used to explain steps to the user
- PRODUCTION LANGUAGE = language spoken in the generated video
- VOICE ACCENT = accent of the recurring character voice

Priority:
1. If the user explicitly specifies the video language, use it.
2. If the user asks to replicate reference videos and does not request localization, preserve the spoken language of the references by default.
3. If the references are mixed or unclear, ask one short clarification question.
4. Never switch to Brazilian Portuguese only because the user is chatting in Portuguese.

For a custom Flow voice, provide a concise Voice Performance prompt and state clearly where it should be pasted. Do not create a voice-profile file unless the user specifically asks for one.

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

A validated fast creator voice may exceed these starting ranges slightly, but only if the line still fits naturally with clean lip sync. Never cram dialogue only to preserve copy.

## Script rules

Every scene must have one clear job.
Typical jobs:

- bizarre visual hook
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

## High-retention bizarre-hook rule

When the reference style relies on aggressive visual hooks, do NOT default to merely relevant or attractive objects such as a neat spread of ingredients.

Prefer a visual that creates an immediate "what is that?" reaction while still having a logical bridge to the topic.

A strong bizarre hook has three requirements:

1. **Pattern interrupt** — oversized, uncanny, contradictory, unexpected or physically strange visual.
2. **Semantic bridge** — Scene 2 can explain why that object/action relates to the topic without feeling random.
3. **Narrative payoff** — the hook naturally leads into the problem, reframe, routine or product later.

Examples of mechanisms:
- oversized metaphorical body/shape prop
- bizarre containers representing an internal concept
- unexpected powder/liquid interaction
- strange object placed extremely close to camera
- contradictory physical demonstration

Do not copy the exact prop or creator identity from a reference video. Rebuild the retention mechanism for the new product.

Do not use random weirdness that cannot be explained cleanly within the story.

For wellness topics, bizarre anatomy-like props should stay non-gory and clearly metaphorical. Do not use them to imply a diagnosis or guaranteed medical effect.

## Hook-to-product bridge

For direct-response UGC with a late product reveal, use this default arc when it fits the references:

1. bizarre hook
2. explain/reframe the hook
3. transition away from random fixes or complexity
4. reveal and demonstrate the product
5. credibility / simple-value beat
6. CTA

The hook prop can remain visible through Scenes 2–3 for continuity, then move to the side and lose prominence once the product is revealed.

The product should not appear in the first frame unless the reference style clearly does that.

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
- foreground/background hierarchy
- camera perspective
- apparent lens / distance when important
- lighting
- realism level
- negative constraints

When possible, use the previous scene image as an additional environment/continuity reference.

For master character and master product references, prefer clean/simple backgrounds so the asset is easy to reuse.

For a recurring bizarre hook prop, preserve its shape, size, texture and location logic across the scenes where it remains visible.

## Dynamic camera choreography

Do not treat every scene as the same locked talking-head composition when the references use stronger camera energy.

Define a camera job per scene.

Validated high-retention pattern:
- Hook: close, slightly wide-angle, dominant foreground object, character leaning toward lens, subtle handheld/push-in.
- Explanation: character slightly closer, prop still visible, different composition from hook.
- Transition: tighter face/upper-body framing, subtle lateral shift or push-in.
- Product reveal: camera follows the physical action with a small tilt or reposition toward hands/glass/product.
- Credibility: close-medium framing, slight sideways drift and subtle push-in near the key line.
- CTA: closest framing, restrained final push-in toward face + product.

Rules:
- camera movement should follow story or physical action
- prefer subtle handheld motion over cinematic dolly moves
- vary distance/framing between blocks so the video does not feel frozen
- slightly wide-angle close perspective can make foreground props feel larger and more surprising
- outdoor or bright natural-light setups can be used when the reference style relies on high clarity and stronger visual contrast
- wardrobe changes such as shirtless presentation are optional structural cues only when they fit the character, context and reference style; never treat them as mandatory

## Full-frame exported-footage rule

A validated failure occurred when "smartphone UGC" was interpreted as showing the scene inside a phone mockup.

When using smartphone/creator-camera language, explicitly state that the model must show only the final exported footage.

Add strong negative constraints when needed:
- no phone frame
- no smartphone bezel
- no notch
- no status icons
- no app UI
- no screen-within-a-screen
- no device mockup
- no black borders
- no mobile overlay

Do not rely on the phrase "smartphone-style" alone.

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
9. camera behavior / choreography
10. voice identity and tone
11. exact spoken dialogue
12. explicit instruction not to paraphrase dialogue
13. lip-sync requirement
14. audio ambience
15. negative constraints
16. full-frame/no-device-overlay rule when relevant

### Dialogue block

Always include a clear block such as:

`Josh must say EXACTLY:`

followed by the full line.

Then state:
- do not paraphrase
- do not add words
- do not remove words
- do not repeat words
- only the intended character speaks
- finish within the selected duration
- use accurate natural lip sync

## Voice consistency

A recurring character must have a recurring voice identity whenever the platform supports it.

Define:
- apparent age
- gender presentation
- production language
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

During product-demo scenes, explicitly constrain the number of repeated objects when generation is prone to duplication, for example:
- exactly one product container
- exactly one scoop
- exactly one glass

## UGC realism defaults

Unless reference videos indicate otherwise:

- vertical 9:16
- full-frame exported footage
- realistic creator-camera perspective
- medium or medium-close framing
- natural daylight
- believable real location
- subtle camera micro-movement
- restrained gestures
- natural blinking and breathing
- minimal cinematic movement
- hard cuts between clips
- no baked-in subtitles during generation

If the reference style is more aggressive, allow closer framing, slightly wide-angle perspective, brighter outdoor light, stronger foreground objects and more intentional camera-following movement.

## Caption rule

Prefer captions in post-production rather than asking the video model to render them, unless there is a specific reason to bake text into the video.

If the user already handles captions in CapCut or another editor, do not waste guided-mode steps explaining captions unless asked.

## Reference analysis rule

Separate what is structural from what is incidental.

Structural examples:
- bizarre visual-hook-first storytelling
- expert-like persona
- strong foreground prop
- close wide-angle creator framing
- bright outdoor setup
- camera following physical action
- 6–8 second scene blocks
- hard cuts
- late product reveal

Incidental examples:
- exact creator face
- exact shirt/no-shirt choice
- exact backyard
- exact prop from the original reference
- exact jar shape

The style profile should preserve the structural DNA while allowing new products, characters, props and environments.

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

A bizarre visual metaphor may illustrate a topic, but it must not be presented as medical proof.

## Validated baselines

### Video 001 — Morning Greens
Validated:
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

### Video 002 — Pep Tonic outdoor bizarre-hook
Validated improvements:
- six scenes using 6/8/8/6/8/6 timing
- bizarre oversized metaphorical prop as the first-frame scroll stopper
- bright outdoor natural light
- closer, slightly wide-angle creator framing
- dominant foreground object in the hook
- character leaning toward lens
- hook prop preserved through explanation, then moved aside as product enters
- late product reveal
- camera follows scoop/pour action
- framing changes between scenes instead of repeating one locked composition
- subtle handheld drift and push-ins
- stronger close CTA framing
- explicit full-frame/no-phone-overlay constraints
- exact object-count constraints during product scenes
- still-image-first generation followed by image-to-video animation

See `examples/video-002-pep-tonic-bizarre-hook/`.
