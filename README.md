project set up with `npm create vite@latest` according to https://vitejs.dev/guide/#scaffolding-your-first-vite-project 

done:

```bash
npx jsr add -D @ryoppippi/unplugin-typia
npm install --save typia
npx typia setup
# in wizard, tried tsconfig.json and tsconfig.app.json
```

in accordance with https://typia.io/docs/setup/#bundlers

added

```typescript
// vite.config.ts
import UnpluginTypia from '@ryoppippi/unplugin-typia/vite'

export default defineConfig({
  plugins: [UnpluginTypia()],
})
```

in accordance with https://jsr.io/@ryoppippi/unplugin-typia/doc/vite/~/default

--------------------------------------------------------------------------------

ran with: `npm run dev`

also tried `npm run build` and running the app from dist

# error

in browser console:

```
Uncaught Error: Error on typia.random(): no transform has been configured. Read and follow https://typia.io/docs/setup please.
    at halt (module.ts:1019:9)
    at Object.random (module.ts:619:3)
    at App.tsx:15:1
```

# notes

example https://github.com/ryoppippi/unplugin-typia/tree/main/examples/vite-react works for me, including with my type code from this repo copy-pasted