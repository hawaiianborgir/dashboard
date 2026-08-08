# Kessoku Band Dashboard

A responsive dashboard UI built with plain HTML and CSS, styled around *Bocchi the Rock!*'s Kessoku Band. The layout features a search-driven header, an icon navigation sidebar, a scrollable project feed, and a sidebar of announcements and trending members.

**Live Demo:** [hawaiianborgir.github.io/dashboard](https://hawaiianborgir.github.io/dashboard/)

## Preview Layout

```
┌─────────────┬──────────────────────────────┐
│             │            Header             │
│   Sidebar   ├──────────────────────────────┤
│             │                                │
│  Logo/Nav/  │          Main Content          │
│   Menu      │   (Projects | Announcements    │
│             │       & Trending)               │
└─────────────┴──────────────────────────────┘
```

## Features

- **CSS Grid layout** — the page shell (`.container`), header, and main content area are all built with `grid-template` / `grid-template-areas` for clear, named regions.
- **Responsive sizing** — `clamp()` is used throughout (search bar width, padding, nav font size, button height) so elements scale fluidly between breakpoints without media queries.
- **Search bar** with an SVG search icon and custom caret styling.
- **Header** with two rows: a search + profile/notifications row on top, and a greeting + quick-action buttons (`New`, `Upload`, `Share`) below.
- **Sidebar navigation** split into a primary nav (Home, Profile, Messages, History, Tasks, Communities) and a secondary menu (Settings, Support, Privacy), each using [Tabler-style](https://tabler.io/icons) inline SVG icons.
- **Project cards** in an auto-fitting grid (`repeat(auto-fit, minmax(400px, 1fr))`) with favorite / follow / fork actions.
- **Announcements panel** with clamped (truncated) text via `-webkit-line-clamp`.
- **Trending panel** showing band members with profile pictures linking out to external content.
- **Micro-interactions** — hover lift (`translateY`) and active press (`scale`) states on buttons, links, and profile icons.
- **Modern CSS reset** included at the top of `style.css` (box-sizing normalization, margin reset, media-friendly defaults, balanced text wrapping, etc.).

## Tech Stack

- HTML5
- CSS3 (Grid, Flexbox, `clamp()`, custom properties)
- [Google Fonts](https://fonts.google.com/) — Inter, Roboto, Playwrite NZ Basic
- Inline SVG icons ([Tabler Icons](https://tabler.io/icons) style)

## Project Structure

```
.
├── index.html       # Page markup and structure
├── style.css        # Layout, theming, and responsive styles
├── bocchi.jpg       # Profile image
├── kita.jpg         # Trending member image
├── nijika.jpg       # Trending member image
├── ryo.jpg          # Trending member image
└── kessoku-logo.png # Sidebar logo image
```

See **Credits** below for image sources.

## Getting Started

No build step or dependencies required. Check out the [live demo](https://hawaiianborgir.github.io/dashboard/), or run it locally:

1. Clone or download this repository.
2. Add the required image assets (see **Project Structure** above) to the project root.
3. Open `index.html` directly in a browser, or serve it locally:

   ```bash
   # Python
   python3 -m http.server 8000

   # Node
   npx serve .
   ```
4. Visit `http://localhost:8000` (or the port shown in your terminal).

## Customization

Theme colors are defined as CSS custom properties at the top of `style.css`:

```css
:root {
  --accent-color: #FCC8DF;
  --soft-color: #D0C8CF;
  --font-color: #FEFEFE;
  --bg-color: #F66864;
  --line-color: #c73732;
  --project-color: #6E8DC4;
  --text-color: #5F6368;
}
```

Update these variables to re-theme the entire dashboard.

## Known Issues / Cleanup Ideas

- Several external links currently point to a placeholder GitHub profile — update these to real destinations.

## Credits

- Icons: [Tabler Icons](https://tabler.io/icons)
- Fonts: [Google Fonts](https://fonts.google.com/) (Inter, Roboto, Playwrite NZ Basic)
- Profile images (`bocchi.jpg`, `kita.jpg`, `nijika.jpg`, `ryo.jpg`): [アカミ on pixiv](https://www.pixiv.net/en/users/33550643)
- Sidebar logo (`kessoku-logo.png`): [pngtree.com](https://pngtree.com/freepng/hair-band-with-transarent-background_13379048.html)
- Theme inspiration: *Bocchi the Rock!* / Kessoku Band

## License

Add a license of your choice (e.g., MIT) if you plan to share or open-source this project.