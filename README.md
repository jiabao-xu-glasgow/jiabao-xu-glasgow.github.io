# The Xu Lab website

Every page here is **generated** from the registry at
`~/Desktop/custom-skills/Jiabao/_landscape/registry/`. Do not edit the HTML or
the stylesheet: the next render overwrites them, and it refuses to run if it
finds a file it did not write, so a hand edit stops the build rather than
surviving it.

To change what the site says, change the registry and re-render:

    cd ~/Desktop/custom-skills/.claude/skills/track-record
    python -m scripts.cli render-site

| What you want to change            | Where it lives                       |
|------------------------------------|--------------------------------------|
| Hero wording, research headings, vacancies | `registry/site.yaml`         |
| Research strands and their detail  | `registry/profile.yaml`              |
| Papers, authors, DOIs              | `registry/publications.yaml`         |
| Funding, awards, dates             | `registry/grants.yaml`               |
| Which papers are "selected"        | `site.yaml: selected_publications`   |
| Which posts are advertised         | `site.yaml: advertised_grants`       |

News is not written by hand at all. It is derived: a paper with a date within
the last year and an award with a decision date become news items on their own.

## Files that are not generated

`assets/img/` and `assets/pdf/` are copied in once and never overwritten, so a
photo swapped in by hand stays swapped in. This README is not generated either.

## Publishing

The site is plain HTML: no Jekyll, no gems, no build step. GitHub Pages serves
it as written, which is what `.nojekyll` asks for. To publish, the contents of
this folder replace the contents of the `jiabao-xu-glasgow.github.io`
repository.

To preview locally, from this folder:

    python3 -m http.server 8000

then open <http://localhost:8000>. Opening `index.html` directly with the
`file://` scheme will not work, because the links are site-absolute.
