# element-up-theme

[![Build Status](https://travis-ci.org/ElementUI/element-theme.svg?branch=master)](https://travis-ci.org/ElementUI/element-theme)
[![npm](https://img.shields.io/npm/v/element-theme.svg)](https://www.npmjs.com/package/element-theme)

> Theme generator cli tool for Element and ElementUp.

![](./media/element.gif)

> The current version is compatible with element-ui@2.x and element-up@0.x. For element-ui@1.x, please check out the legacy branch.

## Installation

install local or global

```shell
npm i element-up-theme -D
```

install `up-theme-chalk`

```shell
npm i element-up-theme-chalk -D
# or from github
npm i https://github.com/savoygu/up-theme-chalk -D
```

## CLI

```shell
# init variables file
eut --init [file path]

# watch then build
eut --watch [--config variable file path] [--out theme path]

# build
eut [--config variable file path] [--out theme path] [--minimize]
```

## Node API

```javascript
var eut = require('element-up-theme')

// watch mode
eut.watch({
  config: 'variables/path',
  out: 'output/path'
})

// build
eut.run({
  config: 'variables/path',
  out: 'output/path',
  minimize: true
})
```

## Options

### config

Variable file path, default `./element-up-variables.css`.

### out

Theme output path, default `./up-theme`.

### minimize

Compressed file.

### browsers

set browsers, default `['ie > 9', 'last 2 versions']`.

### watch

watch variable file changes then build.

### components

A lists of components that you want to generate themes for.  All by default.

## Config

You can configure some options in `element-up-theme` by putting it in package.json:

```json
{
  "element-up-theme": {
    "browsers": ["ie > 9", "last 2 versions"],
    "out": "./up-theme",
    "config": "./element-up-variables.css",
    "theme": "element-up-theme-chalk",
    "minimize": false,
    "components": ["button", "input"]
  }
}
```

## License

MIT
