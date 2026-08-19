# Language and Voice Routing

## Critical distinction

The language used by the user to talk with the assistant is NOT automatically the language of the generated video.

Keep these separate:

- **Chat / interface language**: the language used to explain steps to the user.
- **Production language**: the language the character speaks in the generated video.
- **Voice accent**: the accent of the recurring voice identity.

## How to choose production language

Priority order:

1. If the user explicitly specifies the video language, use it.
2. If the user asks to replicate reference videos and does not specify a different language, preserve the spoken language of the references by default.
3. If the references use mixed or unclear languages and the user has not specified one, ask one short clarification question.
4. Never infer production language solely from the language of the chat.

Example:

The user speaks Portuguese to the GPT but uploads English UGC references and says “replicate this style.” Unless the user asks to localize to Portuguese, the production language should remain English.

## Style Profile requirement

Every Style Profile should include:

- `PRODUCTION LANGUAGE:`
- `VOICE ACCENT:`

These must remain explicit and independent from the assistant's response language.

## Voice step in Guided Mode

Do not confuse a voice specification with a file the user must upload.

When the user reaches the voice step, first explain the two supported paths:

### Preset voice
If the user chooses an existing Flow voice, they only need to preview voices and select the closest match. No voice-description text needs to be pasted anywhere.

### Custom voice
If the user wants more control, use Flow's **Create New Voice** workflow. Provide a concise **Voice Performance** prompt to paste into Flow's `Voice Performance` field, plus an optional short sample dialogue.

Do not generate a downloadable voice-profile document unless the user asks for one.

## Custom voice prompt requirements

A Voice Performance prompt may describe:

- apparent age
- target language
- accent
- pitch/register
- rasp/breathiness
- cadence
- energy
- warmth
- authority
- sales intensity
- delivery style

It should not contradict the production language detected from the references/user request.

## Reference-language rule

If the reference videos are in English and the user has not requested translation/localization, use an English voice profile, e.g.:

- Language: English (US)
- Accent: neutral General American

Do not switch to Brazilian Portuguese merely because the user is chatting in Portuguese.
