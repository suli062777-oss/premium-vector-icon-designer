# Premium Vector Icon Designer

[![License: MIT](https://img.shields.io/badge/license-MIT-0f766e.svg)](LICENSE)
[![Validate Skill](https://github.com/suli062777-oss/premium-vector-icon-designer/actions/workflows/validate.yml/badge.svg)](https://github.com/suli062777-oss/premium-vector-icon-designer/actions/workflows/validate.yml)
[![Codex Skill](https://img.shields.io/badge/Codex-skill-111827.svg)](SKILL.md)
[![SVG](https://img.shields.io/badge/output-editable%20SVG-7c3aed.svg)](references/svg-output-rules.md)

A Codex skill for turning icon briefs into clean, editable SVG assets with design-system discipline.

The skill is built around a simple belief: a good icon should read before it decorates. It starts with metaphor, silhouette, grid, and stroke continuity, then adds color or depth only when those choices improve hierarchy or product fit.

## Why This Exists

Generated SVG icons often fail in small but expensive ways: broken joins, stray ticks, awkward tangents, inconsistent radii, random symbol-like marks, or a lifeless straight-line sketch when the brief asks for a polished product icon.

This skill captures a stricter design-engineering review loop for icon work. It helps Codex produce icons that are not just visually pleasant, but also inspectable, editable, scalable, and easier to hand off to Figma or a codebase.

## What It Enforces

- Clear metaphor before decoration
- Strong silhouette and one-color readability
- Optical balance on the intended grid
- Coherent stroke widths, caps, joins, radii, and curve tension
- Enough shape vocabulary for the requested style: arcs, fills, negative space, duotone, or restrained gradients when useful
- No malformed paths, disconnected strokes, floating fragments, or random glyph-like marks
- SVG output that designers and engineers can actually edit

## Good For

- 24px system UI icons
- Product feature icons
- SaaS and dashboard icon sets
- App-style badges and membership icons
- Figma-ready SVG assets
- Icon critique, cleanup, and redesign prompts

## Quality Gates

The skill checks icons in two passes:

1. Structure pass: metaphor, silhouette, proportions, path continuity, joins, spacing, and small-size readability.
2. Polish pass: controlled color hierarchy, duotone separation, soft highlight, or gradient only when it helps the icon.

This keeps the output away from both extremes: messy decorative SVGs and overly plain straight-line drafts.

## Repository Structure

```text
premium-vector-icon-designer/
  SKILL.md
  skill.json
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

## Included References

| File | Purpose |
| --- | --- |
| `references/failure-prevention.md` | Malformed SVG patterns, broken joins, primitive output, and repair strategy |
| `references/icon-quality-rubric.md` | Metaphor, silhouette, scale, continuity, optical balance, editability, and restraint |
| `references/svg-output-rules.md` | SVG hygiene for monochrome, colored, gradient, and React-friendly output |
| `references/prompt-patterns.md` | Reusable prompt structures for individual icons and icon sets |

## Installation

Clone the repository:

```bash
git clone https://github.com/suli062777-oss/premium-vector-icon-designer.git
```

Copy the folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R premium-vector-icon-designer ~/.codex/skills/
```

On Windows PowerShell:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills"
Copy-Item -Recurse ".\premium-vector-icon-designer" "$env:USERPROFILE\.codex\skills\premium-vector-icon-designer"
```

Restart Codex or refresh the environment so the skill metadata can be discovered.

## Example Prompts

```text
Use premium-vector-icon-designer to design a 24px system-line icon for search. Keep it currentColor-based, grid-aligned, and free of stray paths.
```

```text
Use premium-vector-icon-designer to create a product icon for membership rewards. Use rounded geometry, duotone hierarchy, a readable silhouette, and no decorative clutter.
```

```text
Use premium-vector-icon-designer to audit this SVG icon. Check metaphor clarity, stroke continuity, joins, stray paths, small-size readability, and whether it is too primitive or too decorative.
```

## Maintenance

Use these files as the review surface:

- `SKILL.md`: runtime behavior and decision flow
- `references/`: deeper rules loaded only when needed
- `skill.json`: project metadata for the repository
- `.github/workflows/validate.yml`: package integrity checks

## Validation

If you have the Codex `skill-creator` validation script available, run:

```bash
python path/to/skill-creator/scripts/quick_validate.py path/to/premium-vector-icon-designer
```

This repository also includes `.github/workflows/validate.yml` to check required files, `SKILL.md` frontmatter, `skill.json`, and leftover scaffold markers on every push or pull request.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the review checklist used when changing the skill behavior or adding new references.

## License

MIT License.
