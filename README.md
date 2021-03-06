# image-diff-view
Compares images, inspired by Github's [image diff view modes](https://github.com/blog/817-behold-image-view-modes).

Inspered by https://github.com/cezary/react-image-diff also ([Demo](http://cezary.github.io/react-image-diff/)).

![Gif image diff view swipe demo](https://github.com/cezary/react-image-diff/raw/master/public/img/demo-swipe.gif)
![Gif image diff view fade demo](https://github.com/cezary/react-image-diff/raw/master/public/img/demo-fade.gif)

## Modes
* `difference` (classic diff)
* `fade` (onion skin)
* `swipe`

## Usage
Controls are not delivery out of the box.
You are free to implement your unique diff controls.

`npm install image-diff-view`

Checkout [example](https://github.com/a-x-/image-diff-view/blob/master/example/index.html) and [demo](https://github.com/a-x-/a-x-.github.io/blob/master/image-diff-view/index.html).

```js
import ImageDiff from 'image-diff-view';

var beforeUrl = 'http://cezary.github.io/react-image-diff/public/img/spot-the-difference-a.jpg',
    afterUrl = 'http://cezary.github.io/react-image-diff/public/img/spot-the-difference-b.jpg';

var imageDiff = new ImageDiff(document.getElementById('image-diff'), beforeUrl, afterUrl, 'swipe');
imageDiff.swipe(0.5);
imageDiff.update(beforeUrl, afterUrl, 'fade');
imageDiff.fade(0.8);
imageDiff.tune(0.4); // abstract tune method rather than fade/swipe()
```
```html
<div class='image-diff' id='image-diff'>
  <div class='image-diff__inner'>
    <div class='image-diff__before'><img/></div>
    <div class='image-diff__wrapper'><div class='image-diff__after'><img/></div></div>
  </div>
</div>
```

## Dependencies
No dependencies required

## Our users
* Yandex
