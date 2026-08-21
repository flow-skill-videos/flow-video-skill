# Reference Video Analysis Framework

Analyze uploaded reference videos before writing prompts.

## Extract structural DNA

### Persona
- apparent age
- gender presentation
- body type
- wardrobe
- authority level
- energy
- facial behavior
- eye contact

### Hook
- verbal, visual or both
- what happens in first 1–2 seconds
- curiosity device
- unusual object or action
- whether the hook is merely relevant or deliberately bizarre/contradictory
- what specifically creates the immediate "what is that?" reaction
- whether the hook has a clean semantic bridge into the topic

### Foreground / visual hierarchy
- which object is closest to camera
- how much of the frame the hook prop occupies
- whether perspective makes the object look oversized
- face vs prop priority
- how the visual hierarchy changes after the hook

### Camera
- creator-camera vs cinematic
- distance
- framing
- apparent focal length
- static vs handheld
- zoom/push-in behavior
- lateral drift
- tilt toward hand/product actions
- whether the camera follows the physical demonstration
- whether framing changes meaningfully between scenes

### Lighting / location
- indoor vs outdoor
- daylight intensity
- contrast
- whether bright exterior light contributes to creator energy
- whether environment is part of the style or merely incidental

### Pacing
- average scene length
- number of visual blocks
- frequency of cuts
- whether motion comes from editing, physical action or camera choreography

### Props and demonstrations
- objects used to visualize an abstract concept
- pouring/stirring/pointing/holding
- whether props act as scroll-stoppers
- whether a strange prop stays visible for continuity after the hook
- when the hook prop loses prominence
- whether repeated props need strict shape/size/texture locking

### Voice
- age impression
- production language
- accent
- pitch
- cadence
- warmth
- rasp/breathiness
- sales intensity

Important: production language is independent from the language used to chat with the user.

### Product integration
- first appearance timing
- whether product is held, placed, demonstrated or only mentioned
- how aggressively the product is presented
- whether the camera follows the reveal/demo action
- object-count risks such as duplicate containers, scoops or glasses

### CTA
- soft recommendation
- curiosity
- direct command
- urgency
- camera distance at CTA
- whether a subtle final push-in is used

### Captions
- bold uppercase
- editorial mixed-serif
- word-by-word
- phrase-based
- placement and density

### Generation failure patterns
Check whether the reference-inspired wording could accidentally cause:
- smartphone/device mockup
- phone bezel or notch
- app UI
- screen-within-a-screen
- duplicated products or props
- inconsistent hook prop
- static camera when the reference is dynamic

If using smartphone/creator-camera language, explicitly require full-frame exported footage and prohibit device overlays.

## Separate structure from incidental details

Preserve the production logic, not a specific creator's identity.

Examples of structural DNA:
- bizarre but semantically bridgeable visual hook
- dominant foreground object
- bright outdoor creator lighting
- close slightly wide-angle perspective
- camera following hand/product action
- prop continuity through the explanation
- late product reveal

Examples of incidental details:
- exact creator face
- exact backyard
- exact strange prop
- exact wardrobe choice
- exact object color

Turn findings into a reusable STYLE PROFILE.
