# Number Crush — Notes

## Overview

Number Crush is an arcade-style tile matching game where players select
groups of numbered tiles on a board that satisfy a configurable
constraint rule (e.g. sum equals target, product equals target, etc.).
Matched selections are "crushed" (removed), tiles above fall down, and
new tiles are generated to refill the board.

## Recent Updates

- Added a "← Home" navigation link at the top of the page so players
  can return to the site's main landing page (`/`) at any time without
  using the browser back button.

## Structure

- `index.html` — page markup: header, config menu (game setup form),
  game area (HUD, canvas board, indicator text, restart button), and
  now a home navigation link.
- `css/games-number-crush-index.css` — arcade-themed styling: neon
  gradients, glassmorphism panels, animated grid background, HUD
  cards, config menu, and buttons.
- `src/main.js` — game logic entry point (module script), handles
  configuration, board rendering, tile selection, rule validation, and
  scoring.

## Configuration Options

The config menu (`#config-menu`) allows players to customize:

- Constraint rule (`cfg-rule`)
- Target value (`cfg-target`)
- Board columns/rows (`cfg-cols`, `cfg-rows`)
- Tile size in px (`cfg-size`)
- Min/max tile value (`cfg-val-min`, `cfg-val-max`)
- Min/max selection length (`cfg-min-sel`, `cfg-max-sel`)
- Straight-line selection enforcement (`cfg-straight-line`)
- Suppress zero-valued tiles (`cfg-suppress-zero`)

## Follow-up

- Verify the home link path (`/`) resolves correctly relative to the
  deployment structure (e.g. if the site is served from a subpath,
  this may need to be adjusted to a relative path or computed base
  URL).
- Consider adding a consistent nav/header component shared across all
  games to avoid duplicating this link markup in each game's
  `index.html`.
