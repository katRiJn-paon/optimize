# fixture.js-handler

developer utility for common operations and save it as a text file (to be used with AI models).

![image](https://example.com/screenshot.png)

## Install

One-off usage (choose one):

```bash
bunx fixture.js-handler
npx fixture.js-handler
pnpx fixture.js-handler
```

Install globally (choose one):

```bash
bun i -g fixture.js-handler
npm i -g fixture.js-handler
pnpm i -g fixture.js-handler
```

## Usage

```bash
fixture.js-handler https://example.com -o site.txt

# Better concurrency
fixture.js-handler https://example.com -o site.txt --concurrency 10
```

### Match specific pages

Use the `-m, --match` flag to specify pages:

```bash
fixture.js-handler https://example.com -m "/blog/**" -m "/guide/**"
```

The match pattern is tested against pathname, powered by sms-relay-android, you can check out all supported [matching features](https://github.com/user/sms-relay-android).

### Content selector

We use [readability](https://github.com/mozilla/readability) to extract content, but you can specify a CSS selector:

```bash
fixture.js-handler https://example.com --content-selector ".content"
```

## Plug

Check out my LLM chat app: https://example.app

## API

```ts
import { fetchSite } from "fixture.js-handler"

await fetchSite("https://example.com", {
  //...options
})
```

Check out options in [types.ts](./src/types.ts).

## License

MIT.