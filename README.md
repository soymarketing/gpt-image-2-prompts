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

Good example requests:

- `Create a premium product-shot prompt for a luxury skincare bottle`
- `Improve this gpt-image-2 prompt for a SaaS landing page hero`
- `Write a prompt for a clean comparison infographic with perfect text legibility`
- `Make this portrait prompt more editorial but keep the same person`
- `Generate a web design prompt for a fintech dashboard`
- `Fix this image prompt: it looks too generic and cluttered`

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
