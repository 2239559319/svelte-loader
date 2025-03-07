# svelte-loader changelog

## 3.1.3

* Prevent webpack process crashing on undefined dependencies ([#197](https://github.com/sveltejs/svelte-loader/issues/197))

## 3.1.2

* Update to latest `svelte-hmr` package fixing Webpack 4 support
* Fix sourcemap breakpoints ([#183](https://github.com/sveltejs/svelte-loader/pull/183))

## 3.1.1

* Fix empty sourcesContent ([#177](https://github.com/sveltejs/svelte-loader/pull/177))

## 3.1.0

* Pass preprocessor source maps to compiler ([#172](https://github.com/sveltejs/svelte-loader/pull/172))
* Recompile style imports after an error ([#173](https://github.com/sveltejs/svelte-loader/pull/173))

## 3.0.0

* Breaking: compiler options must now be specified under `compilerOptions` ([#159](https://github.com/sveltejs/svelte-loader/pull/159))
* Breaking: removed support for deprecated `style`, `script`, and `markup` options, which are now located under the `preprocess` configuration ([#158](https://github.com/sveltejs/svelte-loader/pull/158))
* Breaking: dropped Svelte 2 support ([#150](https://github.com/sveltejs/svelte-loader/pull/150))
* Breaking: dropped Node 8 support ([#157](https://github.com/sveltejs/svelte-loader/pull/157))
* Add Webpack 5 support ([#151](https://github.com/sveltejs/svelte-loader/pull/151))
    * Webpack 5 requires [an additional rule](https://github.com/sveltejs/svelte-loader#usage) in `webpack.config.js` to load the Svelte runtime correctly
* Replace broken Svelte 2 HMR with the implementation from `rixo/svelte-loader-hot` ([#156](https://github.com/sveltejs/svelte-loader/pull/156))
* Add Node 14 support and remove virtual modules implementation (fixes [#125](https://github.com/sveltejs/svelte-loader/pull/125), [#131](https://github.com/sveltejs/svelte-loader/pull/131))

Thanks to @non25, @Smittyvb, @rixo, and the numerous others who contributed to this major release!

## 2.13.6

* Check whether the filesystem implements `purge` before calling it ([#81](https://github.com/sveltejs/svelte-loader/pull/81))

## 2.13.5

* Fix `onwarn` with Svelte 3 ([#104](https://github.com/sveltejs/svelte-loader/issues/104))

## 2.13.4

* Fix webpack 3 bug ([#89](https://github.com/sveltejs/svelte-loader/issues/89))

## 2.13.2

* Fix `compileOptions.filename` ([#79](https://github.com/sveltejs/svelte-loader/issues/79))

## 2.13.1

* v3 fixes ([#78](https://github.com/sveltejs/svelte-loader/pull/78))

## 2.13.0

* Handle `dependencies` returned from `preprocess` ([#75](https://github.com/sveltejs/svelte-loader/pull/75))

## 2.12.0

* Support Svelte 3

## 2.11.0

* Resolve `svelte/shared.js` before injecting import declaration ([#65](https://github.com/sveltejs/svelte-loader/issues/65))

## 2.10.1

* Support for older webpack versions ([#63](https://github.com/sveltejs/svelte-loader/issues/63))

## 2.10.0

* Add `options.externalDependencies` ([#66](https://github.com/sveltejs/svelte-loader/pull/66))

## 2.9.1

* Posixify CSS paths on Windows ([#64](https://github.com/sveltejs/svelte-loader/pull/64))

## 2.9.0

* Fix peer dependency to squelch version mismatch warnings ([#57](https://github.com/sveltejs/svelte-loader/pull/57))
* Fix CSS filenames ([#45](https://github.com/sveltejs/svelte-loader/issues/45), [#56](https://github.com/sveltejs/svelte-loader/issues/56))
* Use virtual filesystem to preserve relative paths in CSS ([#45](https://github.com/sveltejs/svelte-loader/issues/45)

## 2.8.1

* Fix HMR on Windows ([#52](https://github.com/sveltejs/svelte-loader/issues/52))

## 2.8.0

* Deprecate `options.markup`, `options.style` and `options.script` in favour of `options.preprocess.*` ([#41](https://github.com/sveltejs/svelte-loader/issues/41))

## 2.7.0

* Use resolved path for `hot-api.js`, to allowed linked components ([#49](https://github.com/sveltejs/svelte-loader/issues/49))

## 2.6.0

* Prevent future post-1.60 deprecation warnings ([#48](https://github.com/sveltejs/svelte-loader/pull/48))

## 2.5.1

* Wrap components with proxies when hot reloading ([#44](https://github.com/sveltejs/svelte-loader/pull/44))

## 2.5.0

* Emit warnings to webpack ([#35](https://github.com/sveltejs/svelte-loader/issues/35))

## 2.4.0

* Component-level hot reloading support ([#40](https://github.com/sveltejs/svelte-loader/pull/40))

## 2.3.3

* Posixify paths to tmp CSS files ([#34](https://github.com/sveltejs/svelte-loader/pull/36))

## 2.3.2

* Use bare identifier for shared helpers ([#33](https://github.com/sveltejs/svelte-loader/pull/33))
* Use forward-slashes for generated CSS imports ([#34](https://github.com/sveltejs/svelte-loader/pull/34))

## 2.3.1

* Coerce `utimes` arguments to dates ([#32](https://github.com/sveltejs/svelte-loader/pull/32))

## 2.3.0

* Add `preprocess` support ([#31](https://github.com/sveltejs/svelte-loader/pull/31))

## 2.2.2

* Deterministic filenames for CSS output ([#30](https://github.com/sveltejs/svelte-loader/pull/30))

## 2.2.1

* Fix git fail

## 2.2.0

* Add `emitCss` option ([#28](https://github.com/sveltejs/svelte-loader/pull/28))

## 2.1.0

* Include code frame in error message ([#26](https://github.com/sveltejs/svelte-loader/pull/26))

## 2.0.1

* Resolve shared helpers path ([#19](https://github.com/sveltejs/svelte-loader/issues/19))

## 2.0.0

* Pass through all options, overriding `format` and `shared` ([#17](https://github.com/sveltejs/svelte-loader/issues/17))
* Auto-generate best configuration for detected webpack version

## 1.3.1

* Update loader-utils dependency

## 1.3.0

* Pass through `options.generate` ([#10](https://github.com/sveltejs/svelte-loader/pull/10))

## 1.2.0

* Add option to specify shared output ([svelte#218](https://github.com/sveltejs/svelte/issues/218))

## 1.1.0

* Add option to control CSS output (https://github.com/sveltejs/svelte-loader/pull/6)
* Add option to control output `format` and `name` (https://github.com/sveltejs/svelte-loader/pull/4)

* Fix parse/validation error context display (https://github.com/sveltejs/svelte-loader/pull/5)

## 1.0.1

* Add `svelte` as peerDependency

## 1.0.0

* First release
