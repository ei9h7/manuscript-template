# My Book

A book written in plain text and typeset with [Manuscript Maker](https://github.com/ei9h7/manuscript-maker).

> **Starting a new book?** On GitHub, click **Use this template → Create a new repository**, give it the book’s name, and choose **Private**. Then replace the sample text below with your own.

## What’s in here

| File | What it is |
|---|---|
| `manuscript.md` | The chapters. `## 1\|Title\|Subtitle` starts a chapter, each line is a paragraph, `[!callout]` makes a callout box. |
| `frontmatter.md` | The pages before chapter 1: half title, praise, title page, copyright. Each page starts with `[type]`. |
| `book.json` | Layout settings that differ from the defaults: trim size, contents page, fonts, spacing… |
| `.github/workflows/build-book.yml` | Builds the PDF and EPUB on GitHub. |

The sample chapters explain the format as they go. The full reference is in the [Manuscript Maker README](https://github.com/ei9h7/manuscript-maker#manuscript-format).

## Previewing and building in the browser

1. Open Manuscript Maker.
2. In the **GitHub** tab, enter this repository (`owner/repo`), the path `manuscript.md`, and a token. To make the token:
   - [create a fine-grained personal access token](https://github.com/settings/personal-access-tokens/new)
   - under **Repository access**, choose *Only select repositories* and pick this repo
   - under **Permissions**, set **Contents** to *Read-only*
3. Click **Load from GitHub**. `frontmatter.md` and `book.json` load with it. Adjust the layout, preview the spreads, and download the PDF or EPUB.
4. To keep layout changes, click **Download book.json** and commit it here.

## Building on GitHub

- **Any time:** Actions → **Build book** → **Run workflow**. The PDF and EPUB are attached to the run.
- **For a proof or a release:** tag a version, and the files are also attached to a GitHub Release:

  ```sh
  git tag v1.0 && git push --tags
  ```

  Or create a release from the GitHub web page.

## More than one work?

Use one repository per book. That keeps each one’s history, settings and builds separate.

For many small works (stories, essays), one repository with a folder per work also works: `stories/manuscript.md`, `stories/frontmatter.md`, … Enter the folder path in the app, or as the workflow’s *Manuscript* input.

---

The sample text is placeholder content from Manuscript Maker and can be reused freely. Your own writing in this repository is yours.
