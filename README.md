# brotli for Laravel Mix

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Latest Version on NPM](https://img.shields.io/npm/v/laravel-mix-brotli.svg?style=flat-square)](https://npmjs.com/package/laravel-mix-brotli)
[![npm](https://img.shields.io/npm/dt/laravel-mix-brotli.svg?style=flat-square)](https://www.npmjs.com/package/laravel-mix-brotli)

A wrapper around brotli-webpack-plugin for Laravel Mix.

```js
let mix = require('laravel-mix');
require('laravel-mix-brotli');

// ...

mix.js('resources/js/app.js', 'public/js')
   .sass('resources/sass/app.scss', 'public/css')
   .brotli();
```

## Installation

Before you get started, make sure you're using `laravel-mix` version 4 or higher.

You can install the package with yarn or npm:

```bash
yarn add laravel-mix-brotli
```

```bash
npm install laravel-mix-brotli
```

Then install the extension by requiring the module in your Mix configuration.

```js
let mix = require('laravel-mix');
require('laravel-mix-brotli');

// ...
```

brotli can then be enabled by calling `.brotli()` in your Mix chain.

```js
mix.js('resources/js/app.js', 'public/js')
   .sass('resources/sass/app.scss', 'public/css')
   .brotli();
```

Custom options can be passed when calling brotli if necessary.

```js
mix.js('resources/js/app.js', 'public/js')
   .sass('resources/sass/app.scss', 'public/css')
   .brotli({
                    enabled: mix.inProduction(),
           			asset: '[path].br[query]',
           			test: /\.(js|css|html|svg)$/,
           			threshold: 10240,
           			minRatio: 0.8
           		});
```

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
