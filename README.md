# Docker Intro

A tutorial on docker, docker-compose, and micro-services.

## Build and Run

- Install [Node.js](https://nodejs.org/en/) (Recommendation: version 10.17.0 LTS - or use nvm)
- Clone this repository
- Run `npm install` to install dependencies
- Run `npm run build` to build presentation into the `dist` folder.
  - You can put this `dist` folder directly on a webserver to publish the material.
- Alternatively run `npm start` during content creation to build in case of changes and serve using a local dev server @ [localhost:8000](http://localhost:8000).
  - To change port you have to open `package.json` and modify  the start script (e.g `serve dist -l 8001`)
