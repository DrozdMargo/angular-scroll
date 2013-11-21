angular-scroll
==============

Only dependent on AngularJS (no jQuery). 2.6K minified or 0.6K gzipped.

Example
-------
Check out [the live demo](http://durated.github.io/angular-scroll/) or the [source code](https://github.com/durated/angular-scroll/blob/master/example/index.html).

Install
-------
With bower:

    $ bower install angular-scroll

Or download the [production version](https://raw.github.com/durated/angular-scroll/master/angular-scroll.min.js) or the [development version](https://raw.github.com/durated/angular-scroll/master/angular-scroll.js).

Usage
-----

### Scrolling observer
```js
angular.module('myApp', ['duScroll']).
  controller('myCtrl', function($scope, scrollPosition){
    scrollPosition.observe(function(scrollY) {
      console.log('Scrolled to ', scrollY);
    });
  }
);
```

### Smooth Anchor Scrolling
```html
<a href="#anchor" du-smooth-scroll>Scroll it!</a>
```

### Scrollspy
```html
<a href="#anchor" du-scrollspy>Am i active?</a>
```

### Manual smooth scrollTo
```js
angular.module('myApp', ['duScroll']).
  controller('myCtrl', function(scroller) {
    var x = 0;
    var y = 400;
    var duration = 2000; //milliseconds

    //Scroll to the exact position
    scroller.scrollTo(x, y, duration);

    var chunk = 200;
    //Scroll 200px down from current scroll position
    scroller.scrollDelta(x, chunk, duration);
  }
);
```

Building
--------

    $ grunt
