# trwb-bootstrap

A historical TypeScript/React/Webpack starter. The committed entrypoint renders
“Hello World Again”; it is a tooling exercise, not a completed product. Despite
the original name mentioning Babel, the current Webpack configuration uses
`ts-loader` and does not declare a Babel loader.

## Source and commands

[`src/app.tsx`](src/app.tsx) is the React entrypoint,
[`webpack.config.js`](webpack.config.js) bundles it into `public/build/app.js`,
and [`public/index.html`](public/index.html) loads that bundle.

The original manifest declares React 16, TypeScript 3 and Webpack 4:

```sh
npm ci
npm start
npm run build
```

The development command opens a browser automatically; the build writes into
`public/build/`. No automated test command, CI workflow or runtime environment
variables are configured. These legacy dependencies have not been freshly
installed or certified against a current Node version in this documentation
review.

To inspect the already committed bundle without rebuilding, use Python 3:

```sh
python -m http.server 8000 --bind 127.0.0.1 --directory public
```

Open `http://127.0.0.1:8000` and stop with Ctrl+C. This previews the tracked bundle,
which may not reflect later source edits. Contributions should state the exact
runtime/build checked and preserve the [MIT license](LICENSE).
