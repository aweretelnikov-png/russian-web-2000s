---
name: russian-web-2000s
description: Create historically plausible Russian-web websites in styles characteristic of Runet circa 2000–2008. Use when the user asks for a site, page, prototype, visual concept, HTML/CSS, or design inspired by early/mid-2000s Russian internet. Select an archetype first, then apply its reference rules. Do not reduce the era to generic retro-web decoration.
---

# Russian Web 2000s

Generate websites that could plausibly have existed in the Russian-speaking web of roughly 2000–2008.

The goal is historical plausibility, not parody.

## Core workflow

1. Determine the requested year or approximate subperiod.
2. Determine the site archetype from the content and purpose.
3. Read only the matching archetype reference.
4. Choose historically plausible internal variants from that reference.
5. Build the page from period-appropriate information architecture first.
6. Apply typography, color, graphics, widgets, and microcopy second.
7. Remove modern UI patterns that leak into the result.
8. Prefer a complete plausible page over a collage of nostalgic details.

If the request does not specify a year, choose the center year of the archetype and state it internally in the implementation.

If the request does not specify an archetype, infer it from the site's purpose rather than asking unless two choices are genuinely equally plausible.

## Archetype router

### Personal / fan / hobby / small community

Use `references/archetypes/narod-2002.md`.

Typical period: 2000–2004.

Choose this when the site is primarily an author's page, fan site, hobby collection, personal photo page, small informal club, or handcrafted topic site.

Key idea: author/topic identity shapes the design.

### Portal / search / service hub

Use `references/archetypes/portal-2001-2003.md`.

Typical period: 2001–2003.

Choose this when the site combines search, catalog/rating, mail, news, weather, currency, TV, shopping, regional links, and other internet services.

Key idea: dense start page for navigating the internet.

### Corporate / company / institutional

Use `references/archetypes/company-2003-2005.md`.

Typical period: 2003–2005.

Choose this for companies, banks, telecoms, industrial groups, institutions, products, investor information, branch networks, and official company representation.

Key idea: official information architecture plus brand identity, not a conversion landing page.

### Forum

Use `references/archetypes/forum-2003-2006.md`.

Typical period: 2003–2006.

Choose this when the primary interaction is category → forum → topic → posts.

Key idea: tables, author column, ranks, avatars, signatures, BBCode, ICQ/UIN, graphical smilies.

### Blog / diary / community

Use `references/archetypes/blog-community-2004-2007.md`.

Typical period: 2004–2007.

Choose this for personal online diaries, friend feeds, communities, journals, posts with comments, archives, userpics, and social graph.

Key idea: author → diary → chronological entry → comments.

### uCoz / site constructor

Use `references/archetypes/ucoz-2006-2008.md`.

Typical period: 2006–2008.

Choose this for modular amateur portals built from news, forum, files, articles, photo albums, guestbook, polls, mini-chat, login, statistics, and global sidebar blocks.

Key idea: shared constructor shell plus switchable content modules.

### News / business media

Use `references/archetypes/media-2004-2006.md`.

Typical period: 2004–2006.

Choose this for newspapers, news sites, business media, editorial publications, newswires, and online magazines.

Key idea: organize the editorial picture of the day with high information density.

## Distinguish commonly confused archetypes

### `narod` vs `ucoz`

Use `narod` when the site feels authored page-by-page around one person or topic.

Use `ucoz` when the site feels assembled from reusable modules and global blocks such as login, poll, calendar, mini-chat, statistics, files, and forum.

### `portal` vs `media`

Use `portal` when search and unrelated services are peers.

Use `media` when editorial news judgment, chronology, rubrics, and stories dominate.

Currency/weather may exist in business media, but they support editorial context rather than define the site.

### `forum` vs `blog-community`

Use `forum` when discussion starts from topics owned by the forum structure.

Use `blog-community` when discussion starts under an author's or community's dated entry.

### `company` vs `portal`

Use `company` when all sections represent one organization and its audiences.

Use `portal` when independent services are aggregated into one entry point.

## Shared period rules

These are defaults, not universal constants.

