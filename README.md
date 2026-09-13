# BJJ Journal

A personal journal and knowledge base for Brazilian Jiu-Jitsu.

The repository uses Markdown files for notes and Jekyll/GitHub Pages to publish them as a simple website.

The goal is to record things I learn during training so I can review them, track mistakes, and build my understanding over time.

## Repository structure

```text
bjj/
├── _config.yml
├── _posts/
├── _templates/
│   └── post-template.md
├── _data/
│   └── taxonomy.yml
├── assets/
│   └── images/
├── index.md
└── README.md
```

### `_posts/`

The actual BJJ journal.

Every useful lesson can become a post.

Posts use the format:

```text
YYYY-MM-DD-short-title.md
```

Example:

```text
2026-09-13-side-control-escape.md
```

### `_templates/`

Templates that are not published.

Copy `post-template.md` when creating a new post.

### `_data/taxonomy.yml`

The list of categories and tags used by the journal.

It is a reference to keep naming consistent. Add new terms when necessary.

### `assets/images/`

Images used by posts.

Keep images organized by subject when useful.

### `index.md`

The website homepage.

### `README.md`

Documentation for using and maintaining the repository.

---

# Creating a post

After training, create a new Markdown file in `_posts/`.

Start by copying:

```text
_templates/post-template.md
```

Rename it using the date and a short description:

```text
_posts/2026-09-13-side-control-escape.md
```

Then fill in the front matter and notes.

Example:

```markdown
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
  - hip-escape
  - needs-drilling
---

# What I learned

I learned that I was trying to push my opponent away
instead of creating space with frames.

# The technique

1. Establish the frames.
2. Create space.
3. Shrimp away.
4. Insert the knee.
5. Recover guard.

# My mistake

I was using too much arm strength.

# What I need to practice

- [ ] Framing
- [ ] Hip escape
- [ ] Knee insertion

# Notes from rolling

...
```

The template is a starting point. Sections can be added, removed, or changed depending on what was learned.

---

# Categories

Use a category for the **main subject of the post**.

For example:

```yaml
categories:
  - escapes
```

A post about a sweep:

```yaml
categories:
  - sweeps
```

A post about understanding a general BJJ principle:

```yaml
categories:
  - concepts
```

Normally use one category. Use more than one only when the post genuinely covers multiple subjects.

---

# Tags

Tags describe the specific things involved in the lesson.

For example:

```yaml
tags:
  - side-control
  - framing
  - shrimp
  - hip-escape
  - needs-drilling
```

Use a few meaningful tags rather than tagging every word in the post.

Use the existing terms in `taxonomy.yml` whenever possible.

Use lowercase and hyphens:

```text
side-control
hip-escape
rear-naked-choke
```

rather than creating variations such as:

```text
sidecontrol
Side Control
side_control
```

If a useful tag doesn't exist, add it to `taxonomy.yml`.

The taxonomy is not meant to be exhaustive. It should evolve with the journal.

---

# Images

Store images in:

```text
assets/images/
```

For example:

```text
assets/images/side-control/
    frame.png
    knee-insertion.png
```

Reference an image from a post using Markdown:

```markdown
![Side control frame](/assets/images/side-control/frame.png)
```

Use descriptive filenames.

---

# Updating posts

A post is a record of what I learned at that point in time.

If my understanding changes later, don't necessarily rewrite the original entry.

Add an update instead:

```markdown
## Update — 2026-10-03

After another class I realized that...

```

This preserves the evolution of my understanding.

---

# Maintaining the taxonomy

Keep `_data/taxonomy.yml` small and useful.

Before adding a new term:

1. Check whether an existing term already covers it.
2. Use consistent naming.
3. Prefer lowercase and hyphens.
4. Add a new term when it will be useful for finding related posts later.

Don't worry about making the taxonomy complete.

It is better to have a small, useful taxonomy than hundreds of rarely-used tags.

---

# Git workflow

After adding or changing posts:

```bash
git add .
git commit -m "Add side control escape notes"
git push
```

GitHub Pages will build the website from the repository.

Use descriptive commit messages, for example:

```text
Add side control escape notes
Add butterfly sweep lesson
Update knee cut notes
Add images for armbar
Update taxonomy
Fix post typo
```

---

# Future development

Keep the project simple until there is a real reason to expand it.

Possible future additions include:

* Technique reference pages
* Dedicated drill pages
* Category pages
* Tag pages
* Search
* Training-session summaries
* Links between related techniques
* A way to track techniques that need more drilling
* A more structured personal BJJ knowledge base

These should be added only when the existing Markdown journal shows a need for them.

## Principle

**Train → learn → write it down → review → refine.**

The repository is primarily a record of my BJJ learning, not an attempt to create an authoritative BJJ encyclopedia.
