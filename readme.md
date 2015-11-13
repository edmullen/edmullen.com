# edmullen.com

This is the personal website of Ed Mullen.


## Local development

* **Uses SCSS** - Run *Scout* to compile to CSS
  * Scout should be configured to output CSS in *CSS* directory
* **Siteleaf is the CMS** - View local server using Siteleaf.com content at edmullen.dev
  * If stopped, in terminal: try running "siteleaf config edmullen.com" inside *edmullen* directory
* **To push theme** - In terminal: *siteleaf push theme*
* **To publish** - In terminal: *siteleaf publish*
* **Redirects** - files for edmullen.com and makinggood.edmullen are in *edmullen-assets* in the *Sites* directory


### Tools

* [Github](https://github.com/edmullen/edmullen.com)
* [Scout](https://mhs.github.io/scout-app/) for compiling CSS https://mhs.github.io/scout-app/
* [Normailize.css](https://necolas.github.io/normalize.css/) instead of a reset
* [jQuery-Stickem](https://github.com/davist11/jQuery-Stickem)
* [Typekit](https://typekit.com/) - (League Gothic, Proximo Nova, Adelle)
* [SiteLeaf](http://www.siteleaf.com/) as CMS
* [Modular Scale](http://www.modularscale.com) - Using 18px @ 1:1.333 - 3:4 Perfect fourth


## Organization of Style Sheets

I have settled on an organizational scheme that I'm comfortable with.

* **_normalize.scss** just duplicates the standardized normalize.css in .scss
* **_variable.scss** establishes some standard variables used throughout; largely influenced by Dan Cederholm.
* **_mixins.scss** establishes a number of reusable shorthand mixins; largely influenced by Dan Cederholm.
* **_baseline.scss** sets a baseline of styles after 'normalization' for preferred defaults and proportions. It is website/branding agnostic.
* **_theme_typography.scss** sets up all the base typographic and branding styles without establishing layout-specific aspects. This file does not really establish a layout of the site. When this file is removed, typographic styles revert to the baseline styles and styles established with variables.
* **_theme_layout.scss** establishes the various styles for screen that are layout-specific. The default is mobile-first with two main breakpoints and two "tweakpoints" between each.
* **screen.scss** simply imports all necessary stylesheets.


### Reference materials

* [_SASS FOR WEB DESIGNERS_](http://www.abookapart.com/products/sass-for-web-designers) by Dan Cederholm - @simplebits
* [_7 Habits of Highly Effective Media Queries_](http://bradfrostweb.com/blog/post/7-habits-of-highly-effective-media-queries/)
* [Modular Scale](http://www.modularscale.com)
