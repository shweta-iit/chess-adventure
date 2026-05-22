# Architecture

## Core Stack

This project is built using:

- TanStack Start
- React 19
- Vite
- Tailwind CSS v4
- shadcn/ui

The project is intentionally optimized for compatibility with the Lovable platform.

---

# Product Philosophy

The app should prioritize:

- simplicity over feature richness
- reusable systems over custom pages
- clean UI over heavy visual effects
- fast iteration over premature optimization

The MVP goal is to build one polished vertical slice:
- learn a chess piece
- solve a puzzle
- play a simple AI game
- earn a reward

---

# Initial App Structure

## Primary Sections

- Home
- Learn
- Practice
- Play
- Rewards

Do not build:
- multiplayer
- authentication
- databases
- parent dashboards
- advanced AI coaching

for the initial MVP.

---

# UI Architecture

## Design Principles

- Mobile-first responsive design
- Card-based layouts
- Rounded corners
- Large spacing
- Minimal visual clutter
- Reusable UI components

---

# Typography

- Fredoka → headings
- Nunito → body text

---

# Color Palette

- Primary Blue → #5B8DEF
- Purple → #8B5CF6
- Gold → #FFD166
- Cream → #FFF8EE

---

# Layout Rules

- Maximum content width: 1400px
- Prefer centered layouts
- Avoid dense dashboards
- Keep screens vertically focused
- Limit primary actions per screen

---

# Chess Libraries

Use existing chess libraries.

Do NOT build custom chess logic.

Libraries:
- chess.js
- react-chessboard

---

# State Management

Initial MVP should use:
- local component state
- minimal global state

Avoid:
- Redux
- overengineered stores
- premature abstractions

Global state may later use Zustand if needed.

---

# Content Strategy

Lessons and puzzles should be data-driven.

Store lesson content separately from components.

Example:

/content
  /lessons
  /puzzles

Avoid hardcoded lesson logic inside UI components.

---

# Component Philosophy

Prefer reusable primitives.

Examples:
- Button
- Card
- SectionHeader
- LessonCard
- ChessBoardWrapper
- ProgressCard

Avoid creating unique layouts for every page.

---

# Routing Philosophy

Keep routing shallow and simple.

Preferred structure:

/home
/learn
/practice
/play
/rewards

Do not introduce world-based routing initially.

Worlds can later become a visual layer on top of the same system.

---

# Animation Philosophy

Use minimal animation initially.

Allowed:
- hover states
- soft transitions
- simple scale effects

Avoid:
- complex motion systems
- particle effects
- heavy animation libraries

---

# Build Rules

- Prefer simple solutions
- Reuse layouts aggressively
- Keep components modular
- Avoid premature optimization
- Avoid deeply nested component trees
- Prioritize readability over abstraction

---

# Current MVP Scope

The first vertical slice should include:

1. Homepage
2. Knight lesson
3. Knight movement puzzle
4. Simple AI play screen
5. Reward/progress screen

No additional systems should be built before this flow works cleanly.
