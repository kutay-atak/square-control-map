# Square Control Map

A Chrome extension that frames every square of the chess.com board by who controls it:

- **blue**: White has more pieces that could capture there
- **red**: Black has more
- **purple**: equal

A thicker frame means a bigger majority (1, 2, 3+). Hover a square for the exact counts.

A piece counts only if the capture would be legal: pinned pieces count only along the pin line, and a king doesn't count on squares the opponent covers.

It runs only on bot games (`/play/computer`) and analysis boards, never in games against people.

## Install

1. Download or clone this repository.
2. Open `chrome://extensions` and turn on **Developer mode**.
3. Click **Load unpacked** and select the folder.
4. Start a game at https://www.chess.com/play/computer.

Toggle it with the button at the bottom left or **Alt+C**.

## Files

- `control.js`: counts the legal attackers of every square
- `content.js`: reads the position from the board and draws the frames
