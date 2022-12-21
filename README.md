## Set up

1. `npm install`

2. ```bash
   npm run dev
   # or
   yarn dev
   ```

3. Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Routing

vennbury.com/ <br />
................../courses <br />
................../......./[course name] <br />
................../......./............/[module name] <br />
................../......./............/............./[lesson name] <br />
................../personal (cabinet) <br />
................../[other services] <br />
................../[404 if nothing matches] <br />

## UI

We use [Chakra-UI](https://chakra-ui.com) component library.

## lib

Polished libraries and functionalities (DB integration, models, controllers, etc.)

## utils

Various cross-concern bits and pieces

## components

React components that our website comprises.

### layouts

Main.js is the layout for the whole website (navbar, footer, etc.). Page.js is a layout for page transition animation.

## .env.local

Necessary production constants. Contact @furilon or @nikitamalinovsky for more information.

## public

Static files (pictures, fonts, etc.)
