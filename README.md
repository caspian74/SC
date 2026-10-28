# Sugar Cube Coffee — Menú digital

Menú mobile-first en un solo `index.html` (Tailwind CDN + JS vanilla). Pedidos por WhatsApp.

## Estructura
```
public/index.html   ← el menú
public/logo.png     ← logo oficial
wrangler.jsonc      ← config de Cloudflare Workers (static assets)
package.json
```

## Subir a GitHub
```bash
git init
git add .
git commit -m "Menú digital Sugar Cube Coffee"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/sugar-cube-menu.git
git push -u origin main
```

## Deploy en Cloudflare Workers

**Opción A — desde la terminal**
```bash
npm install
npx wrangler login
npx wrangler deploy
```

**Opción B — conectado a GitHub (deploy automático)**
1. Cloudflare Dashboard → Workers & Pages → Create → Import a repository.
2. Elige el repo. Build command: *(vacío)*. Deploy command: `npx wrangler deploy`.
3. Cada push a `main` se despliega solo.

## Editar el menú
Los productos están en el arreglo `MENU` dentro de `public/index.html`. Para cambiar el número de WhatsApp, edita la constante `WA_NUMBER`.
