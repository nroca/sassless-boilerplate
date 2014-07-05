## Pages

If you have page-specific styles, I think it’s cool to put them in a `pages/` folder and in a file named after the page. For example, it’s not uncommon to have very specific styles for the home page, so you’d have a `_home.scss` file in `pages/` dealing with this.

* `_home.scss`
* `_contact.scss`

Depending on your deployment process, those files could be called on their own to avoid merging them with the others in the resulting stylesheet. It is really up to you. Where I work, we decided to make them not-partials in order to include them only on pages requiring them. For example, our home page has a very specific layout, compiling to about 200 lines of CSS. To prevent those rules from being loaded on every page, we include this file only on the home page.
