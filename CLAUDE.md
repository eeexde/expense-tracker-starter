# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- `npm run dev` — Start Vite dev server (http://localhost:5173)
- `npm run build` — Production build to `dist/`
- `npm run lint` — ESLint (flat config, JS/JSX)
- `npm run preview` — Preview production build

## Architecture

Single-page React 19 expense tracker using Vite 7. No router, no state management library, no backend.

- **`App.jsx`** — Root component. Owns the transactions array state and composes child components.
- **`Summary.jsx`** — Computes and displays total income, expenses, and balance from transactions.
- **`TransactionForm.jsx`** — Owns form state. Calls `onAddTransaction` callback to add a new transaction.
- **`TransactionList.jsx`** — Owns filter state. Renders filtered transactions table.

Styles are in `src/App.css` and `src/index.css`.

## Known Issues

- "Freelance Work" is marked as `type: "expense"` when it should be `type: "income"`.
