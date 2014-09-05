# SassLess-Boilerplate

Based on article by sitepoint @ http://www.sitepoint.com/architecture-sass-project/

## Installation

1. Download the contents of this repo to your less/sass directory.
2. Begin coding.

## ToDo

* Write more detailed descriptions for each folder.
* Include base files.

## Credit to
Thanks to the original author of the SitePoint article, Hugo Giraudel, for sharing his best practices. http://www.sitepoint.com/author/hgiraudel/

## Descriptions

###Base

The `base/` folder holds what we might call the boilerplate stuff for your project. In there, you might find the reset (or Normalize.css, or whatever), probably some stuff dealing with typography, and, depending on the project, maybe some other files.

* `_reset.scss`gs or `_normalize.scss`
* `_typography.scss`

###Components

For smaller components, there is the `components/` folder (frequently called `modules/`). While layout/ is kind of macro (defining the global wireframe), `components/` is more micro. It can contain all kinds of specific modules like a slider, a loader, a widget, or anything along those lines. There are usually a lot of files in `components/` since your site is should be mostly composed of tiny modules.

* `_media.scss`
* `_carousel.scss`
* `_thumbnails.scss`

### Helpers

The `helpers/` folder (sometimes called `utils/`) gathers all Sass tools and helpers we’ll use across the project. Got a function? A mixin? Put it in there. This folder also contains a _variables.scss file (sometimes `_config.scss`) which holds all global variables for the project (for typography, color schemes, and so on).

`_variables.scss`
`_mixins.scss`
`_functions.scss`
`_placeholders.scss` (frequently named `_helpers.scss`)


### Layout

The `layout/` directory (sometimes called `partials/`) usually contains a number of files, each of them setting some styles for the main sections of the layout (header, footer, and so on). It also contains the `_grid` file which is the grid system used to build the layout.

`_grid.scss`
`_header.scss`
`_footer.scss`
`_sidebar.scss`
`_forms.scss`
Having the navigation file (`_navigation.scss`) in this folder could make sense although I use to put it in `components/`. I think it would be better in the `/layout` folder but I’ll let you decide.

### Pages

If you have page-specific styles, I think it’s cool to put them in a `pages/` folder and in a file named after the page. For example, it’s not uncommon to have very specific styles for the home page, so you’d have a `_home.scss` file in `pages/` dealing with this.

* `_home.scss`
* `_contact.scss`

Depending on your deployment process, those files could be called on their own to avoid merging them with the others in the resulting stylesheet. It is really up to you. Where I work, we decided to make them not-partials in order to include them only on pages requiring them. For example, our home page has a very specific layout, compiling to about 200 lines of CSS. To prevent those rules from being loaded on every page, we include this file only on the home page.

### Themes

If you are working on a large site with multiple themes like I do, having a `themes/` folder can make sense. You can stuff all your theme/design related styles in there. This is definitely project-specific so be sure to include it only if you feel the need.

* `_theme.scss`
* `_admin.scss`

### Vendors

And last but not least, you will probably have a vendors/ folder containing all the CSS files from external libraries and frameworks – Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to tell “Hey, this is not from me, not my code, not my responsibility”.

Example:

* `bootstrap.scss`
* `jquery-ui.scss`
* `select2.scss`

On a side note, where I work we also have a `vendors-extensions/` folder where we store files overriding some tiny bits from vendors. For example, we have a `_bootstrap.scss` file in there that we can use to change some components in Bootstrap. This is to avoid editing the vendor files themselves, which is generally not a good idea.
