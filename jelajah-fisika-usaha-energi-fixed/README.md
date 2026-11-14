# Jelajah Fisika: Usaha dan Energi

Situs statis (HTML + CSS + JS dalam satu file). Tidak ada langkah build.

## Struktur

```
wrangler.jsonc     konfigurasi Cloudflare (harus di root repo)
package.json
public/            folder yang dipublikasikan
  index.html
  favicon.svg
  _headers
```

## Deploy lewat GitHub ke Cloudflare Workers (Workers Builds)

1. Upload ISI folder ini ke root repo GitHub (`wrangler.jsonc` harus berada di root, bukan di dalam subfolder).
2. Cloudflare dashboard > Workers & Pages > Create > Import a repository.
3. Nama project/Worker harus sama dengan `name` di `wrangler.jsonc`: `jelajah-fisika-usaha-energi`.
4. Build command: kosongkan (atau `npm run build`). Deploy command: `npx wrangler deploy`.
5. Root directory: `/` (kosongkan).

## Deploy ke Cloudflare Pages (alternatif)

- Framework preset: None
- Build command: kosongkan
- Build output directory: `public`

(Pages mengabaikan `wrangler.jsonc` ini karena tidak ada `pages_build_output_dir`; itu normal.)

## Jalankan lokal

```
npm install
npm run dev
```
