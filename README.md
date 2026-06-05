# Muscular System Anatomy Challenge

React + TypeScript + Tailwind implementation of the Muscular System Anatomy Challenge.

This version is structured as a reusable game template for future anatomy games such as skull, heart, brain, and digestive system.

## Stack

- React
- TypeScript
- Tailwind CSS
- Vite

## Structure

- `src/types/game.ts` defines reusable game, question, and result contracts.
- `src/data/muscularGame.ts` contains the current muscular system hotspot question set.
- `src/data/gameModes.ts` contains shared mode definitions.
- `src/hooks/useHotspotGame.ts` owns gameplay state, scoring, timing, logs, and results.
- `src/components/` contains reusable UI pieces: HUD, mode selection, hotspot diagram, quiz panel, answer log, and result board.

## Add Another Anatomy Game

Create a new config file under `src/data/`, following the `AnatomyGameConfig` shape:

```ts
export const muscularGame: AnatomyGameConfig = {
  id: 'muscular-system',
  title: 'Muscular System Anatomy Challenge',
  topic: 'Muscular system anatomy',
  description: 'Choose a mode, then tap each named muscular structure.',
  asset: {
    src: '/muscular-system.png',
    alt: 'Muscular system diagram',
  },
  items: [],
}
```

Then pass that config into `useHotspotGame()` and the visual components.

## Development

```bash
npm install
npm run dev
npm run build
```
