# Cube Solver

Show each side of a Rubik's Cube to your camera, check the colors, and get the moves to solve it, one at a time.

Everything runs in the browser. Photos never leave your device.

## How it works

1. **Scan.** The camera shows a 3x3 guide. For each of the 6 sides, the page reads the middle of every square (the median color of a small patch, so glare matters less). You can also take a photo of each side instead.
2. **Read the colors.** Each side's middle sticker decides which color belongs to that side. Every other sticker is matched to the closest middle color, with exactly 8 per side, using the Hungarian method on Lab color distances.
3. **Check.** The page confirms the cube could really exist: every corner and edge piece is real, no corner is twisted, no edge is flipped, and no two pieces are swapped. Problem pieces are highlighted so you can fix them by tapping.
4. **Solve.** The solver finds the moves. Before any answer is shown, the page replays it on its own cube model and only shows it if it really ends solved.

## Files

- `index.html` is the whole app.
- `vendor/cube.js` and `vendor/solve.js` are the solver, unmodified from [cubejs](https://github.com/ldez/cubejs) 1.3.2 (Kociemba's two-phase algorithm). They load only when you press Solve.
- `vendor/LICENSE-cubejs.txt` is the cubejs MIT license.

## Credits

The solver is cubejs by Petri Lehtinen and Ludovic Fernandez, used under the MIT license.
