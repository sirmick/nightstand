# Nightstand

The shelf of Nighttime Books: picture books made with [Moonpress](https://github.com/sirmick/moonpress)
and read on a Bigme HiBreak e-ink tablet. GitHub Pages serves this repo; the reader app syncs from
`catalog.json`, and the web viewer at https://sirmick.github.io/moonpress/ shows the same pages.

    catalog.json                what the reader syncs: every published book with its content hash
    series/<name>.json          a series: brief, set, shared character or cast, the books it wants
    series/<name>/cast/*.webp   shared reference sheets
    books/<slug>/book.json      the authored book: title, character, palette, pages. Edit freely.
    books/<slug>/state.json     derived: stamps, prompts used, costs, inspection verdicts. Moonpress owns it.
    books/<slug>/src/*.webp     master pictures as the model drew them
    books/<slug>/out/           the device folder the reader downloads
    books/<slug>/view/          the pages with the text panel drawn, for the web viewer and review
    work/                       scratch (raw originals, candidates, review sheets); not committed

Edit `book.json` by hand or through `moonpress serve`, then run the passes from the Moonpress checkout
with `NIGHTSTAND` pointing here, commit, push. Text edits reach the reader without new pictures.
