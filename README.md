# Letterlock

A five-letter word deduction game that runs in a single HTML file. A word is locked away, and you have **10 tries** to open it. Each guess tells you *how many* letters landed, but never *which* ones.

## How to play

Type a five-letter word and press **Enter** (or tap **Try**). Each guess is scored with pins:

| Pin | Meaning |
| --- | --- |
| ● Set pin | A letter in the right slot. |
| ○ Loose pin | A letter that is in the word, but in a different slot. |
| ┄ No pins | None of the guessed letters are in the word. |

Repeated letters count only as often as they appear in the hidden word. Guesses must be real words from the built-in word list, and you can't repeat a guess.

### Marking letters

Tap any letter in your guess history to track what you've deduced:

1. Once: mark it **out**
2. Twice: mark it **in**
3. Three times: clear the mark

The on-screen keyboard reflects your marks.

## Running it

There's no build step and no dependencies. Open `index.html` in a browser:

```sh
# or serve it locally
python -m http.server
```

Then visit `http://localhost:8000`.

## Controls

| Input | Action |
| --- | --- |
| `A`–`Z` | Type a letter |
| `Backspace` | Delete a letter |
| `Enter` | Submit the guess |
| `Esc` | Close a dialog |

## Features

- **Saved progress**: the current game is stored in `localStorage`, so reloading keeps your lock.
- **Stats**: games played, open rate and current streak are tracked across sessions. Starting a new lock mid-game counts as a loss.
- **Light and dark themes**: follows your system preference.
- **Responsive**: built to fit on one screen, down to small phone widths.

## Project structure

```
index.html   # markup, styles, word list and game logic
README.md    # this file
```
