# Streaming Site UI (React)

A front-end practice build of a movie-streaming home page, styled after the
familiar streaming-service layout. It has a hero carousel, horizontally
scrolling movie rows and a watch page that plays a local video clip. Movie data
lives in a local file (`src/dummyData.js`); there is no API or backend.

## What's in it

- **Hero carousel.** Full-width slides with title, rating, runtime, cast and genres, built with `react-slick` (`components/homes`).
- **Movie rows.** "Upcoming", "Latest" and "Recommended" rows rendered from the same `Upcomming` slider component, plus a "Trending" section (`components/upcoming`, `components/trending`).
- **Watch page.** `/singlepage/:id` looks up the movie by id and plays its MP4 with the native `<video>` player (`components/watch/SinglePage.jsx`).
- **Responsive header.** Hamburger toggle for the nav menu on small screens.

## Tech stack

- React (Create React App)
- React Router 5 (`Switch` / `component` route API)
- `react-slick` + `slick-carousel`
- Plain CSS per component, Font Awesome icons

## Project layout

```
src/
  App.js              router: home page and watch page
  home/HomePage.jsx   page composition
  components/         header, homes (hero), upcoming, trending, watch, footer
  dummyData.js        movie metadata
public/images, public/video   artwork and sample clips (~23 MB of video)
```

## Running locally

Requires Node.js.

```bash
npm install
npm start
```

The app opens at http://localhost:3000.

Note: `package.json` pairs React 19 with React Router 5. If `npm install`
reports peer-dependency conflicts, `npm install --legacy-peer-deps` installs
the versions as listed.
