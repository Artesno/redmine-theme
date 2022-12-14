# DITine

A free Redmine 3.0+ theme written in SCSS also compatible with redmine 5.x.x+

![The MIT License](https://img.shields.io/badge/license-MIT-584492.svg) [![JavaScript Style Guide](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/) 

---

![Screenshot]

It's written in [SCSS]. It uses [normalize.css] and benefits from some parts of [Bootstrap][bootstrap-sass] like mixins, structure, and stuff.

## Main features

* Bigger, easier to read fonts,
* Github-like wiki content look,
* Sidebar moved to the left for better ergonomy,
* Coloring trackers links (on lists, issue pages and even in the wiki content),
* Jira-inspired priority icons,
* Toggling sidebar visibility,
* Easy to customize via variables.

## How install it

To install DITMine, just download [.zip] and unpack it to your Redmine's `public/themes` folder.

Then go to Redmine > Administration > Settings > Display and select DITMine from the list and save the changes.

## Plugins

This theme also features a new look for [Redmine Backlogs][redmine_backlogs] plugin. To install it, simply copy stylesheets from `DITMine/plugins/redmine_backlogs` and overwrite files in `{redmine}/plugins/redmine_backlogs/assets/stylesheets` and restart Redmine.

Also, [Redmine Time Tracker][redmine_time_tracker],[Redmine People][redmine_crm_people] and [Dashboard (https://github.com/akpaevj/dashboard)] plugins should look nice with DITMine.

## How to customize it

If you want to customize DITMine to your needs, first, make sure that you have installed [node.js](http://nodejs.org/) and `npm` is available in your terminal.

Then, from the directory that contains DITMine run:

    npm install

Now all the dependencies should be ready to use. Run one more command:

    npm run watch

And now the grunt is watching for changes in files placed in `src/` folder. Just change what you need, and it'll run Sass preprocessor automatically.

Regrettably, optional file include is not possible in Sass, so I would recommend creating a new file, e.g. `src/sass/_custom-variables.scss` and importing it a the beginning of the `application.scss` file. That way all the variables with the `!default` flag could be overridden.

The path `src/sass/_custom-variables.scss` is added to `.gitignore` so it should make upgrading DITMine with keeping your changes rather painless, given that the only thing you changed in DITMine's source was adding this one line with `@import "custom-variables";`.

If you need to customize styles for [Redmine Backlogs][redmine_backlogs] remember to include your `_custom-variables.scss` in `src/sass/plugins/redmine_backlogs/_common.scss`.

## Changelog

[Changelog](./CHANGELOG.md).

[SCSS]: http://sass-lang.com/
[normalize.css]: https://github.com/necolas/normalize.css
[bootstrap-sass]: https://github.com/twbs/bootstrap-sass
[redmine_backlogs]: https://github.com/backlogs/redmine_backlogs
[redmine_time_tracker]: https://github.com/hicknhack-software/redmine_time_tracker
[redmine_crm_people]: http://www.redminecrm.com/projects/people/
