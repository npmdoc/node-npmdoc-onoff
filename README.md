# api documentation for  [onoff (v1.1.2)](https://github.com/fivdi/onoff#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-onoff.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-onoff) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-onoff.svg)](https://travis-ci.org/npmdoc/node-npmdoc-onoff)
#### GPIO access and interrupt detection with Node.js

[![NPM](https://nodei.co/npm/onoff.png?downloads=true)](https://www.npmjs.com/package/onoff)

[![apidoc](https://npmdoc.github.io/node-npmdoc-onoff/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-onoff_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-onoff/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-onoff/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-onoff/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "fivdi"
    },
    "bugs": {
        "url": "https://github.com/fivdi/onoff/issues"
    },
    "dependencies": {
        "epoll": "~0.1.21"
    },
    "description": "GPIO access and interrupt detection with Node.js",
    "devDependencies": {},
    "directories": {
        "example": "examples",
        "test": "test"
    },
    "dist": {
        "shasum": "dcd39d3fd559db2d0df5bcd54d8cc9df1d7747a2",
        "tarball": "https://registry.npmjs.org/onoff/-/onoff-1.1.2.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "5fd2bb6911ed5a293c3f8ec550b1f7be3e88a65c",
    "homepage": "https://github.com/fivdi/onoff#readme",
    "keywords": [
        "gpio",
        "embedded",
        "interrupt",
        "beaglebone",
        "bbb",
        "bb",
        "raspberry",
        "raspi",
        "rpi",
        "pi",
        "linux"
    ],
    "license": "MIT",
    "main": "onoff.js",
    "maintainers": [
        {
            "name": "fivdi",
            "email": "fivdiweb@gmail.com"
        }
    ],
    "name": "onoff",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/fivdi/onoff.git"
    },
    "scripts": {
        "test": "echo \"Tests can only be run manually from the command line. They access hardware GPIOs.\" && exit 1"
    },
    "version": "1.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module onoff](#apidoc.module.onoff)
1.  [function <span class="apidocSignatureSpan">onoff.</span>Gpio (gpio, direction, edge, options)](#apidoc.element.onoff.Gpio)
1.  object <span class="apidocSignatureSpan">onoff.</span>Gpio.prototype
1.  string <span class="apidocSignatureSpan">onoff.</span>version

#### [module onoff.Gpio](#apidoc.module.onoff.Gpio)
1.  [function <span class="apidocSignatureSpan">onoff.</span>Gpio (gpio, direction, edge, options)](#apidoc.element.onoff.Gpio.Gpio)

#### [module onoff.Gpio.prototype](#apidoc.module.onoff.Gpio.prototype)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>activeLow ()](#apidoc.element.onoff.Gpio.prototype.activeLow)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>direction ()](#apidoc.element.onoff.Gpio.prototype.direction)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>edge ()](#apidoc.element.onoff.Gpio.prototype.edge)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>options ()](#apidoc.element.onoff.Gpio.prototype.options)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>read (callback)](#apidoc.element.onoff.Gpio.prototype.read)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>readSync ()](#apidoc.element.onoff.Gpio.prototype.readSync)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>setActiveLow (invert)](#apidoc.element.onoff.Gpio.prototype.setActiveLow)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>setDirection (direction)](#apidoc.element.onoff.Gpio.prototype.setDirection)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>setEdge (edge)](#apidoc.element.onoff.Gpio.prototype.setEdge)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>unexport ()](#apidoc.element.onoff.Gpio.prototype.unexport)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>unwatch (callback)](#apidoc.element.onoff.Gpio.prototype.unwatch)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>unwatchAll ()](#apidoc.element.onoff.Gpio.prototype.unwatchAll)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>watch (callback)](#apidoc.element.onoff.Gpio.prototype.watch)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>write (value, callback)](#apidoc.element.onoff.Gpio.prototype.write)
1.  [function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>writeSync (value)](#apidoc.element.onoff.Gpio.prototype.writeSync)



# <a name="apidoc.module.onoff"></a>[module onoff](#apidoc.module.onoff)

#### <a name="apidoc.element.onoff.Gpio"></a>[function <span class="apidocSignatureSpan">onoff.</span>Gpio (gpio, direction, edge, options)](#apidoc.element.onoff.Gpio)
- description and source-code
```javascript
function Gpio(gpio, direction, edge, options) {
  var valuePath,
    directionSet = false,
    tries = 0;

  if (!(this instanceof Gpio)) {
    return new Gpio(gpio, direction, edge, options);
  }

  if (typeof edge === 'object' && !options) {
    options = edge;
    edge = undefined;
  }

  options = options || {};

  this.gpio = gpio;
  this.gpioPath = GPIO_ROOT_PATH + 'gpio' + this.gpio + '/';
  this.opts = {};
  this.opts.debounceTimeout = options.debounceTimeout || 0;
  this.readBuffer = new Buffer(16);
  this.listeners = [];

  valuePath = this.gpioPath + 'value';

  if (!fs.existsSync(this.gpioPath)) {
    // The pin hasn't been exported yet so export it.
    fs.writeFileSync(GPIO_ROOT_PATH + 'export', this.gpio);

    // A hack to avoid the issue described here:
    // https://github.com/raspberrypi/linux/issues/553
    // I don't like this solution, but it enables compatibility with older
    // versions of onoff, i.e., the Gpio constructor was and still is
    // synchronous.
    directionSet = false;
    while (!directionSet) {
      try {
        tries += 1;
        fs.writeFileSync(this.gpioPath + 'direction', direction);
        directionSet = true;
      } catch (e) {
        if (tries === 10000) {
          throw e;
        }
      }
    }

    if (edge) {
      fs.writeFileSync(this.gpioPath + 'edge', edge);
    }

    if (!!options.activeLow) {
      fs.writeFileSync(this.gpioPath + 'active_low', ONE);
    }
  } else {
    // The pin has already been exported, perhaps by onoff itself, perhaps
    // by quick2wire gpio-admin on the Pi, perhaps by the WiringPi gpio
    // utility on the Pi, or perhaps by something else. In any case, an
    // attempt is made to set the direction and edge to the requested
    // values here. If quick2wire gpio-admin was used for the export, the
    // user should have access to both direction and edge files. This is
    // important as gpio-admin sets niether direction nor edge. If the
    // WiringPi gpio utility was used, the user should have access to edge
    // file, but not the direction file. This is also ok as the WiringPi
    // gpio utility can set both direction and edge. If there are any
    // errors while attempting to perform the modifications, just keep on
    // truckin'.
    try {
      fs.writeFileSync(this.gpioPath + 'direction', direction);
    } catch (ignore) {
    }
    try {
      if (edge) {
        fs.writeFileSync(this.gpioPath + 'edge', edge);
      }
      try {
        fs.writeFileSync(this.gpioPath + 'active_low',
          !!options.activeLow ? ONE : ZERO
        );
      } catch (ignore) {
      }
    } catch (ignore) {
    }
  }

  this.valueFd = fs.openSync(valuePath, 'r+'); // Cache fd for performance.

  // Read current value before polling to prevent unauthentic interrupts.
  this.readSync();

  this.poller = new Epoll(pollerEventHandler.bind(this));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.onoff.Gpio"></a>[module onoff.Gpio](#apidoc.module.onoff.Gpio)

#### <a name="apidoc.element.onoff.Gpio.Gpio"></a>[function <span class="apidocSignatureSpan">onoff.</span>Gpio (gpio, direction, edge, options)](#apidoc.element.onoff.Gpio.Gpio)
- description and source-code
```javascript
function Gpio(gpio, direction, edge, options) {
  var valuePath,
    directionSet = false,
    tries = 0;

  if (!(this instanceof Gpio)) {
    return new Gpio(gpio, direction, edge, options);
  }

  if (typeof edge === 'object' && !options) {
    options = edge;
    edge = undefined;
  }

  options = options || {};

  this.gpio = gpio;
  this.gpioPath = GPIO_ROOT_PATH + 'gpio' + this.gpio + '/';
  this.opts = {};
  this.opts.debounceTimeout = options.debounceTimeout || 0;
  this.readBuffer = new Buffer(16);
  this.listeners = [];

  valuePath = this.gpioPath + 'value';

  if (!fs.existsSync(this.gpioPath)) {
    // The pin hasn't been exported yet so export it.
    fs.writeFileSync(GPIO_ROOT_PATH + 'export', this.gpio);

    // A hack to avoid the issue described here:
    // https://github.com/raspberrypi/linux/issues/553
    // I don't like this solution, but it enables compatibility with older
    // versions of onoff, i.e., the Gpio constructor was and still is
    // synchronous.
    directionSet = false;
    while (!directionSet) {
      try {
        tries += 1;
        fs.writeFileSync(this.gpioPath + 'direction', direction);
        directionSet = true;
      } catch (e) {
        if (tries === 10000) {
          throw e;
        }
      }
    }

    if (edge) {
      fs.writeFileSync(this.gpioPath + 'edge', edge);
    }

    if (!!options.activeLow) {
      fs.writeFileSync(this.gpioPath + 'active_low', ONE);
    }
  } else {
    // The pin has already been exported, perhaps by onoff itself, perhaps
    // by quick2wire gpio-admin on the Pi, perhaps by the WiringPi gpio
    // utility on the Pi, or perhaps by something else. In any case, an
    // attempt is made to set the direction and edge to the requested
    // values here. If quick2wire gpio-admin was used for the export, the
    // user should have access to both direction and edge files. This is
    // important as gpio-admin sets niether direction nor edge. If the
    // WiringPi gpio utility was used, the user should have access to edge
    // file, but not the direction file. This is also ok as the WiringPi
    // gpio utility can set both direction and edge. If there are any
    // errors while attempting to perform the modifications, just keep on
    // truckin'.
    try {
      fs.writeFileSync(this.gpioPath + 'direction', direction);
    } catch (ignore) {
    }
    try {
      if (edge) {
        fs.writeFileSync(this.gpioPath + 'edge', edge);
      }
      try {
        fs.writeFileSync(this.gpioPath + 'active_low',
          !!options.activeLow ? ONE : ZERO
        );
      } catch (ignore) {
      }
    } catch (ignore) {
    }
  }

  this.valueFd = fs.openSync(valuePath, 'r+'); // Cache fd for performance.

  // Read current value before polling to prevent unauthentic interrupts.
  this.readSync();

  this.poller = new Epoll(pollerEventHandler.bind(this));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.onoff.Gpio.prototype"></a>[module onoff.Gpio.prototype](#apidoc.module.onoff.Gpio.prototype)

#### <a name="apidoc.element.onoff.Gpio.prototype.activeLow"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>activeLow ()](#apidoc.element.onoff.Gpio.prototype.activeLow)
- description and source-code
```javascript
activeLow = function () {
  return fs.readFileSync(
    this.gpioPath + 'active_low')[0] === ONE[0] ? true : false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.onoff.Gpio.prototype.direction"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>direction ()](#apidoc.element.onoff.Gpio.prototype.direction)
- description and source-code
```javascript
direction = function () {
  return fs.readFileSync(this.gpioPath + 'direction').toString().trim();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.onoff.Gpio.prototype.edge"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>edge ()](#apidoc.element.onoff.Gpio.prototype.edge)
- description and source-code
```javascript
edge = function () {
  return fs.readFileSync(this.gpioPath + 'edge').toString().trim();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.onoff.Gpio.prototype.options"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>options ()](#apidoc.element.onoff.Gpio.prototype.options)
- description and source-code
```javascript
options = function () {
  return this.opts;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.onoff.Gpio.prototype.read"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>read (callback)](#apidoc.element.onoff.Gpio.prototype.read)
- description and source-code
```javascript
read = function (callback) {
  fs.read(this.valueFd, this.readBuffer, 0, 1, 0, function (err, bytes, buf) {
    if (typeof callback === 'function') {
      if (err) {
        return callback(err);
      }

      callback(null, buf[0] === ONE[0] ? 1 : 0);
    }
  });
}
```
- example usage
```shell
...
// Toggle the state of the LED on GPIO #14 every 200ms 'count' times.
// Here asynchronous methods are used. Synchronous methods are also available.
(function blink(count) {
  if (count <= 0) {
return led.unexport();
  }

  led.read(function (err, value) { // Asynchronous read.
if (err) {
  throw err;
}

led.write(value ^ 1, function (err) { // Asynchronous write.
  if (err) {
    throw err;
...
```

#### <a name="apidoc.element.onoff.Gpio.prototype.readSync"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>readSync ()](#apidoc.element.onoff.Gpio.prototype.readSync)
- description and source-code
```javascript
readSync = function () {
  fs.readSync(this.valueFd, this.readBuffer, 0, 1, 0);
  return this.readBuffer[0] === ONE[0] ? 1 : 0;
}
```
- example usage
```shell
...
var Gpio = require('onoff').Gpio, // Constructor function for Gpio objects.
led = new Gpio(14, 'out'),      // Export GPIO #14 as an output.
iv;

// Toggle the state of the LED on GPIO #14 every 200ms.
// Here synchronous methods are used. Asynchronous methods are also available.
iv = setInterval(function () {
led.writeSync(led.readSync() ^ 1); // 1 = on, 0 = off :)
}, 200);

// Stop blinking the LED and turn it off after 5 seconds.
setTimeout(function () {
clearInterval(iv); // Stop blinking
led.writeSync(0);  // Turn LED off.
led.unexport();    // Unexport GPIO and free resources
...
```

#### <a name="apidoc.element.onoff.Gpio.prototype.setActiveLow"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>setActiveLow (invert)](#apidoc.element.onoff.Gpio.prototype.setActiveLow)
- description and source-code
```javascript
setActiveLow = function (invert) {
  fs.writeFileSync(this.gpioPath + 'active_low', !!invert ? ONE : ZERO);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.onoff.Gpio.prototype.setDirection"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>setDirection (direction)](#apidoc.element.onoff.Gpio.prototype.setDirection)
- description and source-code
```javascript
setDirection = function (direction) {
  fs.writeFileSync(this.gpioPath + 'direction', direction);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.onoff.Gpio.prototype.setEdge"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>setEdge (edge)](#apidoc.element.onoff.Gpio.prototype.setEdge)
- description and source-code
```javascript
setEdge = function (edge) {
  fs.writeFileSync(this.gpioPath + 'edge', edge);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.onoff.Gpio.prototype.unexport"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>unexport ()](#apidoc.element.onoff.Gpio.prototype.unexport)
- description and source-code
```javascript
unexport = function () {
  this.unwatchAll();
  fs.closeSync(this.valueFd);
  try {
    fs.writeFileSync(GPIO_ROOT_PATH + 'unexport', this.gpio);
  } catch (ignore) {
    // Flow of control always arrives here when cape_universal is enabled on
    // the bbb.
  }
}
```
- example usage
```shell
...
    throw err;
  }

  led.writeSync(value);
});

process.on('SIGINT', function () {
  led.unexport();
  button.unexport();
});
'''

## How does it work?

Internally onoff uses sysfs files located at /sys/class/gpio to access GPIOs
...
```

#### <a name="apidoc.element.onoff.Gpio.prototype.unwatch"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>unwatch (callback)](#apidoc.element.onoff.Gpio.prototype.unwatch)
- description and source-code
```javascript
unwatch = function (callback) {
  if (this.listeners.length > 0) {
    if (typeof callback !== 'function') {
      this.listeners = [];
    } else {
      this.listeners = this.listeners.filter(function (listener) {
        return callback !== listener;
      });
    }

    if (this.listeners.length === 0) {
      this.poller.remove(this.valueFd);
    }
  }
}
```
- example usage
```shell
...
 }
};

/**
* Remove all watchers for the GPIO.
*/
Gpio.prototype.unwatchAll = function () {
 this.unwatch();
};

/**
* Get GPIO direction.
*
* Returns - string // 'in', or 'out'
*/
...
```

#### <a name="apidoc.element.onoff.Gpio.prototype.unwatchAll"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>unwatchAll ()](#apidoc.element.onoff.Gpio.prototype.unwatchAll)
- description and source-code
```javascript
unwatchAll = function () {
  this.unwatch();
}
```
- example usage
```shell
...
};

/**
 * Reverse the effect of exporting the GPIO to userspace. The Gpio object
 * should not be used after calling this method.
 */
Gpio.prototype.unexport = function () {
this.unwatchAll();
fs.closeSync(this.valueFd);
try {
  fs.writeFileSync(GPIO_ROOT_PATH + 'unexport', this.gpio);
} catch (ignore) {
  // Flow of control always arrives here when cape_universal is enabled on
  // the bbb.
}
...
```

#### <a name="apidoc.element.onoff.Gpio.prototype.watch"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>watch (callback)](#apidoc.element.onoff.Gpio.prototype.watch)
- description and source-code
```javascript
watch = function (callback) {
  var events;

  this.listeners.push(callback);

  if (this.listeners.length === 1) {
    events = Epoll.EPOLLPRI;
    if (this.opts.debounceTimeout > 0) {
      events |= Epoll.EPOLLONESHOT;
    }
    this.poller.add(this.valueFd, events);
  }
}
```
- example usage
```shell
...
should turn off. This can be achieved with the following code:

'''js
var Gpio = require('onoff').Gpio,
  led = new Gpio(14, 'out'),
  button = new Gpio(4, 'in', 'both');

button.watch(function(err, value) {
  led.writeSync(value);
});
'''

Here two Gpio objects are being created. One called led for the LED on GPIO #14
which is an output, and one called button for the momentary push button on
GPIO #4 which is an input. In addition to specifying that the button is an
...
```

#### <a name="apidoc.element.onoff.Gpio.prototype.write"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>write (value, callback)](#apidoc.element.onoff.Gpio.prototype.write)
- description and source-code
```javascript
write = function (value, callback) {
  var writeBuffer = value === 1 ? ONE : ZERO;
  fs.write(this.valueFd, writeBuffer, 0, writeBuffer.length, 0, callback);
}
```
- example usage
```shell
...
}

led.read(function (err, value) { // Asynchronous read.
  if (err) {
    throw err;
  }

  led.write(value ^ 1, function (err) { // Asynchronous write.
    if (err) {
      throw err;
    }
  });
});

setTimeout(function () {
...
```

#### <a name="apidoc.element.onoff.Gpio.prototype.writeSync"></a>[function <span class="apidocSignatureSpan">onoff.Gpio.prototype.</span>writeSync (value)](#apidoc.element.onoff.Gpio.prototype.writeSync)
- description and source-code
```javascript
writeSync = function (value) {
  var writeBuffer = value === 1 ? ONE : ZERO;
  fs.writeSync(this.valueFd, writeBuffer, 0, writeBuffer.length, 0);
}
```
- example usage
```shell
...

'''js
var Gpio = require('onoff').Gpio,
  led = new Gpio(14, 'out'),
  button = new Gpio(4, 'in', 'both');

button.watch(function(err, value) {
  led.writeSync(value);
});
'''

Here two Gpio objects are being created. One called led for the LED on GPIO #14
which is an output, and one called button for the momentary push button on
GPIO #4 which is an input. In addition to specifying that the button is an
input, the constructors optional third argument is used to specify that 'both'
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
