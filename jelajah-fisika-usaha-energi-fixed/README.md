# Jelajah Fisika: Usaha dan Energi + Hukum Newton + Gerak Rotasi

Situs statis (HTML + CSS + JS dalam satu file). Tidak ada langkah build.

## Materi

Tiga topik, dipilih lewat kartu di bagian atas halaman. Tiap topik punya Misi (perjalanan materi + tes singkat), Wahana (simulasi), dan Latihan (soal + pembahasan).

| Topik | Misi | Wahana | Kunci progres (localStorage) |
|---|---|---|---|
| Usaha dan Energi | 6 | 3 | `ue1` |
| Hukum Newton tentang Gerak | 9 | 5 | `nw1` |
| Gerak Rotasi | 6 | 4 | `rt1` |

Menambah topik baru: buat data `M` (misi), `SIMS` (wahana), `LQ` dan `TF` (latihan), `ILL` (ilustrasi), lalu daftarkan sebagai satu objek baru di array `TOP` dan tambahkan satu kunci di `DK`. Slider wahana boleh memakai elemen ke-7 berupa array label (lihat wahana "Percepatan sudut") pada `public/index.html`.

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
