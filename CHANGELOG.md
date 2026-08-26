# Changelog

## 0.3.0 — Exact-remodel + scene-lock + micro-action workflow

Validated several additional end-to-end productions using the same recurring outdoor creator, including a cheesecake recipe remodel, a digestive-model tea remodel, black-to-pink anatomy-prop hooks, fixed-strainer pouring and GUIDE-based funnel CTAs.

### Added
- exact-reference remodel mode for requests such as `same hook`, `same copy`, `same recipe`, `replicate as close as possible`
- frame-by-frame analysis checklist for pose, object distance, camera height, hand positions, action order and copy clause boundaries
- strict still-image-first protocol where every still represents the exact first video frame
- absolute First Frame scene-lock protocol
- explicit instruction that the provided first frame is the exact physical scene and must not be recreated
- environment-reference locking for ground, rocks, vegetation, table, lighting, camera angle and camera distance
- one-continuous-take protocol with no hidden cuts, jump cuts, angle switches or camera teleportation
- physical action chains such as `egg → open → fall → same bowl → whisk`
- micro-action decomposition for fragile Flow generations
- explicit fixed / handheld / receiving-object / moving-content classifications
- repeated stationary-object constraints to prevent floating props
- state-transition rules: full spoon → falling ingredient → empty spoon, empty glass → liquid enters → filled glass, etc.
- one-handed action simplification when the reference uses a casual one-handed move
- transformation-response timing rules such as `CONTACT = IMMEDIATE CHANGE`
- final-result deadline rules so visual transformations finish early enough to hold on the payoff
- crouched ground-level hook protocol with foreground prop close to wide-angle lens
- direct CTA adaptation rules that remove unrelated Amazon / external-brand instructions
- digital-product rule: do not invent a physical book/guide when the funnel product is digital and normally hidden
- camera-distance voice realism rules for outdoor UGC
- famous-person false-positive workaround: simplify to `Animate the provided starting frame` when identity-heavy language triggers safety filters

### Validated physical-generation lessons

#### Scene continuity
Generic language such as `same Texas environment` is not always enough. The animation prompt should state that the provided first frame itself is the exact location and should list the major environmental elements that must remain unchanged.

#### Continuous actions
When a reference has a fluid action, describing it as multiple separate stages can cause Flow to insert visual cuts. Use a single physical chain and aggressively prohibit cuts and instant reframing.

Validated example:

`whole egg → one-handed crack → contents fall into SAME bowl → immediately whisk SAME bowl`

#### Micro-actions
Separating ingredients into individual 4-second clips significantly improved stability:
- chia seeds
- turmeric
- bitters
- black pepper

Each clip used one object transfer only.

#### Floating-object fix
A strainer repeatedly floated when the prompt treated it as a participant in the action.

Successful fix:
- strainer = STATIC / FIXED
- strainer already resting securely over the receiving glass
- nobody touches the strainer
- glass = STATIC / FIXED on table
- pot = only handheld object
- tea = only moving content

#### Transformation timing
A black-lung demonstration effect initially cleaned too slowly. The improved prompt defined:

`liquid contact → contacted black area becomes pink immediately`

and required the lungs to be mostly clean by second 7–8 rather than at the final frame.

#### Environment drift
Animation models sometimes replaced the background during a pour. Successful prompts explicitly said:
- do not recreate location
- do not reinterpret environment
- first-frame background is the physical location
- same ground, rocks, vegetation, table, lighting and camera position

### Video 003 — Outdoor cheesecake remodel

Validated:
- exact reference structure adapted to recurring outdoor character
- same recipe order
- one-handed egg-crack hook
- no-cut crack → bowl → whisk action
- honey + vanilla continuation
- isolated bowl-to-ramekin pour
- baked cheesecake texture reveal
- plate-based benefit explanation
- replacement of original CTA with `GUIDE`

See `examples/video-003-cheesecake-remodel/`.

