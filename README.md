# cyindibee.github.io

Jekyll site for CyIndiBee, served by GitHub Pages at https://cyindibee.github.io.
The main site (news, posts, photos) is the WordPress at https://cyindibee.hpcf.upr.edu/.

## Run locally

Needs Ruby 3.x and Bundler.

```bash
bundle install          # first time only (takes a while)
bundle exec jekyll serve
```

Open http://localhost:4000. Edits reload automatically (restart if you change `_config.yml`).

## Add a publication

1. Create `_publications/<short-name>.md` (copy an existing one).
2. Fill in the front matter: `title`, `authors`, `venue`, `venue_short`, `year`, `date` (used for sorting), `links`, `citation`.
3. Optional: put a figure in `assets/img/publications/` and set `image: /assets/img/publications/<file>.png`.
4. Write a short summary below the `---`.

It shows up automatically on the Publications page (grouped by year), on the home page if it's among the 3 newest, and gets its own page at `/papers/<short-name>/`.

## Add a team member

Edit the `members:` list at the top of `team.md`. Photos go in `assets/img/team/` (square, ~400×400).

## Layout

```
_config.yml           site settings, nav menu, WordPress link
_layouts/             default page + publication page templates
_includes/pub-item.html   one row in a publication list
_publications/        one file per paper
assets/css/style.css  all styles
index.md / team.md / publications.md
```
