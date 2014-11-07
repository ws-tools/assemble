# assemble [![NPM version](https://badge.fury.io/js/assemble.svg)](http://badge.fury.io/js/assemble)  [![Build Status](https://travis-ci.org/assemble/assemble.svg)](https://travis-ci.org/assemble/assemble) 


> Static site generator for Grunt.js, Yeoman and Node.js. Used by Zurb Foundation, Zurb Ink, H5BP/Effeckt, Less.js / lesscss.org, Topcoat, Web Experience Toolkit, and hundreds of other projects to build sites, themes, components, documentation, blogs and gh-pages.


### HEADS UP! This document is incomplete!

### Also, please do not create issues against the v0.6.0 branch unless you have a pull request or would like to discuss an issue that might lead to you doing a pull request. Thanks!


### [Visit the website →](http://assemble.io)

## v0.6.0 Release notes

For v0.6.0, Assemble was completely re-written from the ground up to be a 100% standalone library. Before we dive into the awesome new features that Assemble is introducing in this version, there are a couple of things you need to know:

**Grunt users**

* Rest assured that you will be able to continue using Assemble as a Grunt plugin. However, **going forward you will need to do `npm install grunt-assemble`** instead.
* If you decide to continue using older (pre-v0.6.0) versions of Assemble you will still need to do `npm install assemble`. Visit [grunt-assemble](https://github.com/assemble/grunt-assemble) for more info.

**Gulp users**

* [gulp-assemble](https://github.com/assemble/gulp-assemble) is finally ready to go!


### Influences

_(WIP!)_

We'd like to say "thanks!" to the great libraries that influenced this version of Assemble! We'd also point out some of the special things these libraries bring to Assemble in v0.6.0.

  - **[Vinyl]** - We all know the [Gulp] team over at [Fractal] does amazing work with streams. We decided to follow their lead and use [vinyl] and [vinyl-fs] in Assemble v0.6.0.
  - **[Gulp]** - We also looted some test fixtures, the CLI, and the new Assemble configuration signature from Gulp itself. Also thanks to @tkellen for his great work on [Liftoff]
  - **[Express]** - Engines, routes, and views, general code style.
  - **[Kerouac]** - Parsers, routes
  - **Assemble** - Last but not least, Assemble itself! At heart, Assemble is still very much Assemble in this version. We've introduced a powerful API, new features, and a dramatically different configuration signature, but _no features from previous versions were harmed during the making of this version_, and the goals and vision of the project remain the same.

New Features

  - **API**
  - **CLI** Assemble uses the same config-style and CLI patterns as gulp. To run Assemble the command line, do `assemble`
  - **Streams** (gulp-style)
  - **Plugins** (gulp-style): Not only does Assemble have support for gulp-style streaming plugins, but any gulp plugin can be used with Assemble.
  - **Parsers** (kerouac-style):
  - **Engines** express-style engine support! Engines support has changed so dramatically in this version that we're considering this a new feature. Assemble v0.6.0 allows any engine from **[Consolidate]** or **[Transformers]** to be registered with `assemble.engine()`, just like [express](http://expressjs.com/4x/api.html#app.engine). To add a custom engine, follow the instructions on the [consolidate](https://github.com/visionmedia/consolidate.js) docs or the [transformers](https://github.com/ForbesLindesay/transformers) docs, depending on the type of engine.
  - **Routes** (express/kerouac-style)
  - **Middleware** (express/kerouac-style)
  - **.assemblerc.yml**

Improved Features

  - **Middleware**
  - **Front matter**: support for [gray-matter] was added.


New `options` settings:

* `layouts`: Define a glob of layouts. Allows more flexibility than `layoutdir`.



## Install
#### Install with [npm](npmjs.org):

```bash
npm i assemble --save-dev
```

## API
### [Assemble](lib/assemble.js#L81)

Create an `assemble` task.

* `context` **{Object}**    

```js
var assemble = require('assemble');

assemble.task('site', function() {
  assemble.src('templates/*.hbs')
    .pipe(assemble.dest('_gh_pages'));
});
```

Optionally initialize a new `Assemble` with the given `context`.

```js
var config = new Assemble({foo: 'bar'});
```

## Authors
 
**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 
 
**Brian Woodward**
 
+ [github/doowb](https://github.com/doowb)
+ [twitter/doowb](http://twitter.com/doowb) 


## License
Copyright (c) 2014 Assemble, contributors.  
Released under the MIT license

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on November 04, 2014._


[gulp]: https://github.com/wearefractal/gulp
[fractal]: https://github.com/wearefractal
[vinyl]: https://github.com/wearefractal/vinyl
[vinyl-fs]: https://github.com/wearefractal/vinyl-fs