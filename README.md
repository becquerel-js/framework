@becquerel/framework
====================
[![npm Version][NPM VERSION BADGE]][NPM PAGE]
[![Node.js][NODE VERSION BADGE]][NODE PAGE]
[![GitHub License][LICENSE BADGE]][LICENSE PAGE]
[![Build Status][BUILD BADGE]][BUILD PAGE]

Yet another web framework experiment.

Install
-------
```sh
$ npm install --save @becquerel/framework  # Or alternately: `yarn add @becquerel/framework`
```

Usage
-----
```js
const Bq = require('@becquerel/framework');
const app = new Bq();

app.route('/', {
    get: (request, response) => {
        response.json = {hello: 'world'};
    }
});

app.route('/hello', {
    get: (request, response) => {
        response.html = '<p>...world</p>';
    }
});

app.run();
```

Environment Variables
---------------------
### `BQ_RUN_DEFAULT_PORT` (default: `8080`)
The port that the app will bind to if `settings.port` is not passed to `#run()`.

### `BQ_RUN_DISPLAY_MSG` (default: `true`)
If `true` the app will display the `Now listening at <${uri}>.` message upon launch.

License
-------
The MIT License (Expat). See the [license file](LICENSE) for details.

[BUILD BADGE]: https://img.shields.io/travis/becquerel-js/framework.svg?style=flat-square
[BUILD PAGE]: https://travis-ci.org/becquerel-js/framework
[LICENSE BADGE]: https://img.shields.io/badge/license-MIT%20License-blue.svg?style=flat-square
[LICENSE PAGE]: https://github.com/becquerel-js/framework/blob/master/LICENSE
[NODE PAGE]: https://nodejs.org/
[NODE VERSION BADGE]: https://img.shields.io/badge/node-%3E%3D7.10-%23010101.svg?style=flat-square
[NPM PAGE]: https://www.npmjs.com/package/@becquerel/framework
[NPM VERSION BADGE]: https://img.shields.io/npm/v/@becquerel/framework.svg?style=flat-square