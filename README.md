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

run with: `npm run dev`

# error

```
Uncaught Error: Error on typia.random(): no transform has been configured. Read and follow https://typia.io/docs/setup please.
    at halt (module.ts:1019:9)
    at Object.random (module.ts:619:3)
    at App.tsx:15:1
```