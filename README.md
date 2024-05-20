# UI3kit
Starter development template for building [UIkit v3](https://getuikit.com/) themed [OctoberCMS](https://octobercms.com/) sites.

Includes:
- latest UIkit ^3.21 [source from official repository](https://github.com/uikit/uikit)
- style guide layout with most UI components
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
Install [NodeJS and Node Package Manager](https://nodejs.org/en/) globally (LTS version preferred for Gulp ^3).
Run the following command-line instructions inside *theme root*:
```
npm install --global gulp-cli
npm install
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
Development changes can be automated with command-line instruction from configured Gulpfile (project or theme) *build root*:
```
gulp watch
```
Build versioned, optimized, minified, autoprefixed assets with command-line instruction:
```
gulp upbuild --production
```

## Customizing UIkit Styles
Override global framework/theme styling parameters in the following SCSS files, just don't forget to remove *!default* from variables:
- [assets/scss/uikit3 SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/uikit3.scss)
- [assets/scss/_components-variables SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/_components-variables.scss)
- [assets/scss/uikit3themed SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/uikit3themed.scss)
- [assets/scss/_theme-variables SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/_theme-variables.scss)

Comment out unwanted components/theming for leaner and faster UIkit custom build:
- [assets/scss/_components-import SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/_components-import.scss)
- [assets/scss/_theme-import SCSS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/scss/_theme-import.scss)

For in-depth customizations and optimizations follow the [SASS docs](https://getuikit.com/docs/sass).

## Including Custom JavaScript
Use Gulp-include plugin to require JavaScript source files from anywhere in `paths.include.js` hierarchy, example:
- [assets/es6/detect.JS](https://github.com/Eoler/oc-ui3kit-theme/blob/master/assets/es6/detect.js)
