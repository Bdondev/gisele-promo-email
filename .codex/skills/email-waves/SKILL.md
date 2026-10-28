---
name: email-waves
description: Create or integrate decorative wave separators in table-based HTML emails when a section needs a reliable responsive wave edge or band.
---

# Email Waves

Use this skill for decorative wave bands or section edges in HTML email templates. Preserve live text and table-based structure; the wave must remain decorative and must not be the only carrier of meaning.

## Workflow

1. Inspect the reference artwork and the surrounding email sections before editing. Identify the wave’s fill color, direction, height, side treatment, and the background color on both sides of the seam.
2. Prefer a dedicated, wide raster PNG wave asset for predictable inbox rendering. Use a transparent PNG only when the wave must overlay a different section color. Keep the asset shallow, optimized, and free of text.
3. Place the wave in its own full-width presentation-table row. Use `display:block`, `width:100%`, `height:auto`, `border:0`, and `line-height:0` on the containing cell. Do not add horizontal padding to the wave row.
4. Match the adjacent section’s `bgcolor` and inline `background-color` to the wave’s edge color. This prevents the one-pixel seam that can appear on iPhone and other mobile clients.
5. Avoid CSS-only curves, pseudo-elements, positioned elements, SVG, and background images for critical structure. They are acceptable only as optional enhancements with a solid-color fallback.
6. Keep the wave decorative with `alt=""`; ensure the section remains readable when images are disabled.
7. At mobile widths, keep the wave fluid and remove fixed-height overrides. Center adjacent product art or content using table-cell alignment and margins rather than flexbox or absolute positioning.

## Validation

- Check the wave row at the desktop container width and narrow mobile widths, especially around 320–430px.
- Look for white strips, dark seams, clipped corners, unexpected side gutters, and image distortion.
- Run `git diff --check` and inspect the final HTML for fixed wave heights, missing `display:block`, broken asset paths, or meaningful alt text on decorative waves.
- Report which rendering checks were performed; do not claim inbox-client validation without actually testing an inbox preview.
