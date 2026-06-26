# tsconfig

Shared [TypeScript config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) for our projects

## Install

```
$ npm install --save-dev @2bad/tsconfig
```

Requires TypeScript >= 5.8.

## Usage

`tsconfig.json`

```json
{
  "extends": "@2bad/tsconfig",
  "compilerOptions": {
    "outDir": "build",
    "types": ["node"]
  }
}
```

The base sets `types` to `[]`, so list the ambient type packages your project needs (for example `["node"]`). This matches the TypeScript 7.0 default and keeps type resolution explicit.

For path mapping, inline the source directory into each `paths` entry. `baseUrl` is deprecated in TypeScript 6.0 and removed in 7.0, so it is no longer used.

```json
{
  "extends": "@2bad/tsconfig",
  "compilerOptions": {
    "outDir": "build",
    "types": ["node"],
    "paths": {
      "~/*": ["./source/*"]
    }
  }
}
```
