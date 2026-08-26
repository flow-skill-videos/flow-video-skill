# Video 004 — Outdoor Digestive-Tea Reference Remodel

## Status

Validated guided workflow.

## Goal

Recreate a viral digestive-tea reference as closely as practical while adapting:
- creator → Josh
- environment → recurring outdoor Texas / Southwest scene
- wardrobe → shirtless, dark shorts, barefoot
- final funnel → GUIDE instead of the original external-product / Amazon pitch

## Hook structure

The original hook uses a strange transparent digestive / intestinal demonstration prop held extremely close to the lens while the creator crouches low and pours amber liquid into it.

The visual works because:
- camera is almost at ground level
- prop is the dominant foreground element
- wide perspective makes hand + prop feel unusually large
- creator crouches with one knee raised
- liquid physically moves visible material through the transparent pathways

## Josh adaptation

Preserve:
- crouched pose
- one raised knee
- face close to camera
- prop very close to lens
- low wide-angle smartphone perspective
- one hand stabilizing prop
- other hand pouring from top

Adapt:
- no patio / house / glass walls
- use reddish dirt, rocks, dry vegetation and warm outdoor daylight
- no table in the opening hook
- Josh remains shirtless, dark shorts, barefoot

## Hook dialogue

> You can eat apples, chicken, spinach, yogurt, anything, and it will not clear what has been sitting inside you for years. Let me show you what actually works.

## Hook animation

Required behavior:
- amber liquid enters open top
- internal food-like pieces / residue visibly move downward
- upper tube becomes cleaner
- lower coiled sections receive displaced material
- same prop remains close to lens
- one continuous shot

Do not let the model remain static while liquid pours.

## Recipe sequence

### Lemon scene
Current state:
- one pot with boiling water
- one plate of chopped lemon
- no lemon inside yet

Animation:
> Get a pot of water going. Chop up a fresh lemon and drop it in the boiling water.

Action:
plate tilts → same lemon pieces fall → same pot receives them.

### Chia scene — 4 sec
Still:
- lemon already inside same pot
- one teaspoon of chia above pot
- no seeds falling yet

Animation:
> Add one teaspoon of chia seed,

Action:
full spoon → seeds fall → same pot → spoon mostly empty.

### Turmeric scene — 4 sec
Still:
- lemon + chia already inside
- one teaspoon of turmeric above pot

Animation:
> A teaspoon of turmeric,

Action:
full spoon → yellow powder falls → same pot → spoon empty → liquid begins subtle golden tint.

### Soursop bitters scene — 4 sec
Still:
- lemon + chia + turmeric already inside
- one dark bitters bottle above pot
- no stream yet

Animation:
> A splash or two of soursop bitters,

Action:
bottle tilts → one short dark-amber splash → same pot → bottle upright again.

### Black pepper scene — 4 sec
Still:
- existing amber mixture
- one small pinch of black pepper between fingers

Animation:
> And finish it with a pinch of black pepper.

Action:
fingers open → pepper falls → same pot → fingers empty.

## Straining scene

Dialogue:
> Let it boil for 10 minutes, then strain it out.

Initial failed behavior:
The strainer floated / moved unnaturally.

Validated fix:

Classify objects explicitly:
- POT = HANDHELD
- STRAINER = STATIC / FIXED
- GLASS = STATIC / FIXED
- TEA = MOVING CONTENT

State repeatedly:
- strainer already rests securely on top of glass
- nobody touches strainer
- Josh only moves the pot
- glass remains resting on table
- no strainer wobble / levitation / repositioning

Physical chain:

`POT TILTS → TEA HITS FIXED STRAINER → SOLIDS REMAIN IN MESH → FILTERED TEA FALLS INTO FIXED GLASS`

This eliminated the floating-strainer failure.

## Finished tea payoff

Still:
- one clear glass of amber tea
- Josh holds it at chest level
- no drinking yet

Animation copy used:

> This wakes your entire system up. Bloating gone, gut cleaned right out, and your body is left feeling lighter and happier.

Visual action:
- hold glass only
- subtle free-hand gestures
- no sip
- no pouring

## CTA adaptation

The original reference used a longer external-product / Amazon funnel and a different comment keyword.

For this project, remove that entire section and go directly to the guide CTA.

Validated CTA:

> If you want more natural remedies like this, comment GUIDE and I’ll send you the full guide.

Visual:
- same Josh
- same outdoor setting
- same tea glass may remain in one hand
- one small downward gesture on GUIDE
- no repeated pointing
- no physical guide/book/QR code

## Major lessons

### 1. Reference composition can be preserved while environment changes
Keep crouched pose, low lens, foreground dominance and hand placement; adapt only the surroundings and recurring creator.

### 2. Micro-actions dramatically improve stability
Each ingredient gets its own 4-second clip.

### 3. Carry current pot state forward
Every new still explicitly lists what is already in the pot.

Example:
- lemon
- lemon + chia
- lemon + chia + turmeric
- lemon + chia + turmeric + bitters
- final mixture + pepper

### 4. Fixed objects need explicit immobility
`Same object` is not enough. Say `STATIC`, `FIXED`, `nobody touches it`, and state what is physically supporting it.

### 5. Same-environment language must be concrete
Do not rely only on `same Texas setting`. Lock the exact first-frame ground, rocks, vegetation, table, lighting and camera angle.
