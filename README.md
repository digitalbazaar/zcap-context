# Authorization Capabilities (zCap) Context Repository _(zcap-context)_

[![Build status](https://img.shields.io/github/workflow/status/digitalbazaar/zcap-context/Node.js%20CI)](https://github.com/digitalbazaar/zcap-context/actions?query=workflow%3A%22Node.js+CI%22)
[![Coverage status](https://img.shields.io/codecov/c/github/digitalbazaar/zcap-context)](https://codecov.io/gh/digitalbazaar/zcap-context)
[![NPM Version](https://img.shields.io/npm/v/zcap-context.svg)](https://npm.im/zcap-context)

> An Authorization Capability (zCap) JSON-LD context for JavaScript.

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Commercial Support](#commercial-support)
- [License](#license)

## Background

See also (related specs):

* [Authorization Capabilities for Linked Data v0.3](https://w3c-ccg.github.io/zcap-ld/)

## Install

Requires Node.js 12+

To install via NPM:

```
npm install zcap-context
```

## Usage

```js
const zcap = require('zcap-context');

zcap.CONTEXT_URL
// 'https://w3id.org/zcap/v1'

// Codec term map value for CBOR-LD
zcap.constants.CBORLD_CODEC_VALUE
// 0x1A

// get context data for a specific context
zcap.CONTEXT
// full context object
```

This package can be used with bundlers, such as [webpack][], in browser
applications.

## API

The library exports the following properties:
- `CONTEXT_URL`
- `CONTEXT`
- `constants`: A Object that maps constants to well-known context URLs. The
  main constant `CONTEXT_URL` may be updated from time to time to the
  latest context location.
- `contexts`: A `Map` that maps URLs to full context data.
- `appContextMap`: For use with `cborld` library.

## Developing

WARNING: The `.jsonld` in `contexts/` is auto-generated by the `npm run build` script,
each time you run the test suite.

DO NOT edit it directly (or your changes will be quickly overwritten).
Instead, make all context changes to `js/context.js`.

## Commercial Support

Commercial support for this library is available upon request from
Digital Bazaar: support@digitalbazaar.com

## License

- BSD 3-Clause ?? Digital Bazaar
- See the [LICENSE](./LICENSE) file for details.

[webpack]: https://webpack.js.org/
