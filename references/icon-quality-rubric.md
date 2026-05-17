# Icon Quality Rubric

Use this rubric to audit whether an icon is production-grade rather than decorative noise.

## Required Checks

- Metaphor: The icon communicates the object, action, state, or feature without relying on a label.
- Silhouette: The icon remains understandable when converted to a single solid color.
- Scale: Details survive at the target size. Remove details that disappear or create visual mud.
- Geometry: Stroke, radius, spacing, proportions, and perspective use one coherent system.
- Continuity: Intended joints meet cleanly, open path ends are purposeful, and curves do not kink.
- Optical balance: The icon looks centered and stable in context, even when the math center differs.
- Shape vocabulary: The icon uses enough arcs, curves, fills, negative space, and hierarchy for the requested style.
- Visual weight: The icon matches sibling icons in density, stroke, fill area, and contrast.
- Editability: Shapes are named, grouped logically, and not over-fragmented.
- Restraint: Effects support hierarchy or brand fit. They are not the main idea.

## Complexity Limits

- System icons should usually use 1-3 paths and no decorative effects.
- Product icons should usually use 3-8 meaningful layers.
- App icons may use more layers, but the silhouette should remain simple.
- Avoid micro-details, decorative sparkles, tiny cutouts, heavy shadows, complex masks, broken joins, and stray paths unless the use case requires them.
- Avoid icons that are only straight-line fragments when the request calls for a polished product, feature, or app-style icon.

## One-Color Test

Before finalizing, mentally flatten the icon to one color:

1. If the icon stops being recognizable, simplify the shape.
2. If the meaning depends entirely on gradients or shadows, redesign the metaphor.
3. If small details merge together, increase spacing or remove them.

## Stroke and Join Test

For line icons:

1. Check that endpoints align to the grid or intentional optical anchors.
2. Check that joins use one consistent treatment: round, bevel, or miter.
3. Replace multiple near-touching segments with a continuous path when they represent one contour.
4. Remove floating marks unless they clearly represent state, motion, or emphasis.

## Practical Scoring

- 5: Clear, scalable, editable, and visually disciplined.
- 4: Strong, with minor geometry or complexity issues.
- 3: Usable but needs simplification or alignment.
- 2: Decorative or unclear; significant redesign needed.
- 1: Not production-ready.
