# karma-coffee-preprocessor

> Preprocessor to compile CoffeeScript on the fly.

## Installation

**This plugin ships with Karma by default, so you don't need to install it, it should just work ;-)**

The easiest way is to keep `karma-coffee-preprocessor` as a devDependency in your `package.json`.
```json
{
  "devDependencies": {
    "karma": "~0.9",
    "karma-coffee-preprocessor": "~0.0.1"
  }
}
```

You can simple do it by:
```bash
npm install karma-coffee-preprocessor --save-dev
```

## Configuration
Following code shows the default configuration...
```js
// karma.conf.js
module.exports = function(config) {
  config.set({
    preprocessors: {
      '**/*.coffee': ['coffee']
    },
    
    coffeePreprocessor: {
      // options passed to the coffee compiler
      options: {
        bare: true
      },
      // transforming the filenames
      transformPath: function(path) {
        return path.replace(/\.js$/, '.coffee');
      }
    }
  });
};
```

----

For more information on Karma see the [homepage].


[homepage]: http://karma-runner.github.com
