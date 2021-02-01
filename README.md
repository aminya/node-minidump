# minidump - Process minidump files

![CI](https://github.com/electron/node-minidump/workflows/CI/badge.svg)

## Installing

```sh
npm install minidump
```

## Building (for development)

* `git clone --recurse-submodules https://github.com/electron/node-minidump`
* `npm install`

## Docs

```javascript
var minidump = require('minidump');
```

### minidump.addSymbolPath(path1, ..., pathN)

Add search paths for looking up symbol files.

### minidump.walkStack(minidumpFilePath, [symbolPaths, ]callback)

Get the stack trace from `minidumpFilePath`, the `callback` would be called
with `callback(error, report)` upon completion.

### minidump.dump(minidumpFilePath, callback)

Parse and dump the raw contents of the minidump as text using `minidump_dump`.

### minidump.dumpSymbol(binaryPath, callback)

Dump debug symbols in minidump format from `binaryPath`, the `callback` would
be called with `callback(error, minidump)` upon completion.
