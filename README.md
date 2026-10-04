# russian-web-2000s

A historically grounded design skill for generating websites that resemble the Russian-speaking web of roughly 2000–2008.

This project is **not** a generic “retro web” theme. It models distinct Runet archetypes whose information architecture, interaction patterns, density, graphics, and microcopy differed substantially.

## Status

Pre-repository draft.

Historical research for the first seven archetypes is complete enough for v1. The next step is a short visual smoke test before the material becomes the first GitHub release.

## Archetypes

- `narod-2002` — personal, fan, hobby, small community
- `portal-2001-2003` — search/catalog/service portal
- `company-2003-2005` — corporate and institutional sites
- `forum-2003-2006` — web forums
- `blog-community-2004-2007` — diaries, blogs and communities
- `ucoz-2006-2008` — modular constructor sites
- `media-2004-2006` — news and business media

## Proposed repository layout

```text
russian-web-2000s/
├── SKILL.md
├── README.md
├── VALIDATION.md
├── references/
│   └── archetypes/
│       ├── narod-2002.md
│       ├── portal-2001-2003.md
│       ├── company-2003-2005.md
│       ├── forum-2003-2006.md
│       ├── blog-community-2004-2007.md
│       ├── ucoz-2006-2008.md
│       └── media-2004-2006.md
├── assets/
│   └── README.md
└── examples/              # add only selected examples after validation
```

Keep the repository deliberately small.

The research spreadsheet and large source corpus stay outside GitHub. GitHub contains the distilled rules needed by the skill, not the full research process.

## Design philosophy

1. Evidence first, style second.
2. Site type matters at least as much as year.
3. Information architecture is more important than nostalgic decoration.
4. “Old web” does not mean every page uses GIFs, Comic Sans, marquee and counters.
5. Modern UI conventions should not silently leak into historical recreations.
6. Research stops once rules are stable enough to generate convincing results.

## Two implementation modes

`AUTHENTIC` may use historically appropriate layout and interface techniques.

`MODERN_ENGINE` uses modern implementation internally while preserving historical visible behavior and aesthetics.

## Before first GitHub commit

Run the compact validation in `VALIDATION.md`.

Do not build automated test infrastructure. Generate a small set of HTML pages, render screenshots at desktop sizes, review them side-by-side, correct the rule files if necessary, and then create the repository.

## Research artifacts

The working research corpus lives in the project Google Drive and is intentionally not part of the repository.

The repository should remain a usable skill, not become a historical research platform.