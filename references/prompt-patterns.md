# Prompt Patterns

Use these patterns when the user wants prompt templates or a repeatable design brief.

## Practical SVG Icon Prompt

```text
Design a production-grade editable SVG icon for [feature/object/action].
Use case: [navigation / toolbar / product feature / app icon / badge].
Target size: [24px / 48px / 64px / 1024px].
Style: [system-line / solid-product / duotone / soft-3d-vector].
Geometry: clean silhouette, optical centering, consistent radius and spacing, readable at target size.
Color: [currentColor / flat brand colors / restrained 2-color palette / limited gradient].
Output: clean SVG with a proper viewBox, semantic groups, no background, no embedded bitmap.
Avoid: text, unnecessary detail, stray paths, disconnected strokes, broken joins, random glyph-like marks, heavy shadows, complex masks, and effects that hurt readability.
```

## Premium But Restrained Feature Icon Prompt

```text
Create a high-quality vector feature icon for [feature].
The icon should feel polished but practical: simple silhouette first, coherent joins, limited layers, soft color hierarchy, and no ornamental clutter.
Use a [48px/64px] grid. Keep it readable at small sizes.
Output editable SVG with semantic groups: base, detail, highlight.
Do not include background, text, raster images, stray fragments, disconnected strokes, or excessive filters.
```

## Soft 3D App-Style Icon Prompt

```text
Design a soft 3D vector icon for [object/feature] at 1024x1024.
Use a simple geometric silhouette that still works in one color.
Apply restrained gradients, subtle highlight, and a lightweight contact shadow.
Limit the design to a few meaningful layers and keep all shapes editable SVG.
Avoid photorealism, heavy blur, complex glass effects, tiny details, broken joins, stray marks, text, and background.
```

## Icon Set Prompt

```text
Design an icon set for [product/domain] with these concepts: [list].
Target size: [24px / 48px].
Style: [line / solid / duotone].
System rules: consistent stroke/fill logic, shared radius, shared spacing, matching visual weight.
Output each icon as editable SVG with consistent viewBox and naming.
Before finalizing, check one-color readability, stroke continuity, clean joins, and remove details that do not survive the target size.
```
