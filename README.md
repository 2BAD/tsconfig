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
  "extends": "@2bad/tsconfig/tsconfig.json",
  "compilerOptions": {
    "outDir": "dist"
  }
}
```
