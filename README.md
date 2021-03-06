# [idleTimeout](https://github.com/jackmu95/idle-timeout/)

[![Version](https://badgen.net/npm/v/idle-timeout)](https://www.npmjs.com/package/idle-timeout/)
[![Size](https://badgen.net/badgesize/normal/jackmu95/idle-timeout/master/dist/idle-timeout.min.js)](https://github.com/jackmu95/idle-timeout/blob/master/dist/idle-timeout.min.js)
[![License](https://badgen.net/npm/license/idle-timeout)](https://www.npmjs.com/package/idle-timeout/)

A zero dependency, ~5KB library to make idle state detection in the browser an ease. With it's simple but yet powerful API it features everything you will ever need.

## Installation

### Using npm
```bash
npm install idle-timeout
```

### Using yarn
```bash
yarn add idle-timeout
```

### Using CDN
```html
<script src="https://unpkg.com/idle-timeout/dist/idle-timeout.min.js"></script>
```


## Usage
idleTimeout is totally easy to use. All you basically need to do is:
```javascript
idleTimeout(() => {
  // Do some cool stuff
});
```


## Documentation
The idleTimeout constructor takes two arguments:
  * `callback [Function]` - _The callback function_
  * `options [Object]` - _An **optional** options object_
    * `element [Element]` - _The element to listen for the timeout_
    * `timeout [Number]` - _The idle timeout (in milliseconds)_
    * `loop [Boolean]` - _Wether the timeout should be looped when idle_

```javascript
const instance = idleTimeout(
  () => {
    // Callback
  },
  {
    element: document,
    timeout: 1000 * 60 * 5,
    loop: false
  }
);
```

### Methods
`pause()` - _Pauses the timeout_
```javascript
instance.pause();
```

`resume()` - _Resumes an paused timeout_
```javascript
instance.resume();
```

`reset()` - _Reset the timeout_
```javascript
instance.reset();
```

`destroy()` - _Destroy the instance_
```javascript
instance.destroy();
```

### Getters
`idle [Boolean]` - _Wether the current state is idle_
```javascript
instance.idle; // false
```

### Setters
`timeout = value [Number]` - _Set the timeout (in milliseconds)_
```javascript
instance.timeout = 1000 * 60;
```

`loop = value [Boolean]` - _Set wether the timeout should be looped_
```javascript
instance.loop = true;
```

`idle = value [Boolean]` - _Set the idle state_
```javascript
instance.idle = true;
```


## Browser Support

| Chrome<br><img src="https://cdn.rawgit.com/alrra/browser-logos/master/src/chrome/chrome.svg" width="48" height="48" alt="Chrome"> | Firefox<br><img src="https://cdn.rawgit.com/alrra/browser-logos/master/src/firefox/firefox.svg" width="48" height="48" alt="Firefox"> | Safari<br><img src="https://cdn.rawgit.com/alrra/browser-logos/master/src/safari/safari_128x128.png" width="48" height="48" alt="Safari"> | Opera<br><img src="https://cdn.rawgit.com/alrra/browser-logos/master/src/opera/opera.svg" width="48" height="48" alt="Opera"> | Edge<br><img src="https://cdn.rawgit.com/alrra/browser-logos/master/src/edge/edge.svg" width="48" height="48" alt="Edge"> | IE<br><img src="https://cdn.rawgit.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11.svg" width="48" height="48" alt="IE"> |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Latest 2 | Latest 2 | Latest 2 | Latest 2 | Latest 2 | 11 |


## License
This project is licensed under the terms of the [MIT License](LICENSE).
