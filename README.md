# Premium Vector Icon Designer

A Codex skill for designing practical, production-grade editable SVG icons.

This skill focuses on the parts that usually separate usable product icons from noisy generated artwork: clear metaphor, recognizable silhouette, coherent stroke joins, consistent geometry, small-size readability, clean SVG structure, and restrained polish.

## What It Solves

- Prevents malformed SVG icons with random glyph-like marks.
- Avoids disconnected strokes, awkward joins, stray paths, and accidental fragments.
- Prevents icons from becoming only primitive straight-line marks when a richer product icon is requested.
- Keeps premium icon styles practical, editable, and readable instead of decorative for its own sake.
- Produces prompts, SVG output rules, critique criteria, and repair strategies for icon work.

## Best For

- System UI icons
- Product feature icons
- SaaS and dashboard icon sets
- App-style badges and membership icons
- Figma-ready SVG icons
- Icon critique and cleanup
- Prompt templates for high-quality vector icon generation

## Skill Structure

```text
premium-vector-icon-designer/
  SKILL.md
  agents/openai.yaml
  assets/
    icon-grid-24.svg
    icon-grid-1024.svg
  references/
    failure-prevention.md
    icon-quality-rubric.md
    prompt-patterns.md
    svg-output-rules.md
```

## Core Principles

The skill optimizes icon design in this order:

1. Clear metaphor
2. Recognizable silhouette
3. Small-size readability
4. Consistent geometry
5. Coherent stroke and shape construction
6. Editable SVG structure
7. Restrained polish

It does not treat gradients, shadows, glass effects, or 3D depth as default signs of quality. Those effects are used only when they improve hierarchy, brand fit, or the requested style.

## Installation

Clone or copy this folder into your Codex skills directory:

```bash
~/.codex/skills/premium-vector-icon-designer
```

On Windows, the equivalent path is usually:

```powershell
$env:USERPROFILE\.codex\skills\premium-vector-icon-designer
```

After installation, restart Codex or refresh the environment so the skill metadata can be discovered.

## Example Prompts

```text
Use premium-vector-icon-designer to design a 24px system-line icon for search. Keep it editable SVG, currentColor-based, with clean joins and no stray paths.
```

```text
Use premium-vector-icon-designer to create a polished but practical product icon for membership rewards. Use duotone hierarchy, rounded geometry, readable silhouette, and no decorative clutter.
```

```text
Use premium-vector-icon-designer to audit this SVG icon. Check metaphor clarity, stroke continuity, joins, stray paths, small-size readability, and whether it is too primitive or too decorative.
```

## Validation

If you have the Codex `skill-creator` validation script available, run:

```bash
python path/to/skill-creator/scripts/quick_validate.py path/to/premium-vector-icon-designer
```

The skill is intentionally kept lightweight: no runtime dependencies, no generated code, and no embedded bitmap assets.

This repository also includes a GitHub Actions workflow at `.github/workflows/validate.yml` to check the required skill files, frontmatter, and leftover scaffold markers on every push or pull request.

## Publishing Notes

Before publishing this repository publicly, choose a license that matches how you want others to use the skill. MIT is common for permissive reuse, but no license has been added here by default.
