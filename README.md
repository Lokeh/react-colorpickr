A colorpicker for React
---

[![npm version](http://img.shields.io/npm/v/react-colorpickr.svg)](https://npmjs.org/package/react-colorpickr) [![Circle CI](https://circleci.com/gh/mapbox/react-colorpickr.svg?style=svg&circle-token=7b6e2687ff5804946f2c0ef5a8a93ad92a4c8ff3)](https://circleci.com/gh/mapbox/react-colorpickr)

__[Demo](https://www.mapbox.com/react-colorpickr/example/)__

### Install

    npm install react-colorpickr

You'll also want to include a copy of [react-colorpickr.css](https://github.com/mapbox/react-colorpickr/blob/mb-pages/react-colorpickr.css) in your code.

``` html
<link href='react-colorpickr.css' rel='stylesheet' />
```

### Usage

```js
var React = require('react');
var ColorPicker = require('react-colorpickr');

var App = React.createClass({
  getInitialState: function() {
    return {
      color: 'rgba(56, 130, 184, 1)'
    };
  },

  onChange: function(color) {
    console.log(color);
  },

  render: function() {
    return (
      <div>
        <ColorPicker
          value={this.state.color}
          onChange={this.onChange} />
      </div>
    );
  }
});
```

### Required properties

#### `onChange`

Value should be a function and is called whenever a color is updated from
the colorpicker. Returns a color object.

### Optional properties

#### `value`

Must be a string and a valid `HEX`, `RGB`, or `RGBA` CSS value. If this isn't
provided, a default color is used.

#### `mode`

Defaults to `rgb`. Initializes which color model tab is active.
Possible options: `hsv`, `rgb`.

#### `colorAttribute`

Defaults to `h`. Initializes which color attribute is active.
Possible options: `h`, `s`, `v`, `r`, `g`, `b`.

#### `reset`

If `reset` is provided as a property with a value of `true` a reset button is
added that when pressed, reverts back to the original color when the
colorpicker is initialized on the page. Defaults to `true`.

### Developing

    npm install & npm start & open http://127.0.0.1:3000/example/index.html

Inspired by https://github.com/wangzuo/react-input-color
