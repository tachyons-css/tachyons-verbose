# TACHYONS Verbose

Functional css for humans. Verbose edition.

Quickly build and design new UI without writing css.

## Principles

* Everything should be 100% responsive
* Everything should be readable on any device
* Everything should be as fast as possible
* Designing in the browser should be easy
* It should be easy to change any interface or part of an interface without breaking any existing interfaces
* Doing one thing extremely well promotes reusability and reduces repetition
* Documentation helps promote reusability and shared knowledge
* Css shouldn't impede accessibility or the default functionality of Html
* You should send the smallest possible amount of code to the user

## Features

* Mobile-first css architecture
* 8px baseline grid
* Multiple debugging utilities to reduce layout struggles
* Single-purpose class structure
* Optimized for maximum gzip compression
* Lightweight
* Usable across projects
* Growing open source component library
* Works well with plain html, react, ember, angular, rails, and more
* Infinitely nestable responsive grid system
* Works out of the box but easy to customize and extend

## Verbose?

The main difference between [Tachyons](https://github.com/tachyons-css/tachyons/) and [Tachyons Verbose](https://github.com/tachyons-css/tachyons-verbose) is the latter spells out all of its classes. So instead of `dib`, we will spell it out as `display-inlineblock`. Our naming conventions stay close to the original CSS properties so that you don't have to remember an extra acronym or naming convention. As a bonus, if your memory is rusty about CSS property names and values, using Tachyons Verbose will help you remember that too. In short, it's functional CSS with the lightest cognitive load possible, and the only downside is that the code initially looks ugly because there are a lot of words in the class declaration.

### Verbose class naming conventions

Tachyons Verbose classes use unambiguous naming:

`.propertyname-value-mediaquerysize`

As you can see, hyphens are only used to separate the properties from their values, or to add on a conditional media query. For example:

- `.textalign-center` maps to `{ text-align: center; }`
- `.position-absolute` maps to  `{ position: absolute; }`

Media queries are labeled as `mediaS`, `mediaM`, `mediaL` or `mediaXL` for small, medium and large screen sizes. In the future, we will support container queries as well, which is why we decided there was need to clarify these are for `@media` queries. So:

- `.textalign-center-mediaS` maps to `{ text-align: center; }` when the screen size is `30em` or more. You can set what the media query breakpoints are at in `src/_media-queries.css`.

Because CSS class names don't support most symbols and punctuation marks, we had to make our workarounds for certain values. For example:

- `.width-100percent` maps to `{ width: 100%; }`
- `.lineheight-1p5` maps to `{ line-height: 1.5; }` as in "one point five"
- `.margin-minus2` maps to `{ margin: calc(-1 * var(--spacing-2)); }` where "minus" also means negative

As you can see, some of our class names use double dash `--` variables that you can adjust in `src/_variables.css`.

## Tachyons Verbose specific implementation

This release of Tachyons Verbose is a verbose fork of the [Tachyons v5.0.0.beta](https://github.com/tachyons-css/tachyons/tree/v5-final-final). Aside from different naming conventions, we also made a few additions:

- If specific values are referenced in size scale, you can refer to both as a part of the scale and as the literal value. E.g. 1`backgroundsize-3` and `.backgroundsize-16px` both map to `{ background-size: 16px; }`.
- In parallel to the numerical size scales, we also use `small`, `medium` ad `large` for heights, widths, margins and paddings. In this scheme, `padding-medium` gives 1 rem of padding. To increase the size use `large`, `xlarge`, `xxlarge`, `xxxlarge`, etc. To decrease use `small`, `xsmall`, `xxsmall`, `xxxsmall`, etc.
- Tachyons v5.0.0.beta replaces all media queries with container queries. Tachyons Verbose hasn't changed over yet because a) container query support is still relatively new, and b) we haven't been able to use dynamic variables for container query breakpoints yet.

## What to know if you're an existing user of Tachyons Verbose (v4 from 2018)

- Most of the stuff is still the same! Don't fret about having to learn a completely new thing.
- You can now adjust scales, sizes and colors in `src/_variables.css`.
- The font scale (`f1` or `fontsize-2`) runs linearly with `1` being the smallest and `12` being the biggest.
- The colors have new names. E.g. `backgroundcolor-red` is no longer a class, but you get a whole spectrum from `backgroundcolor-red1` to `backgroundcolor-red11`.
- Media queries are no longer referenced with a simple `-m` or `l` suffix. They are now referenced as `-mediaM` and `mediaL`. Oh and `-ns` is now `-mediaS`.
- But hey, there's a new media query size at `mediaXL`.
- The legacy v4 files are the `css` folder in case previous users want to reference them or want to link to both the legacy and new versions at the same time for a more gradual transition.
- We renamed our CSS files to `tachyons-verbose.css`.

## Getting Started

### Local setup

Download the repo from github and install dependencies through npm.

```
cd tachyons-verbose
npm install
```

#### Dev

If you want to just use everything in tachyons/src as a jumping off point and edit all the code yourself, you can compile all of your wonderful changes by running

```npm start```

This will output both minified and unminified versions of the css to the css directory and watch the src directory for changes. It's aliased to the command:

If you want to recompile everything from src everytime you save a change - you can run the following command, which will compile and minify the css

```npm run build:watch```

If you'd like to just build the css once without watching the src directory run

```npm run build```

If you want to check that a class hasn't been redefined or 'mutated' there is a linter to check that all of the classes have only been defined once. This can be useful if you are using another library or have written some of your own css and want to make sure there are no naming collisions. To do this run the command

```npm run mutations```

## Contributing

Please read our [code of conduct](https://github.com/tachyons-css/tachyons-verbose/blob/master/code-of-conduct.md) for contributors.

## Help

If you have a question or need help feel free to [open an issue here](https://github.com/tachyons-css/tachyons-verbose/issues/new).

## About Tachyons

For more information about (non-verbose) Tachyons, check out [tachyons.io](https://tachyons.io/) and its docs section at [https://tachyons.io/docs/](https://tachyons.io/docs/).