## React Scrollable
[![build status](https://travis-ci.org/yahoo/scrollable.svg)](https://travis-ci.org/yahoo/scrollable)
[![Coverage Status](https://coveralls.io/repos/yahoo/scrollable/badge.svg)](https://coveralls.io/r/yahoo/scrollable)

#### A library that brings smooth scrolling interactions to modern mobile browsers.

React Scrollable is a set of React.js components that provide an abstraction for layer composition and scroll events. The components provide a declarative API for independently positioning of each layer to create high performance, high frame rate interactions.

The project is tested in many iOS devices from iPhone 3GS to iPhone 6/6 plus and some variety of Android phones. Example uses cases can range from simple parallax effects to fully interactive gesture based websites that feel like native iOS/Android Apps.

Many examples are provided on the `examples/` folder.

### Development

##### Tests and coverage

    $ npm test

##### Build

    $ npm run build

##### Development (or just to see the examples)

    $ npm run dev

##### Development auto-watch unit tests (without coverage)

    $ karma start

Notice: The current version throws a lot of warnings about 'owner-based context'. To ignore this messages you can use the following regex on the Chrome Dev-Tools console filter: ^((?!owner-based).)*$

### Contributions Guideline

Pull requests, and issues are welcome. Not only for code but also for documentation and examples.

  * Use a code editor with JSXHint or run `jsxhint` before committing
  * Use a code editor with `.editorconfig` support or read the file
    and follow whitespace conventions
  * Please, pay attention to the tests, and ideally provide new
    tests alongside pull requests. If you are not used to testing, send
    pull requests anyway, but understand it might take a while until a
    maintainer can merge your pull request

### TODO notes

  * Server-side prefixes are hardcoded for webkit now (because of PhamtomJS)
    and ideally it should have multiple props in the compatibility order (e.g.
    -moz-transform:...;-webkit-transform:...;transform:...;)
  * I keep forgetting to create the nested scrolling example and the
    "Flipboard without canvas" example.
  * Size/Position dependencies in lower level, look at ExtJS anchorTo for
    a higher level API eventually
  * FPS meter on examples, maybe optional parameter
  * Styles are currently only on the examples, need to figure out a way to
    be in JavaScript and still be able to override via some API. Should it
    even be allowed?
  * Figure out build system to support:
    * CommonJS require if installed by npm
    * Dev build with warnings and/or performance profiling helpers
    * `require('scrollable/scroller')` or `require('scrollable').Scroller`
    * `npm run dev` as is, but compile examples folder with `react.min.js`
  * `scrollingX` and `scrollingY` props are mandatory `<Scroller>` for now.
    Explore ways to make this both optional with reasonable dafault and
    update/pull request Zynga Scroller to change this at runtime.
