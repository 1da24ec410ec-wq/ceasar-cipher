# 🔐 Caesar Cipher Decoder

A fully standalone, browser-based Caesar cipher decoder with frequency analysis — no dependencies, no install, just open and use.

**[Live Demo →](https://yourusername.github.io/caesar-cipher/)**

---

## Features

- **Manual shift control** — drag a slider from 0–25 to try any shift instantly
- **Auto-detect** — chi-squared frequency analysis finds the most likely shift automatically
- **Frequency chart** — side-by-side bar chart comparing ciphertext letter distribution against standard English
- **Top suggestions** — ranked list of the 5 best candidate shifts with preview text
- **Cipher wheel** — visual outer/inner ring showing the substitution mapping
- **All 26 shifts** — browse every possible decoding ranked by English-language fit
- **Stats panel** — letter count, most frequent letter, index of coincidence
- **Copy to clipboard** — one-click copy of the decoded result
- **Dark mode** — automatically follows system preference

---

## What is a Caesar Cipher?

A Caesar cipher is one of the oldest encryption techniques. Each letter in the plaintext is shifted a fixed number of positions along the alphabet. For example, with a shift of 3:

```
Plain:   A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
Cipher:  D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
```

So `HELLO` becomes `KHOOR`. To decode it, you shift back by the same amount.

---

## How Frequency Analysis Works

Every language has a characteristic letter frequency distribution. In English, `E` is the most common letter (~12.7%), followed by `T`, `A`, `O`, `I`, `N`, and so on.

Because a Caesar cipher only shifts letters without changing their relative frequency, the distribution of letters in the ciphertext mirrors the plaintext — just rotated. By comparing the ciphertext frequency distribution to the known English distribution using **chi-squared distance**, the tool ranks all 26 possible shifts from best to worst match.

The **index of coincidence** (IC) is also shown. English plaintext has an IC of approximately `0.065`. If your IC is well below that, the text may not be a simple Caesar cipher.

---

## Usage

### Online (GitHub Pages)

Just visit the live demo link above — nothing to install.

### Local

```bash
# Clone the repo
git clone https://github.com/yourusername/caesar-cipher.git
cd caesar-cipher

# Open in browser
open index.html
```

Or simply double-click `index.html` — it works entirely offline.

---

## Deploy to GitHub Pages

1. Fork or clone this repo
2. Rename `caesar-cipher-decoder.html` → `index.html`
3. Push to your `main` branch
4. Go to **Settings → Pages → Source → Deploy from branch → main**
5. Your decoder will be live at `https://yourusername.github.io/caesar-cipher/`

---

## Project Structure

```
caesar-cipher/
└── index.html      # Everything — HTML, CSS, and JS in one file
└── README.md       # This file
```

The entire tool is a single self-contained HTML file with no external dependencies or network requests.

---

## Example

Try decoding this ciphertext with **shift 13** (ROT13):

```
Uryyb, Jbeyq!
```

Or paste any text and hit **Auto-detect shift** — the tool will find the right shift automatically.

---

## License

MIT — free to use, modify, and distribute.
