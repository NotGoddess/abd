# ABD: Pattern Lab + Drupal 8

Component-driven prototyping tool using [Pattern Lab v2](http://patternlab.io/) automated via Gulp/NPM. Also serves as _a starterkit_ Drupal 8 theme.

## Requirements

1.  [PHP 7.1](http://www.php.net/)
2.  [Node (we recommend NVM)](https://github.com/creationix/nvm)
3.  [Gulp](http://gulpjs.com/)
4.  [Composer](https://getcomposer.org/)
5.  Optional: [Yarn](https://github.com/yarnpkg/yarn)

## Prototyping (separate from Drupal, Wordpress, etc.)

abd supports both NPM and YARN.

Install with NPM:
`composer create-project notgoddess/abd --stability dev --no-interaction abd && cd abd && npm install`

Install with Yarn:
`composer create-project notgoddess/abd --stability dev --no-interaction abd && cd abd && yarn install`

## Drupal installation

### In a Composer-based Drupal install (recommended)

1. Require abd in your project `composer require notgoddess/abd`
2. Move into the original abd theme `cd web/themes/contrib/abd/`
3. Create your new theme by cloning abd `php abd.php "THEME NAME"` (Run `php abd.php -h` for other available options)
4. Move into your theme directory `cd web/themes/custom/THEME_NAME/`
5. Install the theme dependencies `npm install` or `yarn install`
6. Enable your theme and its dependencies `drush then THEME_NAME -y && drush en components unified_twig_ext -y`


## Windows glitches
A minor patch to emulsify-gulp has been added to allow pa11y testing to work in a Windows environment.

After installing you may need to update the pattern-lab styleguideKitPath variable.
Edit the file pattern-lab/config/config.yml and make `styleguideKitPath:` relative to the theme directory, e.g. `styleguideKitPath: 'vendor/pattern-lab/styleguidekit-twig-default'`

_Note: Once you've created your custom theme, you can remove abd as a dependency of your project. If you'd like to get updates as we push them, solely for educational/best-practice information, feel free to leave it in and receive the updates. Updating abd will not affect your custom theme in any way._

## Starting Pattern Lab and watch task

The `start` command spins up a local server, compiles everything (runs all required gulp tasks), and watches for changes.

1.  `npm start` or `yarn start`

---

## Highlighted Features

<table><tbody>
<tr><td>Lightweight</td><td>✔</td><td>abd is focused on being as lightweight as possible.</td></tr>
<tr><td>SVG sprite support </td><td><strong>✔</strong></td><td>Automated support for creating SVG sprites mixins/classes.</td></tr>
<tr><td>Stock Drupal templates </td><td><strong>✔</strong></td><td>Templates from Stable theme - see /templates directory</td></tr>
<tr><td>Stock Components </td><td><strong>✔</strong></td><td>with Drupal support built-in (https://github.com/notgoddess/abd#abds-built-in-components-with-drupal-support)</td></tr>
<tr><td>Performance Testing </td><td><strong>✔</strong></td><td>Support for testing via Google PageSpeed Insights and WebPageTest.org (https://github.com/notgoddess/abd/wiki/Gulp-Config#performance-testing)</td></tr>
<tr><td>Automated Github Deployment </td><td><strong>✔</strong></td><td>Deploy your Pattern Lab instance as a Github page (https://github.com/notgoddess/abd/wiki/Gulp-Config#deployment)</td></tr>
</tbody></table>

<h3 id="components">abd's Built in Components with Drupal support</h3>
Forms, tables, video, accordion, cards, breadcrumbs, tabs, pager, status messages, grid

View a [demo of these default abd components](https://notgoddess.github.io/abd/pattern-lab/public/).

## Documentation

This theme is based off the Four Kitchens Emulsify theme.  Documentation is currently provided in [their Wiki](https://github.com/fourkitches/emulsify/wiki).
