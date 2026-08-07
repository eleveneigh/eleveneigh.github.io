# Visual Redesign Plan

## 1. Objective

Transform the site from a polished but generic academic portfolio into an editorial research notebook that clearly communicates Leyan Wu's dual identity as an HCI researcher and creative practitioner.

The redesign must preserve the existing Jekyll architecture, content, URLs, accessibility foundation, and GitHub Pages compatibility.

## 2. Design Direction

### Core idea: Editorial Research Notebook

The visual system combines:

- the clarity and credibility of an academic portfolio;
- the material character of collage, film, poetry, and zine making;
- controlled visual friction through asymmetry, layering, numbering, and cropped imagery.

The result should feel authored and memorable without becoming decorative or difficult to scan.

### Principles

1. **Research first, personality always** — the site must remain easy for faculty and collaborators to scan.
2. **Use material cues sparingly** — paper, tape, wash, and rotation are accents rather than universal decoration.
3. **Make images carry information** — existing research diagrams and film stills should appear at overview level, not only inside detail pages.
4. **Reserve italics for voice** — use italic Newsreader for display moments, questions, and short section titles; use roman serif for long project titles.
5. **Create rhythm through contrast** — alternate compact metadata, large imagery, short summaries, and readable long-form text.
6. **Design mobile intentionally** — mobile layouts should recompose, not merely shrink desktop columns.

## 3. Global Design System

### Color

- Warm canvas: `#f4f0e8`
- Raised paper: `#fbf9f4`
- Primary ink: `#252724`
- Secondary ink: `#686d68`
- Terracotta accent: `#9a472b`
- Muted sage accent: `#778477`
- Soft rule: `rgba(37, 39, 36, 0.14)`

Use terracotta for calls to action, active states, indices, and small rules. Use sage only for secondary research metadata and subtle background blocks.

### Typography

- Display and editorial headings: Newsreader.
- Long project titles: Newsreader roman, medium weight.
- Expressive questions and short section labels: Newsreader italic.
- Body copy: system sans-serif for clarity and performance.
- Metadata, numbering, roles, dates, and methods: monospace.

### Layout

- Increase the primary desktop canvas from 800px to approximately 1080px.
- Keep long-form reading columns between 680px and 760px.
- Use asymmetric grids for overview pages and contained reading columns for case studies.
- Introduce a reusable eyebrow/index pattern such as `01 / SELECTED RESEARCH`.

### Interaction

- Add an active navigation state using `aria-current` styling.
- Use small image scale, card lift, rule extension, and arrow movement on hover.
- Respect `prefers-reduced-motion`.
- Keep all primary cards keyboard accessible and avoid hover-only information.

## 4. Page-Level Changes

### Header and footer

- Make the header feel like a compact editorial masthead.
- Add a short role descriptor beside the site name on larger screens.
- Style the current page in the navigation.
- Reduce footer repetition and present contact links as a clean horizontal sign-off.

### Home

- Replace the small two-column introduction with a larger asymmetric hero.
- Add a compact research identity label and stronger typographic hierarchy.
- Enlarge the portrait and layer it with a paper caption/index treatment.
- Add a Selected Research section with three image-led project cards.
- Add a Research ↔ Practice bridge explaining how creative work informs the research agenda.
- Add a compact Practice preview with film stills and links.
- End with a clear opportunity/contact statement.

### Research overview

- Replace text-only white cards with image-led editorial cards.
- Use existing case-study imagery as overview thumbnails.
- Show theme, date, brief, key insight, and a direct case-study action.
- Give the flagship project greater visual weight.
- Remove artificial card staggering and improve mobile scan order.

### Case studies

- Add an At a Glance summary beneath the title with role, period, methods/highlights, and publication status.
- Strengthen section numbering and vertical rhythm.
- Give key insight/findings sections a distinct paper or tinted treatment.
- Keep figures wide while constraining body text to a readable measure.
- Reduce universal italics and improve long-title readability.

### About

- Turn the opening paragraph into an editorial lead.
- Group Research Vision, Interests, Methods, and Goals into clearer visual sections.
- Present interests and methods as numbered compact lists rather than default bullets.
- Retain Wolfgang as a personal closing note but make it feel like a deliberate marginalia card.

### Publications

- Introduce publication numbering and clearer title/venue/status hierarchy.
- Use compact metadata and reduce generic card styling.
- Preserve paper links and external-link accessibility.

### Practice

- Preserve the paper-and-tape language because it is the site's strongest existing identity.
- Harmonize its typography, colors, indices, and spacing with Research.
- Reduce excessive card width on large screens and improve image scale.
- Keep decorative rotation disabled or minimized on small screens.

## 5. Responsive Strategy

### Under 768px

- Stack the home hero instead of keeping a narrow two-column layout.
- Keep the portrait visually prominent but below the primary statement.
- Render all project cards in one column.
- Collapse navigation using the existing accessible Minima menu behavior.
- Reduce oversized wash backgrounds and prevent title clipping.
- Keep minimum touch targets near 44px.
- Prevent metadata rows and footer contacts from overflowing.

### Under 480px

- Use 18–20px page gutters.
- Shorten ornamental offsets and remove rotations.
- Keep long research titles at a readable 30–36px range.

## 6. Content and Asset Mapping

- Juxta thumbnail: `/assets/research/juxta/figure-1.png`
- Digital collage thumbnail: `/assets/research/chi-digital-collage/figure-1-teaser.png`
- Coller thumbnail: `/assets/research/coller/system-overview.png`
- Practice preview: `/assets/practice/june/01.jpg` and `/assets/practice/june/02.jpg`
- Portrait: `/assets/images/contact-hero.jpg`
- Existing title washes remain available as low-opacity accents.

Project overview image paths should be stored in `_data/projects.yml` so overview templates remain data-driven.

## 7. Implementation Sequence

1. Update global tokens, typography, canvas width, header, footer, and shared interaction states.
2. Rebuild the home template and responsive hero.
3. Add project image data and rebuild the Research overview.
4. Add shared case-study summary components and refine long-form styles.
5. Refine About, Publications, and Practice for consistency.
6. Build the site, check generated pages, inspect responsive rules, and fix regressions.

## 8. Acceptance Criteria

- The first desktop viewport communicates identity, research focus, and at least one path to work.
- The home page contains representative Research and Practice content.
- Research overview cards include meaningful imagery and remain fully usable without hover.
- Long project titles are not universally italicized.
- Case studies expose role, period, contribution/highlights, and publication status near the top.
- The 390px home hero no longer compresses body copy into a narrow side column.
- Navigation, focus states, color contrast, reduced-motion behavior, and semantic heading order remain functional.
- `bundle exec jekyll build` completes successfully.
- Existing URLs and content files remain compatible with GitHub Pages.

## 9. Out of Scope

- Rewriting research claims or publication details.
- Adding JavaScript-heavy animation.
- Replacing Jekyll or migrating hosting platforms.
- Publishing changes to the live site without explicit approval.
