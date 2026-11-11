# TransMeme — OMEGA Lab project page

Project page for **TransMeme: A Multi-Agent Framework for Cross-Cultural Meme Transcreation**
(ACM Multimedia 2026), in the OMEGA Lab style.

- Paper: <https://arxiv.org/abs/2608.27127> · <https://doi.org/10.1145/3767308.3836278>
- Code: <https://github.com/Jingyi62/TransMeme>
- Page: <https://omega-hkustgz.github.io/projects/transmeme/> (live once the lab site lists it)

## Working on the page

The page is `index.html` plus `assets/`; there is no build step. Rules for agents are in
[`AGENTS.md`](AGENTS.md).

```sh
node tools/check.mjs     # what CI runs
node tools/serve.mjs     # look at it locally
```

Every pull request gets a preview link, posted on the pull request. A push to `main` asks the
lab site to republish.

## Sources

Everything on the page comes from public material. Keep this list current.

| On the page | Source |
| --- | --- |
| Title, authors, affiliations, text | arXiv 2608.27127v1 (27 Aug 2026), the camera-ready for ACM MM 2026. The text paraphrases the abstract and Sections 2–4; it adds no claims. The paper prints affiliations under each name; the superscript numbers are the page's rendering of them. |
| Venue and DOI | The arXiv record ("Accepted at the 34th ACM International Conference on Multimedia (ACM MM 2026)", related DOI 10.1145/3767308.3836278) and the ACM reference block in the paper. The DOI resolves to dl.acm.org (checked 2026-11-10). |
| `overview.webp`, `llm-results.webp`, `cases.webp` | Figs. 1–3 of the paper, rendered from the arXiv source PDFs at 2400 px wide (`pdftoppm`, then `cwebp -q 90`). `social.jpg` is Fig. 1 on a 1200 × 630 canvas for link previews. The lab site's cover image (`transmeme-cover.png`, supplied by the author) is the same drawing as Fig. 1; the page uses the paper's vector version instead. |
| Human-evaluation table, headline numbers | Table 3, the abstract and Sections 4.1–4.4 of the paper, copied from the LaTeX source. Where the introduction and Section 4.3.1 differ in the last digit (4.180 / 2.839 against 4.177 / 2.838), the page uses Section 4.3.1, which matches the per-dimension scores. |
| Code availability line | The public repository's README (commit `c3f01b6`): pipeline, scripts for systems M, A1–A4 and B1–B3, annotation UI, and `results/m_transmeme_1000/`. |
| Evidence labels | None. The page has no demos section; the memes in Figs. 1 and 3 are source memes and generated outputs, described as such in the caption. |

Not on the page because no public material exists: a demo video or interactive demo, the
DPO-trained Rewriter weights and the preference corpus used to train them. The alignment table
(Table 2), the rewriter-quality chart (Fig. 4) and the full component analysis are left to the
paper.
