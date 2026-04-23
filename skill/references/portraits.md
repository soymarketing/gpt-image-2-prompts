# Portraits

Use this reference when the user wants portraits, headshots, editorial people images, lifestyle portraits, stylized character portraits, or consistent people across a series.

## What matters most

Prioritize:
- flattering composition
- believable pose and gaze
- skin / fabric / hair realism
- identity preservation for edits
- clear mood direction
- anatomy and hand quality

## Prompt structure for portraits

```text
Create a [portrait type] of [subject].
Setting/background: [studio / office / street / home / seamless backdrop]
Subject details: [age range, styling, clothing, features, vibe]
Pose/expression: [looking at camera, candid, half-smile, seated, walking]
Composition: [headshot, half-body, full-body, close-up, eye-level]
Lighting/mood: [soft window light, studio key light, golden hour, moody cinematic]
Style: [photorealistic, editorial portrait, fashion portrait, natural lifestyle]
Constraints: no extra people, natural anatomy, realistic hands, no watermark
```

## Good language for portraits

Use phrases like:
- `photorealistic portrait`
- `editorial portrait photography`
- `natural skin texture`
- `authentic expression`
- `clean background`
- `soft flattering light`
- `realistic fabric texture`
- `hands visible and anatomically correct`

## Common portrait patterns

### 1. Professional headshot

```text
Create a photorealistic professional headshot of a confident startup founder.
Setting/background: soft neutral studio backdrop.
Subject details: modern smart-casual wardrobe, clean grooming, approachable but sharp.
Pose/expression: looking at the camera with a subtle confident smile.
Composition: shoulders-up portrait, eye-level, centered.
Lighting/mood: soft flattering studio light with gentle shadow definition.
Style: premium editorial business portrait.
Constraints: no extra people, natural skin texture, realistic hair, no watermark.
```

### 2. Lifestyle portrait

```text
Create a photorealistic lifestyle portrait of a young chef in a modern kitchen.
Setting/background: bright contemporary kitchen with shallow background detail.
Subject details: white apron, relaxed confidence, slightly flour-dusted hands.
Pose/expression: candid three-quarter pose, looking down at the counter with a natural smile.
Composition: half-body portrait, eye-level.
Lighting/mood: warm natural daylight, authentic and cinematic.
Style: editorial lifestyle photography.
Constraints: no extra people, natural anatomy, realistic hands, no clutter.
```

### 3. Portrait edit

```text
Change only the background to a dark editorial studio backdrop.
Keep the person's face, hairstyle, clothing, pose, camera angle, skin tone, and expression exactly the same.
Do not alter facial identity or add extra accessories.
```

## Consistency for the same person

If the user wants the same person across images, repeat invariants:
- facial structure
- hair style and color
- clothing category
- age range
- expression family
- visual style

Use phrasing like:

```text
Keep the same person's identity, facial proportions, hairstyle, and overall recognizable appearance across all images.
```

## Revision prompts for portrait work

- `Keep the person the same, make the lighting softer and more flattering.`
- `Preserve identity, change only the wardrobe to a dark blazer.`
- `Keep the portrait composition, make it more editorial and premium.`
- `Do not change the face; improve realism in skin and hair texture.`
- `Make the portrait warmer and more approachable without changing identity.`

## Failure fixes

### Face drift
Add:
- `preserve identity`
- exact preserve list
- `change only X`

### Awkward pose or hands
Add:
- stronger pose description
- explicit hand behavior
- better framing

### Too artificial
Add:
- natural skin texture
- authentic expression
- subtle imperfections
- realistic fabric and lighting
