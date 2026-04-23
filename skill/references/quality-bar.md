# Quality Bar and Failure Diagnosis

Apply this reference across **all** specializations. This is the difference between a prompt that is merely correct and a prompt that produces work with taste.

## Core principle

Do not optimize only for completeness. Optimize for **clarity + taste + controllability**.

A bad prompt often has all the requested ingredients but still produces a weak image because it lacks:
- a visual idea
- hierarchy
- restraint
- good tradeoffs
- iteration strategy

## What “great” looks like

A strong prompt usually creates output that feels:
- intentional
- well-composed
- specific without being bloated
- visually confident
- easy to refine in one or two follow-ups

## Universal anti-patterns

Avoid prompts that push toward:
- bland template aesthetics
- “spreadsheet” compositions when a designed poster/explainer is better
- too much on-image text
- decorative clutter
- generic startup gradient soup
- fake-premium buzzwords without composition control
- overstuffed prompts that try to solve everything at once
- excessive micro-details that reduce flexibility but do not improve the image

## Good default behavior

Unless the user explicitly wants something plain, technical, or dense:
- prefer fewer words on the image
- prefer one strong visual concept
- prefer stronger hierarchy over more elements
- prefer a memorable hero area over evenly weighted blocks everywhere
- prefer elegant restraint over “more stuff”

## Taste ladder

Use one of these internal targets when shaping the prompt:

### 1. Safe / production
Use when the user needs reliability, clarity, ecommerce utility, or business polish.

Keywords:
- clean
- premium
- controlled
- presentation-ready
- high legibility
- minimal clutter

### 2. Designed / editorial
Use when the user wants something visually strong, premium, modern, or concept-led.

Keywords:
- editorial
- art-directed
- elegant hierarchy
- stronger focal contrast
- premium composition
- restrained but striking

### 3. Bold / campaign
Use when the user wants impact, novelty, drama, or scroll-stopping visuals.

Keywords:
- campaign energy
- bold contrast
- cinematic mood
- stronger shape language
- memorable silhouette
- high visual tension

## Failure diagnosis

When the user shows a bad output or says “this sucks,” diagnose the failure first.

Classify the output into one or more buckets:

### Bland / template-like
Symptoms:
- feels generic
- no strong focal idea
- could be from any AI tool
- overbalanced, no tension

Fix:
- add a stronger concept or hero contrast
- reduce the number of equally weighted elements
- add clearer style direction
- ask for a more editorial or art-directed composition

### Too literal / over-explained
Symptoms:
- every label is present but the image is dead
- looks like a checklist
- too many text blocks

Fix:
- reduce copy
- keep only the most important text
- shift from table to poster/explainer visual system
- say `no spreadsheet look`

### Too cluttered
Symptoms:
- too many cards, icons, lines, props, or decorations
- weak whitespace
- poor scanability

Fix:
- reduce component count
- define one hero area
- add `minimal visual noise`
- ask for stronger spacing and clearer hierarchy

### Pretty but not useful
Symptoms:
- stylish but unclear
- decorative, not communicative
- weak CTA or weak information hierarchy

Fix:
- restate the communication goal
- define the main takeaway
- strengthen section order and focal point

### Weak premium feel
Symptoms:
- looks cheap, generic, or synthetic
- awkward gradients or stock-style gloss

Fix:
- use more restrained palette language
- ask for editorial taste, elegant spacing, and refined materials
- reduce gimmicks

## Revision strategy

Do not rewrite everything unless necessary.

Prefer this sequence:
1. identify the main failure
2. change the smallest high-leverage thing
3. preserve what already works
4. offer 2-3 focused revision prompts

Good revision prompts are short and surgical:
- `Keep the structure, make it feel more editorial and less template-like.`
- `Reduce the text and make the composition more concept-led.`
- `Preserve the subject, but create a stronger focal hierarchy.`
- `Keep everything else the same, remove clutter and improve spacing.`

## What to return by default

When the user wants a prompt, prefer returning:
1. **Base prompt**
2. **Clean / safer variant**
3. **Bolder / more designed variant**
4. **3 revision prompts**

When the user shows a failed output, prefer returning:
1. **What is wrong** (1-3 bullets)
2. **A better prompt**
3. **3 surgical revision prompts**

## One-question rule

If the brief is missing something, ask only the highest-leverage question.

The best missing questions are usually:
- what kind of deliverable is this really?
- should this feel safe, editorial, or bold?
- what must remain unchanged?
- how much text truly needs to be on the image?

Do not ask broad discovery questionnaires unless the user explicitly wants collaborative ideation.
