# Trust3R · ICML 2026 — project page

Static project page for **Trust3R: Unifying Feed-Forward Pointmap Prediction
and Evidential Learning for Trust-Aware 3D Reconstruction** (ICML 2026,
Seoul, South Korea).

## Layout

```
website_release/
  index.html
  static/
    css/index.css
    images/   <- PNG/JPG figures, see PLACEHOLDERS.txt
    videos/   <- MP4 clips for the carousel, see PLACEHOLDERS.txt
    js/       <- reserved for future carousel/before-after scripts
```

Bulma 0.9.4, FontAwesome 6.4, Academicons, Inter, and JetBrains Mono load
from public CDNs — no build step. Preview locally with:

```bash
python -m http.server -d website_release 8000
```

then open <http://localhost:8000>.

## Design choices

- **Palette.** Deep teal (`#0e7c86`, trust / probability) accented with warm
  coral (`#ef6c5b`, risk / over-confidence). Title letters **T** and **3R**
  use a teal→coral gradient mask; the section dividers and headline numbers
  reuse the same gradient.
- **Hero.** Soft radial gradient on the hero, ICML 2026 pill badge above the
  title, all five action buttons (Paper / arXiv / Video / Code /
  Checkpoints) rendered as dark pill buttons.
- **Highlight cards.** Three large numbers (25% AURC↓, 41% AUSE↓,
  single-pass cost) directly under the teaser figure, lifted from
  Table 1 / Table 3 of the paper.
- **Sections.** Standard ICML-style flow: teaser → highlights → abstract →
  carousel → method → results → qualitative comparisons → cross-architecture
  (VGGT) → downstream (Tricky24) → video → BibTeX → footer.

## Figure / video placeholders

All `<img>` and `<video>` srcs use `PLACEHOLDER_*` filenames. The image
filenames mirror the paper's figure numbers (`fig1_teaser`, `fig2_pipeline`,
`fig3_risk_coverage`, `fig4_qualitative_scannetpp`, `fig5_tricky24_thermos`,
`fig6_tricky24_toilet`, `fig7_qualitative_indoor`,
`fig8_qualitative_outdoor`) so you can usually export them directly from
the LaTeX source. See [static/images/PLACEHOLDERS.txt](static/images/PLACEHOLDERS.txt)
and [static/videos/PLACEHOLDERS.txt](static/videos/PLACEHOLDERS.txt).

The main YouTube embed in the "Video" section points to `about:blank` —
swap that for the real `https://www.youtube.com/embed/...` URL once the
paper video is uploaded.

## Things to fix before going public

1. Update the five hero buttons (Paper / arXiv / Video / Code / Checkpoints)
   with real URLs.
2. Replace every `PLACEHOLDER_*` image and video in `static/images/` and
   `static/videos/`.
3. Swap the YouTube iframe `src` for the real embed URL.
4. Update the BibTeX block once PMLR proceedings pages / volume are final.
5. Add author homepage links (currently `#`).
