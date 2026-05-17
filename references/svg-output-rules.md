# SVG Output Rules

Use these rules for clean, maintainable SVG icons.

## Baseline SVG

- Include `xmlns="http://www.w3.org/2000/svg"`.
- Include a correct `viewBox`.
- Include explicit `width` and `height` unless the target environment prefers responsive SVG.
- Keep coordinates aligned to the intended grid where possible.
- Avoid stray paths, invisible shapes, duplicated fragments, and accidental marks.
- Use transparent background by default.

## Monochrome Icons

- Prefer `fill="none"` and `stroke="currentColor"` for line icons.
- Prefer `fill="currentColor"` for solid monochrome icons.
- Use consistent stroke width, usually `1.5` or `2` on a 24px grid.
- Use `stroke-linecap="round"` and `stroke-linejoin="round"` when the style is rounded.
- Prefer continuous paths for continuous contours instead of many short disconnected segments.
- Make open path endings intentional and visually balanced.

## Colored Icons

- Use flat fills first.
- Use gradients only when they clarify hierarchy or match the requested style.
- When richer hierarchy is requested, prefer controlled duotone or accent color over random decoration.
- Name gradients semantically, such as `paint-base`, `paint-highlight`, or `paint-shadow`.
- Keep gradients limited and easy to edit.

## Effects

- Avoid filters for small UI icons.
- Use blur/shadow filters only for large icons, badges, app icons, or explicit soft-3D requests.
- Keep shadows subtle and removable.
- Avoid nested masks and clipping paths unless they materially simplify the SVG.

## Figma and Code Hygiene

- Group related shapes with semantic ids: `base`, `detail`, `highlight`, `shadow`.
- Avoid random generated ids.
- Avoid embedded raster images and base64 data.
- Avoid text nodes unless requested.
- Avoid excessive decimal precision.
- Avoid output that only works as code but looks malformed when rendered.
- Keep the SVG readable enough to modify by hand.

## React SVG Notes

When exporting as a React component:

- Convert attributes to camelCase.
- Allow `className`, `style`, and color props when useful.
- Keep decorative ids stable or make them unique if multiple instances may appear on one page.
