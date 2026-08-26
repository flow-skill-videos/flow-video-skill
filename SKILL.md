# Flow Video Production Skill

## Purpose

Turn one or more reference videos into a reusable AI-video production plan for Google Flow / Gemini / Veo-style workflows while preserving the visual DNA, timing, physical logic and retention mechanics of the references without copying a specific real person's identity.

This skill is optimized for vertical social video, especially UGC/direct-response formats, guided scene-by-scene production, recurring characters, viral reference remodelling and still-image-first image-to-video generation.

## Operating modes

### Guided mode
Use when the user wants one step at a time.

Rules:
- Give exactly one production step at a time.
- Do not jump ahead.
- If the current step is a still image, give only the still-image prompt and wait.
- If the current step is animation, give only the animation prompt and wait.
- Never assume the user has completed a step until they confirm it.
- When the user reports a generation bug, fix only the current prompt unless they explicitly ask for broader changes.
- Use short completion phrases the user can send back, e.g. `Chia pronta`, `Hook deu certo`, `CTA pronta`.
- Keep explanations simple and concrete; the prompt itself can be highly detailed.

### Full-package mode
Use when the user wants everything at once.

Return:
1. reference analysis
2. style profile
3. character setup
4. voice setup
5. product/reference setup if needed
6. final script
7. scene breakdown
8. image prompt for every scene
9. video prompt for every scene
10. exact duration for every scene
11. continuity rules
12. camera choreography
13. editing notes
14. CTA adaptation

### Replicate / remodel mode
Use when the user uploads reference videos and asks to replicate, remodel, reproduce, adapt or keep the same hook/copy/recipe.

Extract frame-by-frame:
- exact hook visual
- creator pose
- body level: standing / crouching / leaning / seated
- object placement
- object distance to lens
- hand positions
- camera height
- apparent lens / wide-angle behavior
- camera distance
- foreground dominance
- action order
- physical continuity between actions
- spoken copy
- pauses and clause boundaries
- scene duration
- cut points
- ingredient order
- prop lifecycle
- final CTA mechanics

Then separate:

**Keep as close as practical:**
- hook mechanism
- sequence of actions
- pacing
- recipe/order when requested
- spoken structure/copy when user explicitly wants a close remodel
- camera logic
- gesture logic

**Adapt:**
- creator identity
- recurring character
- environment
- wardrobe when requested
- product/funnel CTA
- branded references that do not belong to the new funnel

Do not silently replace a close-remodel request with a looser inspiration-based rewrite.

### Style-profile mode
Extract reusable structural DNA:
- persona archetype
- hook type
- absurdity / contradiction mechanism
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

Save conceptually as a STYLE PROFILE that can be applied to new products and new characters.

## Mandatory production order

Unless the user explicitly asks for another workflow:

1. Analyze reference video frame-by-frame.
2. Transcribe / reconstruct the copy as closely as the source supports.
3. Define what stays identical vs what will be adapted.
4. Define / load the STYLE PROFILE.
5. Resolve recurring character identity and wardrobe.
6. Resolve environment reference.
7. Resolve recurring voice.
8. Resolve product / CTA destination.
9. Build scene map and Flow-compatible durations.
10. Generate the still for Scene 1.
11. Animate Scene 1.
12. Wait for user confirmation.
13. Repeat still → animate → confirm for each scene.
14. Assemble clips with cuts matching the reference.
15. Add captions in post unless specifically requested during generation.
16. Record meaningful new generation lessons in this repository.

If the user has already completed a step, do not repeat it.

## Language routing

Never infer production language solely from chat language.

Keep separate:
- CHAT LANGUAGE
- PRODUCTION LANGUAGE
- VOICE ACCENT

Priority:
1. Explicit user instruction.
2. If remodelling a reference and no localization is requested, preserve the reference's spoken language.
3. If unclear, ask one short question only if it cannot be inferred from the project profile.
4. Never switch to Brazilian Portuguese only because chat is in Portuguese.

## Flow duration rules

Use only:
- 4 seconds
- 6 seconds
- 8 seconds
- 10 seconds

Choose duration from dialogue length + action complexity.

Starting speech budgets:
- 4 sec: ~8–10 words
- 6 sec: ~11–15 words
- 8 sec: ~15–19 words
- 10 sec: ~20–24 words

Validated fast creator voices may exceed these slightly if lip sync still feels natural.

For complex physical actions, prioritize action stability over stuffing more copy into the clip.

