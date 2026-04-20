# Guess Who Digit

Two-player "Guess Who" where the board is a 6×6 grid of random keyboard characters. Played in person; each player uses their own phone.

## Run

```
python3 -m http.server 8000
```

Open `http://<your-lan-ip>:8000/` on both phones. Share the URL (it contains `?seed=…`) so both players load the same grid.

## Play

1. One player clicks **New game** and shares the URL with the other.
2. Each player silently picks a character from the grid as their secret.
3. Take turns asking yes/no questions out loud ("is it a letter?", "is it uppercase?", "does it have a closed loop?").
4. Tap cells to cross them out as you narrow things down.
5. First to correctly guess the other's character wins.

The **seed** in the header is clickable if you want to type a seed instead of using a shared URL.
