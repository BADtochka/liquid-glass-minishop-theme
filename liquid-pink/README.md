# Liquid Glass — Remnawave Minishop theme

Theme API 1 visual override for the standard Minishop user/admin UI.

## 1.4.0

- Removed Android/Telegram WebView system tap highlight from theme interactions.
- Interactive controls no longer trigger text selection/callout while tapping.
- Mobile glass blur is reduced from 24-30px to a cheaper 12-14px material.
- Full-screen dialog backdrop blur is disabled on touch/mobile devices.
- Dialog cards use an opaque-enough glass surface instead of a large live backdrop filter on mobile.
- Underlying blurred cards/nav are temporarily flattened while a dialog is open.
- Background parallax is paused while a dialog is open.

## 1.3.0

- Admin navigation now follows the user rail interaction model: transparent idle rows, subtle hover, glass/accent only on the active row.
- Restored Minishop native `position: fixed` dialog geometry; the theme no longer rewrites every direct child of `.app-shell` to `position: relative`.
- Premium/LTE traffic-scope popup now has a strong dark luminance floor and remains readable over the animated background.
- Mobile `home-compact-summary` keeps the traffic-help button visible by allowing the long label to ellipsize independently.
- Touch/mobile parallax uses a fixed `0px 120dvh` animation range and a smaller motion amplitude, so short pages and rubber-band scrolling no longer swing the background aggressively.
- `prefers-reduced-motion` also disables the pseudo-element background parallax.

## Local assets

The theme CSS expects the existing local files:

- `assets/background.webp`
- `fonts/Onest-VariableFont_wght.ttf`
- `fonts/Unbounded-VariableFont_wght.ttf`

The font faces are loaded from relative package paths with `@font-face`.

- Theme accent is explicitly pinned to `#527462` in both the active dark variant and fallback tokens.
