# availity-uikit

> Availity UI Kit powered by [Bootstrap 3](http://getbootstrap.com/) and sprinkles of [Bootstrap 4](http://v4-alpha.getbootstrap.com/) with overrides to match our style guidelines.

## Table of Contents
* [Demo](#demo)
* [Supported Browsers](#supported-browsers)
* [Quickstart](#quickstart)
* [Icon Fonts](#icon-fonts)
* [Contributing](#contributing)
* [Authors](#authors)
* [Disclaimer](#disclaimer)
* [License](#license)
 
## Demo

[http://availity.github.io/availity-uikit](http://availity.github.io/availity-uikit)

## Supported Browsers

* Internet Explorer 9+
* Google Chrome > 1% market share
* Mozilla Firefox > 1% market share

> Internet Explorer 9 and below requires a CSS post processor in order to get circumvent the 4095 limit on selector on style sheets 

* [gulp-bless](https://github.com/BlessCSS/gulp-bless)
* [bless.js](https://github.com/BlessCSS/bless)
* [grunt-bless](https://github.com/BlessCSS/grunt-bless) 
* [bless-webpack-plugin(https://github.com/BlessCSS/bless-webpack-plugin)

## Quickstart

+ Install with Bower

```bash
$ bower install availity-uikit --save
```

+ Install with npm

```bash
$ npm install availity-uikit --save
```

+ Reference the compiled assets from the `/dist` in `index.html` 
+ If you use a module bundler like Webpack:

```js
import 'availity-uikit';
```

## Icon Fonts

Availity uses [Fontello](http://fontello.com/) to manage the UIKit icon fonts.  Our [font configuration](./fonts/config.json) can be used on Fontello to edit the font catalog.

## Contributing

### Dependencies 

+ [Node v5+](https://github.com/nodejs/node/releases)
+ [NPM v3+](https://docs.npmjs.com/how-npm-works/npm3)

#### CLI

+ `npm start` 
    * runs webpack dev server on `http://localhost:3000`
    * watches library and docs changes and automatically compiles the assets into `./build`
+ `npm run release`
    * prompts for version to tag the release
    * runs linter
    * clean `/dist`
    * runs the webpack build task with `NODE_ENV=production`
    * commits (generated files) and tags (version) the git repository
+ `npm run build`
    * cleans `/dist`
    * runs the webpack module bundler
    * produces regular and minified assets in `/dist
+ `npm run docs`
    * runs metalsmith and outputs to `/build`
    * runs webpack module bundler and outputs to `/dist`
+ `npm run lint`
    * runs Eslint across dev and lib files

### Update the Icon Font

+ Navigate to [Fontello](http://fontello.com/) and click on the wrench and import the config.json file located in /fonts/
+ Use the Fontello browser page to drag and drop and new svg icon fonts to the pre-populated list
+ Select any icon you want to be included in your updated icon font
+ Click the red "Download Webfont" button in the upper right hand corner
+ Extract the .zip file and overwrite the config.json in /fonts/ with the new config.json file within the .zip file
+ Replace the fonts in /fonts/ with those from the /font/ folder in your extracted .zip file
+ Locate the availity-icon-font.css (With the appended version number) and add the new icons css style to /less/availity-icon-fonts.less file
+ Add the new icons to the documentation page located at /docs/guide/pages/icons.html using the given formatting
+ Finally push your changes to the develop branch

## Authors

**Robert McGuinness**
+ [rob.mcguinness@availity.com](rob.mcguinness@availity.com)

**Robert Ventrone**
+ [robert.ventrone@availity.com](robert.ventrone@availity.com)

**Robert Warner**
+ [rob.warner@availity.com](rob.warner@availity.com)

**Bobby Bennett**
+ [bobby.bennett@availity.com](bobby.bennett@availity.com)

## Disclaimer

Open source software components distributed or made available in the Availity Materials are licensed to Company under the terms of the applicable open source license agreements, which may be found in text files included in the Availity Materials.

## License

[MIT](./LICENSE)

Copyright (c) 2016 Availity, LLC
