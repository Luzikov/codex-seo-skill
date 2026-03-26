<p align="center">
  <img src="./assets/readme-banner.svg" alt="Codex SEO banner" width="100%">
</p>

# Codex SEO - SEO Audit Skill for Codex

Comprehensive SEO skill for Codex. Covers full site audits, single-page reviews, technical SEO, content quality, Schema.org, image SEO, AI search readiness, local SEO, and pre-launch source-code SEO reviews for frameworks like Next.js.

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-0ea5e9)](https://github.com/Luzikov/codex-seo-skill)
[![SEO](https://img.shields.io/badge/SEO-Full%20Audit-22c55e)](https://github.com/Luzikov/codex-seo-skill)
[![License: MIT](https://img.shields.io/badge/License-MIT-f5c542.svg)](./LICENSE)

## Table of Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Prompt Examples](#prompt-examples)
- [What It Covers](#what-it-covers)
- [Why This Skill Is Useful](#why-this-skill-is-useful)
- [Architecture](#architecture)
- [Repository Layout](#repository-layout)
- [Documentation](#documentation)
- [Requirements](#requirements)
- [Uninstall](#uninstall)
- [License](#license)

## Installation

### Recommended Install (Unix/macOS/Linux)

Clone directly into the Codex skills directory:

```bash
git clone --depth 1 https://github.com/Luzikov/codex-seo-skill.git ~/.codex/skills/seo
```

### Windows (PowerShell)

```powershell
git clone --depth 1 https://github.com/Luzikov/codex-seo-skill.git "$env:USERPROFILE\.codex\skills\seo"
```

### Update Existing Install

Unix/macOS/Linux:

```bash
git -C ~/.codex/skills/seo pull
```

Windows (PowerShell):

```powershell
git -C "$env:USERPROFILE\.codex\skills\seo" pull
```

> Why clone into `~/.codex/skills/seo`? Because Codex discovers local skills from the skills directory, and this repository is already structured as the skill folder itself.

## Quick Start

Start Codex and invoke the skill with `$seo`:

```text
Use $seo to audit https://example.com and return a simple fix plan.
```

This repository is built for Codex usage, so the main interaction style is:

- explicit skill invocation with `$seo`;
- natural-language SEO requests that match the skill description.

## Prompt Examples

### Live Website Review

```text
Use $seo to run a full SEO audit for https://example.com.
```

### Single Page Review

```text
Use $seo to review the SEO of https://example.com/pricing.
```

### Technical SEO Review

```text
Use $seo to check robots.txt, sitemap.xml, canonicals, redirects, and indexing issues on https://example.com.
```

### Schema Review

```text
Use $seo to validate schema markup on https://example.com and show what is missing.
```

### AI Search Readiness

```text
Use $seo to review whether https://example.com is ready for AI search and llms.txt guidance.
```

### Local SEO Review

```text
Use $seo to review local SEO for this clinic website and tell me what to fix first.
```

### Codebase SEO Review

```text
Use $seo to review my Next.js codebase for SEO issues before launch.
```

### SEO Strategy Planning

```text
Use $seo to create an SEO plan for a SaaS company.
```

## What It Covers

### Full Audits

- representative website audits with prioritized fixes;
- homepage, money-page, content-page, robots, and sitemap review flow;
- practical output focused on what to fix first.

### Single-Page Reviews

- `title`, `meta description`, `H1-H3`, URL quality;
- canonical and robots directives;
- content usefulness and trust signals;
- image and schema checks.

### Technical SEO

- crawlability and indexability;
- canonicals, redirects, duplicate URLs, noindex logic;
- HTTPS and basic technical hygiene;
- speed hints using current metrics: `LCP`, `INP`, `CLS`.

### Content Quality

- intent match;
- proof and first-hand experience;
- author visibility and trust;
- weak, generic, or mass-generated copy detection.

### Schema.org

- `JSON-LD`-first recommendations;
- type validation;
- required-field review;
- outdated markup guardrails.

### Image SEO

- alt text quality;
- sizing and layout-shift prevention;
- file-size and format review;
- social-preview image awareness.

### AI Search Readiness

- `GPTBot`, `OAI-SearchBot`, `ChatGPT-User`, `ClaudeBot`, `PerplexityBot`;
- `/llms.txt` guidance;
- answer-block and citation readiness;
- structure and visibility for AI systems.

### Local SEO

- location page quality checks;
- local trust signals;
- `LocalBusiness` schema guidance;
- safeguards against doorway-style page sprawl.

### Source-Code SEO Review

- Next.js and similar framework review before launch;
- metadata, sitemap, robots, canonicals, schema, and rendering checks;
- code-level SEO mistakes that often slip through before deployment.

### SEO Strategy Templates

Included templates for:

- SaaS
- local business
- ecommerce
- publisher
- agency
- general business

## Why This Skill Is Useful

This skill is built to give Codex a complete SEO operating manual instead of a few disconnected prompts.

What makes it strong:

- current Core Web Vitals logic with `INP`, not outdated `FID`;
- practical schema guardrails;
- AI search readiness checks;
- local SEO safety thresholds;
- pre-launch codebase SEO review support;
- business-type planning templates;
- default output that stays short, clear, and fix-focused.

## Architecture

This repository keeps a single primary Codex skill and loads detailed reference material only when needed.

That is intentional:

- one main trigger makes Codex invocation simpler;
- reference files keep the main skill lean;
- templates live separately so strategy generation stays reusable.

## Repository Layout

```text
.
|-- SKILL.md                     # Main skill instructions and workflow
|-- README.md                    # Repository landing page
|-- agents/
|   `-- openai.yaml              # UI metadata for Codex
|-- references/
|   |-- core-web-vitals.md       # Current performance metrics and rules
|   |-- eeat.md                  # Content quality and trust review guide
|   |-- geo-ai-search.md         # AI search readiness checks
|   |-- local-seo.md             # Local SEO review guidance
|   |-- quality-gates.md         # Thin-content and scale guardrails
|   |-- schema-types.md          # Schema recommendations and restrictions
|   `-- source-code-seo.md       # Codebase SEO review workflow
|-- assets/
|   |-- saas-plan.md
|   |-- local-service-plan.md
|   |-- ecommerce-plan.md
|   |-- publisher-plan.md
|   |-- agency-plan.md
|   |-- generic-plan.md
|   `-- readme-banner.svg
`-- LICENSE
```

## Documentation

Core files:

- [SKILL.md](./SKILL.md)
- [agents/openai.yaml](./agents/openai.yaml)

Reference files:

- [references/core-web-vitals.md](./references/core-web-vitals.md)
- [references/eeat.md](./references/eeat.md)
- [references/geo-ai-search.md](./references/geo-ai-search.md)
- [references/local-seo.md](./references/local-seo.md)
- [references/quality-gates.md](./references/quality-gates.md)
- [references/schema-types.md](./references/schema-types.md)
- [references/source-code-seo.md](./references/source-code-seo.md)

Planning templates:

- [assets/saas-plan.md](./assets/saas-plan.md)
- [assets/local-service-plan.md](./assets/local-service-plan.md)
- [assets/ecommerce-plan.md](./assets/ecommerce-plan.md)
- [assets/publisher-plan.md](./assets/publisher-plan.md)
- [assets/agency-plan.md](./assets/agency-plan.md)
- [assets/generic-plan.md](./assets/generic-plan.md)

## Requirements

- Codex with local skill support
- Git for install and updates
- Internet access for live-site audits
- Optional: a local web project for pre-launch codebase SEO reviews

Python is not required for normal usage of the skill itself.

## Uninstall

Unix/macOS/Linux:

```bash
rm -rf ~/.codex/skills/seo
```

Windows (PowerShell):

```powershell
Remove-Item "$env:USERPROFILE\.codex\skills\seo" -Recurse -Force
```

## License

MIT License. See [LICENSE](./LICENSE).

---

Built for Codex by [@Luzikov](https://github.com/Luzikov)
