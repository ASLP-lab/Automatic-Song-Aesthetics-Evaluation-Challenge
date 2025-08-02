AUDEEG Challenge ICASSP 2023
============================

This repository will generate the website for the AUDEEG challenge for ICASSP 2023.


## Getting started

To install all dependencies, run:
```bash
bash tools/install.sh
```
(You will need `sudo` access)

## Compiling the website

To compile the website, simply run:
```bash
hugo -D
```
The compiled website will show up in the [public](./public) folder.

## Running the website locally

Run:
```bash
hugo -D server
```

## Making adjustments

### The homepage

The general structure for the homepage can be adjusted in [data/homepage.yml](./data/homepage.yml).

#### Extra sections
You can add additional sections by adding markdown documents to [content/homepage_sections](./content/homepage_sections), they will be included automatically.

#### Leaderboard

You can adjust the leaderboard in [content/homepage_sections/leaderboard.md](content/homepage_sections/leaderboard.md).

### Other Pages

You can add pages in [content](./content), and they will automatically show up in the navbar.


## More information

This site is made with [Hugo](https://gohugo.io/), using the [Hugo-chart](https://github.com/Shen-Yu/hugo-chart) and [arcane](https://github.com/half-duplex/hugo-arcana) themes.