- Design for desktop screens of the period, commonly around 800×600 or 1024×768 depending on year and archetype.
- Prefer compact fixed or fluid desktop layouts over mobile-first design.
- Use small system typography: Arial, Verdana, Tahoma, Times New Roman, Georgia where appropriate.
- Preserve visible text links and deep navigation.
- Use thin rules, table-like structure, small images, banners, and service metadata where appropriate.
- Keep information density substantially higher than current marketing websites.
- Treat whitespace as organizational space, not as the main visual effect.
- Allow GIF/JPG, background images, small raster icons, simple gradients, and period-specific widgets when supported by the archetype.
- Prefer authentic Russian web microcopy over modern product language.
- Let imperfect maintenance, timestamps, archive links, counters, old contact methods, and visible site structure contribute to plausibility.

## Modern patterns to suppress

Unless the user explicitly requests a hybrid interpretation, avoid:

- giant fullscreen hero sections;
- modern SaaS landing-page sequences;
- large rounded cards everywhere;
- glassmorphism and blur;
- pastel startup gradients;
- mobile-first hamburger navigation;
- floating mobile navigation;
- oversized typography;
- icon-only primary navigation;
- infinite scroll;
- algorithmic recommendation feeds;
- contemporary social reaction bars;
- generic Lucide/Heroicons as the main visual language;
- modern marketing copy such as “Start free”, “Book a demo”, “Trusted by thousands”.

Do not “fix” period interfaces into current UX conventions.

## Decoration rule

Historical decoration must follow the site's type and subject.

Do not create authenticity by blindly adding:

- Comic Sans;
- marquee;
- blinking text;
- random GIFs;
- 88×31 buttons;
- counters;
- tiled backgrounds.

Use these only where the selected archetype and intensity make them plausible.

A strict technical personal page, a business portal, and an expressive fan page from the same year should not look alike.

## Implementation modes

### AUTHENTIC

Prioritize historical implementation plausibility.

Allowed when appropriate:

- table layout;
- fixed pixel widths;
- GIF/JPG interface assets;
- old-style forms;
- repeated image backgrounds;
- raster buttons;
- obsolete structural techniques when needed for reconstruction.

### MODERN_ENGINE

Default for practical new projects.

Use modern semantic HTML/CSS/JS internally while preserving the historical visual and interaction model.

Modern implementation must not modernize the visible design.

## Content realism

Generate enough content for the page to feel used rather than templated.

Prefer:

- dated news;
- realistic navigation labels;
- archive months;
- usernames;
- counts;
- contact details;
- small advertisements;
- comments/posts;
- update notes;
- section descriptions.

Avoid polished placeholder copy that sounds like a current landing page.

## Asset policy

Do not assume copyrighted historical logos, photos, proprietary smiley packs, or exact branded interface graphics are reusable.

For generic recreation:

- use original or freely licensed assets;
- generate analogous period-style raster assets;
- use text/logos invented for the fictional site.

Historical references inform the design language; they are not an asset library.

For forum messenger-style smilies, prefer an original/free yellow raster set inspired by the visual language of ICQ/QIP-era messengers rather than bundling proprietary originals.

## Output check

Before finishing, inspect the page and ask:

1. Could this plausibly have existed in the target Runet period?
2. Is the archetype recognizable without reading an explanation?
3. Does the information architecture match the era and purpose?
4. Did modern card/hero/mobile patterns leak in?
5. Are nostalgic details supporting the site rather than replacing it?
6. Does the page contain enough realistic content to feel inhabited?

If the answer to 1–3 is no, revise structure before adding more decoration.

## References

Read exactly one main archetype reference unless the user explicitly asks for a hybrid:

- `references/archetypes/narod-2002.md`
- `references/archetypes/portal-2001-2003.md`
- `references/archetypes/company-2003-2005.md`
- `references/archetypes/forum-2003-2006.md`
- `references/archetypes/blog-community-2004-2007.md`
- `references/archetypes/ucoz-2006-2008.md`
- `references/archetypes/media-2004-2006.md`

Use a second reference only to resolve a deliberate hybrid, such as a corporate site with a forum section.

## Research stop rule

The historical corpus behind v1 is sufficient.

Do not perform new broad historical research during normal use of the skill.

Research further only when implementation exposes a specific unresolved question that materially affects historical plausibility.