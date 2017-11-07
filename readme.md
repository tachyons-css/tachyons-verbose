# TACHYONS (verbose)

Functional css for humans. Verbose edition.

Quickly build and design new UI without writing css.

Version 4.9.0.

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
* 490 accessible color combinations
* 8px baseline grid
* Multiple debugging utilities to reduce layout struggles
* Single-purpose class structure
* Optimized for maximum gzip compression
* Lightweight
* Usable across projects
* Growing open source component library
* Works well with plain html, react, ember, angular, rails, and more
* Infinitely nestable responsive grid system
* Built with Postcss

## Verbose?

This "verbose" edition of Tachyons uses an unambiguous naming formula for those of us who are bad at acronyms and for ease of sharing with non-tachyons-using team members:

`classname-value-screensize`

Examples:

* `{ clear: left }` is `clear-left`
* `{ max-width: 100% }` on large screens is `maxwidth-100p-l`
* `{ padding-bottom: 2rem }` for mobile and up is `paddingbottom-medium`

On top of being verbose this edition of Tachyons also adds support for: 1) British spelling for grey/gray, 2) more options for widths and heights, and 3) class name support for .screen-reader-text and .says (used by some systems).

## Getting started

Docs (for the non-verbose original edition) can be found at http://tachyons.io/docs The modules are generally pretty small and thus quick and easy to read.

### Local setup

Download the repo from github and install dependencies through npm.

```
cd tachyons-verbose
npm install
```

#### Dev

If you want to just use everything in tachyons/src as a jumping off point and
edit all the code yourself, you can compile all of your wonderful changes by
running

```npm start```

This will output both minified and unminified versions of the css to the css directory and watch the src directory for changes. It's aliased to the command:

If you want to recompile everything from src everytime you save a change - you can run the following command, which will compile and minify the css

```npm run build:watch```

If you'd like to just build the css once without watching the src directory run

```npm run build```

If you want to check that a class hasn't been redefined or 'mutated' there is a linter to check that all of the classes have only been defined once. This can be useful if you are using another library or have written some of your own css and want to make sure there are no naming collisions. To do this run the command

```npm run mutations```

## Docs
The tachyons docs located at http://tachyons.io are all open source and located at https://github.com/tachyons-css/tachyons-css.github.io

You can clone the docs and use them as a template for documenting your own design system / patterns / components. While not everything is automated, the component library generation makes it extremely easy to generate and organize the documentation for components as demonstrated at http://tachyons.io/components

## Contributing

If you want to make a PR to change part of the css source for tachyons, make sure you make the PR on the corresponding module
that can be found in the [tachyons org](http://github.com/tachyons-css/). Those modules get copied into the main repo so
any changes you make to the css in this repo would get overridden.

Also please read our [code of conduct](https://github.com/tachyons-css/tachyons/blob/master/code-of-conduct.md) for contributors.

## Tachyons in Production

A longer list of sites that use tachyons in production can be found in sites.md
We love letting the community see what people are building so please add your link to sites.md in a PR or by opening an issue if you're willing to share to your site or project.

**Featured Sites**

* https://interfacelovers.com
* https://friendstalkfrontend.com
* https://gohugo.io
* https://coralproject.net
* http://www.philipyoungg.com
* https://gitpoint.co
* https://2017.nodeconf.com.ar
* https://goldenstaterecord.com
* http://hicuties.com
* https://urlbox.io
* https://fontawesome.com
* https://purple3.herokuapp.com
* http://blunt.af/tachy.app/
* https://fenderdigital.github.io/css-utilities/intro/

And of course...
* http://tachyons.io

## Help

If you have a question feel free to open an issue here or jump into the [Tachyons slack channel](http://tachyons-slack-invite.herokuapp.com).

## License

MIT
