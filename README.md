# 2048 — Ultimate Board Challenge

A standalone 4 × 4 number puzzle built with HTML, CSS, and vanilla JavaScript. No external libraries, installation, or build step required.

## Play

Download this repository and open **index.html** in a modern browser.

- **Keyboard:** press the arrow keys to slide tiles.
- **Touch or mouse:** swipe or drag across the board.
- **Restart:** start a new game and reset the score.

## Rules

Tiles slide as far as possible in the chosen direction. Two matching tiles merge into one tile with twice the value. A tile can merge only once per move, and each merge adds its resulting value to the score.

After a move that changes the board, a new tile appears in a random empty cell: **2** with a 90% chance or **4** with a 10% chance. Moves that do not change the board do not spawn tiles.

### Beyond 2048

Reaching **2048 does not end the game**. Keep merging to complete the ultimate board.

You win only when the 16 cells contain exactly one of each of these values, **in any arrangement**:

| | | | |
| --- | --- | --- | --- |
| 65,536 | 32,768 | 16,384 | 8,192 |
| 4,096 | 2,048 | 1,024 | 512 |
| 256 | 128 | 64 | 32 |
| 16 | 8 | 4 | 2 |

This is the custom final board target: **2¹⁶ through 2¹**. Its tile values sum to **131,070**; this sum is not the merge score displayed during play.

You lose if the board is full and no adjacent matching tiles can merge, unless the ultimate board has been completed. The victory check takes priority over the no-moves check.

## Features

- Responsive 4 × 4 board and an English interface.
- 150 ms tile movement, merge bounce, and new-tile appearance animations.
- Distinct colors and appropriately sized text for tiles through 65,536.
- Keyboard, touch, and mouse controls.
- Score tracking and win/loss dialogs.
- One buffered direction while a move animates.
- Safe restart during animations.
- Respects the system's reduced-motion preference.

## Project structure

- **index.html** — all game markup, styling, and logic.
- **README.md** — setup, controls, and rules.

The game runs locally without network access. Game progress is not saved when the page is refreshed or closed.
