# helmi — the website

The marketing site for [Helmi](https://github.com/dresende/helmi-app), the
match-three puzzle for iPhone and iPad. Published with GitHub Pages at
<https://dresende.github.io/helmi/>.

It is plain hand-written HTML with no build step and no dependencies, the
same as Sikku's and Kirjo's.

- `index.html` — the whole page. The hero board is **level 1, played for
  real**: the script is a transliteration of the app's
  `Helmi/Engine/Match3Engine.swift` (same mulberry32 RNG, same deal rules,
  same forging priority), so tide nº 90001 deals the same board here as in
  the app. Only that one level's parameters are inlined — never paste in
  `levels.json`; it carries all 1000 levels and a view-source would hand the
  whole descent away.
- `privacy.html` — the page the app links to from **Settings → i → Privacy
  policy**. The URL is compiled into every shipped build
  (`Helmi/AboutSheet.swift`), so this file cannot be moved or renamed without
  breaking a link inside every copy of the app already installed.
- `icon-180.png`, `icon-512.png` — downscales of the app's 1024px
  `AppIcon.png`. 180 is the favicon and apple-touch-icon; 512 is the
  Open Graph image.

The palette mirrors `Helmi/Theme.swift`, and the creature glyphs are the
app's own 24×24 vector paths from `Helmi/Game/GlyphInk.swift`. If either
changes in the app, change it here.

**App Store:** coming soon.
