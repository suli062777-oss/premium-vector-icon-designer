# Failure Prevention

Use this reference when an icon looks malformed, random, disconnected, overly primitive, or visually inconsistent.

## Common Failure Modes

- Glyph noise: the SVG contains marks that look like random symbols instead of purposeful icon parts.
- Broken joins: strokes that should connect are misaligned, stop short, overshoot, or meet at awkward angles.
- Mixed construction: one icon combines sharp corners, rounded corners, uneven stroke weights, and unrelated curve styles without intent.
- Stray geometry: tiny paths, floating ticks, fragments, or decorative marks appear because they were not tied to the metaphor.
- Primitive output: the icon is only straight segments, only a generic outline, or only one flat color when a richer product icon was requested.
- Low hierarchy: all parts have the same visual weight, so the main idea and secondary details compete.
- Poor spacing: inner gaps are too narrow, tangents create noise, or negative space collapses at small size.

## Construction Guardrails

- Start with 1 primary metaphor and at most 1 secondary cue.
- Use complete primitives: circles, rounded rectangles, continuous paths, arcs, and purposeful cutouts.
- Align endpoints to the grid or to visually meaningful anchor points.
- Use consistent stroke width within a line icon.
- Use consistent corner radius and curve tension within a filled icon.
- Use `stroke-linecap` and `stroke-linejoin` deliberately; default to `round` for friendly UI icons.
- Avoid open path ends unless the open end is part of the metaphor.
- Keep minimum gaps large enough for the target size.

## Anti-Garbled SVG Pass

Before outputting SVG, check:

1. Does every path contribute to the metaphor, hierarchy, or polish?
2. Are there any tiny floating marks or single-use fragments that can be removed?
3. Do all intended joints connect cleanly?
4. Are arcs and curves smooth instead of kinked?
5. Are stroke caps and joins consistent?
6. Does the icon still read if viewed at the target size?
7. Does it remain recognizable when flattened to one color?

If any answer fails, simplify or redraw the icon before adding color.

## Avoiding Over-Primitive Icons

Restraint does not mean lifeless. When the user asks for a high-quality product icon, add controlled richness through:

- A stronger silhouette with distinct outer contour.
- Meaningful negative space.
- A small secondary detail that reinforces the feature.
- Duotone hierarchy for primary and secondary parts.
- A subtle accent color or restrained gradient for large icons.
- Rounded corners, arcs, or filled surfaces instead of only straight strokes.

Do not add richness through random sparkles, disconnected ticks, excessive shadows, tiny decorations, or unrelated geometric marks.

## Repair Strategy

When improving a broken icon:

1. Remove stray paths and decorative noise first.
2. Rebuild the silhouette from simple, complete shapes.
3. Reconnect or replace broken strokes with continuous paths.
4. Normalize stroke width, caps, joins, radii, and spacing.
5. Add hierarchy with fill/stroke contrast or limited color.
6. Re-check small-size readability and one-color recognition.
