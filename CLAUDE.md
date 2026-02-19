# Plinko Pony - Developer Notes

## Overview
Browser-based Plinko game with animated horses, built with vanilla JavaScript and HTML5 Canvas.

## Target Platforms
- Web browsers (desktop & mobile)
- Fire TV (via Silk browser or PWA)

## Architecture
- Single `index.html` file with embedded CSS/JS
- Web Audio API for all sound (procedural, no audio files)
- PWA support via `manifest.json` and `sw.js`
- No external dependencies or downloads

## Key Features
- Physics-based horse dropping through peg board
- Slot multipliers shuffle after each round
- Collectible bonus items (carrots, apples, etc.)
- Remote/keyboard controls (arrow keys + Enter) for TV use
- Classical music rotation (Beethoven, Bach, Pachelbel, Vivaldi)

## Technical Notes
- Horse size: 16-30px, scales with screen via SCALE factor
- Peg layout: 10 rows, 9 columns, alternating offset pattern
- Music: 5 public domain classical pieces encoded as note arrays
- All audio procedurally generated via Web Audio oscillators

## Controls
- **Touch/Click**: Tap above pegs to drop horse
- **Keyboard/Remote**: Left/Right to position, Enter to drop
