*This repository is a mirror of the [component](http://component.io) module [chemzqm/editable](http://github.com/chemzqm/editable). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/chemzqm-editable`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# editable

  Simple and tiny Edit in place for component

  With key bindings, `esc` for cancel `enter` for confirm

  [demo](http://chemzqm.github.io/editable/)

## Installation

  Install with [component(1)](http://component.io):

    $ component install chemzqm/editable

## Usage

``` js
var Editable = require('editable');
var node = document.getElementById('test');
var ed = new Editable(node);
ed.on('change', function(v){
  console.log(v);
})
```
## Events

* `change` emit with the changed value.

* `range error` emit when the value length is not in limited range.

## API

### new Editable(node)

Create Editable instance

### editable#limit(min, max)

`min` number, `max` number of the value length.

### editable#value()

Get current node html.

### editable#reset()

Reset the value to previous, useful for undo no `change` event emitted.

### editable#remove()


Unregist the events

## License

  MIT
