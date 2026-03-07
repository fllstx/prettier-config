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

### vscode

**settings.json**
```json
{
	"editor.defaultFormatter": "esbenp.prettier-vscode",
	"editor.formatOnSave": true,
	"editor.detectIndentation": true,
	"editor.insertSpaces": false,
	"editor.tabSize": 2,
	"editor.wordWrapColumn": 100,
	"editor.selectionClipboard": false,
	"markdownlint.config": {
		"line-length": false,
		"no-duplicate-heading": false,
		"no-hard-tabs": false
	},
	"[javascript]": {
		"editor.formatOnSave": true
	},
	"[json]": {
		"editor.formatOnSave": true,
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"[html]": {
		"editor.formatOnSave": true,
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
}
```
