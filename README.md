# Bible Memory

A single-page scripture recall trainer. The app shows a verse reference and challenges you to recite it from memory before revealing the text. Built with vanilla HTML, CSS, and JavaScript with no dependencies or build step.

## How It Works

On load, a splash screen lets you pick from four translations (ESV, NASB95, CSB, KJV) before starting. Verses are shuffled using the Fisher-Yates algorithm so every verse appears exactly once before the set reshuffles.

Each card follows a three-step flow:

1. The scripture reference is displayed (e.g. "Psalm 34:8 ESV"). Say it aloud from memory.
2. Optionally tap "Show Hint" to reveal the first letter of every word in the verse.
3. Tap "Reveal Verse" to see the full text and check yourself.

The translation can be changed mid-session via a dropdown in the header. Switching reloads the current card in the new translation without advancing.

## Adding Verses

Append an entry to the `verses` array in the script block. Each entry needs a reference string and the verse text for all four translations:

```js
{
  ref: "John 3:16",
  text: {
    CSB: "...",
    ESV: "...",
    NASB95: "...",
    KJV: "..."
  }
}
```

The shuffle logic adapts to any array length automatically.

## Running Locally

Open `index.html` in any modern browser. No server, bundler, or install required.

## Project Structure

```
index.html   -- Entire application (markup, styles, and logic in one file)
README.md
```

## Related

This app is a companion to [Truth Declarations](https://github.com/shanehoving/truth-declarations), a randomized scripture declaration generator built in the same visual style. [GitHub Pages version]: (https://shanehoving.github.io/truth-declarations/)