# AppADay 107 — Knot Locker

A mobile-first field guide and drill for the five knots every scout needs at camp: bowline, clove hitch, taut-line hitch, square knot, and two half hitches.

**Live app:** https://augustineiacopelli.github.io/appaday-107-knot-locker/
**Portfolio:** https://augustineiacopelli.github.io/appaday/

## What it does

Field Guide tab lets you search and filter knots by use case (Camp Setup, First Aid, General Utility), then tap into a step-by-step diagram sequence for each one, with a caption per step and a step counter you page through at your own pace.

Drill tab runs a five-question quiz pulled from the same knot set. Each question shows the finished knot's diagram and asks you to identify it or its job. Score and best score persist locally, and any missed knots are flagged in a review list at the end of the round so you know what to go practice.

The whole app is a single self-contained HTML file. No API calls, no external data, works fully offline once the page has loaded, which matters when you're building this from a scout camp with spotty wifi.

## Tech

Vanilla HTML, CSS, and JavaScript. No frameworks, no build step. Google Fonts (Oswald, Public Sans, JetBrains Mono) loaded from CDN. All diagrams are inline SVG generated from simple path data, no image assets. localStorage used for best score and missed-knot tracking, wrapped in try/catch throughout.

## Backstory

Built from Lake Cheney at Boy Scout camp, on borrowed time between activities, with no guarantee of solid wifi past the point of publishing. The static line diagrams got one real rework pass, rendered and screenshot-checked against a headless browser rather than trusted blind, which took the bowline and square knot from unrecognizable squiggles to something a scout could actually read. They are legible now, but they are still simple line schematics, not illustrations, and it shows most on the two-half-hitches and taut-line frames. Shipping on schedule mattered more than getting the art all the way there this weekend.

## Future version

The original concept for this app was a scrubbable rope animation: drag a finger back and forth along a rope-textured track and watch the knot tie itself forward or untie itself backward in real time, synced to finger position. That's a meaningfully bigger build, either an SVG path that morphs against stroke-dashoffset or a flipbook of ten-plus hand-drawn frames per knot mapped to drag position.

It's a strong signature feature for a future related build: start with the bowline as the hero knot with the full scrubbable treatment, since it's the most requested scouting knot, and leave the rest on the static step-by-step format this version uses. Worth revisiting when there's a full build session to dedicate to it rather than a camp weekend.

Separately, and more immediately: the static diagrams themselves need a real second pass. This version is a legible schematic, not a finished illustration, and the next time this app gets touched, redrawing the knot art with proper rope shading and consistent stroke weight (or replacing it outright with a small set of real illustrated frames) should be the first item on the list, ahead of the scrub animation.

## Category

Educational (E)
