# Pokémon Explorer (PokéAPI + RTK Query)

A small React app I built to learn API handling. It lists Pokémon from the public [PokéAPI](https://pokeapi.co/) and shows a details page for each one.

## Features

- Paginated Pokémon list (20 per page) with **Prev** and **Next** buttons
- **Open** button on each row goes to `/details/:name`, which shows the Pokémon's sprite
- Data fetching and caching with Redux Toolkit Query

## Tech Stack

- React 19 + TypeScript + Vite
- Redux Toolkit (RTK Query)
- React Router 7
- Tailwind CSS 4
- Axios (installed)

## Getting Started

**Prerequisites:** Node.js 18+ and npm

```bash
git clone https://github.com/BALASUBRAMANIYAN-S/Learning_of_pockapi_Application.git
cd Learning_of_pockapi_Application
npm install
npm run dev
```

Open the URL shown in the terminal (usually `http://localhost:5173`).

| Command | What it does |
|---|---|
| `npm run dev` | Start the dev server |
| `npm run build` | Type-check and build for production |
| `npm run preview` | Preview the production build |
| `npm run lint` | Run ESLint |

## Project Structure

```
src/
├── app/store.ts            # Redux store
├── services/UserApi.ts     # RTK Query endpoints (list + by name)
├── Components/
│   ├── ApiPage.tsx         # Paginated list
│   └── ImagePage.tsx       # Details page
├── App.tsx                 # Routes
└── main.tsx
```

## API

Base URL: `https://pokeapi.co/api/v2/`

- `pokemon?limit=20&offset=N` for the list
- `pokemon/{name}` for a single Pokémon

An internet connection is required.