## Scene-job rule

Every scene must have one primary job:
- bizarre visual hook
- verbal hook
- misconception
- problem explanation
- mechanism
- demonstration
- ingredient addition
- transition
- product reveal
- payoff
- credibility
- CTA

Avoid scenes that merely repeat the previous scene.

## Micro-action decomposition protocol

A major validated improvement is to split fragile physical actions into very small clips.

When the model is likely to confuse objects, do NOT combine many ingredient actions in one generation.

Prefer:
- 4 sec: one spoon ingredient falls into one pot
- 4 sec: one pinch falls into one pot
- 4 sec: one bottle gives one short splash
- 6 sec: one pour through one fixed strainer
- 6 sec: one bowl pours into one ramekin
- 8 sec: one egg crack + continuous whisk if physically simple and validated

Rule:
> One fragile physical transformation or object transfer per clip whenever possible.

Benefits:
- fewer duplicates
- fewer floating objects
- fewer teleportations
- better hand continuity
- easier retries
- better physical causality

## Still-image-first protocol

For every scene:
1. Create the exact physical starting state as a still.
2. Do NOT pre-complete the action in the still unless the reference starts mid-action.
3. Use the still as First Frame.
4. Animate only the next simple action.

Typical still state language:
- `NO turmeric is falling yet.`
- `The egg is intact.`
- `The batter is NOT pouring yet.`
- `The strainer is already resting securely over the glass.`

The still is not a vague concept image. It is the exact first video frame.

## First-frame scene-lock protocol

A major validated failure is the model recreating or replacing the environment during animation.

When environment continuity matters, begin animation prompts with a hard lock:

`The provided first frame is the exact physical scene.`

Then explicitly preserve:
- same background
- same ground
- same rocks / vegetation
- same table
- same lighting direction
- same character position
- same camera angle
- same camera distance
- same props

Use language such as:
- `Do NOT recreate the location.`
- `Do NOT reinterpret the environment.`
- `This must look like the provided still image simply came to life.`
- `The first-frame background is the physical location for the entire clip.`

If a dedicated environment reference image exists, treat it as the source of truth and say so explicitly.

Do not merely say `same Texas environment`; generic environment wording can cause the model to invent another similar location.

## Continuous-take protocol

For actions that are continuous in the reference, explicitly require ONE physically continuous take.

Use strong constraints:
- no hard cut
- no jump cut
- no hidden cut
- no match cut
- no transition
- no second angle
- no sudden zoom
- no camera teleportation
- no instant reframing

Describe physical action as a chain:

`EGG → OPENS → CONTENTS FALL → SAME BOWL → WHISK`

or

`POT TILTS → LIQUID HITS FIXED STRAINER → FILTERED LIQUID FALLS → SAME GLASS`

Do not describe a continuous action as multiple cinematic scenes; Flow may interpret each clause as a cut.

## Object anchoring and physics

Every action-heavy prompt should classify props as one of:
- HANDHELD
- FIXED / STATIONARY
- RECEIVING OBJECT
- MOVING CONTENT

Example — straining:
- pot = handheld
- strainer = fixed, resting on glass
- glass = fixed, resting on table
- tea = moving content

Explicitly state what MUST NOT move.

### Stationary-prop rule
If an object should remain still, repeat the constraint:
- `The strainer is STATIC and FIXED.`
- `Nobody touches the strainer.`
- `The glass remains physically resting on the table.`

This prevents floating and levitating props.

### Object-count rule
Use exact counts:
- exactly one pot
- exactly one spoon
- exactly one bowl
- exactly one ramekin
- exactly one cup
- exactly one bottle

For a prop with subparts, define them precisely, e.g. one anatomical model with two connected lung lobes and one trachea.

### State transition rule
Describe before / during / after:
- spoon full → powder falls → spoon empty
- plate full of lemon → lemon falls → plate mostly empty
- glass empty → tea enters → glass partially filled
- egg whole → egg opens → no whole egg remains

The same physical object must persist through the entire transition.

## One-handed action simplification

If the reference uses a simple one-handed action, preserve it.

Validated example:
- hold egg in one hand
- open/crack above bowl with the same hand
- contents fall into bowl
- immediately continue to whisk

Do not over-choreograph simple reference actions. More choreography often creates more cuts and object bugs.

## Transformation-effect protocol

For visual transformations, define the exact causal response.

If the transformation should be immediate:

