# melo · your little music pet

A tiny, self-contained web widget: a little pet you drop music files on. It listens
via the Web Audio API, analyzes the sound (loudness, brightness, beat activity), and
reacts with moods, colors, and chat — asking about your songs and slowly learning
your taste.

## Run it

Just open `index.html` in any modern browser. No build step, no server, no dependencies.

If deployed on GitHub Pages, the pet is the site itself — just visit your
`github.io` URL.

## How it works

- **Listening** — an `AnalyserNode` reads the waveform and frequency data every frame
- **Features** — energy (RMS), brightness (spectral centroid), beat spikes (spectral flux), all smoothed over time
- **Moods** — happy / excited / chill / sad / sleepy, with a 1-second dwell time so moods don't flicker
- **Personality** — a rule-based chat engine that reacts to the music, asks questions, remembers answers, and builds a taste profile from every song you play

## Embed it

Copy the `.pet-card` markup, its CSS, and the `<script>` block from `index.html` into any page.
