# Magical Kittens Reading 🐱 — Learn to Read

A talking reading game for a 4-year-old. Three little kittens — **Pip** ⚡, **Luna** ✨ and
**Boots** 💪 — have superpowers, and across five short chapters they beat the Big Bad Wolf 🐺
and the Sly Fox 🦊. Two ways to play:

- 🐾 **Sound It Out** — the story, one sentence at a time. Drag a finger across a word and
  each letter-sound fires as the finger passes it — *"th… r… ee"* — then the whole word blends
  out loud: *"three!"*. Slower dragging means slower stretching, so the child sets the pace.
- 🃏 **Kitten Flash Cards** — the 40 sight words from the story, as two decks (see below).
- ⭐ **Word Wall** — all 40 words; the ones she's mastered light up with a star. Tap any word
  to hear it.
- 🏅 **Badges** — eight kitten badges to collect.

## How to open it

Double-click **`index.html`** and it opens in any browser. It needs internet the **first**
time (it pulls React and Tailwind from a CDN, the same as Princess Learning Adventure);
after that the browser cache usually covers it. Works great on a tablet.

The first tap wakes the voice up — browsers require one tap before they'll play audio.

## The two reading modes

The 🐾/👉 toggle above the sentence switches how dragging works. It remembers the choice.

| Mode | What dragging does | What it practices |
|------|--------------------|-------------------|
| 🐾 **Sound It Out** (default) | Each letter-sound plays as the finger crosses it, then the word blends at the end | Decoding — turning letters into sounds |
| 👉 **Read Along** | Each whole word lights up and is spoken as the finger touches it | Tracking left-to-right, one-to-one matching |

In both modes, a plain **tap** on a word just says the whole word, and **🔊 Read it to me**
reads the whole sentence.

Letter teams are kept together, so `three` sounds out as **th·r·ee** and `ship` as
**sh·i·p** — not letter by letter. A few sight words are irregular on purpose (`said`,
`one`, `come`); their letter sounds are approximate, but the blend at the end always says
the real word.

## The two flash card decks

| Deck | How it works | When to use it |
|------|--------------|----------------|
| 🎮 **Play Alone** | A kitten says a word, three word-cards appear, she taps the right one | She can play by herself — the game checks the answer |
| 👨‍👩‍👧 **Read with a Grown-Up** | One big word, she reads it aloud, tap to flip and hear it, then 👍 or 🔁 | Real reading practice, with you listening |

Words unlock as the story is read, so the deck grows with her. Three correct in a row
masters a word and lights its star on the Word Wall; missed words come back sooner.

## For grown-ups

- **It talks, and that's the default.** Everything is read out loud so a child who can't
  read yet can still play.
- **Turning speech off.** Tap the 🔊 button (top-right) — same button, same place as
  Butterfly Garden and Princess Learning Adventure. It remembers the choice next time.
- **No microphone.** The game speaks; it never listens. No permission prompts.
- **No timers, no losing.** A wrong tap gets *"that one says look — try again!"* and the
  card stays up. Right answers get a cheer and a sparkle.
- **No accounts, no data collected.** Progress is stored only in the browser on this device.

## The story

Five chapters, four to six short sentences each:

1. 🐱 **Three Little Kittens** — meet Pip, Luna and Boots, and their red, blue and yellow capes
2. ✨ **The Magic Powers** — the powers show up
3. 🐺 **The Big Bad Wolf** — the wolf attacks, and gets zapped
4. 🦊 **The Sly Fox** — the fox tries a trick, and it doesn't work
5. 🎉 **The Kittens Win** — the villains run, the kittens celebrate

The story is written so that **all 40 Dolch pre-primer sight words** appear in it — that's
why the capes are red, blue and yellow, and why Pip counts *one, two, three* before zapping.
Reading the chapters is what unlocks the matching flash cards.

## Make it your own

Open `index.html` in a text editor. Near the top of the `<script>`:

- **The story** — the `STORY` array. Each chapter has `sentences` and a `words` list (the
  sight words that chapter unlocks). Add a chapter and it appears in the picker.
- **The kittens** — the `KITTENS` array (names, powers, cape colors, photo paths).
- **The villains** — the `VILLAINS` object.
- **Letter sounds** — `LETTER_SOUNDS` and `DIGRAPH_SOUNDS`. Add a letter team to
  `DIGRAPH_SOUNDS` and every word chunks with it automatically.
- **How many correct in a row masters a word** — `MASTERY_STREAK` (currently 3).

## Pictures

Kitten photos are **optional**. The game looks for these files and falls back to an emoji
kitten if one is missing, so it always works and never shows a broken image:

| File | Who it is | Fallback | Source / License |
|------|-----------|----------|------------------|
| `assets/photos/kitten1.jpg` | Pip ⚡ (red cape) | 🐱 | *not added yet* |
| `assets/photos/kitten2.jpg` | Luna ✨ (blue cape) | 🐈 | *not added yet* |
| `assets/photos/kitten3.jpg` | Boots 💪 (yellow cape) | 🐈‍⬛ | *not added yet* |

To add real kittens, drop three photos with those names into `assets/photos/` — square-ish
crops of the face work best, since they're shown in a circular frame. Then fill in the
source/license column above, the way `butterfly-garden/README.md` credits its photos.

The villains are always emoji (🐺 🦊) — cartoon villains mix better with cartoon superpowers
than photos would.

---

Built with plain HTML, CSS and JavaScript in one self-contained file. Happy reading! 🐱
