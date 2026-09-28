# Specimen & Signal

A prompt library for dark, technical motion graphics that read like a measuring instrument: glyph specimens with metric lines, live plots, ray diagrams, wireframes and data readouts, with inverted paper scenes and red rubber stamps.

The prompts come from building a two-minute UPI explainer reel. Claude Opus 5.5 wrote the style system and the scene briefs and did the compositing, and Codex agents wrote the scene code. Paste them into any strong coding model.

**Live site:** https://specimen-and-signal.vercel.app

![Specimen & Signal](og.jpg)

## What's on the page

- **Style system prompt.** Palette, five type roles, the glyph specimen, line weights, motion rules and what to leave to compositing. Paste it first.
- **Component kit prompt.** Builds the reusable instruments once: specimen, plot, spectrogram, wireframe, ray fan, callout, data packet, QR matrix, phone, rubber stamp, ledger.
- **12 scene prompts** with `{PLACEHOLDERS}`, each next to the matching frame from the reel.
- **Finishing recipes.** A compositor prompt (HUD, kick zoom punch, snare micro-shake, cut flash and glitch, bloom, chromatic aberration, vignette, grain), a beat-map prompt, and a Puppeteer + ffmpeg render loop.
- **Fonts and tokens.** Anek Devanagari, Archivo, JetBrains Mono, Instrument Serif and Kalam, plus `#0a0a0b`, `#ff5a1f`, `#ede6da` and `#d1242a`.
- **In the wild.** 20 animations made with Claude Opus 5.5, found by Grok with web and X search on 28 Sep 2026. Every link was checked against X's and YouTube's public embed data. The descriptions are ours; the originals belong to their creators.

## How the pipeline works

Each shot is one HTML page with a single 720×1280 SVG. `window.renderFrame(t)` draws the frame for time `t`, and a headless browser steps through `t = i / 24` at `deviceScaleFactor: 1.5` (1080×1920) while ffmpeg encodes the screenshots. Because nothing depends on real time, any frame renders the same way every time, and the model can preview exactly the moments it needs to check.

## Run locally

It's a single static page with no build step.

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Credits

- Fonts load from Google Fonts and are licensed under the SIL Open Font License.
- Stills and the loop come from the UPI explainer reel the prompts were written for. The reaction-card still uses *The Gold Rush* (1925), a public-domain film from Wikimedia Commons, toned to the palette.
- The prompts on the page are free to copy and adapt.
