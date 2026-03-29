# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- `npm run dev` — Start Vite dev server (http://localhost:5173)
- `npm run build` — Production build to `dist/`
- `npm run lint` — ESLint (flat config, JS/JSX)
- `npm run preview` — Preview production build

## Architecture

Single-page React 19 expense tracker using Vite 7. No router, no state management library, no backend — all state lives in `useState` hooks in `src/App.jsx`.

The entire app is one component (`App`) that handles: transaction list with filtering, add-transaction form, and income/expense/balance summary. Styles are in `src/App.css` and `src/index.css`.

## Known Issues

This is a course starter project with intentional bugs and rough edges:
- Transaction amounts are stored as strings, causing summary calculations (income, expenses, balance) to concatenate instead of sum.
- "Freelance Work" is marked as `type: "expense"` when it should be `type: "income"`.
- All UI is in a single component with no extraction.
