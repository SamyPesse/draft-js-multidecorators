# draftjs-multidecorator

[![Build Status](https://travis-ci.org/SamyPesse/draftjs-multidecorator.png?branch=master)](https://travis-ci.org/SamyPesse/draftjs-multidecorator)
[![NPM version](https://badge.fury.io/js/draftjs-multidecorator.svg)](http://badge.fury.io/js/draftjs-multidecorator)


> Combine multiple Draft's decorators into one.

### Installation

```
$ npm install draftjs-multidecorator
```

### Usage

```js
var Draft = require('draft-js');
var MultiDecorator = require('draftjs-multidecorator');

var decorator = new MultiDecorator([
    new SomeCustomDecorator(),

    // This decorator will have more priority:
    new Draft.CompositeDecorator([ ... ])
]);

var editorState = Draft.EditorState.createEmpty(decorator)
```