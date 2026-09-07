# Effective Altruism St. Andrews — Website

This is a [Jekyll](https://jekyllrb.com) site: plain HTML/Markdown pages,
no complicated framework, built to be easy for a non-coder to update.

## File map (where to find things)

| I want to change...             | Edit this file                          |
|----------------------------------|------------------------------------------|
| The top menu links                | `_data/nav.yml`                          |
| Homepage text / hero / accordion  | `index.md`                               |
| Events page content                | `pages/events.html`                     |
| STAIR page content (incl. weeks)   | `pages/stair.html`                      |
| Arete Fellowship page content       | `pages/arete.html`                     |
| Footer "get involved" text/button   | `_includes/footer.html`                |
| Colors, fonts, spacing              | `assets/css/style.css`                 |
| Site name / description             | `_config.yml`                          |
| Hero photo                          | replace `assets/images/hero-photo.jpg` |

Every file above has comments at the top explaining what's safe to edit.

## Adding a new page

1. Copy an existing file in `pages/` (e.g. `arete.html`) and rename it.
2. At the top, change the `title:` and `permalink:` in the three dashed lines.
3. Edit the content below.
4. Add it to the menu in `_data/nav.yml` if you want it in the nav bar.

## Adding a dropdown/accordion section (e.g. a new "week")

Look at the `<details class="accordion-item">...</details>` blocks in
`index.md` or `pages/stair.html`. Copy a whole block, paste it where you
want the new item, and change the text inside `<summary>` (the title)
and `<p>` (the description).

## Running the site locally (to preview changes before publishing)

You'll need [Ruby](https://www.ruby-lang.org) installed once, then:

```bash
bundle install       # installs Jekyll and dependencies (first time only)
bundle exec jekyll serve
```

Then open **http://localhost:4000** in your browser. The preview
auto-refreshes when you save a file.

## Publishing changes

This site is meant to be connected to GitHub, with Cloudflare Pages (or
GitHub Pages) set to auto-deploy on every push:

```bash
git add .
git commit -m "Describe what you changed"
git push
```

A few minutes after pushing, the live site updates automatically —
no separate "publish" step needed.

## Deployment setup (one-time, for whoever sets this up)

**Cloudflare Pages:**
1. Push this folder to a GitHub repository.
2. In Cloudflare dashboard → Pages → Create a project → Connect to Git.
3. Build command: `bundle exec jekyll build`
4. Build output directory: `_site`
5. Add your custom domain (e.g. eaoxford.com) under the project's
   Custom Domains tab, and update your domain's DNS as instructed.

**GitHub Pages (alternative):** GitHub Pages supports Jekyll natively —
just enable Pages in the repo settings, no build command needed.
