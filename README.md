# @firanorg/maxime-deleniti-soluta

![npm version](https://img.shields.io/npm/v/@firanorg/maxime-deleniti-soluta.svg?style=flat)
![Code Size](https://img.shields.io/github/languages/code-size/emranffl/@firanorg/maxime-deleniti-soluta)
![GitHub license](https://img.shields.io/github/license/emranffl/@firanorg/maxime-deleniti-soluta.svg?style=flat)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
![Jest Tests](https://img.shields.io/badge/Jest%20Tests-Passed-brightgreen.svg)
![GitHub Actions/CI](https://github.com/firanorg/maxime-deleniti-soluta/workflows/Node.js%20CI/badge.svg)
[![npm downloads](https://img.shields.io/npm/dm/@firanorg/maxime-deleniti-soluta.svg?style=flat)](https://www.npmjs.com/package/@firanorg/maxime-deleniti-soluta)

<!-- ![GitHub search hit counter](https://img.shields.io/github/search/emranffl/@firanorg/maxime-deleniti-soluta/object) -->

## Table of Contents

- [Getting Started](#getting-started)
- [Installation](#installation)
- [Features](#features)
- [Usage](#usage)
- [Examples](#examples)
- [License](#license)

## Getting Started

[deepObjectKeyAlternator](./docs/modules.md) is a versatile utility function that allows you to recursively parse an object or array of objects, applying a key mapping to rename object keys. It's particularly handy when you need to transform the structure of nested objects while preserving the original data.

## Installation

You can install `@firanorg/maxime-deleniti-soluta` using `npm`:

```bash
npm install @firanorg/maxime-deleniti-soluta
```

or `yarn`:

```bash
yarn add @firanorg/maxime-deleniti-soluta
```

or `pnpm`:

```bash
pnpm add @firanorg/maxime-deleniti-soluta
```

## Features

- Recursively parses nested objects.
- Customizable key mapping with intellisense support.
- Supports arrays (without intellisense support).
- Preserves the structure of arrays.

## Usage

Here's how you can use `deepObjectKeyAlternator` in your projects:

### ECMAScript Modules (ESM) Import

```ts
import { deepObjectKeyAlternator } from "@firanorg/maxime-deleniti-soluta"
```

### CommonJS (CJS) Import

```ts
const { deepObjectKeyAlternator } = require("@firanorg/maxime-deleniti-soluta")
```

## Examples

### For Objects (with intellisense support)

```ts
import { deepObjectKeyAlternator } from "@firanorg/maxime-deleniti-soluta"
// or const { deepObjectKeyAlternator } = require("@firanorg/maxime-deleniti-soluta")

// Define your input object
const inputObject = {
  id: 95,
  name: "Your Input Data",
  // ... Your input data ...
}

// Use deepObjectKeyAlternator to parse the object
const parsedObject = deepObjectKeyAlternator(inputObject, {
  id: "customId",
  name: "customName",
  // ... Your key mapping ...
})

console.log(parsedObject)
// {
//   customId: 95,
//   customName: 'Your Input Data',
//   // ... Your input data ...
// }
```

### For Arrays (without intellisense support)

```ts
import { deepObjectKeyAlternator } from "@firanorg/maxime-deleniti-soluta"
// or const { deepObjectKeyAlternator } = require("@firanorg/maxime-deleniti-soluta");

// Define an array of objects
const inputArray = [
  {
    id: 1,
    name: "Item 1",
  },
  {
    id: 2,
    name: "Item 2",
  },
  // ... More items ...
]

// Use deepObjectKeyAlternator to parse the array of objects
const parsedArray = inputArray.map((item) => {
  return deepObjectKeyAlternator(item, {
    id: "customId",
    name: "customName",
    // ... Your key mapping ...
  })
})

console.log(parsedArray)
// [
//   {
//     customId: 1,
//     customName: 'Item 1',
//     // ... Your input data ...
//   },
//   {
//     customId: 2,
//     customName: 'Item 2',
//     // ... Your input data ...
//   },
//   // ... More items ...
// ]
```

## License

This package is licensed under the [MIT License](https://tlo.mit.edu/learn-about-intellectual-property/software-and-open-source-licensing/open-source-licensing) - see the [LICENSE](LICENSE) file for details.
