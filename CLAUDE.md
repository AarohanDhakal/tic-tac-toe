# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file vanilla JavaScript Tic Tac Toe game (`tictactoe.html`). There is no build system, package manager, or backend — open the file directly in any browser to run it.

## Architecture

Everything lives in `tictactoe.html` in three inline sections:

- **`<style>`** — CSS with dark theme, CSS Grid board layout, and win animations
- **`<script>`** — Game logic with a single state object:
  - `board`: 9-element array for the 3×3 grid
  - `current`: active player (`'X'` or `'O'`)
  - `gameOver`: boolean flag
  - `scores`: cumulative win/draw counts across games
- **HTML body** — Static structure; cells and score display updated via DOM manipulation

Win detection checks 8 hardcoded index combinations (rows, columns, diagonals). Game state resets per round; scores persist for the session.
