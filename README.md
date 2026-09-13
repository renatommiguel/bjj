# BJJ Journal

A personal Brazilian Jiu-Jitsu learning journal.

This repository contains notes about techniques, concepts, mistakes, discoveries, drills, and lessons learned during BJJ training.

The goal is to keep a **simple, searchable, version-controlled record of my BJJ development** using Markdown.

The website is generated from this repository using Jekyll and GitHub Pages.

---

## Repository structure

```text
bjj/
│
├── _config.yml
│
├── _posts/
│   ├── 2026-09-13-side-control-escape.md
│   └── 2026-09-20-knee-cut.md
│
├── _templates/
│   └── post-template.md
│
├── _data/
│   └── taxonomy.yml
│
├── docs/
│   └── taxonomy.md
│
├── assets/
│   └── images/
│
├── index.md
└── README.md
```

### `_posts/`

Contains the actual BJJ journal entries.

Every new learning should normally become a new Markdown post.

Posts are named:

```text
YYYY-MM-DD-short-description.md
```

Example:

```text
2026-09-13-side-control-escape.md
```

The date should normally be the date the lesson was learned, not necessarily the date the post was written.

---

### `_templates/`

Contains templates and other files that should **not be published** on the website.

The main file is:

```text
_templates/post-template.md
```

When creating a new post, copy this template into `_posts/` and rename it.

Do not write journal entries directly in the template.

---

### `_data/`

Contains structured data used by Jekyll.

The main file is:

```text
_data/taxonomy.yml
```

This contains the controlled vocabulary for categories and tags.

It is the reference for deciding how posts should be classified.

---

### `docs/`

Contains documentation about the repository.

For example:

```text
docs/taxonomy.md
```

can explain the meaning of categories and tags in more detail.

This documentation is separate from the actual journal.

---

### `assets/`

Contains files used by the website, primarily images.

For example:

```text
assets/
└── images/
    ├── side-control/
    │   ├── frame-position.png
    │   └── knee-insertion.png
    │
    └── knee-cut/
        └── starting-position.png
```

Keep assets organized by technique or subject rather than putting everything into one large directory.

---

### `index.md`

The website homepage.

It should remain relatively simple and should not contain individual journal entries.

Jekyll automatically uses the posts in `_posts/` to populate the post listing.

---

### `README.md`

This document.

It explains how the repository works and how to maintain it.

The README is primarily for GitHub and is not part of the public journal website.

---

# Creating a new post

Whenever I learn something useful during training, create a new post.

Start by copying:

```text
_templates/post-template.md
```

into:

```text
_posts/
```

Then rename it using:

```text
YYYY-MM-DD-short-description.md
```

Example:

```text
_posts/2026-09-13-side-control-escape.md
```

---

# Post structure

A typical post should contain front matter followed by the actual notes.

Example:

```markdown
---
layout: post
title: "Escaping Side Control: Create Space Before Moving"
date: 2026-09-13
categories:
  - escapes
tags:
  - side-control
  - framing
  - shrimp
  - hip-escape
  - guard-recovery
  - mistake
---

# What I learned

...

# The technique

...

# My mistake

...

# What I need to practice

- [ ] Hip escape
- [ ] Knee insertion
- [ ] Guard recovery

# Drill

...

# Notes from rolling

...
```

The exact sections can change depending on the lesson.

The journal should capture **what was actually learned**, not force every training session into an artificial format.

---

# Front matter

The section between the `---` markers is called front matter.

Example:

```yaml
---
layout: post
title: "Escaping Side Control"
date: 2026-09-13
categories:
  - escapes
tags:
  - side-control
  - framing
  - shrimp
---
```

## `layout`

Normally:

```yaml
layout: post
```

This tells Jekyll to render the entry as a journal post.

Do not normally change this.

---

## `title`

The title shown on the website.

Prefer descriptive titles rather than generic ones.

Good:

```yaml
title: "Stop Pushing From Side Control"
```

Less useful:

```yaml
title: "BJJ Class"
```

The title should describe the actual lesson.

---

## `date`

Use the date the lesson was learned:

```yaml
date: 2026-09-13
```

Use ISO format:

```text
YYYY-MM-DD
```

---

# Categories

Categories describe the **primary subject of a post**.

Use categories sparingly.

A post should normally have **one category**.

Example:

```yaml
categories:
  - escapes
```

If a post genuinely covers two major subjects, two categories are acceptable:

```yaml
categories:
  - guard
  - sweeps
```

Do not use categories for every concept or technique mentioned in a post.

## Category question

Ask:

> "What is this post mainly about?"

The answer should usually be the category.

Examples:

| Post                               | Category        |
| ---------------------------------- | --------------- |
| Learning to escape mount           | `escapes`       |
| Learning a knee cut                | `guard-passing` |
| Understanding frames               | `concepts`      |
| Learning a butterfly sweep         | `sweeps`        |
| Learning a guillotine              | `submissions`   |
| Learning a single-leg              | `takedowns`     |
| Something discovered while rolling | `sparring`      |

---

# Tags

Tags provide more detailed information about a post.

Unlike categories, a post can have several tags.

