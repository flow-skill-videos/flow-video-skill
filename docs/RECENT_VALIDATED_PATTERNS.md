# Recent Validated Patterns — Josh Outdoor Series

This document records production patterns validated after the earlier Pep Tonic baseline. It is project history and a practical reference for new chats.

Use `SKILL.md` for reusable rules and `PROJECT_PROFILE.md` for the canonical current setup.

---

## 1. Hydrogen-peroxide foot hook

Validated hook copy:

> Pour hydrogen peroxide on your feet and watch what happens. If it starts foaming, pay attention.

Structural lessons:
- bizarre / slightly alarming physical hook works well
- Josh remains shirtless outdoors
- foot is grounded close to camera
- action should be readable immediately
- camera stays natural handheld, no phone visible
- visual effect should begin quickly rather than waiting until the end

---

## 2. Potato-water recipe

Validated visual sequence:
- black pot with whole potatoes boiling on small rustic burner
- Josh shirtless in outdoor setting
- potato water poured into a clear glass jar on a wooden stump / rustic surface
- explanation / usage
- GUIDE CTA

Generation lesson:
Flow can sometimes flag identity-heavy language as a famous-person issue even for a generated recurring character.

Successful workaround:
- `Animate the provided starting frame`
- preserve visible scene / wardrobe / props
- avoid repeating `same exact identity`, `same exact face`, celebrity/famous-person language

---

## 3. Baking-soda foot video

Validated hook copy:

> If your feet feel nasty at night, do this before bed.

Validated visual logic:
- Josh shirtless outdoors
- foot grounded close to lens
- baking soda poured from a box onto top of foot
- later basin / foot soak with baking soda + Epsom salt
- GUIDE CTA

Lesson:
Strong foreground body-part + powder interaction is a reliable pattern interrupt in this series.

---

## 4. Five-food-tests remodel

This video validated a multi-test structure adapted to Josh / outdoor environment.

### Fish
Copy:
> Number one, if you bought fish from the market, place it in a bowl of water. If it sinks, it’s fresh. If it floats, it’s gone bad.

Visual:
- two transparent tubs with water
- exactly one fish in each hand at start
- one sinks / one floats

### Egg
Copy:
> Number two, place an egg in a bowl of water. If it sinks, it’s good. If it floats, it’s about to go bad or it’s already gone bad.

Visual:
- two shallow metal bowls with water
- one brown egg per hand
- one sinks / one floats

### Olive oil
Copy:
> Number three, olive oil. Place olive oil in the freezer. If it freezes, it means that the quality is good. If it doesn’t freeze, it means you bought a low-quality olive oil.

Visual solution:
Do not try to show a freezer.
Show two existing oil states:
- one thick/cloudy/semi-solid
- one clear golden liquid

Lesson:
When the spoken copy references an off-screen test, showing the two result states can be more stable than generating the appliance/action.

### Milk
Copy:
> Number four, milk. Add a little bit of alcohol to your milk. If nothing happens, it’s good. If it curdles, you already know.

Validated difficulty:
This was a fragile scene.
Common failures:
- extra glass jar appears
- glass floats
- curdling is weak
- object duplication

Improved prompting:
- exactly two stationary milk glasses
- exactly two small handheld bottles
- bottles remain in hands
- sequential pours
- left stays smooth
- right visibly curdles into white curds + pale whey
- explicit no floating / no new jars / no teleportation

The user ultimately accepted a more-or-less usable generation and moved on.

Lesson:
Do not over-invest in one unstable shot. A usable imperfect result can be better than wasting many generations if the video still reads.

### Honey
Accepted copy:
> Number five, honey. Add honey to a spoon and heat it up. If it turns black, it’s fake. If it caramelizes, it’s real.

Visual:
- one candle
- one metal spoon with honey
- no extra jars

### CTA
The original generic engagement CTA is replaced with GUIDE funnel language.

---

## 5. Cheesecake remodel

See `examples/video-003-cheesecake-remodel/README.md` for the detailed workflow.

Most important new lesson:
A simple action from the reference should remain simple.

The egg hook became successful only after removing the implied edit between:
- crack egg
- drop egg
- whisk

Use one continuous physical chain.

---

## 6. Black-lung demonstration hook

Visual:
- one demonstration lung model with two black lobes + central trachea
- one clear cup of golden/orange liquid
- same outdoor environment

Important failure 1 — environment drift:
The generated animation replaced / altered the outdoor location.

Fix:
- reference image is exact scene
- do not recreate location
- lock ground, rocks, vegetation, table, light, camera position

Important failure 2 — transformation too slow:
The liquid touched the black surface but the clean pink result arrived too late.

Fix:

`LIQUID TOUCHES BLACK = CONTACTED AREA BECOMES PINK IMMEDIATELY`

Require:
- 0.1–0.2 sec conceptual response
- clean trail follows stream
- 90–100% clean by ~7–8 sec in a 10 sec clip
- hold final result for remaining time

---

## 7. Digestive-model tea remodel

See `examples/video-004-digestive-tea-remodel/README.md`.

Most important new lesson:
Objects that should not move must be explicitly defined as static and physically supported.

Successful strainer setup:
- strainer fixed over glass
- glass fixed on table
- nobody touches strainer
- Josh only moves pot
- tea is the only moving content

---

## 8. CTA pattern now standardized

Keyword:
**GUIDE**

Primary line:

> If you want more natural remedies like this, comment GUIDE and I’ll send you the full guide.

Visual:
- direct eye contact
- one subtle downward gesture on GUIDE
- no repeated pointing
- no physical book / ebook / QR code
- existing food/drink can remain in hand or on table

---

## 9. Current production philosophy

The project now favors:

**exact reference logic + Josh adaptation + environmental consistency + minimal physical action per clip**

Over:

**creative reinterpretation + complex multi-action shots + cinematic scene changes**

When in doubt:
1. copy the reference's physical logic closely
2. generate the exact still first
3. animate one thing
4. lock everything else
5. confirm
6. continue
