# Mermaid Unicorn Ocean 🧜‍♀️🦄

A just-for-fun swimming game. You are a mermaid unicorn. You swim around a big ocean,
collect shells, and shoot arrows at the bags of cookies that throw chocolate chips at you.

**This one doesn't teach anything on purpose.** Every other game in this collection has
letters or numbers in it somewhere. This one was designed by a five-year-old who was asked
whether he wanted to learn something and said, very clearly, no.

Open `index.html` in any browser — double-click it, or play it online at
<https://dlb2887.github.io/Games-for-kids/mermaid-unicorn-ocean/>.
It works completely offline. Nothing is downloaded, so it's fine on a plane or in the car.

## How to play

| | |
|---|---|
| 🦄 | **You're the mermaid unicorn.** Drag a finger anywhere on the sea to swim toward it. On a computer, the arrow keys or WASD work too. |
| 🏹 | **Tap the sea** (or press the big arrow button, or the spacebar) to shoot. Arrows aim themselves at whatever is nearest, so it's very hard to miss. |
| 🐚 | **Swim over shells** to collect them. The counter at the top keeps track. |
| 🍪 | **The bag of cookies** throws chocolate chips at you. Two arrows and it pops into crumbs — and drops shells. |
| 😼 | **The cat** is on the cookies' side and chases you around. One arrow sends it tumbling off. |
| 🥒 | **The pickle** is your friend. It hunts down cookie bags all by itself and squirts pickle juice at them, which freezes them for a few seconds. |
| 🐬 | **The purple dolphin** follows you. It fetches shells you've swum past, knocks chocolate chips out of the air, and gives you a speed boost now and then. |
| 🌀 | **Tunnels** are the glowing stone arches. Swim into one and you whoosh out of its partner on the far side of the ocean. |

The little map in the bottom corner shows where you are: pink is you, purple is the dolphin
and the tunnels, brown is the cookie bags.

## For grown-ups

- **Nobody can lose.** There is no health bar, no timer, and no game over. Getting hit by a
  chocolate chip or bumped by the cat makes the mermaid spin and drop up to three shells,
  which scatter right next to her and can be picked straight back up. That's the entire
  penalty. This matches the other games in the collection.
- **Aiming is automatic.** Precise aiming is genuinely hard for a four- or five-year-old, so
  a tap fires at the nearest target within range. Steering is the only real skill.
- **It never runs out.** Shells refill, and cookie bags and cats come back a few seconds
  after they're popped, so a session ends when the kid is finished rather than when the game is.
- **Sound** is one button for everything — the speaker in the top-right mutes both the sound
  effects and the spoken cheers. The choice is remembered.
- **Progress** is just the badges and the best-ever shell count, kept in `localStorage`
  under keys starting with `mo_`. Nothing leaves the device.

## Make it your own

Everything worth tweaking sits near the top of the `<script>` block in `index.html`:

- `BADGES` — the six badges and what they say.
- `MILESTONES` — the shell counts that trigger a celebration.
- `WORLD_W` / `WORLD_H` — how big the ocean is.
- `TARGET_SHELLS`, `BAG_COUNT`, `CAT_COUNT` — how crowded it is.
- `MILESTONES`, `AIM_RANGE`, and the speeds inside each `update…()` function — the difficulty.

Most characters are emoji. The two that aren't are drawn with canvas paths: the mermaid
unicorn in `drawMermicorn()` (her colours, mane, and horn live there) and the purple dolphin
in `drawDolphin()`. The dolphin is drawn rather than recoloured on purpose — tinting the 🐬
emoji relies on canvas `ctx.filter`, which older Safari doesn't support, and on those devices
he came out blue.

## Credits

All the art is either an emoji supplied by the device or drawn in code. No images, no fonts,
no libraries, no network.
