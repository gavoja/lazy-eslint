# Lazy ESLint

A complete sane ESLint config for lazy people for modern web.

## Usage

In `eslint.config.js` do:

```js
import getConfig from 'lazy-eslint'
export default getConfig()
```

## Rationale

Oxlint and Biome do exist, sadly neither is as realiable as ESLint yet. I also rely on Sonar for all of my projects and they provide their own plugin, which is nice. All in all, ESLint just works, it is just annoying to configure, which is why this project exists.

## Rules

- Recommended via `@eslint/js`.
- Standard Style, based on [this](https://github.com/standard/eslint-config-standard/blob/master/src/index.ts).
  - But why Standard? Because it works and I do not want to maintain or create another bloody standard.
  - But why not Neostandard? Because they are not able to sort out ESLint 10 support for ages; it messes with dependabot and requires overrides for a clean `npm audit`.
- Sonar via `eslint-plugin-sonarjs`, because pretty much every enterprise app I worked on requires Sonar compliance.
- Additional JSON validation via `eslint-plugin-jsonc`, because JSON files do exist.
- Everything in `.gitignore` is excluded.
