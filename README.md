# Two Street Water Ice

A single-page website for a Philly-themed water ice stand — Pennsport, South Philly, "since 1988." Built with plain HTML and CSS, no framework or build step.

## Project structure

```
.
├── index.html
├── css/
│   ├── reset.css
│   └── main.css
└── philly-water.jpg       # hero background image
```

## Running it locally

No build step — it's static HTML/CSS. Open `index.html` directly in a browser, or serve the folder with something like VS Code's Live Server extension (recommended, since some browsers restrict local file access for things like relative image paths).

## Fonts

Loaded from Google Fonts in `<head>`:

- **Titan One** — headings (`h1`–`h6`)
- **Nunito** — body text (`p`, `span`, `a`)

## CSS approach

- **`html { font-size: 62.5%; }`** — sets `1rem = 10px`, so type and spacing scale predictably and can be resized globally at breakpoints (`html { font-size: 55%; }`, etc.) instead of touching every rule individually.
- **CSS custom properties** (`:root`) hold the brand color palette — see below.
- **Native CSS nesting** is used throughout (e.g. `.card25 { h4 { ... } }`). This needs a modern browser: Chrome/Edge 2023+, Firefox 2023+, Safari 16.5+.
- **Responsive breakpoints** at `88rem`, `76rem`, `50rem`, and `45rem`, using the `width <= Xrem` range syntax.

## Brand palette

| Color | Value | Used for |
|---|---|---|
| Pink | `rgb(230, 53, 95)` | Header background, accent text, prices |
| Yellow | `rgb(253, 207, 62)` | Primary CTA button, banner, highlights |
| Dark purple | `rgb(57, 36, 52)` | Body/heading text on light backgrounds, footer background |
| Blue | `rgb(58, 167, 224)` | Blue Raspberry accent |
| Orange | `rgb(255, 159, 70)` | Mango accent |
| Lavender | `rgb(206, 150, 232)` | Cotton Candy accent |
| Beige | `rgb(255, 248, 239)` | Section background |
| Light blue | `rgb(191, 228, 245)` | Sizes section background |

## Page sections

1. **Header** — logo + nav (Flavors / Sizes / Find the Stand) + "Call the Window" CTA
2. **Banner** — hours / cash-only notice
3. **Hero** — tagline, headline, two CTA buttons
4. **Flavor board** (`#flavors`) — 5 flavor cards, color-coded by flavor
5. **Sizes** (`#sizes`) — 5 pricing cards
6. **Find the Stand** (`#location`) — hours, address, house rules
7. **Footer** — contact info, hours, copyright

## Known in-progress / notes

- The footer is due for a rework (structure + styling still being finalized).
- `header { position: sticky }` is present but currently commented out.
- `.card30` is defined in the CSS but not currently used in the markup.
- Some breakpoints (`88rem` and below) still need cross-device testing.

## License

Add a license here if this is going public (MIT is a common default for a personal project like this).
