# Lottie View for Polymer
[![GitHub issues](https://img.shields.io/github/issues/AfterWebX/polymate.svg)](https://github.com/AfterWebX/polymate/issues)
[![GitHub stars](https://img.shields.io/github/stars/AfterWebX/polymate.svg)](https://github.com/AfterWebX/polymate/stargazers)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/AfterWebX/polymate/master/LICENSE)

## Wrapper of lottie-web

[bodymovin](https://github.com/bodymovin/bodymovin) is [Adobe After Effects](http://www.adobe.com/products/aftereffects.html) plugin for exporting animations as JSON, also it provide bodymovin.js for vender them as svg/canvas/html.

## Why Lottie?

#### Flexible After Effects features
We currently support solids, shape layers, masks, alpha mattes, trim paths, and dash patterns. And we’ll be adding new features on a regular basis.

#### Manipulate your animation any way you like
You can go forward, backward, and most importantly you can program your animation to respond to any interaction.

#### Small file sizes
Bundle vector animations within your app without having to worry about multiple dimensions or large file sizes. Alternatively, you can decouple animation files from your app’s code entirely by loading them from a JSON API.

[Learn more](http://airbnb.design/introducing-lottie/) › http://airbnb.design/lottie/

Looking for lottie files › https://www.lottiefiles.com/

## Installation

Install through npm:
```js
npm install --save polymate
```

Install through bower:
```js
bower install --save polymate
```

## Usage
1. import the polymate view component
```html
<link rel="import" href="../polymate/polymate-view.html">
```
2. Initialize <polymate-view>
> Download animation json from [LottieFiles.com](https://www.lottiefiles.com/) or use some json from [demo](https://github.com/AfterWebX/polymate/tree/master/demo) folder

- Using path, autoplay and loop
```html
<polymate-view id="loader" path="data.json" autoplay loop></polymate-view>
```
- Using options object
```html
<polymate-view id="polymateElement"></polymate-view>

<script>
    class PolymateElement extends Polymer.Element {
      static get is() { return 'polymate-element'; }

      ready() {
        super.ready();

        this.$.polymateElement.options = {
          path: 'data.json',
          loop: true,
          autoplay: true
        };
      }
    }
  
  window.customElements.define(PolymateElement.is, PolymateElement);
</script>
```

## Configuration

You can pass a configuration object through `options` property:
* animationData: an Object with the exported animation data.
* path: the relative path to the animation object. (animationData and path are mutually exclusive)
* loop: true / false / number
* autoplay: true / false it will start playing as soon as it is ready
* renderer: 'svg' / 'canvas' / 'html' to set the renderer

More information on [Bodymoving Documentation](https://github.com/bodymovin/bodymovin)

## Related Projects

* [Bodymovin](https://github.com/bodymovin/bodymovin) ng-lottie is a wrapper of bodymovin
* [Ionic Lottie](https://github.com/yannbf/ionic-lottie) Thanks for @yannbf demonstrating ng-lottie on ionic3
* [React Lottie](https://github.com/chenqingspring/react-lottie) react implementation
* [Vue Lottie](https://github.com/chenqingspring/vue-lottie) vue implementation
* [React Native Lottie](https://github.com/airbnb/lottie-react-native) react native implementation by airbnb
* [IOS Lottie](https://github.com/airbnb/lottie-ios) ios implementation by airbnb
* [Android Lottie](https://github.com/airbnb/lottie-android) android implementation by airbnb

## Contribution

Appreciate your contributions and suggestions.

## License

MIT
