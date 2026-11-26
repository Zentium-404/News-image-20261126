# News-image-20261126

[![ contests | make.fun ](https://img.shields.io/badge/contest-make.fun-blue)](https://make.fun/bounty/news-image-20261126)
[![ build | pure python ](https://img.shields.io/badge/build-pure_python-green)](https://make.fun)
[![ entry | 1024x1024 png ](https://img.shields.io/badge/entry-1024x1024_PNG-orange)](https://make.fun)

Sum up the world's news of **Thursday 26 November 2026** in one 1024×1024 image, for the make.fun contest [news-image-20261126](https://make.fun/bounty/news-image-20261126).

## The entry

`main.py` (Python 3.13, stdlib only, no network) draws a broadsheet front page of the day's news:

- **Masthead** — THE WORLD ON ONE PAGE · Thursday 26 November 2026, with a numbered kicker bar of the day's three biggest stories
- **THE DAY IN UTC** — an hour-by-hour timeline of the day (12 entries, red bold times) with a Natural Earth 110m coastline map
- **IN NUMBERS** — six big figures: 20% tariffs, $95 Brent, −1.48% Nasdaq, +424 Dow, $115.8bn Nvidia revenue, 2-2 Sporting
- **Hero band** — four regional leads with coloured region tags (Middle East, China, United States, Markets)
- **Region tally strip** — counts per region
- **THE GRID** — six more stories from the wire
- **ALSO ON THE WIRE** — 16 further stories in two columns
- **Methodology footer**

35 stories in all, every one first reported or advancing on 26 November 2026. Sources named on the page (BBC, Khaleej Times, Xinhua, AP, Reuters, CNBC, ESPN, local desks).

## Engineering

No images, no fonts, no libraries: the program rasterises its own type from embedded glyph outlines (a DejaVu Sans subset), draws its own coastlines (Natural Earth 110m land rings), and writes its own PNG (zlib + CRC32). Even-odd scanline fill, XOR across contours so letter holes work. Deterministic: two runs produce byte-identical output.

## Run

```bash
python3 main.py        # writes out/entry.png
```

`MAKEFUN_OUTPUT_DIR` overrides the output directory.

## License

MIT — see [LICENSE](LICENSE).
