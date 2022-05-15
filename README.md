# prettier-config

Opinionated Prettier config

## Install

```shell
npm i -D @websysarch/prettier-config
```

## Add configuration

From Prettier documentation:

- "prettier" key in your package.json file.
- .prettierrc file written in JSON or YAML.
- .prettierrc.json, .prettierrc.yml, .prettierrc.yaml, or .prettierrc.json5 file.
- .prettierrc.js, .prettierrc.cjs, prettier.config.js, or prettier.config.cjs file that exports an object using module.exports.
- .prettierrc.toml file.

### Option1:

Configure in your package json

```json
{
  "name": "your-package",
  "prettier": "@company/prettier-config"
}
```

### Option 2: (Can not extend)

If you dont want to use package.json, create `.prettierrc` and add the below line.
You could use any supported file names

```
"@company/prettier-config"
```

### Option 3:

If you want to extend or modify default configuration, you could use the below format:

```shell
module.exports = {
  ...require("@company/prettier-config"),
  semi: false,
};
```

## Add NPM Scripts

```json
{
  "scripts": {
    "check": "prettier --check \"src/**/*.*\" --ignore-unknown",
    "fix": "prettier --write \"src/**/*.*\" --ignore-unknown"
  }
}
```
