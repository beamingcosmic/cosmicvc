# Policies

The two documents Discord asks an app for, kept at the top level so they are easy to find, read and
review — and the ones the Activity serves to members and to reviewers.

| Document | The document | Served at |
|---|---|---|
| Privacy Policy | `docs/privacy.md` | `https://kiwibot.sparked.network/privacy.html` |
| Terms of Service | `docs/terms.md` | `https://kiwibot.sparked.network/terms.html` |

**The markdown is the document.** The HTML the Activity serves is generated from it, so the two can
never say different things:

```bash
node activity/rps/scripts/policies.mjs          # regenerate the served pages
node activity/rps/scripts/policies.mjs --check   # fail if a served page is stale
```

`tests/activity/policies.test.js` runs the same check inside the suite, so an edit to a document that
was never regenerated fails CI instead of drifting quietly.

Two conventions the generator understands, so one file reads correctly in both places:

- a link to the other document is written `terms.md` / `privacy.md` and becomes `/terms.html` /
  `/privacy.html` in the served page;
- the rest is ordinary markdown: headings, paragraphs, lists, bold, italics, links.
