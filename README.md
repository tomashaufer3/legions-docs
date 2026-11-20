# The Fateful Adventures of the Good Soldiers — project documentation (unlisted)

Generated documentation for a CERGE-EI master's thesis on desertion in the
Czechoslovak Legions (WWI): pipeline, variable construction, data sources, live
descriptives and QA. **Aggregates and methodology; individual records appear only
as record ids, never names.**

- Open **`index.html`**, straight from disk or through GitHub Pages. It needs the
  folders beside it: `pages/` (one file per page, loaded when you open it),
  `scripts/` (one per pipeline script), `images/` (the figures, loaded when their
  fold opens), plus `search.js` (loaded on the first search) and `facts.json`
  (every number the build fills in, with its source).
- Where a few records are listed (the senior officers of the rank bridge; on
  *Birthplace*, up to 20 sampled records per refusal reason, with the place strings
  as written), they are listed by their csol.cz or VÚA record id, never by name.
- It carries a `noindex, nofollow` meta tag, so search engines will not list it —
  it is meant to be shared **by link**, not discovered.
- Built from a private source repository by `utils/docs/build_docs.py`; do not edit
  anything here by hand — regenerate and replace it.

To update, in the source repo:

1. Rebuild: `DOCS_NOINDEX=1 python utils/docs/build_docs.py`.
2. Copy the whole site here: `python utils/docs/publish_docs.py --write`. It adds,
   replaces and removes only the site's own files (`index.html`, `search.js`,
   `facts.json`, `pages/`, `scripts/`, `images/`) and leaves this README and `.git`
   alone. Without `--write` it prints what would change.
3. Commit and push here.