Example:

```yaml
tags:
  - side-control
  - framing
  - shrimp
  - hip-escape
  - guard-recovery
```

Tags can describe:

* positions
* guards
* techniques
* movements
* concepts
* grips
* training context
* mistakes
* discoveries
* rules
* Gi/no-Gi
* specific systems

---

# Categories vs tags

The simplest rule is:

> **Category = what the post is mainly about.**

> **Tags = everything important involved in the lesson.**

For example:

```yaml
categories:
  - escapes

tags:
  - side-control
  - framing
  - shrimp
  - hip-escape
  - guard-recovery
  - mistake
```

The post is fundamentally about an **escape**.

The tags tell me that the escape involves:

* side control
* framing
* shrimping
* hip movement
* guard recovery

---

# Do not over-tag

Tags should make the journal easier to search.

Avoid meaningless tags such as:

```yaml
tags:
  - bjj
  - jiu-jitsu
  - martial-arts
  - grappling
  - technique
```

These are too broad to be useful.

Prefer:

```yaml
tags:
  - side-control
  - framing
  - hip-escape
  - guard-recovery
```

A good rule is to use roughly **3–8 meaningful tags** per post.

There is no requirement to reach a specific number.

---

# Taxonomy

The official list of categories and tags is maintained in:

```text
_data/taxonomy.yml
```

This provides a consistent vocabulary across the journal.

Before creating a new tag, check whether an appropriate existing tag already exists.

For example, don't create:

```text
sidecontrol
```

if:

```text
side-control
```

already exists.

Don't create:

```text
hipescape
```

if:

```text
hip-escape
```

already exists.

Consistency is more important than having many tags.

---

# Adding a new tag

The taxonomy is not fixed.

If I repeatedly encounter a useful concept that does not exist in the taxonomy, add it.

For example, if I start learning about:

```text
wrist-control
```

and it isn't currently present, add it to `_data/taxonomy.yml`.

Use lowercase and hyphens:

```yaml
- wrist-control
```

Prefer:

```text
wrist-control
```

over:

```text
Wrist Control
```

or:

```text
wrist_control
```

---

# When NOT to create a new tag

Do not create a tag just because a word appears in one post.

For example, if a post briefly mentions:

> "I used my left elbow."

that doesn't mean the post needs:

```yaml
- left-elbow
```

A tag should represent something that is useful for finding related knowledge later.

A useful test is:

> "Would I want to find all my notes about this?"

If yes, it may deserve a tag.

---

# Recommended tag groups

The taxonomy is organized conceptually into several groups.

## Positions

Examples:

```text
mount
side-control
north-south
knee-on-belly
back-control
turtle
front-headlock
```

## Guards

Examples:

```text
closed-guard
half-guard
butterfly-guard
de-la-riva
reverse-de-la-riva
spider-guard
lasso-guard
x-guard
single-leg-x
50-50
knee-shield
z-guard
```

## Passing

Examples:

```text
knee-cut
toreando
leg-drag
long-step
smash-pass
over-under
double-under
body-lock
stack-pass
```

## Escapes

Examples:

```text
mount-escape
side-control-escape
back-escape
guard-recovery
submission-escape
```

## Submissions

Examples:

```text
rear-naked-choke
guillotine
triangle
armbar
kimura
americana
heel-hook
ankle-lock
kneebar
```

## Wrestling / takedowns

Examples:

```text
single-leg
double-leg
ankle-pick
snapdown
body-lock
arm-drag
russian-tie
underhook
overhook
whizzer
```

## Movements

Examples:

```text
shrimp
bridge
technical-stand-up
sit-through
granby
hip-heist
pummeling
framing
```

## Concepts

Examples:

```text
posture
base
balance
leverage
frames
wedges
connection
distance
pressure
alignment
inside-position
outside-position
timing
angles
off-balancing
grips
grip-fighting
```

## Training

Examples:

```text
drilling
sparring
positional-sparring
coach-feedback
mistake
breakthrough
problem
solution
refinement
troubleshooting
game-plan
weak-point
```

## Context

Examples:

```text
gi
no-gi
competition
ibjjf
submission-only
```

---

# Assets and images

Images should live inside:

```text
assets/images/
```

Organize them by subject when there are multiple images.

Example:

```text
assets/images/
└── side-control-escape/
    ├── 01-frame.png
    ├── 02-shrimp.png
    └── 03-knee-insertion.png
```

Use descriptive filenames.

Good:

```text
01-frame-neck.png
02-hip-frame.png
03-shrimp.png
```

Avoid:

```text
IMG_4837.png
Screenshot_2026-09-13.png
image1.png
```

---

# Using images in a post

Images can be referenced from Markdown.

Example:

```markdown
![Side control frame](../assets/images/side-control-escape/01-frame.png)
```

If the site configuration requires an absolute path, use the site's configured base URL instead.

Keep images relevant to the lesson.

The purpose of an image is to clarify the technique, not to make the post visually impressive.

---

# Videos and external resources

If a lesson came from a particular instructional, video, article, or other resource, record it in the post.

Example:

