# Prompt Patterns for `gpt-image-2`

Use these templates when generating prompts for ChatGPT Images 2.0 / `gpt-image-2`.

## 1. New image from scratch

Best for: product shots, ad creatives, editorial scenes, landing page heroes, social covers.

Template:

```text
Create a [type of image] for [use case].
Scene/background: [environment]
Main subject: [what must be shown]
Key details: [materials, colors, textures, props]
Composition: [framing, angle, placement, negative space]
Lighting/mood: [soft daylight, studio light, cinematic dusk, etc.]
Style: [photorealistic / editorial / 3D / illustration / infographic]
Constraints: [no watermark, no extra text, no logo, no clutter]
```

## 2. Photorealistic image

Use when realism matters more than style.

Rules:
- Say `photorealistic` explicitly.
- Describe materials, scale, and lighting.
- Use camera language for framing and mood, not fake over-technical camera specs unless they help the look.

Additions that usually help:
- `natural materials`
- `soft realistic shadows`
- `accurate reflections`
- `premium editorial feel`
- `shallow depth of field` or `everything in focus`, whichever fits

## 3. Text-in-image / poster / ad / infographic

Best for: posters, menus, labels, slides, comparison graphics, explainer visuals.

Template:

```text
Create a [poster / infographic / ad / package front / slide] for [use case].
Layout: [portrait, square, horizontal, centered, split layout, top-to-bottom hierarchy]
Main visual: [core image or illustration]
Text to include: "[EXACT TEXT]"
Typography: [bold sans-serif, elegant serif, condensed uppercase, etc.]
Text placement: [top center, bottom-left, right column, etc.]
Color system: [palette]
Style: [clean, premium, modern, technical, playful]
Constraints: no extra text, keep typography perfectly legible, high contrast, no watermark
```

Rules:
- Put important text in quotes.
- For brand names or tricky words, spell them carefully.
- Say `no extra text` whenever stray text would be a problem.

## 4. Edit an existing image

Best for: background swaps, cleanup, relighting, object removal, packaging changes, localized edits.

Template:

```text
Change only [specific element].
Keep the [identity / product / composition / camera angle / proportions / layout / label / colors] exactly the same.
New requirement: [what should change]
Do not alter [important invariants].
```

Useful preserve list:
- identity
- pose
- clothing
- packaging details
- camera angle
- composition
- brand colors
- label text
- surrounding objects
- lighting direction

## 5. Character or object consistency

Best for: campaigns, multi-image series, mascots, product catalogs.

Template:

```text
Create a new image of the same [character / product / object] with these invariant details:
- [trait 1]
- [trait 2]
- [trait 3]
Show it in [new scene or action].
Keep the same visual identity, proportions, and recognizable details.
Style: [same style as prior image / same brand look / same lighting family]
```

Rules:
- Name the invariants as bullets.
- Re-state what must remain recognizable.
- Only add new variables after invariants are locked.

## 6. Layout-sensitive commercial creative

Best for: landing page hero, ecommerce banner, Meta ad, email header.

Include:
- aspect ratio or orientation
- safe empty space for copy
- subject position
- visual hierarchy
- CTA area if relevant

Helpful phrasing:
- `subject slightly right of center with negative space on the left for headline text`
- `clean composition with room for UI overlay`
- `keep the center visually quiet for copy placement`

## 7. Troubleshooting weak outputs

If the output is wrong, change the smallest thing necessary.

Common fixes:

### Too generic
Add:
- materials
- environment
- intended use
- clearer style language
- composition instructions

### Bad text
Add:
- exact text in quotes
- typography details
- placement
- `no extra text`
- request higher visual clarity / cleaner layout

### Too cluttered
Add:
- `minimal background`
- `only essential props`
- `clean composition`
- `no clutter`

### Wrong vibe
Add:
- emotional and commercial framing: `premium`, `editorial`, `playful`, `technical`, `luxury wellness`, `startup landing page`, etc.

### Drift during edit
Repeat:
- `change only X`
- `keep everything else the same`
- specific preserve list

## 8. Iteration style

Prefer short follow-ups such as:

```text
Make it warmer and more premium.
Remove the extra object on the right.
Keep the composition but make the text more legible.
Change only the background to a clean white studio.
Preserve the product exactly; improve reflections and realism.
```

## 9. Recommended default deliverables

When the user is vague, provide:
- one main prompt
- one cleaner/safer variant
- one punchier/premium variant
- three short revision prompts
