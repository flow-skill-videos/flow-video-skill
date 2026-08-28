# Flow Video Production Skill — v0.4 Patch

This file is an additive patch to `SKILL.md`.

Read it **after** `SKILL.md` and treat the rules below as newer whenever they are more specific.

Version focus:
- U.S.-audience signaling
- Flow safety false-positive recovery
- asset-level vs prompt-level diagnosis
- scene-lock refinement
- hands-only microtake rescue
- validated kiwi + baking-soda remodel workflow

---

## 1. U.S.-audience signaling protocol

When the current project explicitly targets viewers in the United States, use a combination of **linguistic** and **visual** U.S. cues without turning every shot into a flag shot.

Preferred linguistic signals:
- neutral General American speech
- natural U.S.-specific phrasing
- hook or CTA language such as `If you're in the U.S.` or `If you're here in the States...`

Preferred visual signal:
- one authentic U.S. flag placed naturally in the established environment
- secondary to the creator / recipe action
- same physical flag position from shot to shot when visible

Do not:
- create a new flag in every microtake
- move or enlarge the flag between shots
- add multiple flags
- add political signage
- force the flag into tight insert shots where it hurts generation stability

Important:
U.S. cues can strengthen semantic / creative targeting, but they do **not guarantee** geographic distribution by Instagram, TikTok or another platform.

---

## 2. Scene-lock refinement — do not redescribe a successful set

A validated failure mode is that Flow rebuilds the environment when an animation prompt re-describes the set in detail.

When a First Frame already has the correct set, prefer:

`The provided first frame is the ACTUAL physical scene.`

`Treat the first-frame background as a locked photographic plate.`

`Do not recreate or reinterpret the environment.`

Then animate only the current action.

Avoid re-explaining the set as:
- Texas desert
- Southwest landscape
- reddish ground
- dry rocks / plants

inside every animation prompt if the still already shows them correctly.

The more successful the First Frame is, the less the animation prompt should try to redesign it.

---

## 3. Flow safety false-positive escalation protocol

Flow can produce safety errors even when the recurring creator is fictional and the requested action is ordinary.

Two recurring false-positive classes in this project:
1. `famous person / public figure` style detection
2. `risk to reputation / current events` style detection

Do not assume every such error is caused by the wording of the prompt.

The **starting frame, face crop, national symbol, character reference or current Flow session** may be the trigger.

### Step A — simplify wording

First retry:
- remove `same exact identity`
- remove `same exact face`
- remove character biography from animation prompt
- remove celebrity / famous-person wording
- say only `Animate the provided starting frame`
- describe the action, not the identity

### Step B — remove nonessential national symbols from the microtake

If the error changes to or remains a reputation/current-events warning:
- do not mention U.S. politics
- remove visible flag / national symbols from that **specific tight insert** if they are not essential
- keep U.S. signaling in the hook, explanation or CTA instead

### Step C — reduce the visible face

If the frame still fails:
- make the creator smaller in frame
- use 3/4 angle rather than a dominant portrait
- or crop the head / face out completely

For a fragile ingredient insert, prefer:
- torso / hands
- object
- receiving container
- no face

### Step D — hands-only microtake + off-camera voice

Validated rescue pattern:
- tight crop on hands + ingredient + receiving object
- no face
- no flag
- no portrait emphasis
- exact physical action only
- dialogue delivered by an off-camera male voice if the shot still needs spoken copy

Example:
`spoon tilts → white cooking powder falls → same blender → spoon ends empty`

with off-camera line:
`Then add a little baking soda.`

This pattern successfully rescued a repeatedly blocked kiwi-recipe microtake.

### Step E — diagnose asset/session trigger

If a stripped prompt still produces the same safety error, stop endlessly rewriting the same prompt.

Likely causes:
- classifier dislikes the starting image itself
- character reference is being linked too strongly
- session / project state is carrying the classification

Use one of these practical resets:
1. regenerate a tight insert from scratch with no face
2. use a crop that contains only the recipe objects / hands
3. start a fresh Flow project / session and upload only the clean insert
4. do not attach the recurring character reference for that microtake
5. re-enter the main full scene on the next successful shot

Do not claim that any prompt can guarantee bypassing a safety error.

---

## 4. Stop-the-loop rule

When the exact same Flow safety warning survives multiple materially simplified prompts, do **not** keep producing ten near-identical prompt rewrites.

After approximately two meaningful simplifications, change the **asset strategy**, not only the wording.

Preferred escalation:

`identity-light prompt → remove flag → reduce/crop face → hands-only insert → fresh session / new clean still`

