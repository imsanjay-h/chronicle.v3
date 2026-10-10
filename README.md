# Chronicle

> *"Some stories entertain us. Others quietly rearrange something inside us."*

My personal corner of the internet — a quiet, cinematic place where I keep the films, anime, and stories that became part of me.

**Live:** [imsanjay-h.github.io/chronicle.v2](https://imsanjay-h.github.io/chronicle.v2)

---

## What this is

Not a portfolio. Not a catalogue. Just a collection of the things I love, discover, and keep coming back to.

Built by hand. No frameworks. No build step. No tracking. Just HTML, CSS, and JavaScript — designed to feel like a warm-lit room at 3am, with old film grain, an amber lamp, and dust in the projector beam.

---

## The pages

| Page | What lives there |
|---|---|
| **Home** | The intro. Who I am, what I'm into, and doors into the rest |
| **About** | A proper introduction. Currently watching / reading / learning. Favourite genres |
| **Movies** | Five tiers — *The Immortals*, *Works of Art*, *Stayed With Me*, *A Good Time*, *Didn't Connect* — plus recently watched and watchlist |
| **Anime** | S-Tier, currently watching, completed, plan-to-watch, and manga |
| **Connect** | Everywhere I exist on the internet, in one place |

---

## The tiers

Films are sorted into five tiers, based on feeling rather than rating:

```
01 · THE IMMORTALS     Films that become part of you. The ones you carry for years.
02 · WORKS OF ART      Exceptional filmmaking, storytelling, performances, or ideas.
03 · STAYED WITH ME    Films that made you feel something or left you thinking.
04 · A GOOD TIME       Enjoyable, entertaining, and absolutely worth watching.
05 · DIDN'T CONNECT    Films that simply weren't for you. No need to pretend otherwise.
```

---

## The feel

- Dark cinematic theme — warm ink black, cream text, amber accents, cold frost highlights on hover
- Playfair Display for headlines, Inter for body, JetBrains Mono for detail
- Layered atmosphere — projector glow, vignette, animated film grain, drifting dust, optional scanlines
- Custom cursor, page transitions, scroll reveal, poster modal on click
- Fully responsive — phone, tablet, desktop

---

## File structure

```
Chronicle/
├── index.html              Home
├── about.html              About
├── movies.html             Movies
├── anime.html              Anime
├── connect.html            Connect
├── README.md               This file
└── assets/
    ├── style.css           All styling
    ├── script.js           Nav, modal, scroll reveal, tabs
    ├── effects.js          Cursor, dust particles, transitions, sound
    ├── movies-data.js      Every film, sorted into tiers
    └── anime-data.js       Every anime, sorted by status
```

---

## Adding new content

### A new film

Open `assets/movies-data.js`, find the right tier, and add an entry:

```js
{ t: "Film Title", y: 2024, r: 4.5, d: "Director", note: "Your thoughts" }
```

- `t` — title
- `y` — year
- `r` — rating (0.5 to 5, in 0.5 steps)
- `d` — director (optional)
- `note` — your review/thought (optional, shows in the modal)

### A new anime

Open `assets/anime-data.js` and add to the right section. For S-Tier and Completed:

```js
{ t: "Anime Title", e: 12, r: 100, note: "Optional note" }
```

- `e` — episode count
- `r` — AniList score (out of 100)

### A new link

Open `connect.html` and copy any `connect-card` block, then change the platform, handle, and href.

---

## Deployment

Hosted on **GitHub Pages** — free, forever, no build step.

### To update the site

1. Edit the file directly on GitHub (click file → pencil icon → commit), **or** re-upload the changed file
2. Wait ~30 seconds
3. Refresh the live URL

That's it. No commands. No deploy pipeline. Just files.

### First-time setup (already done)

1. Create a public repo
2. Upload all files
3. Settings → Pages → Source: `main` branch → `/ (root)` → Save
4. Wait a minute. Live at `https://<username>.github.io/<repo>`

---

## Notes on the data

Film ratings and history come from my Letterboxd export. Anime data comes from my AniList export. I update the files by hand whenever I add something new.

No APIs. No external services. No analytics. Everything is a static file — it loads instantly and works offline.

---

## Credits

- Fonts: [Playfair Display](https://fonts.google.com/specimen/Playfair+Display), [Inter](https://fonts.google.com/specimen/Inter), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) — all via Google Fonts
- Icons: unicode
- Everything else: written from scratch

---

*fin.*
