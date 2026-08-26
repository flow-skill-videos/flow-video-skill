# Project Profile — Josh Outdoor Natural-Remedy UGC

## Purpose

This file is the canonical handoff for the current active project.

Use it when starting a new chat/profile so the workflow does not have to be rebuilt from memory.

General reusable production rules still live in `SKILL.md`. This file contains the project-specific defaults for the recurring Josh / outdoor / GUIDE funnel.

---

## Chat and production language

- Chat with the user in Brazilian Portuguese.
- Generated video dialogue is English (US).
- Default accent: neutral General American.
- Do not switch the production language to Portuguese just because the user chats in Portuguese.

---

## Recurring creator — Josh

Josh is a generated recurring fictional creator, not a real person.

Visual profile:
- mature fit white/Caucasian-looking male
- approximately 45–52 years old
- short sandy-blond / light-brown hair
- natural light stubble
- athletic / fit body, not bodybuilder
- natural skin texture

Default current-series wardrobe:
- SHIRTLESS
- simple dark shorts
- BAREFOOT
- no hat
- no jacket
- no shoes
- usually no glasses unless a specific reference requires them

Performance:
- direct to camera
- confident
- calm
- matter-of-fact
- slightly intense
- natural creator energy
- low sales intensity
- not theatrical
- not polished like an infomercial

---

## Josh voice

Default voice profile:
- native English (US)
- strict neutral General American accent
- mature male
- medium-low natural pitch
- slight natural rasp
- grounded
- conversational
- controlled pace
- calm authority
- low sales intensity

Outdoor recording rule:
The voice must acoustically match the visible camera distance.

Avoid:
- podcast proximity bass
- studio voice-over
- heavy compression
- radio-announcer tone
- polished commercial voice

Prefer:
- natural midrange
- mild distance attenuation
- subtle outdoor ambience
- faint breeze
- real phone-camera recording feel

---

## Canonical outdoor environment

The current series uses one recurring outdoor world.

Visual characteristics:
- dry Texas / Southwest-style landscape
- reddish-orange / reddish-brown earth
- scattered rocks
- dry grass
- sparse scrub vegetation
- occasional small trees / bushes
- bright warm natural daylight
- isolated rustic atmosphere

Recurring recipe setup:
- one rustic wooden table
- compact outdoor burner when cooking is required

Important:
If the user supplies a reference image of this environment, that image is the source of truth.

Animation prompts should not merely say `same Texas environment`.

Use:
- `The provided first frame is the exact physical scene.`
- `Do NOT recreate the location.`
- `Do NOT reinterpret the environment.`
- preserve same ground, rocks, vegetation, table, lighting, camera position and framing

The environment must not drift to:
- patio
- house
- glass doors
- modern kitchen
- indoor cabin
- another generic desert location

---

## Camera style

Default:
- vertical 9:16
- full-frame exported footage
- natural slightly wide smartphone perspective
- raw UGC
- subtle handheld motion
- tiny horizontal drift
- tiny vertical drift
- subtle autofocus breathing
- small imperfect framing corrections

Never show:
- phone frame
- device mockup
- smartphone bezel
- notch
- app UI
- visible phone/camera/operator

For bizarre hooks:
- foreground prop can be extremely close to lens
- low / ground-level camera is allowed and often preferred
- wide perspective can exaggerate foreground size naturally
- Josh may crouch / kneel if the reference does

---

## Current funnel product

Primary funnel product:
**The Encyclopedia of Natural Remedies**

Known project positioning:
- digital guide / ebook
- 300+ natural / home remedies
- guide is delivered after the viewer comments the keyword

The generated videos normally do NOT show:
- physical book
- ebook cover
- printed guide
- QR code

The content itself is the hook/value; the guide is the CTA destination.

---

## CTA keyword

Canonical keyword:

**GUIDE**

Default CTA:

> If you want more natural remedies like this, comment GUIDE and I’ll send you the full guide.

Other accepted variation:

> If you like natural remedies like this, comment GUIDE and I’ll send you a guide with over 300 more.

CTA visual behavior:
- direct eye contact
- one small natural downward point on `GUIDE`
- no repeated pointing
- no overacting
- existing prop/drink may remain in one hand
- no physical guide reveal unless specifically requested

---

## Current content strategy

The user often supplies a proven viral reference and wants a very close remodel.

Default interpretation of:
- `mesmo vídeo`
- `mesmo gancho`
- `mesma copy`
- `mesma receita`
- `replicar o mais próximo possível`

means:

Preserve as closely as practical:
- hook mechanism
- action sequence
- ingredient order
- pacing
- copy structure
- camera logic
- creator pose when structural
- prop placement when structural

Adapt:
- creator → Josh
- location → canonical Josh outdoor environment
- wardrobe → shirtless + dark shorts + barefoot unless user says otherwise
- unrelated brand/product pitch → remove
- original CTA → GUIDE funnel

