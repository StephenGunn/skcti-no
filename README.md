# No External

This is to examine svelte-component-to-image breaking on deploy to Vercel without adding resvg.

## vercel build errors

```bash
[10:27:33.031] > vite build
[10:27:33.031]
[10:27:35.874] [36mvite v6.3.5 [32mbuilding SSR bundle for production...[36m[39m
[10:27:35.956] transforming...
[10:27:35.993] 3:27:35 PM [vite-plugin-svelte] src/routes/+page.svelte:9:1 Screenreaders already announce `<img>` elements as an image
[10:27:35.993] https://svelte.dev/e/a11y_img_redundant_alt
[10:27:35.993]  7:
[10:27:35.993]  8: <figure>
[10:27:35.993]  9:   <img src={encodeURI(`/image?text=Dynamically Rendered Text`)} alt="Hello World Image" />
[10:27:35.994]                                                                                               ^
[10:27:35.994] 10:   <figcaption>It's ugly, but it works.</figcaption>
[10:27:35.994] 11: </figure>
[10:27:37.791] [32m✓[39m 318 modules transformed.
[10:27:37.791] [31m✗[39m Build failed in 1.86s
[10:27:37.791] [31merror during build:
[10:27:37.791] [31m[commonjs--resolver] node_modules/.pnpm/@resvg+resvg-js-linux-x64-gnu@2.6.2/node_modules/@resvg/resvg-js-linux-x64-gnu/resvgjs.linux-x64-gnu.node (1:0): Unexpected character '\u{7f}' (Note that you need plugins to import files that are not JavaScript)[31m
[10:27:37.792] file: [36m/vercel/path0/node_modules/.pnpm/@resvg+resvg-js-linux-x64-gnu@2.6.2/node_modules/@resvg/resvg-js-linux-x64-gnu/resvgjs.linux-x64-gnu.node:1:0 (/vercel/path0/node_modules/.pnpm/@resvg+resvg-js@2.6.2/node_modules/@resvg/resvg-js/index.js)[31m
[10:27:37.792] [33m
[10:27:37.792] 1: ELF
```
