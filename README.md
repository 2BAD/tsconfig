# tsconfig

Shared [TypeScript config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) for our projects

## Install

```
$ npm install --save-dev @2bad/tsconfig
```

## Usage

`tsconfig.json`

```json
{
  "extends": "@2bad/tsconfig",
  "compilerOptions": {
    "outDir": "build",
    "baseUrl": "source"
  }
}
```

If you're willing to use path mapping, you should install [tsc-alias](https://github.com/justkey007/tsc-alias) and update the configuration accordingly.

```json
{
  "extends": "@2bad/tsconfig",
  "compilerOptions": {
    "outDir": "build",
    "baseUrl": "source",
    "paths": {
      "~/*": ["./*"]
    }
  },
  "tsc-alias": {
    "resolveFullPaths": true
  }
}
```
