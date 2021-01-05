<div align="center">
  <div>
    <img width="100" height="100" src="https://webpack.js.org/assets/icon-square-big.svg">
    <h1>Webpack Project</h1>
  </div>
  <p>
    This project requires you to build a web tool that allows users to run Natural Language Processing (NLP) on articles or blogs found on other websites.
  </p>
</div>


## Build Setup:
* Insert your Meaning Cloud API key to .env file like this:
``` bash
API_KEY=****
```

``` bash
# Install dependencies:
npm install
```

``` bash
# Testing with JEST
npm run test
```

* For development mode:
``` bash
# Server with hot reload at http://localhost:8080/
# Please note that the script will start an additional server on the 3000th port for the API
npm run dev
```

* For production mode:
``` bash
# Output will be at dist/ folder
npm run build
# Server at http://localhost:[port]/
npm start [--port=3000]
```

## Project Structure:

* `src/client/index.html` - main app HTML;
* `src/client/assets/styles` - put custom app SCSS styles here. Don't forget to import them in `index.js`;
* `src/client/assets/img` - put images here. Don't forget to use correct path: `assets/img/some.jpg`;
* `src/client/js` - put custom app scripts here;
* `src/client/index.js` - main app file where you include/import all required libs and init app;
* `src/client/static/` - folder with extra static assets that will be copied into output folder;
* `src/server` - folder with server part;
* `webpack.config` - folder with configs for Webpack (both dev and prod).

<div align="center">
  <h2>Settings:</h2>
</div>

## Main const:
Easy way to move all files.
Default:
``` js
const PATHS = {
  // Path to main app dir
  src: path.join(__dirname, '../src'),
  // Path to Output dir
  dist: path.join(__dirname, '../dist'),
  // Path to Second Output dir (js/css/fonts etc folder)
  assets: 'assets'
}
```
## Customize:
Change any folders:
``` js
const PATHS = {
  // src must be src
  src: path.join(__dirname, '../src'),
  // dist to public
  dist: path.join(__dirname, '../public'),
  // assets to static
  assets: 'static'
}
```

## Import Another libs:
1. Install libs
2. Import libs in `./index.js`
``` js
// React example
import React from 'react'
// Bootstrap example
import Bootstrap from 'bootstrap/dist/js/bootstrap.min.js'
import 'bootstrap/dist/js/bootstrap.min.js'
```

## Import js files:
1. Create another js module in `./js/` folder
2. Import modules in `./js/index.js` file