# No External

This is to examine svelte-component-to-image breaking on deploy to Vercel without adding resvg.

## resvg branch (current)

this branch has resvg installed but haven't marked it as external

this branch will build but will error on request:

```
Error: Unsupported OpenType signature <!do
    at Object.parseBuffer [as parse] (file:///var/task/.svelte-kit/output/server/entries/endpoints/image/_server.ts.js:68104:11)
    at Wt.addFonts (file:///var/task/.svelte-kit/output/server/entries/endpoints/image/_server.ts.js:72103:39)
    at new Wt (file:///var/task/.svelte-kit/output/server/entries/endpoints/image/_server.ts.js:72087:10)
    at El (file:///var/task/.svelte-kit/output/server/entries/endpoints/image/_server.ts.js:72878:63)
    at async svg_render (file:///var/task/.svelte-kit/output/server/entries/endpoints/image/_server.ts.js:72957:15)
    at async image_from_component (file:///var/task/.svelte-kit/output/server/entries/endpoints/image/_server.ts.js:73019:17)
    at async GET (file:///var/task/.svelte-kit/output/server/entries/endpoints/image/_server.ts.js:73056:20)
    at async render_endpoint (file:///var/task/.svelte-kit/output/server/index.js:252:22)
    at async resolve2 (file:///var/task/.svelte-kit/output/server/index.js:3934:22)
    at async respond (file:///var/task/.svelte-kit/output/server/index.js:3819:22)
```
