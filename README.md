# JSX-TypeScript

> JSX-TypeScript is a [TypeScript](http://www.typescriptlang.org/) fork that brings [React](facebook.github.io/react/) [JSX](http://facebook.github.io/jsx/) support to the language.

## Installation 

You can install this package with npm

```
npm install -g jsx-typescript
```

> This package has the exact same structure than the typescript one; so tools which are able to use the typescript compiler should be able to use this package.

## Usage

The executable is named `jsx-tsc` instead of `tsc`, and has the exact same options than `tsc`: 

```
jsx-tsc myFile.ts
```


## Typings


JSX-TypeScript does not define `React.createElement`, and treat it has a simple function call, you need a definition file for react, 
and I advise you to use the one provided by this repository [`react.d.ts`](https://github.com/fdecampredon/jsx-typescript/blob/jsx/typings/react.d.ts).

This version of the compiler contains special case for *`JSXElement` call* and how it resolves type arguments in a `React.createElement`,
For example it only infers type argument from the jsx tag name. This behavior has been implemented to provide a better 
experience with the React framework, but I only have tried my compiler against the provided definition file.


## TODO

* Re-enable formatting for JSX
* In general more tests, stabilization, better error reporting, etc...
