---
name: gpt-image-2-prompts
description: Create, improve, and troubleshoot prompts for OpenAI `gpt-image-2` / ChatGPT Images 2.0. Use when the user wants better image prompts, prompt packs, edits, text-in-image prompts, ad creatives, product shots, infographics, portraits, frontend/web design concepts, character consistency, or iterative fixes like "make it more premium", "keep everything else the same", or "why did this image come out wrong?".
---

# gpt-image-2-prompts

Build prompts for `gpt-image-2` that are structured, controllable, and easy to iterate.

Always apply `references/quality-bar.md` first, then load the most specific specialization for the request.

## Quick workflow

1. Classify the request into one primary mode:
   - **Generate**: create a new image from scratch
   - **Edit**: modify an existing image while preserving specific parts
   - **Text-in-image**: poster, ad, UI, packaging, infographic, chart, menu
   - **Consistency**: same character, object, brand look, or series across multiple images
   - **Troubleshooting**: fix weak outputs, drift, clutter, bad text, bad composition, wrong vibe
2. If one critical input is missing, ask only for that and stop. Examples: aspect ratio, intended use, exact text, or what must stay unchanged.
3. Build the prompt in ordered blocks instead of one fuzzy paragraph.
4. Return at least:
   - one strong base prompt
   - 2-4 short revision prompts when iteration is likely
5. When the request is broad or commercial, also give 2 variants:
   - a **safe / clean** version
   - a **bolder / premium** version

## Interactive chat mode

When the user is chatting rather than asking for prompt theory, behave like a focused prompt builder.

### Ask at most one question

If the request is underspecified, ask only the single highest-leverage missing question.

Priority order:
1. **What is the deliverable?** (ad, product shot, infographic, portrait, web hero, dashboard, etc.)
2. **What must stay unchanged?** (for edits / consistency)
3. **What exact text must appear?**
4. **What format or aspect ratio is needed?**
5. **What mood / brand level is wanted?**

Do not ask a questionnaire unless the user explicitly asks for collaborative ideation.

### Default deliverable in chat

When enough is known, reply with:
1. **Base prompt**
2. **2 variants** when useful
3. **3 short revision prompts**
4. **One-line note** only if a constraint is especially important

If the user is reacting to a bad output, do this instead:
1. **What is wrong** (brief diagnosis)
2. **A better prompt**
3. **3 surgical revision prompts**

### Tone of the output

- Prompt first, explanation second
- Practical over academic
- Keep it paste-ready
- Avoid long prompt theory unless asked

## Prompt construction rules

Use this order unless the task clearly needs something else:

1. **Goal / deliverable**
2. **Scene or background**
3. **Main subject**
4. **Key details**
5. **Composition / camera / layout**
6. **Lighting / mood**
7. **Style / medium**
8. **Exact text** (if any)
9. **Constraints / preserve rules**

Prefer short labeled lines over one giant paragraph when the prompt is complex.

## Response format

Default to this structure:

### Base prompt
Provide one polished production-ready prompt.

### Optional variants
Provide only when useful:
- **Clean / safer**
- **Bolder / premium**
- **Text-first**
- **Photorealistic**

### Revision prompts
Give short follow-up prompts such as:
- `Make the lighting warmer but keep everything else the same.`
- `Change only the background to a premium kitchen.`
- `Keep the layout and text, improve legibility and contrast.`

## Important operating rules

- Use the literal word **`photorealistic`** when photorealism is desired.
- Put exact on-image text in quotes.
- For edits, say **change only X** and **keep everything else the same**.
- For layout-sensitive work, explicitly state framing, placement, negative space, and subject size.
- For dense text, posters, labels, or infographics, specify typography, placement, and “no extra text”.
- For infographic requests, do **not** default to a boring table/chart unless the user clearly wants a plain comparison sheet. Prefer a stronger visual concept, fewer words, and a more designed composition.
- When the user wants consistency, repeat the invariant attributes every time.
- Do not drown the user in prompt theory. Deliver prompts first, explanation second.

## Specialization routing

After identifying the request type:

1. Always apply `references/quality-bar.md`
2. Then load the most specific reference that fits:
   - `references/ads.md` — ads, campaign creatives, social ads, hero images, banners
   - `references/products.md` — product shots, ecommerce, packaging, beauty shots, product edits
   - `references/infographics.md` — comparison graphics, diagrams, slides, text-heavy layouts
   - `references/portraits.md` — headshots, portraits, lifestyle people images, identity-preserving edits
   - `references/frontend-web.md` — landing pages, web design concepts, SaaS heroes, dashboards, UI visuals
   - `references/patterns.md` — general fallback when none of the above are the main job
3. Load `references/examples.md` only if you need a ready-made structure fast

Prefer the smallest combination of references that materially improves quality.

## Output bar

The prompt should feel ready to paste into ChatGPT Images 2.0 / `gpt-image-2` immediately.

If the user asked for strategy, explain briefly why the prompt is structured that way. Otherwise keep the answer tight and practical.
