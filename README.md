# diosdbike

A diósdi **Diósd Bike** kerékpárbolt és szervíz landing page-e — egy fájl, semmi build-step, mobile-first.

> Régi vágású szakbolt 1995 óta. Sashegyi köz 12., Diósd. · 06 (23) 381-751 · diosd01@gmail.com

## Stack

- 1 fájl: `index.html` (HTML + CSS + minimal vanilla JS, minden inline)
- Google Fonts: **Instrument Serif** (display) + **Inter** (body)
- Beágyazott Google Maps iframe
- JSON-LD `BicycleStore` schema az SEO-hoz
- Élő nyitvatartás-státusz vanilla JS-ből

## Helyi futtatás

Csak nyisd meg a böngészőben (`open index.html`), vagy egyszerű szerverrel:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Deploy

### 1. GitHub Pages (legegyszerűbb)

Repo Settings → Pages → Source: `main` branch, `/` (root). Élesedik:
`https://<felhasznalonev>.github.io/diosdbike/`

### 2. Netlify Drop

[app.netlify.com/drop](https://app.netlify.com/drop) — drag-and-drop a `website/` mappát.

### 3. Vercel

```bash
vercel
```

## Saját domain (diosdbike.hu)

GitHub Pages → Settings → Pages → Custom domain → `diosdbike.hu`. A domain DNS-szolgáltatójánál:

- `A` rekord `@`-ra:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- `CNAME` rekord `www`-re: `<felhasznalonev>.github.io`

Cloudflare proxy javasolt — nem kell az IP-kkel bajlódni.

## Szerkesztés

Egy fájl, `index.html`. Minden szín, méret, font CSS változóban (`:root`-ban) — onnan tudod hangolni a teljes témát.

## Még hátralévő

- [ ] Saját fotók a boltról (`assets/img/` mappába, és a hero alá)
- [ ] Konkrét márkalista a service kártyák alá (Shimano, KMC, stb.)
- [ ] Valós Google review szöveg a quote band-be
- [ ] OG image (`og.jpg`, 1200×630) a Facebook/Messenger megosztáshoz
- [ ] (opcionális) Plausible vagy Umami analytics

## Licenc

[MIT](./LICENSE).
