# Project instructions

Build accessible, responsive HTML emails that render reliably in the target inboxes. Favor maintainable markup and verified compatibility.

## Project files and workflow

- `index.html` is the hand-authored email source and current output. Edit it directly.
- `SignatureGisele-Lilas.png` is an available local image asset. Production image hosting is not yet specified.
- No build system, package scripts, or automated tests are currently configured. Do not invent commands or claim they ran.
- The ESP (email service provider), production URLs, and final client matrix are not yet specified. Ask for these when required for the task; continue independent layout work with clearly identified placeholders.
- Use plain HTML by default. Introduce a framework only when requested or justified by the project workflow; document its source files, output, and build command.
- If compilation is introduced, source templates are authoritative for edits. Regenerate output and validate the compiled HTML; do not routinely hand-edit generated files.
- Consult [email workflow checklists](docs/email-workflows.md) for scaffolding, modules, buttons, audits, ESP preparation, design conversion, MJML, and debugging. Read only the relevant sections.

## HTML and layout

- Include `<!DOCTYPE html>`, the correct document `lang`, UTF-8 charset, viewport metadata, and a meaningful title.
- Use tables for structural layout, with `role="presentation"` and explicit `cellpadding`, `cellspacing`, and `border` attributes.
- Use semantic headings, paragraphs, and links within the layout where appropriate. Preserve logical reading order.
- Use fluid or hybrid layouts that remain readable without media queries. Use percentage widths and a desktop maximum width, with conditional table fallbacks where required.
- Prefer padding on table cells for structural spacing. Avoid unnecessary nesting and duplicate desktop/mobile content.
- Do not use JavaScript, external scripts, CSS Grid, or Flexbox for critical email layout. Do not rely on floats or positioning for structure.

## CSS and client compatibility

- Inline critical presentation. Reserve embedded `<style>` blocks for resets, responsive overrides, dark mode, and client-specific enhancements; avoid external stylesheets.
- Use descriptive hyphenated class names, simple selectors, and explicit properties when shorthand is less reliable. Use `!important` only for necessary overrides.
- Keep essential content usable without custom fonts, background images, advanced selectors, pseudo-elements, animation, or interactive features.
- Verify uncertain support using current client documentation or Can I Email. Browser support and framework output do not establish inbox compatibility.
- Support Word-based Outlook rendering where required, using conditional comments and VML only when needed. Validate Outlook desktop separately from Outlook web and mobile.
- Treat dark mode CSS and metadata as progressive enhancements. Check text, backgrounds, logos, and transparency when clients alter colors.
- Use AMP only when explicitly requested and supported by the ESP and target inboxes. Provide complete HTML and plain-text fallbacks.

## Content, images, and accessibility

- Include meaningful subject and preheader copy. Keep important information as live text and readable when images are disabled.
- Use fallback font stacks such as `Arial, Helvetica, sans-serif`, readable font sizes, and comfortable line height, including footer text.
- Maintain strong contrast and generous touch targets. Do not communicate meaning through color alone or hide essential content on mobile.
- Optimize images: prefer JPEG for photos, PNG for transparency or sharp graphics, and GIF when animation is needed. Provide a useful static fallback for animated media.
- Set image dimensions and inline scaling styles. Give informative images meaningful `alt` text and decorative images `alt=""`.
- Avoid base64 images, oversized assets, and reliance on SVG or video for critical content.
- Build table-based buttons with descriptive live text. Verify spacing and clickable area in target clients; rounded corners and other decoration must be optional.
- Use absolute HTTPS URLs for hosted images and web destinations. Preserve intentional `mailto:`, `tel:`, and documented ESP links. `target="_blank"` is optional.
- Provide plain-text content for production delivery, including the message, primary links, sender identity, and unsubscribe information where applicable. Verify that the sending platform includes it as the plain-text MIME part.

## ESP integration and sender information

- Use only documented ESP syntax for personalization, loops, conditionals, tracking, unsubscribe, and preference-center links. Never invent merge tags.
- Preserve required sender identity, mailing address, unsubscribe links, analytics tags, and editable regions. Do not hide required footer information.
- Handle missing, empty, and long personalization values; avoid hardcoding recipient-specific data into reusable templates.
- Use accurate subject lines, sender names, preview text, and destinations. Do not invent legal requirements; flag unresolved requirements when relevant to production delivery.
- Keep secrets, credentials, and unnecessary private data out of email markup. Do not collect sensitive information directly inside an email.
- During production preparation, verify sender authentication with the sending platform; template code alone cannot establish deliverability.
- Sending or uploading emails requires authorization for that action. A local edit or review does not itself authorize sending.

## Size and cleanup

- Use a project budget below 100 KB for final HTML, preferably below 80–90 KB before ESP transformations. This budget does not guarantee freedom from clipping.
- Measure the final HTML and check the ESP-processed result, since tracking and personalization can increase its size.
- Remove unused CSS, dead modules, and unnecessary comments. Preserve Outlook conditional comments, ESP directives, and functional template annotations.

## Validation and completion

- Check HTML structure, table nesting, closing tags, image dimensions and alt text, links, asset paths, placeholder values, and file size.
- Use browser previews for local layout checks, then validate actual inbox rendering or available tools such as Litmus or Email on Acid before production approval.
- Unless a narrower matrix is agreed, target Gmail web/iOS/Android, Apple Mail/macOS and iOS Mail, Outlook desktop/web/mobile, Yahoo Mail, and AOL Mail. Specify other Android clients when relevant.
- Check desktop and mobile widths, light and dark mode, images enabled and disabled, and short, long, or missing personalized content.
- For production preparation, validate the ESP-transformed HTML, tracked destinations, unsubscribe/preferences links, hosted assets, and plain-text version.
- Report what changed, checks actually performed, known rendering compromises, and checks still pending. Never invent test results or imply one client proves broad compatibility.
- If inbox or ESP tooling is unavailable, complete local checks and identify the remaining validation. Do not label the email production-ready until required checks have passed.
