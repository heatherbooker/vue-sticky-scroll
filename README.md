# vue-sticky-scroll
#### update: this directive is for vue 1.x. a vue 2.0 compatible version is available by theomessin [here](https://github.com/theomessin/vue-chat-scroll).  
## a vue.js directive that keeps an element scrolled to the bottom


vue-sticky-scroll keeps an eye on your element and whenever content is added inside of it, it scrolls down so that the viewer can remain focused on the newest content!  


### install  

NPM:  
note: vue-sticky-scroll requires vue 1.x; check your version by running `npm list vue`; a 2.0 compatible version is available [here](https://github.com/theomessin/vue-chat-scroll)  
```bash
npm i --save vue-sticky-scroll
```
Require it in your vue.js component file:

```javascript
// ES5
var stickyScroll = require('vue-sticky-scroll');
// ES6
import 'vue-sticky-scroll';
```

### usage instructions  

Add `v-sticky-scroll` as an attribute on the element you wish to always scroll to the bottom of:

```html
<div class='i-wish-this-would-scroll' v-sticky-scroll></div>
```

### options: animate

the scrolling will jump to the bottom by default.   
if you prefer a smooth scroll, add:
- argument 'animate'
- optional: expression <numOfMilliseconds> (default is 300)

```html
<div class='i-wish-this-would-scroll' v-sticky-scroll:animate></div>

<div class='i-wish-this-would-scroll' v-sticky-scroll:animate=500></div>
```


### how it works

vue-sticky-scroll uses a wonderful, highly underrated browser feature: [mutation observers](https://developer.mozilla.org/en/docs/Web/API/MutationObserver). By creating a `new MutationObserver` and telling it which events to `.observe()`, you can do wonderful things!  
This method is much simpler than some implementations of sticky scrolling that use requestAnimationFrame.

### license

WTFPL
