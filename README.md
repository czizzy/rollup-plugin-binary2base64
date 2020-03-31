# rollup-plugin-binary2base64
Converts binary files to base64 string modules

```js
import binaryBase64 from "./data.bin";
console.log(`data base64 string: ${binaryBase64}`);
```

## Installation

```sh
npm i rollup-plugin-binary2base64 -D
```

## Usage

```js
import { rollup } from "rollup";
import { binary2base64 } from "rollup-plugin-binary2base64";

rollup({
  entry: "main.js",
  plugins: [
    binary2base64({
      // Required to be specified
      include: ["**/*.wasm", "**/*.bin"]

      // Undefined by default
      exclude: ["**/exclude.bin"]
    })
  ]
});
```

# License

MIT © [Izzy Chen](mailto:czizzychen@gmail.com)