Do not loosely rewrite a reference if the user asked for a near-copy remodel.

---

## Guided production workflow

The user strongly prefers one production step at a time.

Default sequence:
1. analyze reference frame-by-frame
2. explain the structural plan briefly
3. give Scene 1 still-image prompt only
4. wait for user to say image is ready
5. give Scene 1 animation prompt only
6. wait for `deu certo`
7. give next still
8. repeat

Never dump all future scenes unless explicitly asked.

---

## Still-image rules

Every still should represent the exact first frame of the next animation.

Explicitly define:
- exact current recipe state
- exact object counts
- exact hand positions
- what has already happened
- what has NOT happened yet
- future props that must not appear yet

Examples:
- `NO chia seeds are falling yet.`
- `The spoon remains full.`
- `The batter is NOT pouring yet.`
- `The egg is intact.`

---

## Animation rules

Default opening:

`Animate the provided first frame as ONE SINGLE CONTINUOUS [duration]-second vertical 9:16 raw UGC video.`

Then lock:
- first frame is exact scene
- environment does not change
- same character / wardrobe
- same prop counts
- same table / pot / bowl / glass as applicable

For fluid actions aggressively prohibit:
- hard cuts
- jump cuts
- hidden cuts
- match cuts
- transitions
- second angles
- sudden zooms
- camera teleportation
- instant reframing

---

## Object-physics rules

Flow frequently creates:
- floating objects
- duplicate glasses
- extra jars
- teleporting bowls
- utensils that transform

Fix by classifying each object.

Example — straining tea:
- pot = handheld
- strainer = STATIC and FIXED
- glass = STATIC and FIXED
- tea = moving content

Say explicitly:
- nobody touches the strainer
- strainer rests securely on the glass
- glass rests on table
- Josh only moves the pot

Use exact object counts repeatedly.

---

## Micro-action defaults

For fragile ingredient actions, prefer separate clips.

Validated:
- 4 sec chia
- 4 sec turmeric
- 4 sec bitters
- 4 sec black pepper
- 6 sec straining
- 6 sec bowl → ramekin pour

Do not combine multiple fragile transfers if not necessary.

---

## Validated transformation rule

If a hook uses a visual cleaning transformation and the reference is fast:

**CONTACT = IMMEDIATE CHANGE**

Example:
- orange liquid touches black lung coating
- contacted area instantly reveals pink beneath
- clean trail follows liquid in real time
- final result should be mostly complete before the last 1–2 seconds

Avoid slow wording such as:
- gradually softens
- eventually dissolves
- slowly peels

unless that is what the reference actually shows.

---

## Famous-person false-positive workaround

Flow may occasionally flag a generated recurring character when prompts over-emphasize identity locking.

If that happens:
- do not repeat `same exact identity/face`
- avoid unnecessary celebrity/famous-person language
- use the simpler instruction:

`Animate the provided starting frame.`

Then lock only visible scene, clothing, props and actions.

---

## Validated recent production patterns

### Cheesecake reference remodel
Structure:
- egg + Greek yogurt hook
- one-handed egg crack
- immediate whisk in same continuous shot
- raw honey + vanilla
- pour into ramekin
- baked cheesecake payoff
- texture scoop
- slice on plate
- benefit/explanation blocks
- GUIDE CTA

Key lesson:
The egg crack looked better when treated as one natural action rather than separate cinematic stages.

### Digestive-tea reference remodel
Structure:
- bizarre transparent digestive prop close to lens
- Josh crouched at ground level
- amber liquid flush visual
- pot + fresh lemon
- chia
- turmeric
- soursop bitters
- black pepper
- strain
- finished tea payoff
- GUIDE CTA

Key lessons:
- ingredient micro-clips are stable
- preserve exact current pot state from clip to clip
- fixed strainer must be explicitly stationary
- no table in the crouched hook if the reference hook works at ground level

### Lung demonstration hook
Structure:
- black lung demonstration model
- orange/yellow liquid pour
- touched black area becomes pink immediately

Key lessons:
- environment needs First Frame lock
- transformation must be immediate on contact
- do not wait until the final second for the clean result

---

## Safety / claims

The reference ecosystem often contains aggressive wellness claims.

Do not invent additional medical claims beyond what is present/supplied.

Anatomy visuals should be framed as demonstration props/models, with:
- no blood
- no gore
- no real exposed organs

Do not treat a visual prop as medical proof.

---

## Quick handoff instruction for a new chat

When a new chat starts with this repository connected:

1. Read `PROJECT_PROFILE.md`.
2. Read `SKILL.md`.
3. If the user uploads a reference, analyze it frame-by-frame.
4. Preserve the reference closely when requested.
5. Adapt to Josh + canonical outdoor scene + GUIDE funnel.
6. Work one still/animation step at a time.
7. Treat every successful user confirmation as the locked state for the next scene.
