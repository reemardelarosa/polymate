<h1 align="center">
  Polymate - Lottie Animation View for Polymer 2
</h1>
<p align="center">
  <a href="https://github.com/AfterWebX/polymate/issues"><img src="https://camo.githubusercontent.com/0ace69e0fdebdcfc2721242595e876ecb96de266/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6973737565732f4166746572576562582f706f6c796d6174652e737667" alt="GitHub issues" data-canonical-src="https://img.shields.io/github/issues/AfterWebX/polymate.svg" style="max-width:100%;"></a>
<a href="https://github.com/AfterWebX/polymate/stargazers"><img src="https://camo.githubusercontent.com/072e91a4db3a6570604993401009b06a80f95c98/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f4166746572576562582f706f6c796d6174652e737667" alt="GitHub stars" data-canonical-src="https://img.shields.io/github/stars/AfterWebX/polymate.svg" style="max-width:100%;"></a>
<a href="https://raw.githubusercontent.com/AfterWebX/polymate/master/LICENSE" rel="nofollow"><img src="https://camo.githubusercontent.com/890acbdcb87868b382af9a4b1fac507b9659d9bf/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6c6963656e73652d4d49542d626c75652e737667" alt="GitHub license" data-canonical-src="https://img.shields.io/badge/license-MIT-blue.svg" style="max-width:100%;"></a>
</p>

<h2 align="center">
  wrapper of <a href="https://github.com/airbnb/lottie-web">lottie-web</a>
</h2>
<p align="center">
  Lottie is a mobile library for Web,  and iOS that parses <a href="http://www.adobe.com/products/aftereffects.html">Adobe After Effects</a> animations exported as json with <a href="https://github.com/airbnb/lottie-web">Bodymovin</a> and renders them natively on mobile!
</p>
<p align="center">
  For the first time, designers can create <b>and ship</b> beautiful animations without an engineer painstakingly recreating it by hand. They say a picture is worth 1,000 words so here are 13,000:
</p>

<p align="center" class="rich-diff-level-zero">
  <img src="/gifs/polymate-preview5.gif" alt="Example2">
  <img src="/gifs/polymate-preview0.gif" alt="Example1">
  <img src="/gifs/polymate-preview1.gif" alt="Example3">
  <img src="/gifs/polymate-preview4.gif" alt="Example4">
</p>

## Why Lottie?


#### Flexible After Effects features
We currently support solids, shape layers, masks, alpha mattes, trim paths, and dash patterns. And we’ll be adding new features on a regular basis.

#### Manipulate your animation any way you like
You can go forward, backward, and most importantly you can program your animation to respond to any interaction.

#### Small file sizes
Bundle vector animations within your app without having to worry about multiple dimensions or large file sizes. Alternatively, you can decouple animation files from your app’s code entirely by loading them from a JSON API.

Download lottie files › [lottiefiles.com](https://www.lottiefiles.com/)

## View documentation, FAQ, help, examples, and more at [airbnb.io/lottie](http://airbnb.io/lottie/)

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
1. Import the polymate view component
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
