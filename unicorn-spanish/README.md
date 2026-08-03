# Unicorn Spanish 🦄 — Count & Match

A talking Spanish game for a 4-year-old who speaks English. Three unicorns —
**Estrella** (Star), **Luna** (Moon) and **Arcoíris** (Rainbow) — teach counting and first
words. Two modules:

- 🔢 **Count in Spanish** — count from uno all the way to cien, in three steps.
- 🧠 **Memory Match** — every pair is one **English** card and one **Spanish** card for the
  same thing. Match `moon` to `luna`.
- ⭐ **Number Ladder** — all 28 numbers the game teaches; mastered ones get a star. Tap any
  number to hear it.
- 🏅 **Badges** — eight unicorn badges to collect.

## How to open it

Double-click **`index.html`** and it opens in any browser. It needs internet the **first**
time (React and Tailwind come from a CDN, same as the other games here). Works great on a
tablet.

The first tap wakes the voice up — browsers require one tap before they'll play audio.

## Counting: a ladder, not a hundred flashcards

A hundred number words is far too much at four, and Spanish numbers are patterned, so the
game teaches ~30 words and lets the patterns do the rest. Each level unlocks the next.

| Level | Numbers | What she learns |
|-------|---------|-----------------|
| 🦄 **Uno a Diez** | 1–10 | uno, dos, tres … diez |
| 🌈 **Once a Veinte** | 11–20 | once, doce … veinte |
| ⭐ **Cuenta de Diez en Diez** | 10, 20 … 100 | diez, veinte, treinta … **cien** |

Two ways to play inside each level, picked with the toggle at the top:

| Mode | What happens | Good for |
|------|--------------|----------|
| 🦄 **Count Along** | Tap to add a unicorn; it says the next number in Spanish and shows the numeral | Building the sequence. No wrong answers, no score |
| 🌟 **Which One?** | A unicorn says a number in Spanish, she taps the matching numeral out of three | Practising alone — the game checks the answer |

A wrong tap in Which One? gets *"that one is ocho — listen again: cinco"*, and the question
stays up. Three correct in a row masters a number and stars it on the Number Ladder.

## Memory: English on one card, Spanish on the other

Pick a board — 🦄 4 pairs, 🌈 6 pairs, or ⭐ 8 pairs — then find the pairs. Both cards in a
pair show **the same picture**, so a child who can't read yet can still match them, and each
flip says its word in its own language. When a pair matches, both words play together
(*"moon… luna"*) so the link is what she hears.

Two kinds of pair:

- **Pictures** — 🦄 unicorn/unicornio, 🌈 rainbow/arcoíris, ⭐ star/estrella, 🌙 moon/luna,
  🌸 flower/flor, 👑 crown/corona, ☁️ cloud/nube, 🍰 cake/pastel, 💖 heart/corazón,
  ☀️ sun/sol, plus the colors (rojo, azul, amarillo, verde, morado).
- **Numbers** — the numeral `5` matches the card showing 🦄🦄🦄🦄🦄 and *cinco*, so she counts
  to find the pair. Only 1–10 get number cards; sixty unicorns is not something you can count
  on a card, so the bigger numbers stay in the counting module where the ladder teaches them.

Number cards only use numbers from levels she has reached, so memory never quizzes a word
counting hasn't introduced yet.

## For grown-ups

- **Two voices, on purpose.** Instructions and praise are spoken in English; the Spanish
  words use a Spanish voice, slowed down. Hearing the difference is part of the point.
- **Latin American Spanish.** The game prefers an `es-MX` / `es-US` voice, falling back to
  any Spanish voice on the device.
- **If your device has no Spanish voice**, the game says so on the front page and tells you
  how to add one. It still works meanwhile — the Spanish just comes out with an English
  accent. On iPad: Settings → Accessibility → Spoken Content → Voices → Español. On Windows:
  Settings → Time & Language → Speech.
- **Turning speech off.** Tap the 🔊 button (top-right) — same button, same place as the
  other games here. It remembers the choice.
- **No microphone.** The game speaks; it never listens. No permission prompts.
- **No timers, no losing.** Wrong answers get a gentle correction and another go.
- **No accounts, no data collected.** Progress lives in the browser on this device only.

## Make it your own

Open `index.html` in a text editor. Near the top of the `<script>`:

- **Number words** — `SPANISH_NUMBERS`.
- **The levels** — `LEVELS`. Each has a list of `numbers`; add a level and it appears in the
  picker, locked until the one before it is done.
- **Memory vocabulary** — `WORD_PAIRS` (icon + English + Spanish). Add a row and it joins the
  deck; give it an icon no other pair uses.
- **Board sizes** — `DECK_SIZES`.
- **How many unicorns a number card may show** — `COUNTABLE_MAX` (currently 10).
- **How many correct in a row masters a number** — `MASTERY_STREAK` (currently 3).
- **The unicorns** — `UNICORNS` (names, meanings, colors).

No image files — the unicorns are emoji tinted with CSS, so there's nothing to download and
nothing to credit.

---

Built with plain HTML, CSS and JavaScript in one self-contained file. ¡Vamos a contar! 🦄