If a single ingredient insert remains impossible and the user wants to keep moving, acceptable production fallbacks are:
- merge that spoken line into the next visually stable scene
- use a static insert with subtle motion in CapCut plus voice/TTS
- omit the isolated microtake while preserving recipe continuity in the next still

The goal is completing the video, not winning an endless retry battle with one shot.

---

## 5. Tight-insert continuity rule

A safety-rescue insert does not need to show the full recurring character or every background branding cue.

Continuity can be maintained through:
- same table surface
- same blender / pot / bowl
- same ingredient state
- same lighting direction
- same general camera texture
- matching voice

After the insert succeeds, the next scene can return to the normal wider established setup.

Do not force every continuity element into every 4-second clip.

---

## 6. Ingredient-transfer microtake template

For a fragile ingredient transfer, use the smallest possible state change.

Starting still:
- ingredient already held above receiving container
- no falling material yet
- receiving container already contains all previous ingredients
- no future ingredients visible

Animation:

`HAND / SPOON TILTS → MATERIAL FALLS UNDER GRAVITY → ENTERS SAME RECEIVING CONTAINER → SOURCE OBJECT ENDS EMPTY / PARTLY EMPTY → HAND RETREATS`

Keep:
- one source object
- one receiving object
- one transfer
- one voice line

Do not combine a second recipe action unless already validated.

---

## 7. Finished-drink explanation protocol

For recipe payoff scenes, separating the explanation from drinking improved stability.

Preferred sequence:
1. smoothie / drink finished inside blender or container
2. creator explains while the container stays still
3. next still shows exactly one serving glass
4. creator explains / closes while holding the glass
5. do not drink unless the reference specifically needs a sip

For the serving-glass shot:
- exactly one glass
- same drink color / texture
- glass remains in the same hand
- free hand can make one small explanatory gesture
- no duplicated glass
- no straw unless reference requires it

---

## 8. CTA for U.S.-targeted GUIDE funnel

When the active funnel still uses the keyword `GUIDE` and U.S. targeting is desired, the current preferred CTA is:

> If you're in the U.S. and want more natural recipes like this, comment GUIDE and I'll send you the full guide.

Animation defaults:
- 8 seconds if needed for natural delivery
- direct eye contact
- exactly one stronger gesture on `GUIDE`
- pronounce `GUIDE` clearly
- no written GUIDE text generated in Flow
- no ebook / physical book / QR code
- no drink consumption during the CTA unless explicitly requested

If a U.S. flag already exists in the scene, keep it in its established physical position; do not add another.

---

## 9. Validated Video 005 — Kiwi + baking-soda smoothie remodel

Validated structure:
1. close kiwi + baking-soda visual hook
2. kiwi into blender
3. small baking-soda microtake
4. squeeze half lemon
5. add one glass of water
6. blend until smooth
7. finished green smoothie payoff in blender
8. serving-glass explanation
9. U.S.-targeted GUIDE CTA

Validated hook adaptation:

> Put baking soda on kiwis and watch what happens. If you're in the U.S., you've probably never seen this simple kitchen trick.

This replaced a more provocative pharmacy / Big Pharma line that Flow rejected.

Validated ingredient lines:
- `Grab 2 cups of fresh kiwis.`
- `Then add a little baking soda.`
- `And squeeze in half a lemon.`
- `Add a glass of water.`
- `And blend that whole squad till it's smooth.`

Validated payoff line:

> This juice hits your insides like a reset button nobody told you existed.

Validated CTA:

> If you're in the U.S. and want more natural recipes like this, comment GUIDE and I'll send you the full guide.

### Most important production lesson from Video 005

The baking-soda ingredient shot repeatedly triggered Flow safety warnings even after prompt simplification.

The working direction was to stop emphasizing the creator and convert the shot into a simple object-focused insert:
- tight recipe framing
- no dominant face
- no unnecessary flag
- spoon + powder + blender
- off-camera voice if needed
- exact one-action transfer

After that insert, the project returned to normal wider creator shots successfully.

---

## 10. Updated decision hierarchy

When generating a new clip, prioritize in this order:

1. preserve the reference's physical logic
2. preserve the exact successful First Frame
3. animate only one primary action
4. preserve object counts / current recipe state
5. preserve voice continuity
6. preserve creator identity only as strongly as needed
7. preserve U.S. cues when they do not destabilize the shot
8. if Flow safety repeatedly blocks, simplify the asset rather than endlessly expanding the prompt

A stable 4-second insert that preserves the story is better than a visually richer shot that never generates.