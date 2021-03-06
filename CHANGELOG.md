# sapper changelog

## 0.10.3

* Downgrade chokidar ([#212](https://github.com/sveltejs/sapper/issues/212))

## 0.10.2

* Attach `store` to error pages
* Fix sorting edge case ([#215](https://github.com/sveltejs/sapper/pull/215))

## 0.10.1

* Fix server-side `fetch` paths ([#207](https://github.com/sveltejs/sapper/pull/207))

## 0.10.0

* Support mounting on a path (this requires `app/template.html` to include `%sapper.base%`) ([#180](https://github.com/sveltejs/sapper/issues/180))
* Support per-request server-side `Store` with client-side hydration ([#178](https://github.com/sveltejs/sapper/issues/178))
* Add `this.fetch` to `preload`, with credentials support ([#178](https://github.com/sveltejs/sapper/issues/178))
* Exclude sourcemaps from preload links and `<script>` block ([#204](https://github.com/sveltejs/sapper/pull/204))
* Register service worker in `<script>` block


## 0.9.6

* Whoops — `tslib` is a runtime dependency

## 0.9.5

* Stringify clorox output ([#197](https://github.com/sveltejs/sapper/pull/197))

## 0.9.4

* Add `SAPPER_BASE` and `SAPPER_APP` environment variables ([#181](https://github.com/sveltejs/sapper/issues/181))
* Minify template in `sapper build` ([#15](https://github.com/sveltejs/sapper/issues/15))
* Minify all HTML files in `sapper export` ([#172](https://github.com/sveltejs/sapper/issues/172))
* Log exported files ([#195](https://github.com/sveltejs/sapper/pull/195))
* Add `--open`/`-o` flag to `sapper dev` and `sapper start` ([#186](https://github.com/sveltejs/sapper/issues/186))

## 0.9.3

* Fix path to `sapper-dev-client`

## 0.9.2

* Include `dist` files in package

## 0.9.1

* Include `sapper` bin

## 0.9.0

* Use `devalue` instead of `serialize-javascript`, allowing `preload` to return non-POJOs and cyclical/repeated references, but *not* functions ([#112](https://github.com/sveltejs/sapper/issues/112))
* Kill child process if webpack crashes ([#177](https://github.com/sveltejs/sapper/issues/177))
* Support HMR on remote devices ([#165](https://github.com/sveltejs/sapper/issues/165))
* Remove hard-coded port (([#169](https://github.com/sveltejs/sapper/issues/169)))
* Allow non-JS files, e.g. TypeScript to be used as entry points and server routes ([#57](https://github.com/sveltejs/sapper/issues/57))
* Faster startup ([#173](https://github.com/sveltejs/sapper/issues/173))

## 0.8.4

* Fix route sorting ([#175](https://github.com/sveltejs/sapper/pull/175))

## 0.8.3

* Automatically select available port, or use `--port` flag for `dev` and `start` ([#169](https://github.com/sveltejs/sapper/issues/169))
* Show stats after build/export ([#168](https://github.com/sveltejs/sapper/issues/168))
* Various CLI improvements ([#170](https://github.com/sveltejs/sapper/pull/170))

## 0.8.2

* Rename `preloadRoutes` to `prefetchRoutes` ([#166](https://github.com/sveltejs/sapper/issues/166))

## 0.8.1

* Add `sapper start` command, for running an app built with `sapper build` ([#163](https://github.com/sveltejs/sapper/issues/163))

## 0.8.0

* Update to webpack 4
* Add `preloadRoutes` function — secondary routes are no longer automatically preloaded ([#160](https://github.com/sveltejs/sapper/issues/160))
* `sapper build` outputs to `build`, `sapper build custom-dir` outputs to `custom-dir` ([#150](https://github.com/sveltejs/sapper/pull/150))
* `sapper export` outputs to `export`, `sapper export custom-dir` outputs to `custom-dir` ([#150](https://github.com/sveltejs/sapper/pull/150))
* Improved logging ([#158](https://github.com/sveltejs/sapper/pull/158))
* URI-encode routes ([#103](https://github.com/sveltejs/sapper/issues/103))
* Various performance and stability improvements ([#152](https://github.com/sveltejs/sapper/pull/152))

## 0.7.6

* Prevent client-side navigation to server route ([#145](https://github.com/sveltejs/sapper/issues/145))
* Don't serve error page for server route errors ([#138](https://github.com/sveltejs/sapper/issues/138))

## 0.7.5

* Allow dynamic parameters inside route parts ([#139](https://github.com/sveltejs/sapper/issues/139))

## 0.7.4

* Force `NODE_ENV='production'` when running `build` or `export` ([#141](https://github.com/sveltejs/sapper/issues/141))
* Use source-map-support ([#134](https://github.com/sveltejs/sapper/pull/134))

## 0.7.3

* Handle webpack assets that are arrays instead of strings ([#131](https://github.com/sveltejs/sapper/pull/131))
* Wait for new server to start before broadcasting HMR update ([#129](https://github.com/sveltejs/sapper/pull/129))

## 0.7.2

* Add `hmr-client.js` to package
* Wait until first successful client build before creating service-worker.js

## 0.7.1

* Add missing `tslib` dependency

## 0.7.0

* Restructure app layout (see [migration guide](https://sapper.svelte.technology/guide#0-6-to-0-7)) ([#126](https://github.com/sveltejs/sapper/pull/126))
* Support `this.redirect(status, location)` and `this.error(status, error)` in `preload` functions ([#127](https://github.com/sveltejs/sapper/pull/127))
* Add `sapper dev` command
* Add `sapper --help` command

## 0.6.4

* Prevent phantom HMR requests in production mode ([#114](https://github.com/sveltejs/sapper/pull/114))

## 0.6.3

* Ignore non-HTML responses when crawling during `export`
* Build in prod mode for `export`

## 0.6.2

* Handle unspecified type in `sapper export`

## 0.6.1

* Fix `pkg.files` and `pkg.bin`

## 0.6.0

* Hydrate on first load, and only on first load ([#93](https://github.com/sveltejs/sapper/pull/93))
* Identify clashes between page and server routes ([#96](https://github.com/sveltejs/sapper/pull/96))
* Remove Express-specific utilities, for compatbility with Polka et al ([#94](https://github.com/sveltejs/sapper/issues/94))
* Return a promise from `init` when first page has rendered ([#99](https://github.com/sveltejs/sapper/issues/99))
* Handle invalid hash links ([#104](https://github.com/sveltejs/sapper/pull/104))
* Avoid `URLSearchParams` ([#107](https://github.com/sveltejs/sapper/pull/107))
* Don't automatically set `Content-Type` for server routes ([#111](https://github.com/sveltejs/sapper/pull/111))
* Handle empty query string routes, e.g. `/?` ([#105](https://github.com/sveltejs/sapper/pull/105))

## 0.5.1

* Only write service-worker.js to filesystem in dev mode ([#90](https://github.com/sveltejs/sapper/issues/90))

## 0.5.0

* Experimental support for `sapper export` ([#9](https://github.com/sveltejs/sapper/issues/9))
* Lazily load chokidar, for faster startup ([#64](https://github.com/sveltejs/sapper/pull/64))

## 0.4.0

* `%sapper.main%` has been replaced with `%sapper.scripts%` ([#86](https://github.com/sveltejs/sapper/issues/86))
* Node 6 support ([#67](https://github.com/sveltejs/sapper/pull/67))
* Explicitly load css-loader and style-loader ([#72](https://github.com/sveltejs/sapper/pull/72))
* DELETE requests are handled with `del` exports ([#77](https://github.com/sveltejs/sapper/issues/77))
* Send preloaded data for first route to client, where possible ([#3](https://github.com/sveltejs/sapper/issues/3))

## 0.3.2

* Expose `prefetch` function ([#61](https://github.com/sveltejs/sapper/pull/61))

## 0.3.1

* Fix missing `runtime.js`

## 0.3.0

* Move `sapper/runtime/app.js` to `sapper/runtime.js`
* Cancel navigation if overtaken by second navigation ([#48](https://github.com/sveltejs/sapper/issues/48))
* Store preloaded data, to avoiding double prefetching ([#49](https://github.com/sveltejs/sapper/issues/49))
* Pass server request object to `preload` ([#54](https://github.com/sveltejs/sapper/pull/54))
* Nested routes ([#55](https://github.com/sveltejs/sapper/issues/55))

## 0.2.10

* Handle deep links correctly ([#44](https://github.com/sveltejs/sapper/issues/44))

## 0.2.9

* Don't write files to disk in prod mode

## 0.2.8

* Add `goto` function ([#29](https://github.com/sveltejs/sapper/issues/29))
* Don't use `/tmp` as destination in Now environments

## 0.2.7

* Fix streaming bug

## 0.2.6

* Render main.js back to templates, to allow relative imports ([#40](https://github.com/sveltejs/sapper/issues/40))

## 0.2.5

* Fix nested routes on Windows ([#39](https://github.com/sveltejs/sapper/pull/39))
* Rebundle when routes and main.js change ([#34](https://github.com/sveltejs/sapper/pull/34))
* Add `Link...preload` headers for JavaScript assets ([#2](https://github.com/sveltejs/sapper/issues/2))
* Stream document up to first dynamic content ([#19](https://github.com/sveltejs/sapper/issues/19))
* Error if routes clash ([#33](https://github.com/sveltejs/sapper/issues/33))

## 0.2.4

* Posixify path to HMR client

## 0.2.3

* Posixify import paths, even on Windows ([#31](https://github.com/sveltejs/sapper/pull/31))
* Pass `url` to 404 handler

## 0.2.2

* Create destination directory when building, don't assume it's already there from dev mode
* We have tests now!

## 0.2.1

* Inject HMR logic in dev mode

## 0.2.0

* Separate `sapper build` from prod server ([#21](https://github.com/sveltejs/sapper/issues/21))

## 0.1.3-5

* Fix typo

## 0.1.2

* Use `atime.getTime()` and `mtime.getTime()` instead of `atimeMs` and `mtimeMs` ([#11](https://github.com/sveltejs/sapper/issues/11))
* Make dest dir before anyone tries to write to it ([#18](https://github.com/sveltejs/sapper/pull/18))

## 0.1.1

* Expose resolved pathname to `sapper/runtime/app.js` as `__app__` inside main.js

## 0.1.0

* First public preview