# Ananya R — Product Designer Portfolio

## Five-line implementation plan
1. Extract and compress all supplied PDF pages and raster images into `site/assets/`, keeping the original portfolio PDF available for download.
2. Build a semantic, crawler-visible single-page site in plain HTML/CSS/vanilla JS with GSAP + ScrollTrigger and data-driven case-study/lightbox overlays.
3. Use the supplied portfolio/supporting PDF pages and photos as the only visuals, mapped across the ten requested projects with copy grounded in the files.
4. Add the requested editorial interactions, responsive navigation, filtering, reduced-motion path, accessibility labels, and `manus-routes.json`.
5. Run static checks, responsive preview checks, checkpoint the project, publish the static `site/` output, and package the source ZIP.

## Implementation approach
- **Frontend:** `site/index.html`, `site/styles.css`, `site/script.js`; no framework, bundler, server, or database.
- **Assets:** compressed WebP page renders at no more than 1600px wide plus supplied raster images re-encoded as WebP. The original `Portfolio-I-Ananya-R.pdf` is preserved for the download CTA.
- **Content:** ten case-study records in `script.js`; each record names the supplied cover/gallery assets, categories, tags, year/type label, first-person summary, and a process list. Missing details are marked `Add detail here`.
- **Motion:** GSAP/ScrollTrigger powers preloader, masked hero reveal, scroll reveals, card entrances, process progress, overlay transitions, and parallax. CSS/JS fallbacks keep the site usable if CDN scripts are unavailable.
- **Serving:** static output is the committed `site/` directory with `site/index.html` at its root. A root-level route manifest declares `/`.

## Design direction
- **Design movement:** contemporary editorial portfolio / Swiss-inspired art direction softened with warm material tones.
- **Core principles:** (1) quiet confidence through whitespace and restraint, (2) process made visible through numbered structure, (3) raw project evidence over decoration, (4) interaction that feels physical but never loud.
- **Color philosophy:** warm off-white gives the work room to breathe; ink anchors reading; muted grey recedes into the background; burnt orange is reserved for cues, progress, and moments of emphasis; the contact section becomes a dark, high-contrast closing page.
- **Layout paradigm:** asymmetrical editorial rhythm—offset cards, narrow metadata rails, and wide visual fields replace a centered app grid.
- **Signature elements:** orange index numbers, 1px dividers, and a small rotating availability seal.
- **Interaction philosophy:** hover and scroll interactions echo handling a physical object: subtle weight shifts, slow zooms, and directional transitions.
- **Animation:** transform and opacity only for primary motion; overlay clips vertically; project cards tilt gently; reduced-motion users see immediate content with interaction still available.
- **Typography system:** Instrument Serif regular/italic for display and emphasis, Manrope for reading/UI, JetBrains Mono for labels, navigation, tags, numbers, and captions. All use explicit fallback stacks.
- **Brand essence:** a product designer who turns research, ergonomics, and making into thoughtful objects; **observant, tactile, clear**.
- **Brand voice:** direct and process-led. Example lines: “I design thoughtful products from research to render.” / “The work is in the details—and in the questions before them.”
- **Wordmark & logo:** the `A` favicon is a small orange seal; the wordmark remains the typographic “ANANYA R” with an italic serif surname cue.
- **Signature brand color:** burnt orange `#E4572E`.

## Project structure
- `site/index.html` — semantic page shell, SEO metadata, preloader, sections, overlays, and no-JS project index.
- `site/styles.css` — responsive design system, editorial layout, grain, cursor states, transitions, and reduced-motion rules.
- `site/script.js` — project data, filtering, navigation, overlay/lightbox behavior, GSAP/ScrollTrigger enhancements, cursor/magnetic interactions, and copy-email toast.
- `site/assets/` — optimized supplied visuals, PDF page render galleries, original portfolio PDF, and favicon.
- `manus-routes.json` — declared public route set.
- `TODO.md` — delivery outcomes and status.
