---
title: GameVortex
track_code: SPTC120523GV
date: 2023-05-12T00:00
summary: Gaming portal
status: In Progress
link: https://surfscape.github.io/gamevortex/
---

A small web portal focused on gaming, specially on Flash and HTML5 games.

**Note 2:** GameVortex is being rewritten under Astro framework with a new, cleaner, design, additional features, and new (broken before) games.

**Note 1:** An old, working version of {{title}} is available.

## Current Implementation & Issues

The current version of {{title}} is confusing but it does work with most pre 2005 Flash games and there's experimental support for Unity games since the game [Slope](https://surfscape.github.io/gamevortex/games/slope/) does work without issues.

The main issues with {{title}} `v0.0.1` are:

- Inconsistent layout (and not responsive)
- Missing features (genres, game controls, and game summary)
- Request a game
- Missing game banners
- Broken HTML5 game support
- Current folder structure<sup>1</sup>

Even though GameVortex has a lot of flaws on it's architecture, some of the main goals were achived: fullscreen support and experimental support for Unity games.

Because of all the issues, a rewritten version will take a long time and effort and most of GameVortex users have abandoned it.

---

<sup>1</sup> Some Flash games require an additional game data folder like Extreme Pamplona which does not work in GameVortex due to it's current folder structure and because of Eleventy permalink limitations.
