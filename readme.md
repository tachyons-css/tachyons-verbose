# TACHYONS (verbose)

Functional CSS for humans. Verbose edition.

Quickly build and design new UI without writing CSS.

## Principles

* Everything should be 100% responsive
* Everything should be readable on any device
* Everything should be as performant as possible
* Designing in the browser should be easy
* It should be easy to change any interface or part of an interface without breaking any existing interfaces
* Doing one thing extremely well promotes reusability and reduces repetition
* CSS is global. HTML is not. Send the smallest amount of code to the user as possible.

## Features

* Mobile-first css
* Single-purpose class structure
* Optimized for maximum gzip compression
* Usable across projects
* Infinitely nestable responsive grid system
* Built with Postcss

## Verbose?

This "verbose" edition of Tachyons uses an unambiguous naming formula for those of us who are bad at acronyms and for ease of sharing with non-tachyons-using team members:

`classname-value-screensize`

Examples:

* `{ clear: left }` is `clear-left`
* `{ max-width: 100% }` on large screens is `maxwidth-100p-l`
* `{ padding-bottom: 2rem }` for mobile and up is `paddingbottom-medium`

On top of being verbose this edition of Tachyons also adds support for: 1) British spelling for grey/gray, 2) more options for widths and heights, 3) a .f7 type scale, and 4) class name support for .screen-reader-text and .says (used by some systems).

## Getting started

Docs (for the non-verbose original edition) can be found at http://tachyons.io/docs The modules are generally pretty small and thus easy to read and grock if you're familiar with css at all.

### Local setup

Download the repo from github and install dependencies through npm.

```
cd tachyons-verbose
npm install
```

#### Build

##### First time

Tachyons is available as a series of small self contained css modules. They aren't dependent on each other but are designed to play well together. But tachyons is also just css. And you should feel free to edit css that is in your project. The first time you build tachyons all of the css gets installed via npm, but the modules then get copied over to your local src directory and then the [`tachyons-cli`](https://github.com/tachyons-css/tachyons-cli) uses a series of postcss plugins to compile the source down to vanilla css.

##### Updating

If you want to update a tachyons partial, install the desired module version via npm and run the build command again. Note this will copy over all source files, so if you've modified src/ your changes might will be overwritten but you can use version control (like git!) to undo these changes.
```npm run build```

Warning: updating from npm modules will override any verbose naming conventions because the original modules all use the default, abbreviated naming scheme.

#### Dev

If you want to just use src as a jumping off point and edit all the code yourself, you can compile all of your wonderful changes by running

```npm start```

This will output both minified and unminified versions of the css to the css directory.

If you want to recompile everything from src everytime you save a change - you can run the following command, which will compile and minify the css

```npm run build:watch```

If you want to check that a class hasn't been redefined or 'mutated' there is a linter to check that all of the classes have only been defined once. This can be useful if you are using another library or have written some of your own css and want to make sure there are no naming collisions. To do this run the command

```npm run mutations```

## Contributing

If you want to make a PR to change part of the css source for tachyons, make sure you make the PR on the corresponding module
that can be found in the [tachyons org](http://github.com/tachyons-css/). Those modules get copied into the main repo so
any changes you make to the css in this repo would get overridden.

Also please read our [code of conduct](https://github.com/tachyons-css/tachyons/blob/master/code-of-conduct.md) for contributors.

## Some websites that use modules from the tachyons project
(if you have a project that uses tachyons feel free to make a PR to add it to this list)

* http://spenhar.com
* http://www.csspurge.com
* http://bluebottlecoffee.com
* http://aboutlife.com
* http://clrs.cc
* http://mrmrs.io/gradients
* http://joinoneroom.com
* https://www.getnoodl.es
* https://natwelch.com
* http://mrmrs.io/profile/
* http://mn-ml.cc
* http://pesticide.io
* http://mrmrs.io/btns/
* http://zachhurd.com
* http://mrmrs.cc
* http://mrmrs.io/up/
* http://mrmrs.io/beats/
* http://mrmrs.io/writing
* http://fade.pics
* http://gfffs.com
* https://wordpress.org/themes/vanilla-milkshake/
* http://comics.hongkonggong.com/
* http://jon.gold/txt
* http://rene.jon.gold

And of course...
* http://tachyons.io

## Help

If you have a question feel free to open an issue here or jump into the [Tachyons slack channel](http://tachyons-slack-invite.herokuapp.com).

## License

MIT
