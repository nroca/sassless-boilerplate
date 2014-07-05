## Vendors

And last but not least, you will probably have a vendors/ folder containing all the CSS files from external libraries and frameworks – Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to tell “Hey, this is not from me, not my code, not my responsibility”.

Example:

* `bootstrap.scss`
* `jquery-ui.scss`
* `select2.scss`

On a side note, where I work we also have a `vendors-extensions/` folder where we store files overriding some tiny bits from vendors. For example, we have a `_bootstrap.scss` file in there that we can use to change some components in Bootstrap. This is to avoid editing the vendor files themselves, which is generally not a good idea.
