# Memento Mori

A self-contained "weeks of your life" widget. Enter your birthday, set a lifespan
(defaults to 80 years), and your life is illustrated as a grid where **1 row = 1 year**
and **1 square = 1 week**.

![preview](assets/preview.png)

## Features

- **Birthday + lifespan input** — type your date of birth and how many years you expect to live.
- **Weeks-of-life grid** — 52 squares per row, one row per year. Lived weeks are filled,
  the week you're in now pulses red, and remaining weeks stay dim.
- **Live stats** — current age, weeks lived, weeks remaining, and percent of life completed,
  plus a progress bar.
- **Color-coded life eras** — define phases of your life (e.g. school, college, a job) with a
  label and color. Each era's start/end accepts either an **age** (`18`) or a **date** (`2020-08`),
  and `now` marks an ongoing era. Lived weeks show the era color at full strength; future weeks in
  a planned era are faded so "lived vs remaining" stays clear. The legend builds itself from your
  eras, and hovering any square shows its date, age, and era.
- **Decade markers** — a subtle outline every 10 years for orientation.
- **Remembers you** — your birthday and lifespan are saved in the browser (`localStorage`),
  so it's there next time.
- **Responsive** — the grid scales to its container, so nothing gets cut off.

## Use it

Just open `index.html` in any browser. No build step, no dependencies.

## Embed in Notion / Life OS

This is a single HTML file, so it embeds anywhere that accepts an iframe/URL:

1. Host `index.html` (e.g. GitHub Pages, Netlify, Vercel, or any static host).
2. In Notion, type `/embed`, paste the hosted URL, and resize the block.

Because it's one file, you can also drop it into any static host by copying `index.html` alone.

## Customize

All colors live in the `:root` CSS variables at the top of `index.html`
(`--lived`, `--current`, `--future`, `--accent`, etc.) — tweak to match your theme.