`CONTACT = IMMEDIATE CHANGE`

Example:
- liquid touches black coating
- the contacted area becomes pink immediately
- the clean trail follows the liquid stream

Do not use slow verbs such as `soften`, `gradually dissolve`, `eventually peel` if the desired reference effect is instant.

Specify:
- trigger
- response time
- direction of progression
- final state deadline

Example:
`By second 7–8, both lungs should already be ~90–100% clean so the viewer gets final-result hold time.`

## High-retention bizarre-hook rule

When the reference relies on aggressive visual hooks, do NOT default to ordinary ingredients.

Prefer a visual that creates immediate `what is that?` curiosity while still having a logical bridge.

Strong bizarre hooks require:
1. pattern interrupt
2. semantic bridge
3. narrative payoff

Validated mechanisms:
- oversized metaphorical body prop
- anatomical demonstration model
- transparent digestive model packed with visible material
- black-to-pink lung demonstration prop
- unusual powder/liquid interaction
- strange object placed extremely close to lens
- contradictory physical demonstration

For anatomical props:
- make them clearly props / demonstration models
- no blood
- no gore
- no exposed-real-organ framing

## Foreground / crouched-hook protocol

When a reference hook uses a strange prop very close to the lens:
- match the low camera height
- use slightly wide smartphone perspective
- let the prop dominate the lower foreground
- allow the creator's hand to appear larger due to perspective
- preserve crouched / kneeling pose if structural to the hook
- keep face visible above / behind the prop

Do not automatically force the recurring table into a hook if the reference works because the creator is on the ground.

The table can return in later recipe scenes.

## Reference-copy adaptation

When the user explicitly says `same copy`, `same recipe`, `same hook`, or `replicate as close as possible`:
- preserve the original clause order
- preserve ingredient order
- preserve hook wording as closely as practical
- preserve action-to-copy synchronization
- only adapt the portions requested, usually creator, location, product mention and CTA

Do not unnecessarily rewrite every sentence into a different style.

If a source line is unclear, say what is uncertain rather than inventing exact wording.

## CTA adaptation protocol

When replacing a reference CTA with a funnel CTA:
- remove unrelated brand / Amazon / profile-search instructions
- preserve the creator's natural closing rhythm
- use the user's keyword exactly
- use one small gesture on the keyword
- no repeated pointing
- do not require showing the digital product unless requested

Typical structure:
`If you want more natural remedies like this, comment GUIDE and I’ll send you the full guide.`

CTA visual defaults:
- same environment
- same creator
- one existing prop may remain in hand
- direct eye contact
- one subtle downward point on keyword
- no physical guide/book/QR code unless requested

## Camera choreography

Do not make every scene identical when the reference changes composition.

Validated patterns:
- hook: close, wide, dominant foreground prop
- ingredient scene: medium-close, ingredient above pot
- pour: camera stays stable with tiny downward emphasis
- explanation/payoff: glass/food visible at chest or table level
- CTA: direct eye contact, small emphasis gesture

Camera movement should follow action, not decorate it.

Default UGC camera motion:
- tiny handheld tremor
- slight horizontal drift
- slight vertical drift
- subtle autofocus breathing
- minor imperfect framing corrections

Avoid cinematic dolly moves unless the reference clearly uses them.

## Full-frame exported-footage rule

`Smartphone UGC` can be misread as content displayed inside a phone mockup.

When vulnerable, explicitly prohibit:
- phone frame
- smartphone bezel
- notch
- status icons
- app UI
- screen-within-screen
- device mockup
- black borders
- mobile overlay

The output should be final full-frame 9:16 footage.

## Image prompt requirements

Every scene image prompt should include:
- character reference instruction
- exact wardrobe
- environment reference / continuity
- exact first-frame physical state
- scene-specific pose
- prop counts
- prop positions
- current recipe/product state
- future objects that must NOT appear yet
- composition
- foreground/background hierarchy
- camera perspective
- apparent lens/distance when important
- lighting
- realism
- negative constraints
- explicit success condition

When possible, use the previous successful frame as continuity reference.

## Video prompt requirements

Every animation prompt must be ready to copy/paste and contain:
1. exact duration
2. aspect ratio
3. first-frame / scene lock
4. character continuity
5. environment continuity
6. object counts
7. fixed vs moving objects
8. starting state
9. exact physical action
10. timing blocks
11. physical-state transitions
12. camera behavior
13. performance
14. exact dialogue
15. do-not-paraphrase instruction
16. voice/audio profile
17. Foley
18. negative rules
19. final state / success condition

