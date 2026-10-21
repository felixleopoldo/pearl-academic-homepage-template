# pearl-academic-homepage-template

A Jekyll template that faithfully recreates the retro academic-homepage look of
[Judea Pearl's homepage](https://bayes.cs.ucla.edu/jp_home.html) — olive sidebar,
ivory content pane, navy headings, standard blue links, "(R-N): [pdf]"
bibliography-style publication list, numbered-icon lecture markers — rebuilt as
a modern, frame-free Jekyll site (no actual `<frameset>`) so it's responsive,
accessible, and easy to fork, theme, and deploy on GitHub Pages.

**[Live demo →](https://felixleopoldo.github.io/pearl-academic-homepage-template/)**

![Preview](docs/preview.png)

## Use this template

1. Click **"Use this template"** on GitHub (or fork the repo).
2. Rename the repo to `<your-github-username>.github.io` if you want it served at
   the root of your GitHub Pages domain (otherwise it'll be served under
   `https://<username>.github.io/<repo-name>/`).
3. Edit `_config.yml`:
   - `title`, `author.*` (name, position, affiliation, email)
   - `url` (leave `baseurl` blank — the workflow sets it automatically based
     on whether your repo is a `username.github.io` root site or served
     under a subpath, so it works either way without editing)
   - `nav`, `social`, `news`, `reviewer_for`
4. Edit `index.md`, `bio.md`, `publications.md`, `talks.md`, `software.md` with
   your own content.
5. (Optional) Add a profile photo to `assets/images/` and point
   `author.photo` at it in `_config.yml`. If left empty, a circular avatar
   with your initials is shown instead.
6. In your repo's **Settings → Pages**, set **Source** to **GitHub Actions**.
7. Commit and push to `main` — the included workflow
   (`.github/workflows/pages.yml`) builds the site with current Jekyll 4.x
   and deploys it automatically on every push.

## Run locally

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Structure

```
_config.yml       site settings, nav, social links, news items
_layouts/         default.html — sidebar + content wrapper
_includes/        sidebar.html
assets/css/       style.css — single stylesheet, the retro Pearl-homepage palette
assets/images/    01-g.gif..04-g.gif — numbered lecture-marker icons
index.md          home page (intro, current position, research interests, news, reviewer-for)
bio.md            positions & education
publications.md   "(R-N): [pdf]"-style reference list
talks.md          talks list, incl. numbered-icon "Selected Lectures"
software.md       software/projects list
```

This uses current Jekyll 4.x (not the legacy `github-pages` gem, which pins
Jekyll/Liquid versions too old to run on modern Ruby) and deploys via the
included GitHub Actions workflow rather than GitHub's legacy Jekyll build —
set Pages source to "GitHub Actions" in repo settings, as above.

## Assets

`assets/images/0{1,2,3,4}-g.gif` are the small numbered icon markers from the
original Judea Pearl homepage, carried over as-is for the "Selected Lectures"
list style on the Talks page.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, strip the credit line if you want;
a mention of the original Judea Pearl homepage inspiration is appreciated but not required.
