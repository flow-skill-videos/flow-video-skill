# Recent Validated Patterns — Josh Outdoor Series

This document records production patterns validated after the earlier Pep Tonic baseline. It is project history and a practical reference for new chats.

Use `SKILL.md` for reusable rules, `SKILL_PATCH_0_4.md` for the newest Flow safety / U.S.-targeting rules, and `PROJECT_PROFILE.md` for the canonical current setup.

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

Current U.S.-targeted line:

> If you're in the U.S. and want more natural recipes like this, comment GUIDE and I'll send you the full guide.

Visual:
- direct eye contact
- one subtle emphasis gesture on GUIDE
- no repeated pointing
- no physical book / ebook / QR code
- existing food/drink can remain in hand or on table
- if an existing U.S. flag is visible, keep it in the same physical position

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

---

## 10. Kiwi + baking-soda smoothie remodel

This production validated a new combination of U.S.-audience signaling, strict scene lock and Flow safety recovery.

See `examples/video-005-kiwi-baking-soda-remodel/README.md`.

### Sequence
- kiwi halves + baking-soda hook
- kiwi into blender
- baking-soda microtake
- squeeze half lemon
- add one glass of water
- blend until smooth
- finished smoothie payoff in blender
- finished smoothie in one clear serving glass
- explanation / benefit shot
- U.S.-targeted GUIDE CTA

### Hook adaptation

A more provocative pharmacy / Big Pharma line repeatedly caused Flow safety trouble.

Validated replacement:

> Put baking soda on kiwis and watch what happens. If you're in the U.S., you've probably never seen this simple kitchen trick.

This preserved an aggressive curiosity hook while avoiding the blocked framing.

### Stronger scene-lock lesson

When the successful First Frame already contained the exact outdoor set, animation became more stable after removing repeated environment descriptions.

Use:
- first frame = actual physical set
- locked photographic plate
- animate only the requested movement

Do not repeatedly re-prompt `Texas / Southwest / reddish earth` if the image already contains the correct set.

### Baking-soda microtake — important safety recovery

The baking-soda-to-blender shot repeatedly produced safety warnings even after identity-heavy wording had been removed.

The warning shifted beyond the older famous-person false positive and included reputation/current-events style blocking.

Important diagnosis:
The prompt itself was no longer the only likely trigger. The starting asset / face / flag / session state could be involved.

Validated rescue direction:
- tight recipe insert
- creator face not dominant / cropped out
- no unnecessary U.S. flag in that microtake
- one spoon
- one small amount of white cooking powder
- same blender
- one action only
- off-camera male voice allowed

Physical chain:

`SPOON TILTS → POWDER FALLS → SAME BLENDER → SPOON ENDS EMPTY → HAND RETREATS`

Validated spoken line:

> Then add a little baking soda.

After the rescue insert succeeded, later scenes returned to the wider established creator environment normally.

### Stop-the-loop lesson

When the same safety warning survives multiple materially different simplified prompts, stop cycling wording.

Change the asset strategy:
1. strip identity-heavy prompt language
2. remove nonessential flag / national symbol from the insert
3. reduce or crop face
4. use hands + object only
5. use off-camera voice
6. if necessary, start a fresh Flow project / session with a clean insert image

The goal is a stable clip, not endless retries of one shot.

### Water / lemon / blender continuity

The following micro-actions worked cleanly as isolated steps:
- half lemon held above blender → squeeze into same blender
- one clear glass full of water → one continuous pour → glass ends mostly empty
- blender lid already on → one control activation → chunks gradually become a smooth green drink

### Finished-drink payoff

A stable serving sequence was:
1. finished green smoothie remains inside blender while creator explains
2. next still presents exactly one clear glass of smoothie
3. creator holds the glass at chest level while speaking
4. no sip required
5. free hand can make one small explanatory gesture

This reduces glass duplication and avoids unnecessary object interaction.

### U.S. CTA

Validated final CTA:

> If you're in the U.S. and want more natural recipes like this, comment GUIDE and I'll send you the full guide.

Useful defaults:
- 8 sec
- General American accent
- exact word `GUIDE` pronounced clearly
- one stronger gesture on GUIDE
- no written GUIDE text
- no physical ebook / book / QR code
- smoothie stays in the same hand
- no drinking during the CTA

---

## 11. New hierarchy after Video 005

For difficult Flow shots, prioritize:

1. exact reference logic
2. exact successful First Frame
3. one primary action
4. object count and state continuity
5. voice continuity
6. creator identity only as strongly as needed
7. U.S. visual cues only when they do not destabilize generation
8. asset-level recovery when safety warnings persist

A simple insert that generates and preserves continuity is better than a richer shot that repeatedly fails.