### Dialogue block
Always include:

`He must say EXACTLY:`

Then:
- do not paraphrase
- do not add words
- do not remove words
- do not repeat words
- only intended character speaks
- final word must be audible before clip ends

## Voice consistency and distance realism

Recurring character voice should remain stable:
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

For outdoor UGC, match sound to visible camera distance.

Avoid:
- studio microphone sound
- podcast proximity bass
- heavy radio compression
- polished announcer delivery

Prefer:
- natural midrange
- mild distance attenuation
- faint outdoor ambience
- subtle breeze
- real phone-camera feel

A visually distant creator should not sound like their mouth is 5 cm from a condenser microphone.

## Character consistency

Treat recurring character identity as a locked asset.

Preserve:
- face
- age
- skin tone
- eyes
- hairstyle
- hair color
- facial hair
- body proportions
- recurring wardrobe

Do not silently beautify, age-shift or redesign.

### Famous-person false-positive workaround
If Flow flags a recurring generated character because prompts over-emphasize identity:
- simplify the animation instruction
- use `Animate the provided starting frame`
- preserve visible clothing, props and environment
- avoid unnecessary `exact identity`, `same face`, `celebrity`, `famous person` language

The first frame already carries the visual identity.

## Product consistency

If a physical product is important across scenes, create a master product reference.

Preserve:
- container type
- shape
- proportions
- lid
- label layout
- colors
- brand-name placement

If the funnel product is digital and the content strategy does not show it, do NOT invent a physical book/product reveal.

## UGC realism defaults

Unless reference indicates otherwise:
- vertical 9:16
- full-frame exported footage
- natural daylight
- believable real location
- subtle camera micro-movement
- restrained gestures
- natural blinking/breathing
- minimal cinematic movement
- hard cuts between independent clips
- no baked-in subtitles

For aggressive hooks, allow:
- closer framing
- wide perspective
- larger foreground props
- low-angle / ground-level camera
- brighter outdoor contrast

## Caption rule

Prefer captions in post-production.

If user handles captions in CapCut or another editor, do not spend guided-mode steps on captions unless asked.

## Wellness / claims

Do not invent verified medical efficacy.

When remodelling a viral wellness reference, distinguish:
- visual metaphor / prop
- recipe demonstration
- source copy
- verified medical claim

Bizarre anatomy props are demonstration props, not medical proof.

Do not add new diagnoses or guaranteed outcomes that were not supplied.

## Iteration protocol

After meaningful generation tests, classify observations:
- Worked
- Failed
- Keep
- Change
- New rule

Promote repeated improvements into this SKILL.md.
Record history in CHANGELOG.md.

## Validated baselines

### Video 001 — Morning Greens
Validated:
- recurring character
- persistent voice
- six scenes
- 6/8/8/6/8/6 timing
- visual curiosity hook
- still-first generation
- image-to-video animation
- hard-cut assembly

See `examples/video-001-morning-greens/`.

### Video 002 — Pep Tonic outdoor bizarre-hook
Validated:
- bizarre oversized hook prop
- bright outdoor natural light
- closer wide creator framing
- dominant foreground object
- late product reveal
- camera follows scoop/pour
- varying framing by narrative block
- full-frame/no-phone constraints
- exact object counts

See `examples/video-002-pep-tonic-bizarre-hook/`.

### Video 003 — Outdoor cheesecake recipe remodel
Validated:
- close reference-copy preservation
- one-handed egg crack
- no-cut crack → bowl → whisk flow
- separate honey/vanilla step
- bowl → ramekin pour isolated into its own clip
- finished-food payoff scenes
- same outdoor character continuity
- reference CTA replaced with GUIDE CTA

See `examples/video-003-cheesecake-remodel/`.

### Video 004 — Outdoor digestive-tea reference remodel
Validated:
- crouched ground-level bizarre digestive-prop hook
- prop extremely close to lens
- outdoor setting adapted while preserving hook composition
- ingredient-by-ingredient 4-second micro-actions
- exact current-pot-state continuity
- fixed strainer + fixed glass + moving pot protocol
- no floating strainer after stationary-object lock
- finished-tea payoff
- direct GUIDE CTA instead of original external-product/Amazon funnel

See `examples/video-004-digestive-tea-remodel/`.
