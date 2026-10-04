# Validation

Minimal validation plan before the first GitHub commit.

The purpose is **not** to prove historical accuracy statistically. The purpose is to catch obvious failures in the rule files:

- archetypes collapsing into the same generic retro style;
- modern UI patterns leaking into outputs;
- historical markers being overused as decoration;
- missing information architecture;
- unclear routing between neighboring archetypes.

Do one validation round, fix obvious problems, then stop.

## Test method

Generate one complete desktop homepage per case.

Use:

- `MODERN_ENGINE`;
- fictional brands/names;
- no copied historical logos or screenshots;
- enough real-looking content to fill at least one 1024×768 viewport;
- screenshot at 1024×768;
- optionally inspect at 1366×768 only to ensure the layout does not accidentally become modern-responsive.

Do not create a test framework.

A folder of generated HTML/CSS plus screenshots is sufficient.

## Test set

### A. Fan site: `narod` vs `ucoz`

Same subject for both outputs:

> Russian fan site about a fictional rock band, circa 2007 for uCoz and circa 2002 for Narod. Include news, photos and links to other fan sites.

#### Expected `narod-2002`

- handcrafted author/fan identity;
- irregular section structure;
- personal update notes;
- optional 88×31/friends links;
- guestbook/e-mail plausible;
- design follows the fandom.

#### Expected `ucoz-2006-2008`

- obvious reusable shell;
- news as central module;
- login plus several sidebar blocks;
- poll/calendar/mini-chat or statistics;
- repeated module-style headers;
- explicit material metadata.

#### Failure

The two outputs look like the same template with different colors.

---

### B. Information site: `portal` vs `media`

Same broad subject:

> Russian technology/internet site.

#### Expected `portal-2001-2003`

- search is prominent;
- catalog/rating;
- mail/login or service access;
- weather/currency/other unrelated utility blocks are plausible;
- page acts as an internet start page.

#### Expected `media-2004-2006`

- editorial hierarchy;
- timestamps/newsline;
- lead story;
- rubrics;
- related stories/archive;
- page answers “what happened today?”

#### Failure

The media looks like a search portal or the portal looks like a news publication.

---

### C. Community: `forum` vs `blog-community`

Same subject:

> Community of PDA/smartphone enthusiasts, 2005–2006.

#### Expected `forum-2003-2006`

- category/topic hierarchy;
- author column beside each post;
- ranks, avatars, signatures;
- BBCode/Quote;
- some ICQ/UIN;
- small graphical smilies.

#### Expected `blog-community-2004-2007`

- chronological authored entries;
- userpics;
- friends/community links;
- threaded comments below entries;
- archive/calendar;
- mood/music or similar metadata may appear.

#### Failure

Blog comments look like forum posts or forum content looks like a chronological personal feed.

---

### D. Corporate standalone

Brief:

> Regional Russian internet provider, 2004. Services for households and companies, coverage map, company information, news, vacancies and contacts.

#### Expected `company-2003-2005`

- official representation rather than landing page;
- deep navigation;
- separate customer audiences;
- visible telephone/address;
- news;
- corporate graphics;
- no giant CTA;
- no testimonial/pricing-card SaaS layout.

## Common visual acceptance criteria

Score each output manually as pass/fail.

### 1. Archetype recognition

Could someone familiar with old Runet identify the broad site type without being told its filename?

### 2. Period plausibility

Does the page plausibly fit its target year range?

### 3. Structure before decoration

Would the page still feel period-correct if decorative GIFs/backgrounds were removed?

If not, the skill is relying too much on nostalgia props.

### 4. Modern leakage

Fail if the output prominently contains:

- giant hero;
- rounded card grid;
- glass/blur;
- huge headings;
- mobile-first controls;
- modern reaction bar;
- current SaaS marketing sequence.

### 5. Density

Does the amount of visible content match the archetype?

A dense portal and a personal diary should not receive the same spacing system.

### 6. Microcopy

Do labels sound native to the period and site type?

Examples:

- `Гостевая`, `Карта сайта`, `ICQ`, `Последнее обновление`;
- `Темы`, `Сообщения`, `Последнее сообщение`;
- `Архив`, `Друзья`, `Оставить комментарий`;
- `Добавил`, `Просмотров`, `Наш опрос`;
- `Все новости`, `Пресс-центр`, `Инвесторам`.

### 7. No historical cosplay overload

Fail if every page contains the same collection of:

- counter;
- 88×31 buttons;
- marquee;
- animated GIF;
- tiled background;
- ICQ;
- “best viewed in IE”.

Each feature must come from the selected archetype.

## What to keep after validation

Do **not** commit all generated tests.

Keep only 2–3 especially representative examples if they are useful to users:

```text
examples/
├── narod-fan-page/
├── portal-start-page/
└── forum-topic/
```

Or keep no examples at all for v1 if they add noise.

## Exit criteria for GitHub

Create the repository when:

- all seven archetypes can produce a visibly distinct result;
- the three pairwise confusion tests pass;
- the corporate standalone test passes;
- no systematic modern UI leak remains;
- no archetype requires another broad research pass.

One corrective iteration is enough.

If the first outputs are broadly convincing, do not keep testing for marginal improvements.