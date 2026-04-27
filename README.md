# Guess Who Digit

Two-player "Guess Who" where the board is a 5×5 grid of random keyboard characters. Played in person — each player uses their own phone.

**Play it:** https://c0webster.github.io/guess-who-digit/

## How to play

1. One player opens the link, taps **New game**, and shares the URL (the **Share** button uses your phone's native share sheet).
2. Both players open the same URL — the seed in the URL guarantees both phones show an identical grid.
3. Each player taps their secret character (gold ★). This stays private to their phone.
4. Take turns asking yes/no questions out loud: *is it a letter? is it uppercase? does it have a closed loop?*
5. Tap cells to cross them out as you narrow things down.
6. First to correctly guess the other's character wins.

The **seed** input in the header is editable if you want to type a seed instead of using a shared link.

## How it works

Single static `index.html` with no backend. The grid is deterministically generated from the seed in the URL (`?seed=…`), so any two phones on the same seed get identical boards. Each player's secret and cross-outs live in their own phone's `localStorage`.

## Local development

```
python3 -m http.server 8000
```

Then open `http://localhost:8000/`. Any change to `index.html` is picked up on refresh. Push to `main` to deploy — GitHub Pages auto-rebuilds.
