# UI3kit
Starter development template for building [UIkit v3](https://getuikit.com/) themed [OctoberCMS](https://octobercms.com/) sites.

Includes:
- latest UIkit v3 (beta) [source from official repository](https://github.com/uikit/uikit)
- [GulpJS-based build system](https://nystudio107.com/blog/a-gulp-workflow-for-frontend-development-automation) for development and production
- [NPM-based config system](https://nystudio107.com/blog/a-better-package-json-for-the-frontend) for development and production


## Installation
Add the theme to existing project while logged into OctoberCMS account online,
or interactively by searching it inside Settings/System/Updates/Themes in backend,
or with the following command-line instructions inside *project root*:
```
php artisan theme:install castus.ui3kit ui3kit
php artisan theme:use ui3kit
```

## One-time Development Environment Setup
Install [NodeJS and Node Package Manager](https://nodejs.org/en/) globally (LTS version required).
Run the following command-line instructions inside *theme root*:
```
npm install --global gulp-cli
npm i
```
Alternative NPM-compatible package manager [Yarn](https://yarnpkg.com/en/) could be used:
```
yarn
```
Integrating build process into OctoberCMS project is easy - copy (or merge into existing) files into *project root*:
```
gulpfile.js
package.json
```
Adjust `paths.root` configuration variable to **themes/castus-ui3kit/** and start using command-line tasks from *project root*. 

## Using and Editing
Check [intro page](https://github.com/Eoler/oc-ui3kit-theme/blob/master/pages/ui3kit.htm)
for example HTML page structure and mandatory includes.
Development changes can be automated with command-line instruction inside *theme root*:
```
gulp watch
```
Build versioned, optimized, minified, autoprefixed assets with command-line instruction inside *theme root*:
```
gulp upbuild --production
```

## Customizing UIkit
Global framework/theme styling parameters are overridable in the following SCSS files:
- [assets/scss/uikit3 SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/uikit3.scss)
- [assets/scss/uikit3themed SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/uikit3themed.scss)
Just copy definitions from base variables/mixins (don't forget to remove !default from variables).  

Comment out unwanted components/theming for leaner and faster UIkit custom build:
- [assets/scss/_components-import SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/_components-import.scss)
- [assets/es6/_theme-import SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/_theme-import.scss)

For in-depth customizations and optimizations follow the [SASS docs](https://getuikit.com/docs/sass).
