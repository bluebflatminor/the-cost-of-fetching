# the cost of fetching

A one-screen explainer, built so a teenager gets it in ten seconds:
**doing the math is nearly free — going to *get* the numbers is what costs.**

Open `index.html` (or visit the Pages link). Five everyday computer jobs are drawn at
the *same* scale. By default the four arithmetic/cache jobs are near-invisible slivers
beside a wall of DRAM — that gap is the whole point. A toggle lets you "zoom in on the
cheap ones" (a log scale), and the toggle teaches its own lesson: you have to *distort*
the chart to see them, because in true proportion they really are that small.

## Why it matters

The intuition most people carry — that a computer's energy goes into *computing* — is
backwards. The arithmetic is almost free; the energy goes into **moving data** to where
the math happens. Fetching one number from main memory costs hundreds of times more than
adding two numbers, and that ratio is why data centres and AI training burn the power
they do. The chart is a gut-level handle on that fact.

## The numbers

Energy per operation on 45&nbsp;nm CMOS, from the standard reference figures
(Horowitz, *Computing's Energy Problem*, ISSCC 2014; Dally):

| operation | energy |
|---|---|
| add two integers (8-bit) | ~0.03 pJ |
| add two floats (32-bit) | ~0.9 pJ |
| multiply two floats (32-bit) | ~3.7 pJ |
| read from cache (SRAM, 32-bit) | ~5 pJ |
| read from main memory (DRAM, 32-bit) | ~640 pJ |

A DRAM read is roughly **700×** a floating-point add. The "money tag" in the page
(≈1¢ … ≈$7) is an anchor for intuition, not a literal price. The deeper twist, worth
knowing: across process generations the compute energy fell while the DRAM-access energy
stayed roughly flat — so the gap widened over time. There is no free lunch; the cost just
moved to the part nobody pictures.

## Notes

- Pure HTML/CSS/JS, no dependencies, no network. Open the file or host it on GitHub Pages.
- Adapts to light or dark mode so the text always contrasts with the background.

CC0 — public domain. Reuse it in a classroom, a slide, anywhere.
