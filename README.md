# Specimen & Signal

Copy-paste prompts for dark, technical motion graphics that look like a measuring instrument.

**Live site:** https://specimen-and-signal.vercel.app

![Specimen & Signal](og.jpg)

13 prompts. Each one is complete on its own: it carries the look (palette, fonts, motion rules) plus one scene. Paste it into Claude or any coding model, fill in the `{braces}` with your narration and beat times, and render the HTML frame by frame.

The look: a near-black background, cream type and hairlines, and one signal orange. Fonts are Anek Devanagari, Archivo, JetBrains Mono, Instrument Serif and Kalam, all from Google Fonts (SIL Open Font License). Paper scenes swap to cream paper, black ink and a red rubber stamp.

## Run locally

It's a single static page with no build step.

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Credits

Stills come from a UPI explainer reel made with these prompts. The film-card still uses *The Gold Rush* (1925), a public-domain film from Wikimedia Commons. The prompts are free to copy and adapt.
