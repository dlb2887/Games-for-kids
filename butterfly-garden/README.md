# Butterfly Garden 🦋 — Learn & Play

A bright, talking little game for a 4-year-old. Butterflies are the characters, and they show up
everywhere. Three things to do:

- 🌼 **Butterfly Math** — count one group of butterflies, then watch new groups **fly in and add on**
  or some **fly away to take away**, building and changing the total (up to 20), then a big
  celebration and a fresh garden
- 🐝 **Spell Words** — tap the letter-carrying butterflies in order to spell short words
- 🎨 **Dress Up & Play** — just for fun: it shows a **real butterfly photo** you can recolor (tints
  the photo), then add items — 🎩 hat, 🎀 bow, 👑 crown, 🕶️ sunglasses, 🌸 flower, and **dresses**
  (👗 dress, 🥻 fancy dress, 👚 shirt) — and **drag each item anywhere** on the butterfly. Swap for a
  **New butterfly!**, tap the garden to make butterflies sparkle, or hit **Surprise!** / **Make it fly!**

> **Personal project.** This is private and is not part of any work. It just lives here in a
> `personal/` folder.

## How to open it

Double-click **`index.html`** — it opens in any web browser (Chrome, Edge, Safari). No internet
needed, nothing to install. Works great on a tablet or a laptop.

The first time you tap or click, the sounds wake up (browsers require one tap before playing
audio). Tap any butterfly to hear it flap!

## For grown-ups

- **It talks.** The game reads the questions, numbers, and letters out loud using the browser's
  built-in voice, so a child who can't read yet can still play.
- **Sound effects on/off.** Tap the 🔊 button (top-right). It remembers the choice next time.
  Turning effects off keeps the spoken instructions but mutes the chimes/cheers.
- **No timers, no "you lose."** Wrong answers get a gentle "try again." Right answers get a cheer,
  a star ⭐, and a flutter of confetti butterflies.
- **No accounts, no internet, no data collected.** Everything runs right in the browser.

## Make it your own

Open `index.html` in a text editor. Near the top of the `<script>` you'll find easy lists:

- **Words** — edit the `WORDS` array (each is a word + an emoji picture). Add as many as you like.
- **Numbers** — the building-up math lives in `startMath()` / `mathStep()`. Change `CAP_MATH`
  (currently 20) to raise or lower how high the total grows before the garden resets.
- **Butterfly colors** — the `WING_COLORS` array (game butterflies) and `PLAY_COLORS` (dress-up palette).
- **Dress-up accessories** — the `ACCESSORIES` array (emoji + name).

## Pictures

Real butterfly photos live in `assets/photos/`. If they're ever missing, the game automatically
shows hand-drawn butterflies instead, so it always works.

| File | What it is | Source / License |
|------|------------|------------------|
| `butterfly1.jpg` | Monarch butterfly (home hero) | Wikimedia Commons — *"Monarch In May"* (Creative Commons) |
| `butterfly2.jpg` | Common buckeye butterfly (home hero) | Wikimedia Commons — *"Common Buckeye Butterfly"* (Creative Commons) |
| `dressup1.jpg` | Blue morpho (Dress Up) | Wikimedia Commons — *"Blue morpho butterfly"* (Creative Commons) |
| `dressup2.jpg` | Peacock pansy (Dress Up) | Wikimedia Commons — *"Peacock pansy"* (Creative Commons) |
| `dressup3.jpg` | Question mark butterfly (Dress Up) | Wikimedia Commons — *"Question Mark Polygonia"* (Creative Commons) |

The **Dress Up & Play** screen rotates through `dressup*.jpg` (plus the two home photos). If any photo
is missing, that screen automatically falls back to a hand-drawn butterfly, so it always works.

To swap in your own photo, just drop a JPG named `butterfly1.jpg` into `assets/photos/`.

---

Built with plain HTML, CSS, and JavaScript — one self-contained file. Have fun! 🦋
