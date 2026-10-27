# forgetting.fyi

The Forgetting whitepaper: one hand-written HTML file, no build step, no
JavaScript, no external requests. Served by GitHub Pages from this `docs/`
directory on `main`, with the custom domain in `CNAME`.

Unlike particulars.fyi and intentions.fyi, this page is not an introduction
to something kept elsewhere. `index.html` is the paper, and the only copy of
it. `whitepaper.md` at the root is a stub pointing here; its git history holds
the paper up to the move. Edit the prose in `index.html`.

Nothing in the paper is normative. Anything it says about what particulars or
intentions does must agree with that format's README on `main`.

## Editing

- One block element per paragraph (`<p>`, `<li>`), wrapped near 78 columns,
  so that a one-word fix diffs as one or two lines.
- No inline `style` attributes. The markup is limited to `p`, `em`, `strong`,
  `code`, `a`, `ul`, `table`, `aside class="draft-note"` and `h2`/`h3`.
- A draft note is
  `<aside class="draft-note"><p class="label">Draft note</p> … </aside>`.
- Cross-references to other sections link to their ids, as in
  `<a href="#gaps">section 8</a>`.
- Typographic quotes and apostrophes are written as characters (`“ ” ’`), not
  entities.

## Section ids

These are the page's deep-linking interface. They are chosen by hand and do
not change when a heading is reworded. Add new ones; don't rename these.

| id | Section |
|---|---|
| `summary` | Summary |
| `why-forget` | 1. Why forget |
| `overthinker` | The overthinker |
| `active-forgetting` | Active forgetting |
| `ready-to-hand` | The ready-to-hand |
| `becoming` | Becoming who you are |
| `what-the-store-needs` | What this asks of the store |
| `memory` | 2. Memory, briefly |
| `why-agents-forget` | 3. Why agents forget, and why it matters to the person |
| `provenance` | 4. The provenance spine |
| `semantic` | 5. Semantic memory: particulars |
| `prospective` | 6. Prospective memory: intentions |
| `surfacing` | What surfaces with a breakdown |
| `how-they-meet` | 7. How they meet |
| `gaps` | 8. The gaps |
| `episodic` | Episodic memory |
| `procedural` | Procedural memory |
| `measuring` | 9. Measuring it |
| `open-questions` | 10. Open questions |
| `references` | References |

## Deployment

Repository settings → Pages: source **Deploy from a branch**, branch `main`,
folder `/docs`, custom domain `forgetting.fyi`, **Enforce HTTPS** once the
certificate is issued.

## DNS (for forgetting.fyi)

Apex `A` records, all four GitHub Pages addresses, DNS-only (grey cloud, if
the zone is on Cloudflare) so GitHub can issue the certificate:

```
forgetting.fyi.  A  185.199.108.153
forgetting.fyi.  A  185.199.109.153
forgetting.fyi.  A  185.199.110.153
forgetting.fyi.  A  185.199.111.153
```

Optional: `www` as a `CNAME` to `nodelogicau.github.io` (GitHub redirects it
to the apex once the custom domain is set).

Every other subdomain is deliberately left free.
