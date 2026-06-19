# Games for Kids 🎮

A small monorepo of fun, friendly browser games for little kids. Each game is self-contained
(plain HTML, CSS, and JavaScript), works offline, and needs no install. Just open it in a browser.

**Play online:** https://dlb2887.github.io/Games-for-kids/

## Games

| Game | Folder | What it is |
|------|--------|------------|
| 🦋 **Butterfly Garden** | [`butterfly-garden/`](butterfly-garden/) | A talking learning game for ages ~4: counting, building-up addition, spelling short words, plus a dress-up sandbox with real butterfly photos and draggable accessories. |

More games will be added as their own folders.

## How it's organized

```
Games-for-kids/
├── index.html            # landing page that links to each game
├── README.md             # this file
└── butterfly-garden/     # one game per folder, fully self-contained
    ├── index.html
    ├── README.md
    └── assets/
```

Each game folder has its own `index.html` (the game) and `README.md` (how it works, credits).
The root `index.html` is a simple landing page linking to every game, and it's what
[GitHub Pages](https://dlb2887.github.io/Games-for-kids/) serves.

## Adding a new game

1. Create a new folder at the repo root (e.g. `space-counting/`).
2. Put a self-contained `index.html` (and any `assets/`) inside it.
3. Add a card linking to it in the root `index.html`, and a row in the table above.
