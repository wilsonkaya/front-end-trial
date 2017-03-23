[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# ember-template

A template for starting projects with Ember as a client. Build pipeline and
development server provided by `ember-cli`. Bootstrap and Sass included.

## Updating Dependencies

At the beginning of each cohort update [`package.json`](package.json):
### npm
-   replace all dependent package versions in `package.json` with a glob (`*`).
-   `rm -r node_modules`.
-   `npm update --save`.
-   `npm update --save-dev`.
-   `npm install`

### bower
Currently bower [cannot automatically save updated versions](https://github.com/bower/bower/issues/2348) to `bower.json`.

-   `rm -r bower_components`
-   `bower update`
-   `bower list`
-   Take the new version numbers from the top level of the list and paste
    them into `bower.json`
-   `bower install`
-   `ember test`

Fix errors and conflicts as necessary.

## Dependencies

Install build dependencies with `npm install`. Install runtime dependencies with
`bower install`.
If you have not installed phantomjs, you will need to install it globally:
`npm install --global phantomjs-prebuil`

-   [ember.js](http://emberjs.com/)
-   [ember-cli](http://www.ember-cli.com/)
-   [Bootstrap](http://getbootstrap.com)

At the beginning of each cohort, update this template by upgrading `ember-cli`
and generating a new Ember application in another location. Copy files over a
handful at a time and check diffs. You should preserve the pods structure and
other customizations, including Bootstrap.

## Installation

1.  [Download](../../archive/master.zip) this template.
1.  Unzip and rename the template directory.
1.  Empty [`README.md`](README.md) and fill with your own content.
1.  Move into the new project and `git init`.
1.  Replace all instances of `'front-end-trial'` with your app name. This
    includes [`package.json`](package.json), [`bower.json`](bower.json),
    [`app/index.html`](app/index.html), [`tests/index.html`](tests/index.html),
    and [`config/environment.js`](config/environment.js), possibly others.
1.  Install dependencies with `npm install` and `bower install`.
1.  Run the development server with `ember server`. Use the `--proxy` flag to
    avoid writing development-specific CORS and CSP settings.

## Structure

Build dependencies are stored in [`package.json`](package.json). Client
dependencies are stored in [`bower.json`](bower.json).

Do not configure `grunt` packages directly in the
[`Gruntfile.js`](Gruntfile.js). Instead, store configurations in the
[`grunt`](grunt) directory. You won't need a top-level key, since that's
generated by the `Gruntfile.js` based on the filename of the configuration
object stored in the `grunt` directory.

Developers should store source code following Ember conventions. This template
uses the "pods" layout for organizing code. For an introduction, see [Organize
Your Ember App with Pods](http://cball.me/organize-your-ember-app-with-pods/).

## Tasks

Developers should run these often!

-   `grunt nag` or just `grunt`: runs code quality analysis tools on your code
    and complains
-   `grunt reformat`: reformats all your code in a standard style
-   `ember server`: generates bundles, watches, and livereloads (use the
    `--proxy` flag when developing locally)
-   `ember test`: runs any automated tests
-   `ember build`: prepare a distribution for deployment (use the
    `--environment` flag if you've customized builds)
-   `ember generate`: make use of the many generators for code (try `ember help
    generate` for more details)

## Additional Resources

-   [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
-   [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
