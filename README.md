# humble-localstorage

> wraps localStorage and adds .getObject, .setObject, .isPersistent methods

`localStorage` is a simple key/value store API for browsers, perfectly
suited to store little amount of data like configurations.

`humbleLocalStorage` provides additional APIs to store / retrieve
JSON objects, and also handles several circumstances in which Browsers
do not support or persist localStorage (e.g. private modes,
Cookies disabled, etc).

In case data cannot be persisted in localStorage,  `humbleLocalStorage`
falls back to in-memory storage. To determine if data is being persisted,
use `humbleLocalStorage.isPersistent()` method.


## Installation

Download [humble-localstorage.js](#)
or [humble-localstorage.min.js](#).

Install via Bower

```
bower install -S humble-localstorage
```

Install via npm

```
npm install -S humble-localstorage
```


## Usage

```js
humbleLocalStorage.getItem('mykey') // string value or null
humbleLocalStorage.setItem('mykey', 123) // stored as '123'
humbleLocalStorage.removeItem('mykey')
humbleLocalStorage.clear() // removes all data
humbleLocalStorage.key(0) // name of key by numeric index, or null
humbleLocalStorage.length // number of stored keys

humbleLocalStorage.getObject('mykey') // JSON value or null
humbleLocalStorage.setObject('mykey', {foo: 'bar'}) // stored as '{"foo": "bar"}'
humbleLocalStorage.toJSON() // JSON object of all keys & values
humbleLocalStorage.isPersistent() // true if data persists page reload, false if not
```


## License

MIT
