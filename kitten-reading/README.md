# Magical Kittens Reading 🐱 — Learn to Read

A talking reading game for a 4-year-old. Three little kittens — **Pip** ⚡🧊, **Luna** ✨ and
**Boots** 💪 — have superpowers, and across **four stories** they beat the Big Bad Wolf, a Big
Bad Dog, and the Sly Fox. Two ways to play:

- 📖 **Read Along** — the stories, one sentence at a time. Slide a finger across the words and
  each one lights up and is read out loud, left to right.
- 🃏 **Kitten Flash Cards** — the 40 sight words from the stories, as two decks (see below).
- ⭐ **Word Wall** — all 40 words; the ones she's mastered light up with a star. Tap any word
  to hear it.
- 🏅 **Badges** — nine kitten badges to collect, including one for each story.

## How to open it

Double-click **`index.html`** and it opens in any browser. It needs internet the **first**
time (it pulls React and Tailwind from a CDN, the same as the other games here); after that
the browser cache usually covers it. Works great on a tablet.

The first tap wakes the voice up — browsers require one tap before they'll play audio.

## The four stories

Pick a story, then a chapter. Chapters unlock in order inside each story, but all four
stories are open from the start — they're separate adventures, and they also run in order if
you want them to.

| # | Story | What happens |
|---|-------|--------------|
| 1 | 🐺 **The Big Bad Wolf** | Meet the kittens, find their powers, and beat the wolf |
| 2 | 🗡️ **The Silver Sword** | A big bad dog comes to town; Pip digs down deep and finds a silver sword |
| 3 | 🧊 **The Ball of Ice** | Pip finds a new power, freezes the dog in a ball of ice, and Boots throws it to the sky |
| 4 | 🐺 **The Wolf Comes Back** | The wolf returns — you finally see his whole body — and the kittens beat him with everything |

Five chapters each, four to six short sentences per chapter, three to five words per
sentence. **Stories 2, 3 and 4 introduce no new sight words** — they re-use the same 40 words
story 1 teaches, so the reading gets longer without getting harder.

The new stories were dictated by a 4-year-old, so the silver sword, the digging, the belly
poke, the ball of ice thrown up to the sky, and the ear-pull are all his.

## Reading

Slide a finger across the sentence and each whole word lights up and is spoken as the finger
touches it — that's the tracking-left-to-right, one-word-at-a-time practice. A plain **tap**
on a word just says that word, and **🔊 Read it to me** reads the whole sentence.

## The two flash card decks

| Deck | How it works | When to use it |
|------|--------------|----------------|
| 🎮 **Play Alone** | A kitten says a word, three word-cards appear, she taps the right one | She can play by herself — the game checks the answer |
| 👨‍👩‍👧 **Read with a Grown-Up** | One big word, she reads it aloud, tap to flip and hear it, then 👍 or 🔁 | Real reading practice, with you listening |

Words unlock as story 1 is read, so the deck grows with her. Three correct in a row masters a
word and lights its star on the Word Wall; missed words come back sooner.

## For grown-ups

- **It talks, and that's the default.** Everything is read out loud so a child who can't
  read yet can still play.
- **Turning speech off.** Tap the 🔊 button (top-right) — same button, same place as
  Butterfly Garden, Princess Learning Adventure and Unicorn Spanish. It remembers the choice.
- **No microphone.** The game speaks; it never listens. No permission prompts.
- **No timers, no losing.** A wrong tap gets *"that one says look — try again!"* and the
  card stays up. Right answers get a cheer and a sparkle.
- **No accounts, no data collected.** Progress is stored only in the browser on this device.

## Pictures

Two kinds, and neither needs a download.

**Drawings.** Four illustrations are drawn in code as inline SVG, so there's nothing to fetch
and nothing to license:

| Drawing | Where it shows up |
|---------|-------------------|
| The Big Bad Wolf, head to feet | Story 4, chapters 2 and 4 — his hands, his feet, the whole wolf |
| The silver sword in the dirt | Story 2, chapters 2 and 4 |
| The big dog in a ball of ice | Story 3, chapters 3 and 4 |
| A kitten in a red cape | Story 1's card |

**Kitten photos** are optional. The game looks for these files and falls back to an emoji
kitten if one is missing, so it always works and never shows a broken image:

| File | Who it is | Fallback | Source / License |
|------|-----------|----------|------------------|
| `assets/photos/kitten1.jpg` | Pip ⚡🧊 (red cape) | 🐱 | *not added yet* |
| `assets/photos/kitten2.jpg` | Luna ✨ (blue cape) | 🐈 | *not added yet* |
| `assets/photos/kitten3.jpg` | Boots 💪 (yellow cape) | 🐈‍⬛ | *not added yet* |

To add real kittens, drop three photos with those names into `assets/photos/` — square-ish
crops of the face work best, since they're shown in a circular frame. Then fill in the
source/license column above, the way `butterfly-garden/README.md` credits its photos.

The villains are emoji (🐺 🦊 🐕) apart from the full-body wolf drawing.

## Make it your own

Open `index.html` in a text editor. Near the top of the `<script>`:

- **The stories** — `STORY_ONE` … `STORY_FOUR`, collected in `STORIES`. Each chapter has
  `sentences`, a `words` list (the sight words it unlocks — leave it `[]` to keep the reading
  level where it is), a `cast`, and an optional `art` key.
- **The kittens** — the `KITTENS` array (names, powers, cape colors, photo paths).
- **The villains** — the `VILLAINS` object.
- **The drawings** — `WolfFullBody`, `SilverSword`, `IceBall` and `KittenHero`, registered in
  the `ART` map. Add a component there and any chapter can use it by name.
- **How many correct in a row masters a word** — `MASTERY_STREAK` (currently 3).

Adding a fifth story is just another array in `STORIES`; chapter ids follow the `s5c1` shape
and progress saved under the old numbering still migrates.

---

Built with plain HTML, CSS and JavaScript in one self-contained file. Happy reading! 🐱