```markdown
## Source

- Coach instruction during class
- Lachlan Giles instructional
- [Relevant video or article]
```

The journal should distinguish between:

* something taught by my coach
* something I discovered myself
* something learned from an instructional
* something inferred or experimented with during rolling

This helps preserve the origin of an idea.

---

# Recording uncertainty

The journal is a record of my learning.

It is **not an authoritative BJJ encyclopedia**.

If I am unsure whether something is correct, say so.

For example:

```markdown
## What I think

I believe the important detail is controlling the hip,
but I need to test this again during live rolling.
```

Useful tags might include:

```yaml
tags:
  - untested
  - needs-drilling
```

Do not present uncertain observations as established facts.

---

# Updating old posts

Posts are historical records.

If I later discover that something I wrote was incomplete or wrong, I should generally **not erase the original learning**.

Instead, add an update.

Example:

```markdown
## Later update — 2026-10-03

After discussing this with my coach, I realized that
the original explanation was incomplete.

The important detail is actually...
```

This preserves the evolution of my understanding.

---

# Journal vs technique knowledge

The journal and consolidated technique knowledge serve different purposes.

## Journal

The journal answers:

> "What did I learn?"

Posts are chronological and personal.

Example:

```text
2026-09-13
I learned that I was using my arms incorrectly
when escaping side control.
```

## Technique reference

A future technique page answers:

> "What do I currently believe about this technique?"

For example:

```text
techniques/
└── side-control-escape.md
```

This page could eventually consolidate information from many journal entries.

The original journal posts should remain unchanged as historical records.

---

# Do not create technique pages too early

Initially, only use `_posts/`.

Do not create a separate technique page simply because a technique appears in one post.

Create a consolidated technique page when:

* I have learned the technique multiple times
* I have refined my understanding
* I have discovered common mistakes
* I have tested it during rolling
* I want a permanent reference

This prevents the repository from becoming unnecessarily complicated.

---

# Naming conventions

Use lowercase filenames with hyphens.

Good:

```text
2026-09-13-side-control-escape.md
2026-09-20-knee-cut.md
2026-10-02-butterfly-sweep.md
```

Avoid:

```text
Side Control.md
SideControl.md
my-new-bjj-note.md
BJJ Class 20 September.md
```

Post filenames should be descriptive but short.

---

# Writing style

Posts do not need to be polished articles.

They are training notes.

It is perfectly acceptable to write:

```markdown
# What I learned

I keep trying to force the knee cut.

Coach pointed out that I'm losing the underhook
before I actually establish the position.

Need to slow down.

# Drill

Start from headquarters.

Get the underhook.

Pause.

Then knee cut.
```

The goal is to preserve useful information, not to produce perfect prose.

---

# What should become a post?

Create a post when something is worth remembering.

Examples:

* A new technique
* A detail that made a technique work
* A mistake discovered during rolling
* Something a coach corrected
* A new conceptual understanding
* A successful combination
* A failed approach and why it failed
* A useful drill
* A recurring problem
* A breakthrough
* A competition lesson
* A question that needs investigation

Not every training session needs a post.

A single training session can also produce several posts if several independent lessons were discovered.

---

# Git workflow

The repository is also a training history.

After creating or updating a post:

```bash
git add .
git commit -m "Add notes on side control escape"
git push
```

GitHub Pages will then rebuild the website.

Use meaningful commit messages.

Examples:

```text
Add side control escape notes
Add butterfly sweep lesson
Update knee cut details
Add new taxonomy tags
Add images for armbar escape
Fix typo in mount escape post
```

---

# Maintenance

Periodically review the repository for:

* Duplicate tags
* Inconsistent spelling
* Unused tags
* Tags that should be merged
* Categories that have become unnecessary
* Missing images
* Broken links
* Incorrect dates
* Posts that need later updates

Do not reorganize the repository simply for the sake of organization.

The primary goal is to make recording BJJ knowledge easy.

---

# Taxonomy maintenance

When adding a new category or tag:

1. Check whether an existing term already covers it.
2. Prefer existing terminology used consistently in BJJ instruction.
3. Use lowercase.
4. Use hyphens between words.
5. Avoid synonyms unless there is a genuine reason to support both.
6. Update `_data/taxonomy.yml`.
7. If the change is significant, update `docs/taxonomy.md`.
8. Update existing posts only when consistency or searchability would materially improve.

Example:

If the repository uses:

```text
side-control
```

do not introduce:

```text
sidecontrol
side-control-position
side-control-positioning
```

for the same concept.

---

# Philosophy

This repository should remain:

* Simple
* Markdown-first
* Git-based
* Searchable
* Easy to maintain
* Easy to write to after training
* Useful years later

Avoid adding technology unless it solves a real problem.

The content is more important than the website.

The repository should make it easier to answer questions such as:

> What have I learned about side control?

> What mistakes do I repeatedly make?

> What escapes have I been working on?

> What techniques need more drilling?

> What did my understanding of this technique look like six months ago?

> Which concepts keep appearing across different techniques?

The long-term goal is not simply to create a BJJ blog.

It is to build a **personal, evolving BJJ knowledge base** from actual training experience.
