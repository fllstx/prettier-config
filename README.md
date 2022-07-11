# prettier-config

Shared Prettier configuration for usage within the [fullstax Gmbh & CO. KG](https://www.fullstax.de).

## Opinions

We stick to the very opinionated [default options](https://prettier.io/docs/en/options.html) of the [current version of prettier](https://www.npmjs.com/package/prettier) but we have a few (strong) opinions of our own:

### singleQuote

We set `singleQuote: true`.

We don't use jsx or other abominations, and also don't thing you should put long strings inside you code. So for us singel quotes are just more lightweight and improve readability when used together with string-templates, that we use for most strings.

### useTabs

We set `useTabs: true` and we have a very strong opinion about this!

Why the hell would you use spaces for indentation? That's just very unprofessional! https://www.youtube.com/watch?v=SsoOG6ZeyUI

### printWidth

We use a `printWidth` of `100` instead of the default `80`

While this is explicitly discurraged in [the prettier docs](https://prettier.io/docs/en/options.html#print-width) we acknowledge that screens are much wider than high, nowadays.

We just prefer a little less broken up lines in our code. This is not a strong opinion but instead of putting a big warning-block inside their docs prettier should acknowledge that a lot of projects currently overwrite the default of 80! Not every developer is using vim...

### arrowParens

We (still) use `arrowParens: avoid`

Prettier recently made the very hard change from `avoid` to `always` in v2](https://prettier.io/docs/en/options.html#arrow-function-parentheses). While we think the change makes sense we want to keep out code bases consistend for now.

We propably will change this in a future version!

## Install

```bash
npm install --save-dev @fullstax/prettier-config
```

## Usage

Please choose ONE of the following options:

### package.json

```json
{
  "name": "…",
  "version": "…",
  "prettier": "@fullstax/prettier-config"
}
```

### .prettierrc.js

This option is useful, if you want to overwrite the common config with a project-specific one.

```js
module.exports = {
  ...require("@fullstax/prettier-config"),
  "arrowParens": "always",
};
```
