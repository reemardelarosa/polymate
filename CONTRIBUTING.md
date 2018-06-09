# Contributing to Polymate

We welcome your help to make this component better. This document will help to streamline the contributing process and save everyone's precious time.

# Development Setup

This component has been setup with [polymer-cli](https://github.com/Polymer/tools/tree/master/packages/cli).
Refer to [Polymer Project Docs](https://www.polymer-project.org/2.0/docs/tools/polymer-cli) to get started with the development.


## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) and all pre-requisites installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application
```
$ bower install
```

```
$ polymer serve
```

## Building Your Application

```
$ polymer build
```

This will create builds of your application in the `build/` directory, optimized to be served in production. You can then serve the built versions by giving `polymer serve` a folder to serve from:

```
$ polymer serve build/default
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.