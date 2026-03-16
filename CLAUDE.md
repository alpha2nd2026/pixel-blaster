# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Collection of single-file browser games (no build system, no dependencies, no external assets). Each game is a standalone `.html` file with embedded CSS and JS.

## Current Games

- **shooter.html** — "Pixel Blaster": top-down retro shooter with canvas rendering, 10 levels, 5 enemy types, particle effects
- **tictactoe.html** — Tic Tac Toe

## Development

No build/lint/test commands — open any `.html` file directly in a browser to run. Use `open <file>.html` on macOS.

## Architecture Conventions

- **Single-file pattern**: each game is one self-contained HTML file (~500-1000 lines) with all HTML, CSS, and JS inline
- **No external assets**: all visuals are procedurally drawn (canvas API, pixel-art rectangles)
- **Canvas games** use `requestAnimationFrame` with fixed-timestep update + variable render
- **Color palette**: Pico-8 inspired (see `COL` object in shooter.html)

## Git Workflow

- Remote: GitHub (`origin`)
- Branch: `main`
- **Commit and push to GitHub regularly as you work** — after every meaningful change (new feature, bug fix, refactor). Never leave work uncommitted. Clean, descriptive commit messages so it's easy to understand and revert any change.
- This is a hard requirement: always `git add`, `git commit`, and `git push` so progress is saved to GitHub and nothing is lost.
