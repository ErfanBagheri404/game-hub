# Game Hub

Game discovery app on top of the RAWG API: browse games, filter by genre and
platform, sort by popularity/score/date, and search by name. Built while working
through Mosh Hamedani's React course, extended with TypeScript, Chakra UI,
skeletons and infinite-ish grid paging.

**Live:** https://rawg-gamehub.netlify.app

## Features

- Genre sidebar with cover images (`GenreList`).
- Platform selector with icons (`PlatformSelector`, `PlatformIconList`).
- Sort selector: relevance, date added, name, release date, popularity, average rating.
- Debounced search (`SearchInput`).
- Light/dark toggle (`ColorModeSwitch`) via Chakra's colour mode.
- Loading skeletons (`GameCardSkeleton`) and critic score badges (`CriticScore`).

## Stack

React 18 - TypeScript - Vite - Chakra UI - Axios - RAWG API.

## Run

```bash
git clone https://github.com/ErfanBagheri404/game-hub.git
cd game-hub
```

```bash
npm install
npm run dev
```

The RAWG key is set as the `key` param in `src/services/api-client.ts`. RAWG has
a free tier; swap in your own key for anything beyond local use.

## Structure

| path | role |
|---|---|
| `src/App.tsx` | layout + `GameQuery` state |
| `src/services/api-client.ts` | axios instance for `api.rawg.io/api` |
| `src/hooks/` | data fetching hooks (games, genres, platforms) |
| `src/components/` | navbar, filters, cards, grid |
