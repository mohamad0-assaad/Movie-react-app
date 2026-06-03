# Movie React App

A modern React + Vite movie discovery app with TMDb search and Appwrite-powered trending recommendations.

Users can search thousands of movies, view poster cards, ratings, language, and release year, and discover trending titles saved in Appwrite.

## Features

- Search movies using the TMDb API
- Debounced live search input for efficient querying
- Trending movies section powered by Appwrite document counts
- Responsive movie cards with posters, ratings, language, and year
- Loading and error handling states

## Getting Started

### Requirements

- Node.js 18+ or compatible version
- TMDb API key
- Appwrite project with database and collection configured

### Install

```bash
npm install
```

### Environment Variables

Create a `.env` file in the project root with:

```env
VITE_TMDB_API_KEY=your_tmdb_api_key
VITE_APPWRITE_DATABASE_id=your_appwrite_database_id
VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
```

> Note: The Appwrite endpoint is currently set to `https://fra.cloud.appwrite.io/v1` in `src/appwrite.js`.

### Run Locally

```bash
npm run dev
```

### Build

```bash
npm run build
```

### Preview

```bash
npm run preview
```

## Appwrite Integration

This app uses Appwrite to store search counts and retrieve trending movie cards.

- `updateSearchCount` stores or updates a search term count
- `getTrendingMovies` fetches the top 5 most searched movies

## Tech Stack

- React 19
- Vite
- Appwrite
- Tailwind-style CSS classes

## Project Structure

- `src/App.jsx` — main app and movie search logic
- `src/components/Search.jsx` — search input component
- `src/components/MovieCard.jsx` — movie display card
- `src/components/Spinner.jsx` — loading indicator
- `src/appwrite.js` — Appwrite database integration

## License

Distributed under the MIT License.
