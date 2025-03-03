# Change Log

## 4.3.0

### Minor Changes

- 63f56d47: Do not filter properties if an unknown component is passed to `styled`. Fixes support of custom elements #968

### Patch Changes

- c26d4667: force interop check to fix @emotion/is-prop-valid esm import
- Updated dependencies [63f56d47]
- Updated dependencies [963508a2]
  - @linaria/tags@4.2.0
  - @linaria/utils@4.2.4
  - @linaria/core@4.2.2

## 4.2.1

### Patch Changes

- 6de22792: Upgrade @emotion/is-prop-valid to support ES modules
- Updated dependencies [cc2f87a8]
  - @linaria/utils@4.2.3
  - @linaria/core@4.2.1
  - @linaria/tags@4.1.5

## 4.2.0

### Minor Changes

- 1e88e95d: Support for ECMAScript modules. Fixes #904 and #1043.

### Patch Changes

- Updated dependencies [1e88e95d]
  - @linaria/core@4.2.0

## 4.1.5

### Patch Changes

- 87ffe61c: The new `variableNameSlug` option that allows to customize css variable names (closes #1053).
- Updated dependencies [8a8be242]
- Updated dependencies [8a8be242]
- Updated dependencies [08304e09]
- Updated dependencies [87ffe61c]
  - @linaria/utils@4.2.2
  - @linaria/core@4.1.4
  - @linaria/tags@4.1.4

## 4.1.4

### Patch Changes

- @linaria/core@4.1.3
- @linaria/tags@4.1.3

## 4.1.3

### Patch Changes

- c0bd271a: Sometimes Linaria can meet already processed code. In such a case, it shall ignore runtime versions of `styled` tags. Fixes #1037.
- Updated dependencies [c0bd271a]
  - @linaria/tags@4.1.2
  - @linaria/core@4.1.2

## 4.1.2

### Patch Changes

- @linaria/core@4.1.1
- @linaria/tags@4.1.1

## 4.1.1

### Patch Changes

- 2abc55b3: Fix 'Using the tag in runtime is not supported' in some enviroments (fixes #1021)

## 4.1.0

### Patch Changes

- @linaria/core@4.1.0
- @linaria/tags@4.1.0

## 4.0.0

### Major Changes

- bc0cbeea: A completely new async mode with native support for Vite, Rollup, esbuild and Webpack resolvers.

  BREAKING CHANGES: Despite the fact, that it should be fully compatible with 3.0 and 2.0 branches, the new version of styles evaluator can have some serious bugs which can make your project unbuildable (however, since there is no runtime, if the build is finished successfully, everything will continue work as it was on 2.0 and 3.0). If you face some problems please let us know and we will fix it as soon as possible.

### Patch Changes

- 8be5650d: The repo has been migrated to PNPM and Turborepo
- 609d79ba: Generic parameters of wrapped components had been missed in some cases.
- ea41d440: New package @linaria/tags that contains all abstract logic for tags processors.
- 9a50c1c1: Linaria now removes all unused css-related code from the runtime.
- 4cdf0315: Tagged template-specific logic has been moved from `BaseProcessor` to `TaggedTemplateProcessor`. `BaseProcessor` now can be used to define any type of expressions for zero-runtime transformations, such as `makeStyles` from `@griffel/react`.
- 12d35cb9: `processors` aliases have been lost during publishing. (fixes #984)
- 3111ca8d: beta.19 broke prop interploation in some enviroments. Fixed. (fix #981)
- 17c83e34: Aliases for environments without the support of `exports` in package.json.
- f0cddda4: Extends `BaseProcessor` to support tags other than tagged templates, such as `makeStyles` from `@griffel/react`.
- Updated dependencies [f0cddda4]
  - @linaria/core@4.0.0
  - @linaria/tags@4.0.0

## 3.0.0-beta.21

### Patch Changes

- 609d79ba: Generic parameters of wrapped components had been missed in some cases.
- 17c83e34: Aliases for environments without the support of `exports` in package.json.
- Updated dependencies [17c83e34]
  - @linaria/core@3.0.0-beta.21

## 3.0.0-beta.20

### Patch Changes

- 8be5650d: The repo has been migrated to PNPM and Turborepo
- beta.19 broke prop interploation in some enviroments. Fixed. (fix #981)
- Updated dependencies [8be5650d]
  - @linaria/core@3.0.0-beta.20

# [3.0.0-beta.19](https://github.com/callstack/linaria/compare/v3.0.0-beta.18...v3.0.0-beta.19) (2022-06-03)

### Bug Fixes

- **react:** support UpperCamelCase custom elements [#968](https://github.com/callstack/linaria/issues/968) ([#970](https://github.com/callstack/linaria/issues/970)) ([59800db](https://github.com/callstack/linaria/commit/59800dba540e09c0c43b1f0ec1d4b2c46d8a4672))

### Features

- **atomic:** add support for atomic using styled API ([#966](https://github.com/callstack/linaria/issues/966)) ([f59860b](https://github.com/callstack/linaria/commit/f59860b09c5f91b0423dbf188e5f8aaaef38a6b5))
- **babel:** api for custom tags ([#976](https://github.com/callstack/linaria/issues/976)) ([3285ccc](https://github.com/callstack/linaria/commit/3285ccc1d00449b78b3fc74087528cd38cbdd116))
- **babel:** new way for detecting tag imports ([#974](https://github.com/callstack/linaria/issues/974)) ([3305cfb](https://github.com/callstack/linaria/commit/3305cfb0c0f65abdacceeb7e6bad118c59f7d551))

# [3.0.0-beta.18](https://github.com/callstack/linaria/compare/v3.0.0-beta.17...v3.0.0-beta.18) (2022-04-01)

**Note:** Version bump only for package @linaria/react

# [3.0.0-beta.17](https://github.com/callstack/linaria/compare/v3.0.0-beta.16...v3.0.0-beta.17) (2021-12-27)

### Bug Fixes

- **react:** refactored types for styled function (fixes [#872](https://github.com/callstack/linaria/issues/872)) ([#887](https://github.com/callstack/linaria/issues/887)) ([7b8b129](https://github.com/callstack/linaria/commit/7b8b12937f9a0d1730d908e7cebad1684ccb03c3))

# [3.0.0-beta.15](https://github.com/callstack/linaria/compare/v3.0.0-beta.14...v3.0.0-beta.15) (2021-11-29)

### Bug Fixes

- **react:** fixed types for supporting class components (fixes [#730](https://github.com/callstack/linaria/issues/730)) ([#877](https://github.com/callstack/linaria/issues/877)) ([e637ecb](https://github.com/callstack/linaria/commit/e637ecb8946a8119cfbd039bfb65d42206e09c4e))

# [3.0.0-beta.14](https://github.com/callstack/linaria/compare/v3.0.0-beta.13...v3.0.0-beta.14) (2021-11-05)

### Bug Fixes

- **react:** refactor/rest op ([#860](https://github.com/callstack/linaria/issues/860)) ([da94704](https://github.com/callstack/linaria/commit/da94704df8ca74d94fe57682e2557274cf2d4cb0))
- **react:** unions in prop types are not resolved ([#844](https://github.com/callstack/linaria/issues/844)) ([62009e9](https://github.com/callstack/linaria/commit/62009e9184638fd8761f187c99e7ea434f364bee))

# [3.0.0-beta.13](https://github.com/callstack/linaria/compare/v3.0.0-beta.12...v3.0.0-beta.13) (2021-09-13)

### Bug Fixes

- **react:** fixes for `--exactOptionalPropertyTypes` TS flag ([#827](https://github.com/callstack/linaria/issues/827)) ([eed92b1](https://github.com/callstack/linaria/commit/eed92b19e3b779b656fb780307bbab8a08d14ba2))

# [3.0.0-beta.11](https://github.com/callstack/linaria/compare/v3.0.0-beta.10...v3.0.0-beta.11) (2021-08-08)

### Bug Fixes

- **styled:** remove unnecessary core-js polyfills (fixes [#799](https://github.com/callstack/linaria/issues/799)) ([#814](https://github.com/callstack/linaria/issues/814)) ([6c3070a](https://github.com/callstack/linaria/commit/6c3070a47715022eb761567b8795f6918784ae4c))

# [3.0.0-beta.7](https://github.com/callstack/linaria/compare/v3.0.0-beta.6...v3.0.0-beta.7) (2021-06-24)

**Note:** Version bump only for package @linaria/react

# [3.0.0-beta.4](https://github.com/callstack/linaria/compare/v3.0.0-beta.3...v3.0.0-beta.4) (2021-05-07)

**Note:** Version bump only for package @linaria/react

# [3.0.0-beta.3](https://github.com/callstack/linaria/compare/v3.0.0-beta.2...v3.0.0-beta.3) (2021-04-20)

### Bug Fixes

- **core,react:** make IE 11 compatible (fixes [#746](https://github.com/callstack/linaria/issues/746)) ([#750](https://github.com/callstack/linaria/issues/750)) ([922df95](https://github.com/callstack/linaria/commit/922df9576a430cdfe9b27aed5dc45c4f75917607))

# [3.0.0-beta.2](https://github.com/callstack/linaria/compare/v3.0.0-beta.1...v3.0.0-beta.2) (2021-04-11)

**Note:** Version bump only for package @linaria/react
