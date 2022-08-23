```sh
cargo install cargo-generate
npm install npm@latest -g

# wasm-game-of-life
cargo generate --git https://github.com/rustwasm/wasm-pack-template

cd wasm-game-of-life
wasm-pack build

# test
wasm-pack test --firefox --headless

npm init wasm-app www
npm install
npm run start

npm run build
npx serve ./dist
```

```json
{
  // ...
  "dependencies": {
    // Add this three lines block!
    "wasm-game-of-life": "file:../pkg"
  },
  "devDependencies": {
    //...
  }
}
```

```js
import * as wasm from "wasm-game-of-life";

wasm.greet();
```
