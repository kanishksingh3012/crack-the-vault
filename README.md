# Crack the Vault

A 16-level isometric safecracking game by Kanishk. Turn the dial, listen for the deep thunk, rest on it to set a number, then reverse direction. Beat the alarm.

## Play

Open `public/index.html` in a browser, or visit the deployed site. No install and no network access are needed; the game is one self-contained HTML file.

- **Mouse or touch:** circle the pointer around the dial.
- **Keyboard:** left and right arrows step the dial; up and down switch dials on multi-dial safes.

## The safes

| # | Safe | Rule |
| --- | --- | --- |
| 1 | Cash box | Tutorial |
| 2 | Fire safe | Finer dial |
| 3 | Wall safe | Hidden behind a picture |
| 4 | Floor safe | Overshoot penalty |
| 5 | Jeweller's safe | Decoy clicks |
| 6 | Cannonball safe | Sound only |
| 7 | Commercial safe | Relocker |
| 8 | Time-lock safe | Time lock |
| 9 | Twin-dial safe | Twin dials |
| 10 | Bank vault | Faint thunk, decoys, relocker |
| 11 | Deposit boxes | Three dials |
| 12 | Antique strongbox | Spring dial |
| 13 | Purser's safe | Silent stops |
| 14 | Museum case | Guard and noise meter |
| 15 | Casino cage | Trap number |
| 16 | Gold reserve | Everything |

One safe hides a cat. It moves every time a safe is cracked.

## Project layout

- `src/crack-the-vault.html` is the source: page, styles and game code, with placeholders for the shared runtime.
- `public/index.html` is the built, playable file.
- `public/README.md` carries the licence notices for the runtime and must stay next to the built file.

## Rebuilding

The game is drawn with the [IsometricAnimation](https://github.com/DrishtantKaushal/IsometricAnimation) skill, whose builder inlines its SVG runtime into the page. With Node 22 or later and a clone of that repo:

```sh
node IsometricAnimation/skills/isometric-animation/scripts/build.mjs src/crack-the-vault.html public/index.html
node IsometricAnimation/skills/isometric-animation/scripts/validate.mjs public/index.html
```

## Credits

Built with the IsometricAnimation skill by Drishtant Kaushal, which adapts work by Tolga Cohce (ai-iso-skill) and Lucas Marques (Hairline). Their MIT notices are in `public/README.md`. The interface styling follows the look of HeroUI's default theme, written as plain CSS.