### Video 004 — Outdoor digestive-tea remodel

Validated:
- bizarre transparent digestive demonstration model close to lens
- ground-level crouched creator hook
- outdoor-environment adaptation while preserving reference composition
- lemon → chia → turmeric → bitters → black pepper → strain sequence
- 4-second ingredient micro-actions
- exact current-pot-state continuity between clips
- stationary strainer/glass fix
- finished-tea payoff shot
- GUIDE CTA replacing the original external-product/Amazon funnel

See `examples/video-004-digestive-tea-remodel/`.

### Project handoff

Added `PROJECT_PROFILE.md` as the canonical handoff file for the current recurring Josh / outdoor / natural-remedy project so a new chat or profile can recover the production setup without rebuilding it from scratch.

---

## 0.2.0 — Bizarre-hook + dynamic creator-camera workflow

Validated a second end-to-end production using a brighter, more aggressive outdoor UGC style.

### Added
- explicit separation between chat language and production language
- reference-language preservation when the user does not request localization
- stronger bizarre-hook selection rules
- requirement that bizarre hooks be semantically bridgeable rather than merely random
- hook-prop lifecycle across scenes
- dominant foreground-object analysis
- dynamic camera choreography per scene
- closer slightly wide-angle creator framing
- bright outdoor natural-light option
- camera-following motion for scoop/pour demonstrations
- subtle lateral drift and push-in behavior
- stronger CTA framing
- explicit full-frame exported-footage rule
- negative constraints for phone frames, bezels, notches, status icons, app UI, screen-within-screen and device mockups
- exact object-count constraints for product-demo scenes
- support for skipping caption guidance when the user handles captions separately

### Validated narrative structure

Bizarre Visual Hook → Explain/Reframe Hook → Transition to Simpler Routine → Product Reveal/Demonstration → Credibility Beat → CTA

### Important lessons

- A visually relevant but ordinary hook is not enough when the reference style depends on a strong "what is that?" reaction.
- The best strange props create contradiction/curiosity first and can still be explained naturally in the next scene.
- Random weirdness without a narrative bridge should be rejected.
- Keep the strange hook prop visible through the explanation, then progressively move it out of prominence as the product enters.
- Changing camera distance and composition between scenes improves perceived energy.
- Camera movement works best when it follows the story or a physical action instead of being decorative.
- Slightly wide-angle close framing makes foreground props feel larger and more attention-grabbing.
- Bright outdoor natural light can create stronger creator energy and body/face definition when it matches the reference style.
- "Smartphone UGC" can be misread as a phone mockup; explicitly request final full-frame footage and prohibit phone UI/device framing.
- Product-demonstration prompts should specify exactly one container, one scoop and one glass when duplication is a risk.
- Preserve the exact product master reference through reveal, demonstration and CTA.

### Second validated baseline

See `examples/video-002-pep-tonic-bizarre-hook/`.

---

## 0.1.0 — Initial validated workflow

Created the first reusable production method from an end-to-end Google Flow / Gemini Omni Flash test.

### Added
- guided mode
- full-package mode
- replicate/style-profile mode
- 4/6/8/10-second scene planning
- approximate speech budgets
- character identity locking
- recurring voice profile rules
- master product-reference workflow
- still-image-first scene creation
- required video-prompt structure with exact dialogue
- UGC realism defaults
- post-production caption preference
- iteration protocol

### First validated narrative structure

Visual Hook → Common Belief → Reframe → Simple Routine → Product Demonstration → Anti-Hype Credibility → Soft CTA

### Initial lessons

- Give one step only in guided mode.
- Put the exact spoken line directly inside every video prompt.
- Explicitly request no paraphrasing and no extra dialogue.
- Preserve environment by reusing the previous scene image when possible.
- Create a product master reference before repeated product appearances.
- Avoid baked-in subtitles in generated clips.
- Prefer restrained gestures and smartphone realism over cinematic motion for organic UGC.
