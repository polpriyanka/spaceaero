# How to edit spaceaero.org yourself

Everything is edited on **github.com/polpriyanka/spaceaero**, in the browser.
After you click **Commit changes**, the live site updates in 1–2 minutes.
If you don't see the change, refresh with **Cmd + Shift + R**.

Basic steps for any file: **click the file → click the pencil icon (✏️) → edit → Commit changes.**

---

## 1. Change homepage text (tagline, About, Plan boxes, footer)

Open **`_data/home.yml`**. Every piece of homepage text is there, in quotes.

- Change the words inside the quotes. **Keep the quotes.**
- To add a Plan box, copy a `- title:` / `text:` pair and edit it. Keep the same indentation (spaces).

## 2. Edit an existing build log or article

- Build logs are in the **`_logs`** folder.
- Articles are in the **`_posts`** folder.

Open the file, click the pencil, edit the text below the `---` lines, commit.

## 3. Add a new build log

1. Open the **`_logs`** folder → **Add file → Create new file**.
2. Name it like `02-short-name.md` (e.g. `02-b6-4-flight.md`).
3. Paste this, fill it in, and commit:

```
---
layout: article
title: "Log 02: Your title"
date: 2026-12-01
number: 2
tags: [b6-4, flight data]
summary: "One or two sentences shown on the homepage."
---

## First section heading

Write here. Leave a blank line between paragraphs.
```

`number` controls the order on the homepage (0, 1, 2, 3...).

## 4. Add a new article

1. Open the **`_posts`** folder → **Add file → Create new file**.
2. Name it `YYYY-MM-DD-short-title.md` (e.g. `2026-12-05-why-rockets-weathercock.md`). The date in the name is the article's date.
3. Paste this, fill it in, and commit:

```
---
layout: article
title: "Your article title"
summary: "One sentence shown on the homepage."
---

Write here.
```

## 5. Add a photo

1. Open the **`images`** folder → **Add file → Upload files** → drag in the photo → commit.
   (Use simple names with no spaces, e.g. `alpha-iii-build.jpg`.)
2. In a log or article, put this line where the photo should appear:

```
![Short description of the photo](/images/alpha-iii-build.jpg)
```

## Formatting cheat sheet

| You type | You get |
|---|---|
| `## Heading` | Section heading |
| `**bold**` | **bold** |
| `- item` | Bullet point |
| `1. item` | Numbered list |
| `[link text](https://...)` | A link |

## If something breaks

If the site stops updating after a change, a quote, dash or space in the top `---` block is usually the cause. Open the repo's **Actions** tab to see the error, or undo your last change from the file's **History**.

Don't edit or delete: `CNAME`, `_config.yml`, `_layouts`, `assets`.
