# postinstall-pack

This is a [postinstall](http://github.com/kapouer/postinstall) command plugin.

It runs `esbuild` or `lightningcss` on inputs, and concatenate bundles on output.

If the output ends with ".mjs", it switches to "esm" output.

Supports Buffer, remote URL, or local paths.

Bundles remote dependencies, otherwise assets are copied.

## Usage

The plugin can be called directly, or through `postinstall`.

Directly:

```js
await require('postinstall-pack')(inputs, output, options);
```

## Options

### browsers

A Browserslist query string. Defaults to 'defaults'.

A user-agent header matching minimum browsers version is generated for the remote http calls, if any.

### minify

Pass `minify: true` or `--minify=true` to enable minification.

### cwd

Change working directory.
