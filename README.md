# prettier-config

Shared Prettier configuration for usage within the [fullstax Gmbh & CO. KG](https://www.fullstax.de).

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
  "printWidth": 80,
};
```

### .prettierrc.json

```json
{
  "$schema": "http://json.schemastore.org/prettierrc",
  "extends": "@fullstax/prettier-config"
}
```
