# 🧁 CupChess

**A cozy chess adventure for beginners.** A box of freshly baked cupcakes falls off the delivery truck, and the only way to reach Puffy Bakery is to win your way past every obstacle on the road. Each stop is a chess game, and each game teaches you something new.

CupChess is made for people who have never played chess before. It teaches the rules step by step and helps you while you play. It also gives you reasons to come back every day: ratings to climb, stars to collect, and new characters and accessories to unlock.

---

## The story

> *Mmm… freshly baked cupcakes! The bakery will be full today.*
> *Let's package them and deliver.*
> *Vroom vroom…*
> *Bump! A box of cupcakes tumbles off the truck.*
> *To find the bakery, the cupcake box has to get past every obstacle.*

The cupcakes travel along a winding map. At every stop, a different crowd blocks the road:

| Stop | Opponents | Lesson |
|---|---|---|
| Road | Rocks | How pawns move and capture |
| Farm | Flowers | Knights jump in an L |
| Market | Figs | Bishops slide diagonally |
| Burger Shop | Burgers | Rooks and castling |
| Castle | Chessmen | The queen and check |
| Haunted House | Ghosts | Checkmate |
| Puffy Bakery | Donuts | Putting it all together |

Win a stop and you unlock the next chapter. Beat the final stop and the cupcakes reach Puffy Bakery, where Baker Bun and every friend you met along the way are waiting.

## Pieces that look different but stay easy to recognize

Every level has its own army, so the rocks, flowers, figs, burgers, chessmen, ghosts and donuts all look different. To make sure beginners never get lost, **each piece always wears the same hat**, whatever it's made of:

| Piece | Hat |
|---|---|
| King | Gold crown with a cross |
| Queen | Pink tiara with gold balls |
| Rook | Castle tower |
| Bishop | Pointed mitre |
| Knight | Horse head |
| Pawn | Small round ball (a cherry on the cupcakes) |

Kings are the tallest and pawns the smallest. A small chess-symbol badge on each piece can be turned off once players know the pieces.

## Learning while you play

- **A lesson before every level** introduces one piece or idea.
- **Tap any piece** to see its name and how it moves. Dots show every square it can go to.
- **Coach Cupcake** cheers when you capture, castle or give check, and warns you when you leave a piece unprotected.
- **Hints:** 3 per game, showing a good move.
- **Take backs:** undo a move and try again.
- **Pieces guide:** see every piece side by side with how it moves.
- **Opponents get smarter** at every stop. The rocks make lots of mistakes; the donuts don't.

## Profile and ratings

Every player has a profile with:

- **Rating**, which goes up when you win and down when you lose (Elo-style)
- Best rating, wins, losses and draws, and a rating-over-time chart
- XP level, total stars and longest win streak
- Learning helpers you can turn on or off

## Unlocks

Reaching certain ratings unlocks new cupcake characters and accessories to wear:

| Rating | Unlock |
|---|---|
| 420 | Sprinkles |
| 480 | Strawberry cupcake |
| 550 | Chef hat |
| 620 | Chocolate cupcake |
| 700 | Bow |
| 780 | Blueberry cupcake |
| 860 | Star glasses |
| 950 | Golden wrapper |
| 1050 | Rainbow cupcake |
| 1150 | Royal crown |

## Why players keep coming back

- **Up to 3 stars per level:** win, win without hints or take backs, and win while keeping your queen
- **Daily goal:** play 3 games for bonus XP
- **Day streak:** a candle that grows with every day you play
- **Next reward bar:** always shows how close the next unlock is
- **Celebrations:** falling blossom petals for every win and unlock

## Art and design

The art direction is soft watercolor: dusty rose, mauve, butter yellow, sky blue, sage and woodblock blue, with paper texture, sleepy faces and pink cheeks. Every level has its own painted background and board colors.

The game screens are designed in Figma, and the story was planned in hand-drawn wireframes. The characters and animations are hand drawn. Right now the game uses placeholder drawings made in code; hand-drawn art can be dropped in through the `ART` section at the top of the game's script.

### Adding drawings

1. Draw on top of the template in `art/` (PNG for Procreate, SVG for Figma) and hide the guide layer before exporting.
2. Export PNG with a transparent background, or GIF for animation.
3. Add the image link to the matching slot in `ART`, for example `"rocks-K"` for the rock king or `intro1` for the first story panel.

| Art | Size | Example name |
|---|---|---|
| Pieces | 1024×1024 | `rocks-K.png`, `ghosts-N.png` |
| Level background | 1080×1920 | `farm-bg.png` |
| Map stop picture | 512×512 | `castle-icon.png` |
| Story panels | 1080×1350 | `intro1.png`, `finale2.png` |
| Profile cupcake | 1024×1024 | `avatar.png` |

## How it's built

- One self-contained `index.html` with HTML, CSS and JavaScript, no frameworks or build step
- Its own chess engine with every rule, including castling, en passant and promotion
- Computer opponents use minimax search with alpha-beta pruning, tuned per level with depth, randomness and occasional mistakes
- All art is drawn as SVG with watercolor filters
- Progress saves in the browser (localStorage)
- Works on phones, tablets and desktop, with light and dark mode

## Run it locally

Download the repo and open `index.html` in any browser.

## Credits

Created by **Elima Zholdubaeva**: game concept, story, wireframes, Figma design and art direction.
