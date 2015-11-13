# Redeveloping edmullen.com

## Setup

### Process

1. Created a repo in Github
1. Define an Anvil directory
1. I Started out using HTML 5 Boilerplate, but have stripped most of that out. There are a few remnants.
1. Laid out basic HTML structure
1. Set up some base SCSS @mixins based on Dan Cederholm's recommendations
   1. I am using Scout to compile the CSS
1. I've got my basic mixins set and working now.
1. I have set up my media queries. 
   * The site is mobile first. 
   * I have three main breakpoints: small-(default), medium-, large-screens. 
   * These are all set up with "@media only screen and (min-width:", meaning each breakpoint cascades up to larger sizes. 
   * I've also included two "tweakpoints" within each main breakpoint. 
   * "Large-screens" is the major shift to two columns.
1. Set up typography defaults - Using Normalize.css and a modular scale for type sizing
1. Site-specific typography, layout, and style applied.
[ ] Get Github back on track.
[ ] Migrating feedburner and rss subscriptions.
[ ] Add facebook open graph.
[ ] Add Google+ author stuff.
[ ] Make sure redirects are working right.
[ ] Adjust hr spacing.


### Tools I'm using

* Github desktop
* Anvil - For local development - Using xip.io for mobile local dev server only seems to work over personal wifi, not the office network.
* Normailize.css instead of a reset
* [jQuery-Stickem](https://github.com/davist11/jQuery-Stickem)
* Typekit (League Gothic, Proximo Nova, Adelle)
* SiteLeaf as CMS
* [Modular Scale](http://www.modularscale.com) - Using 18px @ 1:1.333 - 3:4 Perfect fourth 


### Reference materials

* [_SASS FOR WEB DESIGNERS_](http://www.abookapart.com/products/sass-for-web-designers) by Dan Cederholm - @simplebits
* [_7 Habits of Highly Effective Media Queries_](http://bradfrostweb.com/blog/post/7-habits-of-highly-effective-media-queries/)
* [Modular Scale](http://www.modularscale.com)


## Organization of Style Sheets

I have settled on an organizational scheme that I'm comfortable with. 

* **_normalize.scss** just duplicates the standardized normalize.css in .scss
* **_variable.scss** establishes some standard variables used throughout; largely influenced by Dan Cederholm.
* **_mixins.scss** establishes a number of reusable shorthand mixins; largely influenced by Dan Cederholm.
* **_baseline.scss** sets a baseline of styles after 'normalization' for preferred defaults and proportions. It is website/branding agnostic.
* **_theme_typography.scss** sets up all the base typographic and branding styles without establishing layout-specific aspects. This file does not really establish a layout of the site. When this file is removed, typographic styles revert to the baseline styles and styles established with variables. 
* **_theme_layout.scss** establishes the various styles for screen that are layout-specific. The default is mobile-first with two main breakpoints and two "tweakpoints" between each.
* **screen.scss** simply imports all necessary stylesheets. 

## Color palette

* Accent: #dc685d
* Dark neutral: #363d45
* Middle neutral: #757f8f
* Light Neutral: #e1d8d8


## Tasks

[ ] Remove and replace README.md
[ ] Remove LICENSE.md
[ ] Complete humans.txt, robotos.txt
[ ] Print CSS needed


