# Contributing

This repository is a design-engineering skill, so changes should improve the review process, the SVG quality bar, or the clarity of the handoff.

## Change Guidelines

- Keep `SKILL.md` focused on behavior that must be loaded at runtime.
- Put deeper design rules in `references/` instead of expanding the main skill file.
- Avoid broad marketing language. Prefer concrete checks, failure modes, and repair rules.
- Keep SVG guidance practical for both designers and engineers.
- Do not add generated bitmap assets, private examples, credentials, or local machine paths.

## Icon Quality Checklist

Before changing the skill behavior, confirm it still protects these standards:

- Clear metaphor before decoration
- Recognizable silhouette at the target size
- Coherent stroke caps, joins, radii, and curve tension
- No disconnected strokes, stray paths, or random glyph-like marks
- Enough visual hierarchy for product icons without ornamental clutter
- Editable SVG output with meaningful grouping

## Validation

Run the skill validator when available:

```bash
python path/to/skill-creator/scripts/quick_validate.py path/to/premium-vector-icon-designer
```

The GitHub Actions workflow also checks the required files, `skill.json`, frontmatter, and leftover scaffold markers.
