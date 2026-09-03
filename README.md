# SYBL public pages

The two pages the app stores require to be reachable on the open web, plus a
small landing page that links to them.

**Nothing here is published yet.** These files exist locally only.

```
site/
  index.html              landing page, links to the other two
  privacy/index.html      privacy policy
  delete-account/index.html   account deletion instructions
  style.css               shared stylesheet, no external requests
  .nojekyll               serve the files as-is, no Jekyll processing
```

## The details these pages state

Every placeholder has been filled in. The values below appear across the pages;
if any of them changes, it has to be changed here too.

| Detail | Value |
|---|---|
| Developer / data controller | SYBL |
| Contact address | adictbart@gmail.com |
| Where the database lives | Ireland (Supabase's West EU region) |
| Last updated | September 3, 2026 |

The stylesheet rule that made an unfilled placeholder glow red has been
removed, since there is nothing left for it to mark.

## Publishing

These files are meant to go in their own **public** repository, not this one.
GitHub Pages on a free account can only serve a public repository, and this
repository is not one — it holds the app source and `docs/DECISIONS.md`, which
describes the security model in detail and is not written for an audience.

The intended layout is a repository named `sybl` under the GitHub account
`syblmotivation`, containing the contents of this folder at its root, with
Pages serving the `main` branch. That produces:

```
https://syblmotivation.github.io/sybl/
https://syblmotivation.github.io/sybl/privacy/
https://syblmotivation.github.io/sybl/delete-account/
```

The last two are what Google Play and App Store Connect ask for.

Note that the links between the pages are relative (`../privacy/`,
`../delete-account/`, `../`), so they resolve correctly under the `/sybl/`
sub-path and would keep working just as well at a custom domain root.
