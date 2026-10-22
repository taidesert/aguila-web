# Águila Integrated Systems website

## Project and audience
This is a proof-of-concept landing page for Águila Integrated Systems, a Sierra Leone-based technology consultancy specializing in business process automation, systems integration, ERP implementation, and AI-powered business solutions. It is intended to be maintained through conversational instructions to Codex by a non-developer colleague.

## Technical stack
- Plain UTF-8 HTML, CSS, and minimal browser JavaScript.
- No frameworks, package manager, build tools, backend, database, or external fonts.
- `index.html` contains the content and inline decorative SVG; `styles.css` contains the responsive design; `script.js` enhances keyboard navigation.
- Hosting target: Hostinger standard static web hosting. No deployment is authorized by default.

## Branding and content
- Always spell the full company name **Águila Integrated Systems**, preserving the accented Á. Save all text as UTF-8.
- Use a professional, clear, approachable tone. Navy, ivory, muted green, and amber form the palette, defined in CSS variables.
- Subtle eagle geometry, connections, precision, and forward movement guide the design. The SVG is a concept mark, not an approved final logo.
- Never invent testimonials, customers, contact details, certifications, or credentials. Keep missing details explicitly labelled as placeholders.
- Preserve semantic HTML, visible keyboard focus, reduced-motion support, sufficient contrast, and mobile layouts.

## Workflow and validation
- Use the existing isolated checkout. Do not create worktrees unless explicitly requested.
- Always create a feature branch and submit changes via a pull request targeting `main`. Never commit application changes directly to `main`, merge a PR, publish, or modify production without explicit authorization.
- Keep changes small and explain them in plain language.
- Preview from the repository with `python3 -m http.server 8000 --bind 0.0.0.0`. Stop with Ctrl+C.
- Check desktop and mobile sizes, internal links, keyboard navigation, missing assets, and browser console errors. No build step is required.
- The contact section deliberately has no working form or invented email. Add real contact details only when supplied by the owner.

## Hosted review previews
- Use Netlify Deploy Previews for browser-based review once the owner has connected the GitHub repository. See `docs/preview-setup.md`; `netlify.toml` specifies the static publish directory with no build command.
- After opening or updating a PR, check the Netlify deployment status for its latest commit. Validate the actual hosted URL at desktop and mobile widths, including navigation, assets, and console errors. Give the reviewer the direct working preview URL in chat. Do not substitute a GitHub file link or screenshot when a hosted preview is available.
- Never invent a preview URL or claim a deploy succeeded before verifying it. If Netlify is not connected or a deploy is pending/failed, state that clearly and diagnose the specific prerequisite.
- Netlify is authorized for review copies only. Do not connect a custom domain, change DNS, modify Hostinger, merge PRs, or buy a paid service without explicit authorization.
- Treat previews as public unless verified otherwise. Keep secrets and private material out of the publish directory.
- The owner-provided main-branch review site is https://aguilaintegrationsystems.netlify.app/. Unmerged changes must be reviewed using their own verified Deploy Preview URL, not this main-branch address.
