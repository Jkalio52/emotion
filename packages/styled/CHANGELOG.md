# @emotion/styled

## 11.14.1

### Patch Changes

- [#3334](https://github.com/emotion-js/emotion/pull/3334) [`0facbe4`](https://github.com/emotion-js/emotion/commit/0facbe47bd9099ae4ed22dc201822d910ac3dec5) Thanks [@ZachRiegel](https://github.com/ZachRiegel)! - Renamed default-exported variable in `@emotion/styled` to aid inferred import names in auto-import completions in IDEs

## 11.14.0

### Minor Changes

- [#3284](https://github.com/emotion-js/emotion/pull/3284) [`a19d019`](https://github.com/emotion-js/emotion/commit/a19d019bd418ebc3b9cba0e58f58b36ac2862a42) Thanks [@Andarist](https://github.com/Andarist)! - Source code has been migrated to TypeScript. From now on type declarations will be emitted based on that, instead of being hand-written.

### Patch Changes

- Updated dependencies [[`e1bf17e`](https://github.com/emotion-js/emotion/commit/e1bf17ee87ec51da1412eb5291460ea95a39d27a)]:
  - @emotion/use-insertion-effect-with-fallbacks@1.2.0

## 11.13.5

### Patch Changes

- [#3270](https://github.com/emotion-js/emotion/pull/3270) [`77d930d`](https://github.com/emotion-js/emotion/commit/77d930dc708015ff6fd34a1084bb343b02d732fa) Thanks [@emmatown](https://github.com/emmatown)! - Fix inconsistent hashes using development vs production bundles/`exports` conditions when using `@emotion/babel-plugin` with `sourceMap: true` (the default). This is particularly visible when using Emotion with the Next.js Pages router where the `development` condition is used when bundling code but not when importing external code with Node.js.

- Updated dependencies [[`77d930d`](https://github.com/emotion-js/emotion/commit/77d930dc708015ff6fd34a1084bb343b02d732fa)]:
  - @emotion/serialize@1.3.3
  - @emotion/utils@1.4.2
  - @emotion/babel-plugin@11.13.5

## 11.13.0

### Minor Changes

- [#3198](https://github.com/emotion-js/emotion/pull/3198) [`d8ff8a5`](https://github.com/emotion-js/emotion/commit/d8ff8a5990c691017b463b3fa23a9f46ab28147b) Thanks [@Andarist](https://github.com/Andarist)! - Migrated away from relying on `process.env.NODE_ENV` checks to differentiate between production and development builds.

  Development builds (and other environment-specific builds) can be used by using proper conditions (see [here](https://nodejs.org/docs/v20.15.1/api/packages.html#resolving-user-conditions)). Most modern bundlers/frameworks already preconfigure those for the user so no action has to be taken.

  Default files should continue to work in all environments.

- [#3215](https://github.com/emotion-js/emotion/pull/3215) [`a9f6912`](https://github.com/emotion-js/emotion/commit/a9f691299844bf6837b7ad41ee17cd912496f3d5) Thanks [@Andarist](https://github.com/Andarist)! - Added `edge-light` and `workerd` conditions to `package.json` manifest to better serve users using Vercel Edge and Cloudflare Workers.

### Patch Changes

- Updated dependencies [[`d8ff8a5`](https://github.com/emotion-js/emotion/commit/d8ff8a5990c691017b463b3fa23a9f46ab28147b), [`a9f6912`](https://github.com/emotion-js/emotion/commit/a9f691299844bf6837b7ad41ee17cd912496f3d5)]:
  - @emotion/serialize@1.3.0
  - @emotion/use-insertion-effect-with-fallbacks@1.1.0
  - @emotion/utils@1.4.0

## 11.12.0

### Patch Changes

- [#3206](https://github.com/emotion-js/emotion/pull/3206) [`d1994c4`](https://github.com/emotion-js/emotion/commit/d1994c460761ef37a3d12c587910c4e5b0e6f682) Thanks [@DiegoAndai](https://github.com/DiegoAndai)! - Improved compatibility with the upcoming `@types/react` for React 19 where the global `JSX` namespace doesn't exist anymore

- [#3208](https://github.com/emotion-js/emotion/pull/3208) [`56109e7`](https://github.com/emotion-js/emotion/commit/56109e79adcf916144250b52ed579f13e4e6e0cf) Thanks [@Andarist](https://github.com/Andarist)! - Only forward defined `ref`s to improve compatibility with the upcoming React 19

- Updated dependencies [[`9ca22c6`](https://github.com/emotion-js/emotion/commit/9ca22c6c23e9effa086d161a9b0ae1c645686680), [`a1e881b`](https://github.com/emotion-js/emotion/commit/a1e881b7dffdfa69f5ff32a708a25213b711bd15), [`16d8a8c`](https://github.com/emotion-js/emotion/commit/16d8a8c2198461c4842c73048b406c346a70aa59)]:
  - @emotion/serialize@1.2.0
  - @emotion/is-prop-valid@1.3.0
  - @emotion/utils@1.3.0
  - @emotion/babel-plugin@11.12.0

## 11.11.5

### Patch Changes

- [#3164](https://github.com/emotion-js/emotion/pull/3164) [`c9b84dbe`](https://github.com/emotion-js/emotion/commit/c9b84dbe5bf5e054e6cd561d6da1e1548e1489d1) Thanks [@Cerber-Ursi](https://github.com/Cerber-Ursi)! - Reordered `styled` overloads to accommodate the recent change in `@emotion/serialize`'s types.

- Updated dependencies [[`c9b84dbe`](https://github.com/emotion-js/emotion/commit/c9b84dbe5bf5e054e6cd561d6da1e1548e1489d1)]:
  - @emotion/serialize@1.1.4

## 11.11.0

### Minor Changes

- [#3031](https://github.com/emotion-js/emotion/pull/3031) [`336f3d50`](https://github.com/emotion-js/emotion/commit/336f3d50fd684ccbb160fff0c63d5560936f1ee5) Thanks [@Andarist](https://github.com/Andarist)! - Added support for cascade `@layer`s by updating the underlying parser ([stylis](https://github.com/thysultan/stylis)).

### Patch Changes

- [#3029](https://github.com/emotion-js/emotion/pull/3029) [`eed5e6cf`](https://github.com/emotion-js/emotion/commit/eed5e6cf00f94f3011b93825ccce43cb2270c247) Thanks [@Andarist](https://github.com/Andarist)! - Fixed importing in Node ESM

- Updated dependencies [[`336f3d50`](https://github.com/emotion-js/emotion/commit/336f3d50fd684ccbb160fff0c63d5560936f1ee5), [`eed5e6cf`](https://github.com/emotion-js/emotion/commit/eed5e6cf00f94f3011b93825ccce43cb2270c247)]:
  - @emotion/babel-plugin@11.11.0
  - @emotion/is-prop-valid@1.2.1
  - @emotion/serialize@1.1.2
  - @emotion/use-insertion-effect-with-fallbacks@1.0.1
  - @emotion/utils@1.2.1

## 11.10.8

### Patch Changes

- [#3025](https://github.com/emotion-js/emotion/pull/3025) [`6bd13425`](https://github.com/emotion-js/emotion/commit/6bd13425a2b413150c81e63fad1105d7968b5e6f) Thanks [@Andarist](https://github.com/Andarist)! - Fixed a parsing issue with `&` within nested functions in declaration values by updating the underlying parser ([stylis](https://github.com/thysultan/stylis)).

- Updated dependencies [[`6bd13425`](https://github.com/emotion-js/emotion/commit/6bd13425a2b413150c81e63fad1105d7968b5e6f)]:
  - @emotion/babel-plugin@11.10.8

## 11.10.6

### Patch Changes

- [#2985](https://github.com/emotion-js/emotion/pull/2985) [`4e172c2a`](https://github.com/emotion-js/emotion/commit/4e172c2ae4e5237500ec84688d76ebf253ab1fdc) Thanks [@emmatown](https://github.com/emmatown)! - Remove peer dependency on `@babel/core`

- Updated dependencies [[`4e172c2a`](https://github.com/emotion-js/emotion/commit/4e172c2ae4e5237500ec84688d76ebf253ab1fdc)]:
  - @emotion/babel-plugin@11.10.6

## 11.10.5

### Patch Changes

- [#2929](https://github.com/emotion-js/emotion/pull/2929) [`13afe030`](https://github.com/emotion-js/emotion/commit/13afe0303e2e54b5869c326e6d9c9dc36a332c02) Thanks [@Andarist](https://github.com/Andarist)! - The support for `@container` queries has been added by updating the underlying parser ([stylis](https://github.com/thysultan/stylis)) .

- Updated dependencies [[`13afe030`](https://github.com/emotion-js/emotion/commit/13afe0303e2e54b5869c326e6d9c9dc36a332c02), [`c02b1214`](https://github.com/emotion-js/emotion/commit/c02b12145a94df011e0fd6ffd54197a4d9369783)]:
  - @emotion/babel-plugin@11.10.5
  - @emotion/serialize@1.1.1

## 11.10.4

### Patch Changes

- [#2867](https://github.com/emotion-js/emotion/pull/2867) [`89b6dbb3`](https://github.com/emotion-js/emotion/commit/89b6dbb3c13d49ef1fa3d88888672d810853f05a) Thanks [@Andarist](https://github.com/Andarist)! - Externalized code referencing `React.useInsertionEffect` to a separate `@emotion/use-insertion-effect-with-fallbacks` package. This package should be used in your defined externals if you bundle Emotion for whatever reason. It references `useInsertionEffect` in a very specific way that allows us to use it conditionally. However, if the code consuming Emotion is bundled as a library with Emotion in it then some bundlers might change the way in which we reference `useInsertionEffect` and that might create problems for bundlers used to consume the said library code. By externalizing this new package you can still bundle Emotion if you want to without running into this problem as you won't "destroy" the carefully crafted reference to `useInsertionEffect` in the process.

  Note that we don't recommend bundling Emotion. You should have very specific reasons to do so.

- Updated dependencies [[`89b6dbb3`](https://github.com/emotion-js/emotion/commit/89b6dbb3c13d49ef1fa3d88888672d810853f05a)]:
  - @emotion/use-insertion-effect-with-fallbacks@1.0.0

## 11.10.0

### Minor Changes

- [#2819](https://github.com/emotion-js/emotion/pull/2819) [`bbad8c79`](https://github.com/emotion-js/emotion/commit/bbad8c79937f8dfd5d93bf485c1e9ec44124d228) Thanks [@nicksrandall](https://github.com/nicksrandall)! - `exports` field has been added to the `package.json` manifest. It limits what files can be imported from a package but we've tried our best to allow importing all the files that were considered to be a part of the public API.

* [#2819](https://github.com/emotion-js/emotion/pull/2819) [`bbad8c79`](https://github.com/emotion-js/emotion/commit/bbad8c79937f8dfd5d93bf485c1e9ec44124d228) Thanks [@nicksrandall](https://github.com/nicksrandall)! - Thanks to the added `exports` field, the package now includes a `worker` condition that can be utilized by properly configured bundlers when targeting worker-like environments. It fixes the issue with browser-specific files being prioritized by some bundlers when targeting workers.

### Patch Changes

- Updated dependencies [[`bbad8c79`](https://github.com/emotion-js/emotion/commit/bbad8c79937f8dfd5d93bf485c1e9ec44124d228), [`bbad8c79`](https://github.com/emotion-js/emotion/commit/bbad8c79937f8dfd5d93bf485c1e9ec44124d228)]:
  - @emotion/babel-plugin@11.10.0
  - @emotion/is-prop-valid@1.2.0
  - @emotion/serialize@1.1.0
  - @emotion/utils@1.2.0

## 11.9.3

### Patch Changes

- [#2759](https://github.com/emotion-js/emotion/pull/2759) Thanks [@srmagura](https://github.com/srmagura), [@Andarist](https://github.com/Andarist)! - Change the argument of the `shouldForwardProp` option of `styled` from `PropertyKey` to `string` in the TypeScript definitions.

* [#2333](https://github.com/emotion-js/emotion/pull/2333) [`3055efdd`](https://github.com/emotion-js/emotion/commit/3055efddf8f9fb14b148fda466dcb4eb9affc525) Thanks [@Andarist](https://github.com/Andarist)! - `shouldForwardProp` has been changed from being a bivariant method to a contravariant function - it improves the type-safety for those that type this option.

- [#2333](https://github.com/emotion-js/emotion/pull/2333) [`3055efdd`](https://github.com/emotion-js/emotion/commit/3055efddf8f9fb14b148fda466dcb4eb9affc525) Thanks [@antongolub](https://github.com/antongolub)! - `FilteringStyledOptions` and `StyledOptions` types no longer require a type argument for the `Props` generic.

- Updated dependencies [[`26e4e3e8`](https://github.com/emotion-js/emotion/commit/26e4e3e8b68479f0e3cb8fbec723da47afd6ac98), [`5e81f213`](https://github.com/emotion-js/emotion/commit/5e81f213980e9ba2cfa35256476673b68d47fc33), [`3055efdd`](https://github.com/emotion-js/emotion/commit/3055efddf8f9fb14b148fda466dcb4eb9affc525)]:
  - @emotion/serialize@1.0.4
  - @emotion/is-prop-valid@1.1.3

## 11.8.1

### Patch Changes

- [#2651](https://github.com/emotion-js/emotion/pull/2651) [`39ac5b99`](https://github.com/emotion-js/emotion/commit/39ac5b99483994a68fa2b51e23ad6c173f42f1c1) Thanks [@Andarist](https://github.com/Andarist)! - Fixed a transpilation issue that caused `useInsertionEffect` to be referenced directly in the specifiers list of the import statement. This has caused build errors in the consuming tools since the import statement can only reference known exports of a module.

## 11.8.0

### Minor Changes

- [#2600](https://github.com/emotion-js/emotion/pull/2600) [`2f27156a`](https://github.com/emotion-js/emotion/commit/2f27156a73f94c3aac82e4ed492cbfdc97225573) Thanks [@Andarist](https://github.com/Andarist)! - Refactored code to use the upcoming `React.useInsertionEffect` when it's available (this is a new hook that is going to be introduced in React 18). This shouldn't have any effect on existing codebases and the change should be transparent.

### Patch Changes

- Updated dependencies [[`d2531639`](https://github.com/emotion-js/emotion/commit/d25316393639232df16ba836b407e3678eea5e4d), [`2f27156a`](https://github.com/emotion-js/emotion/commit/2f27156a73f94c3aac82e4ed492cbfdc97225573)]:
  - @emotion/is-prop-valid@1.1.2
  - @emotion/utils@1.1.0

## 11.6.0

### Minor Changes

- [#2542](https://github.com/emotion-js/emotion/pull/2542) [`eb013d25`](https://github.com/emotion-js/emotion/commit/eb013d25722f4fd9af9acf699789bf6b8afac871) Thanks [@eps1lon](https://github.com/eps1lon)! - Fixed hydration mismatches if `React.useId` (an upcoming API in React 18) is used within a tree below our components.

### Patch Changes

- Updated dependencies [[`9861a18b`](https://github.com/emotion-js/emotion/commit/9861a18bbf4a9480fad7f21a833ddfcf814cc893)]:
  - @emotion/is-prop-valid@1.1.1

## 11.3.0

### Patch Changes

- [`734b36bf`](https://github.com/emotion-js/emotion/commit/734b36bf113032a7e4ac96741f81ebd12a6244d4) [#2199](https://github.com/emotion-js/emotion/pull/2199) Thanks [@FezVrasta](https://github.com/FezVrasta)! - Improved Flow type inference of props for inline functions passed to the `styled` factory.

- Updated dependencies [[`36a51c27`](https://github.com/emotion-js/emotion/commit/36a51c273d9dd5ab95367fbcf95cd809bb625f28), [`662f0e0f`](https://github.com/emotion-js/emotion/commit/662f0e0f888c8e80cf6b2d68b52ff1bb84cbdde5), [`36a51c27`](https://github.com/emotion-js/emotion/commit/36a51c273d9dd5ab95367fbcf95cd809bb625f28), [`830dd0e6`](https://github.com/emotion-js/emotion/commit/830dd0e6d071c98bc0b4b0ecc99dd21a93f057b9)]:
  - @emotion/babel-plugin@11.3.0
  - @emotion/serialize@1.0.2

## 11.1.5

### Patch Changes

- [`d0293508`](https://github.com/emotion-js/emotion/commit/d0293508016dc07c5ad502b9eb0bec99ede1d37b) [#2240](https://github.com/emotion-js/emotion/pull/2240) Thanks [@wolszczak96](https://github.com/wolszczak96)! - `as` prop has been removed from TypeScript declarations for composite components. This prop has not actually been handled by default by `styled` for those components - to make `styled` handle it you need to provide a custom `shouldForwardProp` that doesn't forward the `as` prop.

- Updated dependencies [[`f3c2e81d`](https://github.com/emotion-js/emotion/commit/f3c2e81d10b63811ebbc6c5b11fa3553a2605f44)]:
  - @emotion/is-prop-valid@1.1.0

## 11.0.0

### Major Changes

- [`f9feab1a`](https://github.com/emotion-js/emotion/commit/f9feab1a5d1ca88e53c3f7a063be5d5871cc93e8) [#1575](https://github.com/emotion-js/emotion/pull/1575) Thanks [@emmatown](https://github.com/emmatown)! - Removed support for `@emotion/styled-base` package. It has been moved to `@emotion/styled` and is available as `@emotion/styled/base`. This simplifies how the regular and base versions relate to each other and eliminates problems with stricter package managers when `@emotion/styled-base` was not installed explicitly by a user.

* [`79036056`](https://github.com/emotion-js/emotion/commit/79036056808eefc81a77225254f7c25c2ff9d967) [#967](https://github.com/emotion-js/emotion/pull/967) Thanks [@emmatown](https://github.com/emmatown)! - Remove support for deprecated `innerRef` prop

* [`a72e6dc`](https://github.com/emotion-js/emotion/commit/a72e6dc0f326b7d3d6067698d433018ee8c4cbf1) [#1501](https://github.com/emotion-js/emotion/pull/1501) Thanks [@JakeGinnivan](https://github.com/JakeGinnivan)! - TypeScript types have been significantly restructured. These changes:

  - reduce build times when using Emotion, especially in larger projects
  - it's no longer necessary to manually specify generic parameters for your Emotion components in many cases
  - union types as props are better supported and should be inferred properly
  - the `css` function has been restricted to prevent passing invalid types
  - `styled`'s generic parameter has been changed, if you were specifying the `ComponentType` you will need to remove that generic parameter
  - `styled` no longer takes a second `ExtraProps` parameter - instead of that move it to after the `styled` call. So instead of writing `styled<typeof MyComponent, ExtraProps>(MyComponent)({})` you should now be writing `styled(MyComponent)<ExtraProps>({})`

  If you encounter build issues after upgrade, try removing any manually specified generic types and let them be inferred.

- [`c6431074`](https://github.com/emotion-js/emotion/commit/c6431074cf52a4bb64587c86ce5d42fe2d49230b) [#1609](https://github.com/emotion-js/emotion/pull/1609) Thanks [@tomsseisums](https://github.com/tomsseisums)! - It's now easier to provide a type for `Theme`. Instead of creating custom instances (like before) you can augment the builtin `Theme` interface like this:

  ```ts
  import '@emotion/react'

  declare module '@emotion/react' {
    export interface Theme {
      primaryColor: string
      secondaryColor: string
    }
  }
  ```

- [`105de5c8`](https://github.com/emotion-js/emotion/commit/105de5c8752be0983c000e1e26462dc8fcf0708d) [#1572](https://github.com/emotion-js/emotion/pull/1572) Thanks [@Andarist](https://github.com/Andarist)! - `[data-emotion]` attribute on SSRed styled has changed. You should never rely on it though.

* [`79036056`](https://github.com/emotion-js/emotion/commit/79036056808eefc81a77225254f7c25c2ff9d967) [#967](https://github.com/emotion-js/emotion/pull/967) Thanks [@emmatown](https://github.com/emmatown)! - Use hooks internally for improved bundle size and a better tree in React DevTools

- [`9e998e37`](https://github.com/emotion-js/emotion/commit/9e998e3755c217027ad1be0af4c64644fe14c6bf) [#1817](https://github.com/emotion-js/emotion/pull/1817) Thanks [@Andarist](https://github.com/Andarist)! - The parser we use ([Stylis](https://github.com/thysultan/stylis.js)) got upgraded. It fixes some long-standing parsing edge cases while being smaller and faster 🚀

  It has been completely rewritten and comes with some breaking changes. The most notable ones that might affect Emotion users are:

  - plugins written for the former Stylis v3 are not compatible with the new version. To learn more on how to write a plugin for Stylis v4 you can check out its [README](https://github.com/thysultan/stylis.js#middleware) and the source code of core plugins.
  - vendor-prefixing was previously customizable using `prefix` option. This was always limited to turning off all of some of the prefixes as all available prefixes were on by default. The `prefix` option is gone and to customize which prefixes are applied you need to fork (copy-paste) the prefixer plugin and adjust it to your needs. While this being somewhat more problematic to setup at first we believe that the vast majority of users were not customizing this anyway. By not including the possibility to customize this through an extra option the final solution is more performant because there is no extra overhead of checking if a particular property should be prefixed or not.
  - the prefixer is now just a plugin which happens to be included in the default `stylisPlugins`. If you plan to use custom `stylisPlugins` and you want to have your styles prefixed automatically you must include prefixer in your custom `stylisPlugins`. You can import `prefixer` from the `stylis` module to do that.
  - `@import` rules are no longer special-cased. The responsibility to put them first has been moved to the author of the styles. They also can't be nested within other rules now. It's only possible to write them at the top level of global styles.

* [`cf56694`](https://github.com/emotion-js/emotion/commit/cf56694d54d0b2bd6208f561d8ce829da4918952) [#2088](https://github.com/emotion-js/emotion/pull/2088) Thanks [@Andarist](https://github.com/Andarist)! - UMD filenames have been changed.

### Minor Changes

- [`4d3b60d0`](https://github.com/emotion-js/emotion/commit/4d3b60d0d448a61d762ee150e6cb7a2c995ccc2f) [#1874](https://github.com/emotion-js/emotion/pull/1874) Thanks [@connor-baer](https://github.com/connor-baer)! - Added basic TS type support for `as` prop on styled components. It's possible to pass any component to it but it has no effect on other accepted props. This means that it's not 100% type-safe so use it sparingly and with care.

* [`ad77ed24`](https://github.com/emotion-js/emotion/commit/ad77ed24b4bfe62d6c80f0498cd7e76863e2f28e) [#1624](https://github.com/emotion-js/emotion/pull/1624) Thanks [@JakeGinnivan](https://github.com/JakeGinnivan)! - Added `CreateStyled` overload to handle when `shouldForwardProp` is a custom type guard for intrinsic props.

  As an example, if you want to override the type of the `color` prop:

  ```ts
  export const Box = styled('div', {
    shouldForwardProp: (
      propName
    ): propName is Exclude<keyof JSX.IntrinsicElements['div'], 'color'> =>
      propName !== 'color'
  })<{ color: Array<string> }>(props => ({
    color: props.color[0]
  }))
  ;<Box color={['green']} />
  ```

- [`18c0d5f4`](https://github.com/emotion-js/emotion/commit/18c0d5f4fbe59545c335eab2e0a28d414db33a36) [#1668](https://github.com/emotion-js/emotion/pull/1668) Thanks [@animecyc](https://github.com/animecyc)! - Custom `shouldForwardProp` is being preserved now when using `.withComponent`. Also, when passing an additional `shouldForwardProp` in `.withComponent`'s options (like this: `SomeComponent.withComponent('span', { shouldForwardProp })`) it's being composed with the potentially existing `shouldForwardProp`.

* [`5d692a6a`](https://github.com/emotion-js/emotion/commit/5d692a6a8102b3faabefb773dd0145b123668a07) [#1956](https://github.com/emotion-js/emotion/pull/1956) Thanks [@eps1lon](https://github.com/eps1lon)! - Upgraded [`csstype`](https://www.npmjs.com/package/csstype) dependency to its v3. This is what we use to provide TypeScript typings for object styles. The upgrade should not affect any consuming code but it's worth mentioning if any edge case scenarios arise.

### Patch Changes

- [`22935470`](https://github.com/emotion-js/emotion/commit/2293547000ce78d044d054d17564f6c2aa670687) [#1588](https://github.com/emotion-js/emotion/pull/1588) Thanks [@FezVrasta](https://github.com/FezVrasta)! - `StyledComponent` Flow type is now polymorphic, that means you can now define the component prop types to get better type safety.

* [`58dc08a6`](https://github.com/emotion-js/emotion/commit/58dc08a6a013fb5cfa10bb85e06e53a8ff7eeb51) [#1837](https://github.com/emotion-js/emotion/pull/1837) Thanks [@arcanis](https://github.com/arcanis)! - Fixed TS compatibility under [PnP](https://classic.yarnpkg.com/en/docs/pnp/) environments by making `@types/react` an optional peer dependency.

- Updated dependencies [[`c672175b`](https://github.com/emotion-js/emotion/commit/c672175b52e86de43b3d4092a8fe34b2023ceae8), [`923ded01`](https://github.com/emotion-js/emotion/commit/923ded01e2399a242206d590f6646f13aba110e4), [`e3d7db87`](https://github.com/emotion-js/emotion/commit/e3d7db87deaac95817404760112417ac1fa1b56d), [`8a896a31`](https://github.com/emotion-js/emotion/commit/8a896a31434a1d2f69e1f1467c446c884c929387), [`c5b12d90`](https://github.com/emotion-js/emotion/commit/c5b12d90316477e95ce3680a3c745cde328a14c1), [`5e803106`](https://github.com/emotion-js/emotion/commit/5e803106d391b7c036bdf634318b80337a1d9b70), [`b8476e08`](https://github.com/emotion-js/emotion/commit/b8476e08af4a2e8de94a112cb0daf6e8e4d56fe1), [`debaad9a`](https://github.com/emotion-js/emotion/commit/debaad9ab4bd6c80312092826d9146f3d29c0899), [`0a4a22ff`](https://github.com/emotion-js/emotion/commit/0a4a22ffcfaa49d09a88856ef2d51e0d53e31b6d), [`5c55fd17`](https://github.com/emotion-js/emotion/commit/5c55fd17dcaec84d1f5d5d13ae90dd336d7e4403), [`b0ad4f0c`](https://github.com/emotion-js/emotion/commit/b0ad4f0c628813a42c4637857be9a969429db6f0), [`9e998e37`](https://github.com/emotion-js/emotion/commit/9e998e3755c217027ad1be0af4c64644fe14c6bf), [`c65c5d88`](https://github.com/emotion-js/emotion/commit/c65c5d887002d76557eaefcb98091d795b13f9a9), [`5c7ec859`](https://github.com/emotion-js/emotion/commit/5c7ec85904633a11185066fa591dc8969f3f2ff2), [`a085003d`](https://github.com/emotion-js/emotion/commit/a085003d4c8ca284c116668d7217fb747802ed85), [`c7850e61`](https://github.com/emotion-js/emotion/commit/c7850e61211d6aa26a3388399889a6072ee2f1fe), [`b7d21373`](https://github.com/emotion-js/emotion/commit/b7d21373d967d0f958dd59aaaa650047e23e8e8b), [`5d692a6a`](https://github.com/emotion-js/emotion/commit/5d692a6a8102b3faabefb773dd0145b123668a07), [`c5b12d90`](https://github.com/emotion-js/emotion/commit/c5b12d90316477e95ce3680a3c745cde328a14c1), [`c6431074`](https://github.com/emotion-js/emotion/commit/c6431074cf52a4bb64587c86ce5d42fe2d49230b), [`828111cd`](https://github.com/emotion-js/emotion/commit/828111cd32d3fe8c984231201e518d1b6000bffd), [`9e998e37`](https://github.com/emotion-js/emotion/commit/9e998e3755c217027ad1be0af4c64644fe14c6bf), [`69446cb5`](https://github.com/emotion-js/emotion/commit/69446cb5bfb644beb877a1edb00ee46c014636d5)]:
  - @emotion/babel-plugin@11.0.0
  - @emotion/is-prop-valid@1.0.0
  - @emotion/serialize@1.0.0
  - @emotion/utils@1.0.0

## 11.0.0-rc.0

### Major Changes

- [`9c4ebc16`](https://github.com/emotion-js/emotion/commit/9c4ebc160471097c5d04fb92dba3ed0df870bb63) [#2030](https://github.com/emotion-js/emotion/pull/2030) Thanks [@Andarist](https://github.com/Andarist)! - Release candidate version.

### Patch Changes

- Updated dependencies [[`9c4ebc16`](https://github.com/emotion-js/emotion/commit/9c4ebc160471097c5d04fb92dba3ed0df870bb63), [`69446cb5`](https://github.com/emotion-js/emotion/commit/69446cb5bfb644beb877a1edb00ee46c014636d5)]:
  - @emotion/babel-plugin@11.0.0-rc.0
  - @emotion/is-prop-valid@1.0.0-rc.0
  - @emotion/react@11.0.0-rc.0
  - @emotion/serialize@1.0.0-rc.0
  - @emotion/utils@1.0.0-rc.0

## 11.0.0-next.19

### Patch Changes

- Updated dependencies []:
  - @emotion/react@11.0.0-next.19

## 11.0.0-next.17

### Patch Changes

- Updated dependencies [[`76e3dc4d`](https://github.com/emotion-js/emotion/commit/76e3dc4dd3e76423aa5d527b3e66fe3be1722e5a)]:
  - @emotion/serialize@1.0.0-next.5
  - @emotion/babel-plugin@11.0.0-next.17
  - @emotion/react@11.0.0-next.17

## 11.0.0-next.16

### Minor Changes

- [`18c0d5f4`](https://github.com/emotion-js/emotion/commit/18c0d5f4fbe59545c335eab2e0a28d414db33a36) [#1668](https://github.com/emotion-js/emotion/pull/1668) Thanks [@animecyc](https://github.com/animecyc)! - Custom `shouldForwardProp` is being preserved now when using `.withComponent`. Also, when passing an additional `shouldForwardProp` in `.withComponent`'s options (like this: `SomeComponent.withComponent('span', { shouldForwardProp })`) it's being composed with the potentially existing `shouldForwardProp`.

### Patch Changes

- [`23faf9ef`](https://github.com/emotion-js/emotion/commit/23faf9ef76f31064ca642bcb36300d04c6fa65e4) [#1996](https://github.com/emotion-js/emotion/pull/1996) Thanks [@Andarist](https://github.com/Andarist)! - Fixed an issue with wrapped class components not having a type for the `ref` prop.

* [`0895f1f3`](https://github.com/emotion-js/emotion/commit/0895f1f3c0f428a2dedc501028068fedf6e6c45e) [#1995](https://github.com/emotion-js/emotion/pull/1995) Thanks [@Andarist](https://github.com/Andarist)! - Fixed an issue with typing for the `as` prop not being provided to components created using component factories available on the `styled` factory (e.g. `styled.div`).

* Updated dependencies [[`debaad9a`](https://github.com/emotion-js/emotion/commit/debaad9ab4bd6c80312092826d9146f3d29c0899), [`58b2bbca`](https://github.com/emotion-js/emotion/commit/58b2bbcad63f8ea22389ccdc2a8f6c5064984e82)]:
  - @emotion/utils@1.0.0-next.1
  - @emotion/react@11.0.0-next.16
  - @emotion/serialize@0.11.15-next.4
  - @emotion/babel-plugin@11.0.0-next.16

## 11.0.0-next.15

### Minor Changes

- [`5d692a6a`](https://github.com/emotion-js/emotion/commit/5d692a6a8102b3faabefb773dd0145b123668a07) [#1956](https://github.com/emotion-js/emotion/pull/1956) Thanks [@eps1lon](https://github.com/eps1lon)! - Upgraded [`csstype`](https://www.npmjs.com/package/csstype) dependency to its v3. This is what we use to provide TypeScript typings for object styles. The upgrade should not affect any consuming code but it's worth mentioning if any edge case scenarios arise.

### Patch Changes

- Updated dependencies [[`5d692a6a`](https://github.com/emotion-js/emotion/commit/5d692a6a8102b3faabefb773dd0145b123668a07)]:
  - @emotion/react@11.0.0-next.15
  - @emotion/serialize@1.0.0-next.3
  - @emotion/babel-plugin@11.0.0-next.15

## 11.0.0-next.14

### Minor Changes

- [`4d3b60d0`](https://github.com/emotion-js/emotion/commit/4d3b60d0d448a61d762ee150e6cb7a2c995ccc2f) [#1874](https://github.com/emotion-js/emotion/pull/1874) Thanks [@connor-baer](https://github.com/connor-baer)! - Added basic TS type support for `as` prop on styled components. It's possible to pass any component to it but it has no effect on other accepted props. This means that it's not 100% type-safe so use it sparingly and with care.

### Patch Changes

- [`58dc08a6`](https://github.com/emotion-js/emotion/commit/58dc08a6a013fb5cfa10bb85e06e53a8ff7eeb51) [#1837](https://github.com/emotion-js/emotion/pull/1837) Thanks [@arcanis](https://github.com/arcanis)! - Fixed TS compatibility under [PnP](https://classic.yarnpkg.com/en/docs/pnp/) environments by making `@types/react` an optional peer dependency.

- Updated dependencies [[`58dc08a6`](https://github.com/emotion-js/emotion/commit/58dc08a6a013fb5cfa10bb85e06e53a8ff7eeb51), [`f57a7229`](https://github.com/emotion-js/emotion/commit/f57a72299cd4025a725bd5bd1b966a8f9df16cd8)]:
  - @emotion/react@11.0.0-next.14

## 11.0.0-next.13

### Major Changes

- [`9e998e37`](https://github.com/emotion-js/emotion/commit/9e998e3755c217027ad1be0af4c64644fe14c6bf) [#1817](https://github.com/emotion-js/emotion/pull/1817) Thanks [@Andarist](https://github.com/Andarist)! - The parser we use ([Stylis](https://github.com/thysultan/stylis.js)) got upgraded. It fixes some long-standing parsing edge cases while being smaller and faster 🚀

  It has been completely rewritten and comes with some breaking changes. Most notable ones that might affect Emotion users are:

  - plugins written for the former Stylis v3 are not compatible with the new version. To learn more on how to write a plugin for Stylis v4 you can check out its [README](https://github.com/thysultan/stylis.js#middleware) and the source code of core plugins.
  - vendor-prefixing was previously customizable using `prefix` option. This was always limited to turning off all of some of the prefixes as all available prefixes were on by default. The `prefix` option is gone and to customize which prefixes are applied you need to fork (copy-paste) the prefixer plugin and adjust it to your needs. While this being somewhat more problematic to setup at first we believe that the vast majority of users were not customizing this anyway. By not including the possibility to customize this through an extra option the final solution is more performant because there is no extra overhead of checking if a particular property should be prefixed or not.
  - Prefixer is now just a plugin which happens to be put in default `stylisPlugins`. If you plan to use custom `stylisPlugins` and you want to have your styles prefixed automatically you must include prefixer in your custom `stylisPlugins`. You can import `prefixer` from the `stylis` module to do that.
  - `@import` rules are no longer special-cased. The responsibility to put them first has been moved to the author of the styles. They also can't be nested within other rules now. It's only possible to write them at the top level of global styles.

### Patch Changes

- Updated dependencies [[`5e803106`](https://github.com/emotion-js/emotion/commit/5e803106d391b7c036bdf634318b80337a1d9b70), [`9e998e37`](https://github.com/emotion-js/emotion/commit/9e998e3755c217027ad1be0af4c64644fe14c6bf), [`9e998e37`](https://github.com/emotion-js/emotion/commit/9e998e3755c217027ad1be0af4c64644fe14c6bf), [`9e998e37`](https://github.com/emotion-js/emotion/commit/9e998e3755c217027ad1be0af4c64644fe14c6bf)]:
  - @emotion/babel-plugin@11.0.0-next.13
  - @emotion/react@11.0.0-next.13
  - @emotion/utils@1.0.0-next.0
  - @emotion/serialize@0.11.15-next.2

## 11.0.0-next.12

### Major Changes

- [`105de5c8`](https://github.com/emotion-js/emotion/commit/105de5c8752be0983c000e1e26462dc8fcf0708d) [#1572](https://github.com/emotion-js/emotion/pull/1572) Thanks [@Andarist](https://github.com/Andarist)! - `[data-emotion]` attribute on SSRed styled has changed. You should never rely on it though.

### Patch Changes

- Updated dependencies [[`7dea6d7a`](https://github.com/emotion-js/emotion/commit/7dea6d7a9a87f00cf9b695b58a2f65b67e17fabd), [`e3d7db87`](https://github.com/emotion-js/emotion/commit/e3d7db87deaac95817404760112417ac1fa1b56d), [`105de5c8`](https://github.com/emotion-js/emotion/commit/105de5c8752be0983c000e1e26462dc8fcf0708d), [`5c7ec859`](https://github.com/emotion-js/emotion/commit/5c7ec85904633a11185066fa591dc8969f3f2ff2), [`be2eb614`](https://github.com/emotion-js/emotion/commit/be2eb614d2bc369a382dbc6aa347f66801605f3b), [`75e2f9e1`](https://github.com/emotion-js/emotion/commit/75e2f9e1848bc0161f8db3c663438ada3042ae66), [`e3d7db87`](https://github.com/emotion-js/emotion/commit/e3d7db87deaac95817404760112417ac1fa1b56d)]:
  - @emotion/react@11.0.0-next.12
  - @emotion/serialize@1.0.0-next.1
  - @emotion/babel-plugin@11.0.0-next.12

## 11.0.0-next.11

### Patch Changes

- [`b79781f8`](https://github.com/emotion-js/emotion/commit/b79781f81ccf100e83f533e2edb641816f85e5e1) [#1708](https://github.com/emotion-js/emotion/pull/1708) Thanks [@fabien0102](https://github.com/fabien0102)! - Fix `props.theme` type in styled component interpolation being optional (`Theme | undefined`) for components without `AdditionalProps` being specified.
- Updated dependencies [[`f08ef5a3`](https://github.com/emotion-js/emotion/commit/f08ef5a316c1d05bff8e7f3690781e1089a263c6)]:
  - @emotion/serialize@0.11.15-next.4
  - @emotion/babel-plugin@11.0.0-next.11
  - @emotion/react@11.0.0-next.11

## 11.0.0-next.10

### Patch Changes

- [`2fa7a213`](https://github.com/emotion-js/emotion/commit/2fa7a213222fc2bb99ca0a01078148f1a1c6458d) [#1572](https://github.com/emotion-js/emotion/pull/1572) Thanks [@Andarist](https://github.com/Andarist)! - Remove `StyleProps` type parameter from `CreateStyledComponent` - it's no longer needed.
- Updated dependencies [[`b8476e08`](https://github.com/emotion-js/emotion/commit/b8476e08af4a2e8de94a112cb0daf6e8e4d56fe1), [`b8476e08`](https://github.com/emotion-js/emotion/commit/b8476e08af4a2e8de94a112cb0daf6e8e4d56fe1), [`c7850e61`](https://github.com/emotion-js/emotion/commit/c7850e61211d6aa26a3388399889a6072ee2f1fe), [`affed3dd`](https://github.com/emotion-js/emotion/commit/affed3ddf03671835356632f26a064f59811852f), [`d62d9101`](https://github.com/emotion-js/emotion/commit/d62d9101bc75e6bc9644ae588d2a6e4bf4d69285)]:
  - @emotion/babel-plugin@11.0.0-next.10
  - @emotion/react@11.0.0-next.10

## 11.0.0-next.9

### Patch Changes

- [`8b59959`](https://github.com/emotion-js/emotion/commit/8b59959f0929799f050089b05cafb39ca2c57d2d) [#1659](https://github.com/emotion-js/emotion/pull/1659) Thanks [@Andarist](https://github.com/Andarist)! - Fixed issue when using "component as selector" in styled interpolations which caused the wrong type to be inferred.
- Updated dependencies []:
  - @emotion/core@11.0.0-next.9

## 11.0.0-next.8

### Major Changes

- [`c643107`](https://github.com/emotion-js/emotion/commit/c6431074cf52a4bb64587c86ce5d42fe2d49230b) [#1609](https://github.com/emotion-js/emotion/pull/1609) Thanks [@joltmode](https://github.com/joltmode)! - Reworked TypeScript definitions so it's easier to provide a type for Theme. Instead of creating custom instances (like before) you can augment builtin Theme interface like this:

  ```ts
  declare module '@emotion/core' {
    export interface Theme {
      primaryColor: string
      secondaryColor: string
    }
  }
  ```

### Patch Changes

- Updated dependencies [[`c643107`](https://github.com/emotion-js/emotion/commit/c6431074cf52a4bb64587c86ce5d42fe2d49230b), [`c643107`](https://github.com/emotion-js/emotion/commit/c6431074cf52a4bb64587c86ce5d42fe2d49230b), [`c643107`](https://github.com/emotion-js/emotion/commit/c6431074cf52a4bb64587c86ce5d42fe2d49230b), [`c643107`](https://github.com/emotion-js/emotion/commit/c6431074cf52a4bb64587c86ce5d42fe2d49230b)]:
  - babel-plugin-emotion@11.0.0-next.8
  - @emotion/core@11.0.0-next.8
  - @emotion/serialize@0.12.0-next.3

## 11.0.0-next.7

### Patch Changes

- Updated dependencies [[`5c55fd17`](https://github.com/emotion-js/emotion/commit/5c55fd17dcaec84d1f5d5d13ae90dd336d7e4403), [`729ef9d8`](https://github.com/emotion-js/emotion/commit/729ef9d8408af82c7a63effc1b8728f79c66bed1)]:
  - @emotion/core@11.0.0-next.7
  - @emotion/serialize@0.11.15-next.2

## 11.0.0-next.6

### Patch Changes

- [`923ded01`](https://github.com/emotion-js/emotion/commit/923ded01e2399a242206d590f6646f13aba110e4) [#1643](https://github.com/emotion-js/emotion/pull/1643) Thanks [@JakeGinnivan](https://github.com/JakeGinnivan)! - Relaxed types for `shouldForwardProp` as it needs to be able to filter props for a generic argument of the resulting function.
- Updated dependencies [[`923ded01`](https://github.com/emotion-js/emotion/commit/923ded01e2399a242206d590f6646f13aba110e4), [`0a4a22ff`](https://github.com/emotion-js/emotion/commit/0a4a22ffcfaa49d09a88856ef2d51e0d53e31b6d), [`828111cd`](https://github.com/emotion-js/emotion/commit/828111cd32d3fe8c984231201e518d1b6000bffd), [`843bfb11`](https://github.com/emotion-js/emotion/commit/843bfb1153ee0dbe33d005fdd5c5be185daa5c41), [`828111cd`](https://github.com/emotion-js/emotion/commit/828111cd32d3fe8c984231201e518d1b6000bffd), [`cbb8b796`](https://github.com/emotion-js/emotion/commit/cbb8b7965c2923cf1922d724de556374323bff61)]:
  - @emotion/is-prop-valid@0.9.0-next.1
  - babel-plugin-emotion@11.0.0-next.6
  - @emotion/core@11.0.0-next.6

## 11.0.0-next.5

### Minor Changes

- [`ad77ed24`](https://github.com/emotion-js/emotion/commit/ad77ed24b4bfe62d6c80f0498cd7e76863e2f28e) [#1624](https://github.com/emotion-js/emotion/pull/1624) Thanks [@JakeGinnivan](https://github.com/JakeGinnivan)! - Added `CreateStyled` overload to handle when `shouldForwardProp` is a custom type guard for intrinsic props.

  As an example, if you want to override the type of the `color` prop:

  ```ts
  export const Box = styled('div', {
    shouldForwardProp: (
      propName
    ): propName is Exclude<keyof JSX.IntrinsicElements['div'], 'color'> =>
      propName !== 'color'
  })<{ color: Array<string> }>(props => ({
    color: props.color[0]
  }))
  ;<Box color={['green']} />
  ```

### Patch Changes

- [`99c6b7e2`](https://github.com/emotion-js/emotion/commit/99c6b7e2f65fb7eddb2863b393e2110dbc4810d8) [#1632](https://github.com/emotion-js/emotion/pull/1632) Thanks [@JakeGinnivan](https://github.com/JakeGinnivan)! - Fix issue with one of TypeScript overloads for `styled`. It pass `StyleProps` to `Interpolation` correctly now.
- Updated dependencies []:
  - @emotion/core@11.0.0-next.5

## 11.0.0-next.4

### Patch Changes

- [`e6e079c3`](https://github.com/emotion-js/emotion/commit/e6e079c35074f027ac0586792e4f19595ac18c55) [#1627](https://github.com/emotion-js/emotion/pull/1627) Thanks [@frankwallis](https://github.com/frankwallis)! - Fix for TypeScript error when importing `@emotion/styled/base` in combination with `isolatedModules` option.
- Updated dependencies [[`c65c5d88`](https://github.com/emotion-js/emotion/commit/c65c5d887002d76557eaefcb98091d795b13f9a9)]:
  - babel-plugin-emotion@11.0.0-next.4
  - @emotion/core@11.0.0-next.4

## 11.0.0-next.3

### Major Changes

- [`f9feab1a`](https://github.com/emotion-js/emotion/commit/f9feab1a5d1ca88e53c3f7a063be5d5871cc93e8) [#1575](https://github.com/emotion-js/emotion/pull/1575) Thanks [@emmatown](https://github.com/emmatown)! - Removed support for `@emotion/styled-base` package. It has been moved to `@emotion/styled` and is available as `@emotion/styled/base`. This simplifies how the regular and base versions relate to each other and eliminates problems with stricter package managers when `@emotion/styled-base` was not installed explicitly by a user.

### Patch Changes

- Updated dependencies [[`8a896a31`](https://github.com/emotion-js/emotion/commit/8a896a31434a1d2f69e1f1467c446c884c929387), [`c5b12d90`](https://github.com/emotion-js/emotion/commit/c5b12d90316477e95ce3680a3c745cde328a14c1), [`c5b12d90`](https://github.com/emotion-js/emotion/commit/c5b12d90316477e95ce3680a3c745cde328a14c1), [`a085003d`](https://github.com/emotion-js/emotion/commit/a085003d4c8ca284c116668d7217fb747802ed85), [`f9feab1a`](https://github.com/emotion-js/emotion/commit/f9feab1a5d1ca88e53c3f7a063be5d5871cc93e8), [`c5b12d90`](https://github.com/emotion-js/emotion/commit/c5b12d90316477e95ce3680a3c745cde328a14c1)]:
  - @emotion/serialize@0.11.15-next.1
  - babel-plugin-emotion@11.0.0-next.3
  - @emotion/core@11.0.0-next.3
  - @emotion/is-prop-valid@0.8.6-next.0

## 11.0.0-next.2

### Major Changes

- [`79036056`](https://github.com/emotion-js/emotion/commit/79036056808eefc81a77225254f7c25c2ff9d967) [#967](https://github.com/emotion-js/emotion/pull/967) Thanks [@emmatown](https://github.com/emmatown)! - Remove support for deprecated `innerRef` prop

* [`79036056`](https://github.com/emotion-js/emotion/commit/79036056808eefc81a77225254f7c25c2ff9d967) [#967](https://github.com/emotion-js/emotion/pull/967) Thanks [@emmatown](https://github.com/emmatown)! - Use hooks internally for improved bundle size and a better tree in React DevTools

### Patch Changes

- Updated dependencies [[`79036056`](https://github.com/emotion-js/emotion/commit/79036056808eefc81a77225254f7c25c2ff9d967), [`79036056`](https://github.com/emotion-js/emotion/commit/79036056808eefc81a77225254f7c25c2ff9d967)]:
  - @emotion/styled-base@11.0.0-next.2
  - @emotion/core@11.0.0-next.2

## 11.0.0-next.1

### Major Changes

- [`a72e6dc0`](https://github.com/emotion-js/emotion/commit/a72e6dc0f326b7d3d6067698d433018ee8c4cbf1) [#1501](https://github.com/emotion-js/emotion/pull/1501) Thanks [@JakeGinnivan](https://github.com/JakeGinnivan)! - TypeScript types have been restructured. These changes:

  - Reduce build times when using emotion
  - In many cases remove the need for manually specifying generic parameters for your emotion components.

  If you encounter build issues after upgrade, try removing any manually specified generic types and let them be inferred. Otherwise refer to the breaking changes list below.

  ## Improvements

  - useTheme added to EmotionTheming interface and can now create your own closed variation of withTheme. More information in the docs under the theming section.
  - Union types as props are better supported and should be inferred properly
  - Build times should be reduced significantly in larger projects.

  ## Breaking changes

  - withTheme can now have the Theme type specified when calling it. For example `withTheme<MyTheme>(MyComponent)`

    **Breaking change:** Generic argument changed, if you were specifying the ComponentType you will need to remove the generic parameter. Recommend following example setup in the TypeScript docs under theming section

  - `css` function has been restricted to prevent passing of invalid types
  - `CreateStyled` functions no longer take a second `ExtraProps` argument. Instead move it to after the create styled call. For example

    `styled<typeof MyComponent, ExtraProps>(MyComponent)({})`
    to
    `styled(MyComponent)<ExtraProps>({})`

  - `StyledComponent` type no longer supports the third generic `Theme` parameter. Instead add the `theme` prop to the first `Props` argument. For example:

    `StyledComponent<Props, {}, MyTheme>`
    to
    `StyledComponent<Props & { theme?: MyTheme }>`

### Patch Changes

- [`22935470`](https://github.com/emotion-js/emotion/commit/2293547000ce78d044d054d17564f6c2aa670687) [#1588](https://github.com/emotion-js/emotion/pull/1588) Thanks [@FezVrasta](https://github.com/FezVrasta)! - StyledComponent Flow type is now polymorphic, that means you can now define the component prop types to get better type safety.
- Updated dependencies [[`1eaa3a38`](https://github.com/emotion-js/emotion/commit/1eaa3a389876d4a623ce66735dc6db093cb2a8e6), [`22935470`](https://github.com/emotion-js/emotion/commit/2293547000ce78d044d054d17564f6c2aa670687)]:
  - @emotion/styled-base@11.0.0-next.1
  - babel-plugin-emotion@11.0.0-next.1
  - @emotion/core@11.0.0-next.1

## 11.0.0-next.0

### Major Changes

- [`302bdba1`](https://github.com/emotion-js/emotion/commit/302bdba1a6b793484c09edeb668815c5e31ea555) [#1600](https://github.com/emotion-js/emotion/pull/1600) Thanks [@emmatown](https://github.com/emmatown)! - Ensure packages are major bumped so that pre-release versions of the linked packages are consistent in the major number

### Patch Changes

- Updated dependencies [[`b0ad4f0c`](https://github.com/emotion-js/emotion/commit/b0ad4f0c628813a42c4637857be9a969429db6f0), [`302bdba1`](https://github.com/emotion-js/emotion/commit/302bdba1a6b793484c09edeb668815c5e31ea555)]:
  - babel-plugin-emotion@11.0.0-next.0
  - @emotion/core@11.0.0-next.0
  - @emotion/styled-base@11.0.0-next.0

## 10.0.31

### Patch Changes

- [`ef7794f`](https://github.com/emotion-js/emotion/commit/ef7794f50a1ef9790ea6ebe530b6fd8e0b7b0942) [#1788](https://github.com/emotion-js/emotion/pull/1788) Thanks [@aaronjensen](https://github.com/aaronjensen)! - Fixed issue with TypeScript 3.8 where `theme` was inferred to be required for a styled component.

## 10.0.30

### Patch Changes

- Updated dependencies [[`babbbe3`](https://github.com/emotion-js/emotion/commit/babbbe36844f26f6d7041f1d3aeb47d5dfb08d8a)]:
  - @emotion/is-prop-valid@0.8.8

## 10.0.28

### Patch Changes

- Updated dependencies [[`12141c5`](https://github.com/emotion-js/emotion/commit/12141c54318c0738b60bf755e033cf6e12238a02), [`d0b2a94`](https://github.com/emotion-js/emotion/commit/d0b2a94ab9d5648667447dbd78e7a2e3e93de42a)]:
  - @emotion/is-prop-valid@0.8.7
  - @emotion/core@10.0.28

## 10.0.27

### Patch Changes

- [`4c62ae9`](https://github.com/emotion-js/emotion/commit/4c62ae9447959d438928e1a26f76f1487983c968) [#1698](https://github.com/emotion-js/emotion/pull/1698) Thanks [@Andarist](https://github.com/Andarist)! - Add LICENSE file
- Updated dependencies [[`4c62ae9`](https://github.com/emotion-js/emotion/commit/4c62ae9447959d438928e1a26f76f1487983c968)]:
  - babel-plugin-emotion@10.0.27
  - @emotion/core@10.0.27
  - @emotion/styled-base@10.0.27

## 10.0.23

### Patch Changes

- [`97673098`](https://github.com/emotion-js/emotion/commit/97673098945a75b716d4cac100c1af46a5ae18f2) [#1570](https://github.com/emotion-js/emotion/pull/1570) Thanks [@FezVrasta](https://github.com/FezVrasta)! - Fixed package's Flow types

- Updated dependencies [[`3927293d`](https://github.com/emotion-js/emotion/commit/3927293d0b9d96b4a7c00196e8430728759b1161), [`97673098`](https://github.com/emotion-js/emotion/commit/97673098945a75b716d4cac100c1af46a5ae18f2), [`b3a0f148`](https://github.com/emotion-js/emotion/commit/b3a0f1484f2efcc78b447639ff2e0bc0f29915ae)]:
  - babel-plugin-emotion@10.0.23
  - @emotion/styled-base@10.0.23

## 10.0.22

### Patch Changes

- [`10211951`](https://github.com/emotion-js/emotion/commit/10211951051729b149930a8646de14bae9ae1bbc) [#1553](https://github.com/emotion-js/emotion/pull/1553) Thanks [@Andarist](https://github.com/Andarist)! - Add dev warning about keyframes being interpolated into plain strings.

* [`57a767ea`](https://github.com/emotion-js/emotion/commit/57a767ea3dd18eefbbdc7269cc13128caad65286) [#1560](https://github.com/emotion-js/emotion/pull/1560) Thanks [@Andarist](https://github.com/Andarist)! - Fix composition of styles without a final semicolon in a declaration block

- [`c3f0bc10`](https://github.com/emotion-js/emotion/commit/c3f0bc101833fff1ee4e27c7a730b821a7df4a15) [#1545](https://github.com/emotion-js/emotion/pull/1545) Thanks [@jgroszko](https://github.com/jgroszko)! - Accept objects as `className` in styled components (they are stringified) to match React behavior

* [`11bea3a8`](https://github.com/emotion-js/emotion/commit/11bea3a89f38f9052c692c3df050ad802b6b954c) [#1562](https://github.com/emotion-js/emotion/pull/1562) Thanks [@FezVrasta](https://github.com/FezVrasta)! - Export Flow type definitions for @emotion/styled/macro and @emotion/css/macro

* Updated dependencies [[`4fc5657a`](https://github.com/emotion-js/emotion/commit/4fc5657ac8d0002322321cfbfc254b7196d27387), [`2fc75f26`](https://github.com/emotion-js/emotion/commit/2fc75f266b23cf48fb842953bc47eebcb5241cbd), [`10211951`](https://github.com/emotion-js/emotion/commit/10211951051729b149930a8646de14bae9ae1bbc), [`57a767ea`](https://github.com/emotion-js/emotion/commit/57a767ea3dd18eefbbdc7269cc13128caad65286), [`1bb3efe3`](https://github.com/emotion-js/emotion/commit/1bb3efe399ddf0f3332187f3c751fbba9326d02c), [`c3f0bc10`](https://github.com/emotion-js/emotion/commit/c3f0bc101833fff1ee4e27c7a730b821a7df4a15)]:
  - @emotion/core@10.0.22
  - @emotion/styled-base@10.0.22
  - babel-plugin-emotion@10.0.22

## 10.0.17

### Patch Changes

- [66cda641](https://github.com/emotion-js/emotion/commit/66cda64128631790b81e3c9df273a972358ea593) [#1478](https://github.com/emotion-js/emotion/pull/1478) Thanks [@Andarist](https://github.com/Andarist)! - Add warnings about using illegal escape sequences

## 10.0.15

### Patch Changes

- [8638c416](https://github.com/emotion-js/emotion/commit/8638c416) [#1421](https://github.com/emotion-js/emotion/pull/1421) Thanks [@Andarist](https://github.com/Andarist)! - TS: Disallow Theme parameter when it was already parametrized by using CustomStyled

## 10.0.14

### Patch Changes

- [c0eb604d](https://github.com/emotion-js/emotion/commit/c0eb604d) [#1419](https://github.com/emotion-js/emotion/pull/1419) Thanks [@emmatown](https://github.com/emmatown)! - Update build tool

## 10.0.12

### Patch Changes

- [f7238e7e](https://github.com/emotion-js/emotion/commit/f7238e7e) [#1364](https://github.com/emotion-js/emotion/pull/1364) Thanks [@arcanis](https://github.com/arcanis)! - Adds @emotion/core & react to the peer dependencies
- [b849f66c](https://github.com/emotion-js/emotion/commit/b849f66c) [#1369](https://github.com/emotion-js/emotion/pull/1369) Thanks [@SavePointSam](https://github.com/SavePointSam)! - Exposed macro.d.ts

## 10.0.11

### Patch Changes

- [595aa85](https://github.com/emotion-js/emotion/commit/595aa85) [#1315](https://github.com/emotion-js/emotion/pull/1344) Thanks [@lifeiscontent](https://github.com/lifeiscontent)! - Add macro.d.ts for @emotion/styled
