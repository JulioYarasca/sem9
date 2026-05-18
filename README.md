# Sparky To Do

A simple React Native to-do list app built with Expo, developed as part of the Week 9 lab for the DBP 2025-2 course.

## Features

- Add new to-do items with an animated floating action button
- Edit to-do text inline
- Mark items as complete/incomplete with a toggle icon
- Delete individual items
- Auto-focuses the text input when a new item is created
- Scroll-aware FAB that collapses when scrolling down

## Tech Stack

| Tool | Version |
|------|---------|
| Expo | ~51.0.26 |
| React Native | 0.74.5 |
| React | 18.2.0 |
| React Native Paper | ^5.12.5 |
| TypeScript | ~5.3.3 |

## Project Structure

```
.
├── App.tsx                  # Root component — state management and layout
├── components/
│   └── TodoItem.tsx         # Individual to-do row component
├── interfaces/
│   └── Todo.ts              # Todo TypeScript interface
├── constants/
│   └── Colors.ts            # App color palette
├── assets/
│   ├── favicon.png
│   └── splash.png
├── app.json                 # Expo configuration
├── babel.config.js
└── tsconfig.json            # Path aliases (@components, @interfaces)
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS recommended)
- [Expo CLI](https://docs.expo.dev/get-started/installation/)

### Install dependencies

```bash
npm install
```

### Run the app

```bash
# Start the Expo dev server
npm start

# Run on Android
npm run android

# Run on iOS
npm run ios

# Run in the browser
npm run web
```

## Data Model

```ts
interface Todo {
  id: string;
  title: string;
  isCompleted: boolean;
}
```

## Notes

- State is held in memory only — todos are not persisted between sessions.
- Path aliases (`@components/*`, `@interfaces/*`) are configured via `tsconfig.json` and resolved at build time by `babel-preset-expo`.
# sem9
