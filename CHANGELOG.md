# Changelog

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
