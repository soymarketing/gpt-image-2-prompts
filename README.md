# gpt-image-2-prompts

A reusable AgentSkill for creating, improving, and troubleshooting prompts for OpenAI `gpt-image-2` / ChatGPT Images 2.0.

It is built for practical prompt work in chat, not prompt theory. The skill is designed to:

- ask for at most one critical missing input
- return a paste-ready **base prompt**
- add **variants** when useful
- suggest **short revision prompts** for iteration
- route to specialized playbooks for common visual tasks

## What it covers

Specialized prompt playbooks are included for:

- ads / campaign creatives
- product shots / ecommerce / packaging
- infographics / diagrams / text-heavy visuals
- portraits / identity-preserving edits
- frontend design / web design / SaaS heroes / dashboards
- general fallback patterns and example prompts

## Repository structure

```text
.
├── README.md
├── dist/
│   └── gpt-image-2-prompts.skill
└── skill/
    ├── SKILL.md
    └── references/
```

## Installation

### Option 1: Manual install from source

Copy the `skill/` directory contents into a skills directory on your machine using the folder name `gpt-image-2-prompts`.

Examples of common skill locations:

- `~/clawd/skills/gpt-image-2-prompts`
- `~/.agents/skills/gpt-image-2-prompts`
- `~/.codex/skills/gpt-image-2-prompts`
- another skills directory used by your agent runtime

Example:

```bash
git clone https://github.com/soymarketing/gpt-image-2-prompts.git
mkdir -p ~/clawd/skills/gpt-image-2-prompts
cp -R gpt-image-2-prompts/skill/* ~/clawd/skills/gpt-image-2-prompts/
```

### Option 2: Use the packaged artifact

This repository also includes a packaged artifact:

- `dist/gpt-image-2-prompts.skill`

If your workflow prefers packaged skills, download the release asset or use the file in `dist/`.

## How to use

Trigger the skill when you want a better prompt for `gpt-image-2` / ChatGPT Images 2.0.

The most natural way to use it is to ask for the image outcome you want, not to talk like a skill author.

More natural example requests:

- `Hazme un prompt para una foto de producto premium de un serum de lujo.`
- `Mejora este prompt para que la landing de mi SaaS se vea más premium.`
- `Quiero una infografía comparativa clara, elegante y con texto súper legible.`
- `Quiero mantener la misma persona pero con look más editorial.`
- `Necesito una imagen estilo dashboard fintech moderno.`
- `Este prompt me está saliendo muy genérico y saturado, ayúdame a arreglarlo.`

The same idea in English:

- `Make me a prompt for a premium skincare product shot.`
- `Improve this prompt so my SaaS landing page looks more premium.`
- `I need a clean comparison infographic with very legible text.`
- `Keep the same person, but make the portrait feel more editorial.`
- `I want a modern fintech dashboard visual.`
- `This prompt keeps coming out generic and cluttered. Help me fix it.`

### Specialization examples

The skill includes specialized playbooks. You do not need to name them explicitly, but these examples show the kinds of requests each one is meant to handle.

#### Ads / campaign creatives

- `Hazme un prompt para un anuncio premium de café con espacio para copy.`
- `Quiero una imagen hero para campaña de Meta Ads de una marca de skincare.`
- `Make this ad visual feel more expensive and conversion-focused.`

#### Products / ecommerce / packaging

- `Necesito una foto de producto limpia para ecommerce con fondo blanco.`
- `Hazme un prompt para un beauty shot de un perfume de lujo.`
- `Edita esta imagen: cambia solo el fondo y deja intacto el empaque.`

#### Infographics / diagrams / text-heavy visuals

- `Quiero una infografía comparativa de dos herramientas con texto muy claro.`
- `Hazme un prompt para un diagrama de 4 pasos con estilo editorial.`
- `I need a slide-ready visual with crisp labels and no extra text.`

#### Portraits / identity-preserving edits

- `Hazme un retrato profesional estilo editorial para LinkedIn.`
- `Quiero la misma persona pero con un fondo más premium y oscuro.`
- `Keep the same face and expression, just make the portrait warmer and more flattering.`

#### Frontend / web design / SaaS heroes / dashboards

- `Hazme un prompt para una landing SaaS premium.`
- `Quiero un dashboard fintech moderno, limpio y fácil de escanear.`
- `Make this homepage concept feel less template-like and more premium.`

### What the skill returns

When enough context is present, the skill aims to return:

1. **Base prompt**
2. **2 variants** when useful
3. **3 revision prompts** for iteration
4. a brief note only when a key constraint matters

### If the request is underspecified

The skill should ask only one high-leverage question, usually one of:

- What is the deliverable?
- What must stay unchanged?
- What exact text must appear?
- What format or aspect ratio is needed?
- What mood or brand level is wanted?

## Included references

- `references/ads.md`
- `references/products.md`
- `references/infographics.md`
- `references/portraits.md`
- `references/frontend-web.md`
- `references/patterns.md`
- `references/examples.md`

## Publishing / packaging

The packaged `.skill` artifact in `dist/` was produced by validating and packaging the source skill.

If you want to rebuild it yourself, use the OpenClaw `package_skill.py` flow against the `skill/` directory contents arranged as a normal skill folder.

## Privacy note

This repository is intended to contain only generic reusable skill content.
No user-specific secrets, tokens, local absolute paths, or personal data should be included.
