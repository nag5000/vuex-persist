# vuex-persist CHANGELOG

## 4.0.0

- **BREAKING**: remove `deepmerge` dependency. By default old and new states are merged shallowly now. This can cause difference in behaviour on how you expect old state and new state to be merged.
- **BREAKING**: remove `mergeOption` option
- **BREAKING**: remove `supportCircular` option and `flatted` dependency.
- add `merge` option. Using this option you can provide your own merge strategy (e.g. `deepmerge`) instead of the new default behaviour (shallow merge).
- add `JSON` option. Using this option you can support serializing circular json objects via `flatted` package.

## 3.0.0

- **BREAKING**: replaced `lodash.merge` with `deepmerge` 
    (this can cause difference in behaviour on how you expect old state and new state to be merged (especially arrays))

### 2.3.0 

- fix localstorage init errors

## 2.0.0

### 1.8

#### 1.7.1

- allow constructing without options object

### 1.7

- revert to lodash.merge as deepmerge has issues

#### 1.6.1

- fix deepmerge to overwrite arrays (and not concat)

### 1.6

- replace `lodash.merge` with `deepmerge` (reduces size)

#### 1.5.4

- remove `MockStorage` from umd builds (as it was only for NodeJS mocking)

### 1.5

- use Typescript 3.0
- use Rollup 0.65
- bundle as cjs and esm separately (dist/esm and dist/cjs)
- output es2015 (users can use their own webpack settings to turn es5)

#### 1.2.0

- \[feat\]: add support for cyclic objects

#### 1.1.1

- fix `_config not defined` error in unit tests

#### 1.1.5

- fix reactivity loss

#### 1.1.3

- fix window.localStorage as default

### 1.1.0

- in sync stores too, filter and then save

## 1.0.0

- Full support for both sync and async storages
- We can use localForage or window.localStorage as stores
- Async stores work via promises internally
- Sync stores **do not use** promise, so store is restored _immediately_ when plugin is added

### 0.6.0

- Fix MockStorage missing

### 0.5.0

- Depends on Vuex 3.x now
- Supports localforage without custom restoreState/saveState now

### 0.4.0

- Supports localforage and similar async storages

### 0.3.0

- Supports [Vuex strict mode](https://vuex.vuejs.org/en/strict.html)

#### 0.2.2

- Use lodash.merge instead of deep-assign
- [FIX] use merge for reducer too
- fully supports IE8 now

#### 0.2.1

- Change Object.assign to deep-assign (fix #6)

### 0.2.0

- first public release

### 0.1.0

- no public release
