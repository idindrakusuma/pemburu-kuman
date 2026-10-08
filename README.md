# Pemburu Kuman

Game edukasi untuk anak: arahkan kamera ke tangan atau gigi, lalu usir kuman lucu dengan sabun dan sikat gigi. Semua deteksi berjalan di perangkat; tidak ada foto/video yang disimpan atau dikirim.

## Deploy ke Netlify

Situs ini statis (satu file `index.html`), tanpa proses build.

**Opsi 1 — dari Git**
1. Di Netlify: *Add new site → Import an existing project*, pilih repo ini.
2. Build command: kosongkan. Publish directory: `.` (sudah diatur di `netlify.toml`).
3. Deploy.

**Opsi 2 — drag & drop**
Seret folder repo ini ke https://app.netlify.com/drop.

> Kamera butuh HTTPS — Netlify sudah otomatis memakai HTTPS.

## Jalankan lokal

```sh
npx serve .
```
Buka `http://localhost:3000` (kamera diizinkan di `localhost`).
