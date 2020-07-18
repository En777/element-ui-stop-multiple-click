# vue-stop-multiple-click

[![gzip size](http://img.badgesize.io/https://unpkg.com/vue-stop-multiple-click/vue-prevent-multiple-click.js?compression=gzip&label=gzip%20size&style=flat-square)](https://unpkg.com/vue-stop-multiple-click/vue-prevent-multiple-click.js)
[![downloads](https://img.shields.io/npm/dm/vue-stop-multiple-click.svg?style=flat-square)](https://www.npmtrends.com/vue-stop-multiple-click)
[![MIT License](https://img.shields.io/npm/l/vue-stop-multiple-click.svg?style=flat-square)](https://github.com/fisker/vue-stop-multiple-click/blob/master/license)
[![jsdelivr](https://data.jsdelivr.com/v1/package/npm/vue-stop-multiple-click/badge)](https://www.jsdelivr.com/package/npm/vue-stop-multiple-click)

a simple way prevent button multiple clicks.

一个非常简单的方式，防止按钮重复点击。
使用一个指令，把异步 Promise 函数 ```v-click-async="ajaxPromiseFn"``` 传入，程序会自动防止按钮重复点击（一定要等到异步函数结束，才能再次点击）。

## Usage
```js
const StopMultipleClick = require('vue-stop-multiple-click')

Vue.directive('clickAsync', StopMultipleClick)
```

```html
<button v-click-async="ajaxPromiseFn">a simple way prevent button multiple clicks</button>
```

or use CDN script:
```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.11/dist/vue.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/vue-stop-multiple-click@0/vue-prevent-multiple-click.min.js"></script>

<script>
var StopMultipleClick = window.StopMultipleClick

Vue.directive('clickAsync', StopMultipleClick)
</script>

<button v-click-async="ajaxPromiseFn">button will auto prevent multiple clicks</button>
```