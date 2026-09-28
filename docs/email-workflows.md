# Email workflow checklists

Use the checklist relevant to the current task. These are reference workflows, not installed agent skills. Follow the project rules in [AGENTS.md](../AGENTS.md). Report unavailable checks as pending rather than claiming they passed.

## Scaffold a Basic HTML Email
When creating a new email template:

1. Confirm the email type:
   - marketing
   - transactional
   - lifecycle
   - newsletter
   - receipt
   - notification
2. Confirm the target ESP if known.
3. Create a table-based HTML structure.
4. Add DOCTYPE, lang, charset, viewport, and title.
5. Add inline base styles.
6. Add progressive <style> rules for mobile and dark mode only when useful.
7. Add a preheader.
8. Add accessible live text.
9. Add image dimensions and alt text.
10. Add bulletproof buttons.
11. Add unsubscribe and compliance regions for marketing emails.
12. Provide a plain-text version.
13. Keep final HTML under clipping thresholds.
14. Provide testing notes.

## Build a Responsive Email Module
When building a reusable module:

1. Start with a table-based structure.
2. Make the default layout readable without media queries.
3. Add inline padding, typography, color, and spacing.
4. Add mobile overrides in embedded CSS.
5. Avoid unsupported layout CSS.
6. Test with short, normal, and long content.
7. Test with images disabled.
8. Confirm dark mode behavior.
9. Document any client-specific compromises.

## Create a Bulletproof Button
When creating a button:

1. Use a table-based button.
2. Use live text, not image text.
3. Use inline styles.
4. Use a high-contrast background and text color.
5. Use generous padding.
6. Use an absolute HTTPS URL.
7. Use descriptive button text.
8. Test in Outlook desktop.
9. Ensure it remains visible in dark mode.

## Audit Email Accessibility
When auditing accessibility:

1. Check document language.
2. Check reading order.
3. Check heading structure where applicable.
4. Check layout tables for role="presentation".
5. Check image alt text.
6. Check link text.
7. Check color contrast.
8. Check text size and line height.
9. Check touch target size.
10. Check images-disabled rendering.
11. Check plain-text fallback.
12. Check dark mode readability.

## Audit Email Client Compatibility
When auditing compatibility:

1. Identify the required client matrix.
2. Check for unsupported CSS.
3. Check for fragile layout techniques.
4. Check Outlook desktop behavior.
5. Check Gmail clipping risk.
6. Check mobile scaling.
7. Check dark mode behavior.
8. Check image blocking behavior.
9. Check ESP-transformed output.
10. Record known issues and acceptable compromises.

## Prepare Email for ESP Upload
When preparing for ESP use:

1. Confirm the ESP.
2. Replace placeholder merge tags with documented ESP syntax.
3. Preserve unsubscribe tags.
4. Preserve preference center tags.
5. Preserve sender identity and address requirements.
6. Inline production CSS.
7. Confirm image hosting URLs.
8. Confirm link tracking behavior.
9. Test with real preview data.
10. When sending is explicitly authorized, send test emails to the agreed inboxes; otherwise document this pending check.
11. Verify final rendered HTML after ESP processing.

## Convert a Web Design to an Email
When converting a web design:

1. Identify what must be simplified.
2. Replace div-based layout with table-based layout.
3. Replace CSS Grid and Flexbox with tables.
4. Replace web fonts with safe font stacks or fallbacks.
5. Replace interactive elements with static fallbacks.
6. Replace complex backgrounds with solid colors unless tested.
7. Convert important text in images into live text.
8. Simplify spacing, columns, shadows, and overlays.
9. Add mobile behavior.
10. Test across email clients.

## Review an MJML Email
When reviewing MJML:

1. Review the MJML source for maintainability.
2. Compile the MJML.
3. Review the generated HTML.
4. Confirm critical styles are inline.
5. Check for excessive file size.
6. Check Outlook rendering.
7. Check Gmail clipping risk.
8. Check mobile behavior.
9. Check dark mode behavior.
10. Test the compiled email, not only the MJML preview.

## Debug a Broken Email Layout
When debugging layout issues:

1. Identify the failing client.
2. Confirm whether the issue appears before or after ESP processing.
3. Check for broken tables.
4. Check for unsupported CSS.
5. Check image dimensions.
6. Check width attributes and inline widths.
7. Check media queries.
8. Check Outlook conditional comments.
9. Reduce the email to the smallest failing example.
10. Fix with the simplest compatible solution.
11. Retest in the failing client and adjacent clients.
