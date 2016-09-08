[![Build Status](https://travis-ci.org/apolakipso/Swiper.svg?branch=master)](https://travis-ci.org/apolakipso/Swiper)
[![devDependency Status](https://david-dm.org/apolakipso/Swiper/dev-status.svg)](https://david-dm.org/apolakipso/Swiper?type=dev)
[![Flattr the original git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=nolimits4web&url=https://github.com/nolimits4web/swiper/&title=Framework7&language=JavaScript&tags=github&category=software)

This Swiper fork
==========

This fork adds a few tweaks to integrate Swiper with Polymer.

## Additional options

The following options have been added to the original [API](http://www.idangero.us/swiper/api/).

### getEventTarget(e): Function

Pass in this custom function to return the correct target element from the given event.
This is used to make Swiper's `findElementInEvent(e)` work with both Shady and Shadow DOM,
effectively resetting Polymer's [event retargeting](https://www.polymer-project.org/1.0/docs/devguide/events#retargeting).

Example:
```
options.getEventTarget = function(e) {
    return Polymer.dom(e).rootTarget;
};
```

### wrapper: Node

Used to pass in a wrapper node directly . The wrapper can be passed in as a simple node 
via parameter `wrapper`, it'll be wrapped with the active DOM library in here.
The fallback is to find it in the container with the specified `wrapperClass`.

### normalizeSlideIndex: Boolean

Enabling the `groupSlides` option prevents selection of single slides, as the click index is normalized to
the first slide of the visible group. Set `normalizeSlideIndex: false` to enable selecting single slides on click.
Defaults to `true`.

*Please note* This is currently only implemented for `loop: false`

Swiper
==========

Swiper - is the free and most modern mobile touch slider with hardware accelerated transitions and amazing native behavior. It is intended to be used in mobile websites, mobile web apps, and mobile native/hybrid apps. Designed mostly for iOS, but also works great on latest Android, Windows Phone 8 and modern Desktop browsers

Swiper is not compatible with all platforms, it is a modern touch slider which is focused only on modern apps/platforms to bring the best experience and simplicity.

# Getting Started
  * [Getting Started Guide](http://www.idangero.us/swiper/get-started/)
  * [API](http://www.idangero.us/swiper/api/)
  * [Demos](http://www.idangero.us/swiper/demos/)
  * [Forum](http://www.idangero.us/swiper/forum/)

# Dist / Build

On production use files (JS and CSS) only from `dist/` folder, there will be the most stable versions, `build/` folder is only for development purpose

### Build

Swiper uses `gulp` to build a development (build) and dist versions.

First you need to have `gulp-cli` which you should install globally.

```
$ npm install --global gulp
```

Then install all dependencies, in repo's root:

```
$ npm install
```

And build development version of Swiper:
```
$ gulp build
```

The result is available in `build/` folder.

### Dist/Release

After you have made build:

```
$ gulp dist
```

Distributable version will available in `dist/` folder.

# Contributing

All changes should be committed to `src/` files. Swiper uses LESS for CSS compliations, and concatenated JS files (look at gulpfile.js for concat files order)

Swiper 2.x.x
==========

If you still using Swiper 2.x.x or you need old browsers support, you may find it in [Swiper2 Branch](https://github.com/nolimits4web/Swiper/tree/Swiper2)
* [Download Latest Swiper 2.7.6](https://github.com/nolimits4web/Swiper/archive/v2.7.6.zip)
* [Source Files](https://github.com/nolimits4web/Swiper/tree/Swiper2/src)
* [API](https://github.com/nolimits4web/Swiper/blob/Swiper2/API.md)
