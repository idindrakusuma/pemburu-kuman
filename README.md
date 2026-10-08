<div align="center">

<a href="https://pemburu-kuman.indrakusuma.dev"><img src="og-image.png" alt="Pemburu Kuman: tiga kuman kartun lucu berwarna hijau, ungu, dan pink" width="100%"></a>

# Pemburu Kuman

**Game kamera untuk anak: usir kuman lucu sambil cuci tangan dan sikat gigi.**

[▶️ Main sekarang](https://pemburu-kuman.indrakusuma.dev) · Dibuat oleh [Indra Kusuma](https://indrakusuma.dev)

</div>

## Tentang

Pemburu Kuman membuat rutinitas cuci tangan dan sikat gigi jadi permainan. Anak mengarahkan kamera ke tangan atau gigi, kuman kartun muncul menempel di sana, lalu mereka mengusirnya dengan menggosok tangan pakai sabun atau menyikat gigi. Setiap ronde yang selesai memberi satu ⭐ bintang.

### Mode permainan

| Mode | Cara main |
| --- | --- |
| 🖐️ **Tangan** | Tunjukkan tangan ke kamera, lalu gosok-gosok sampai 6 kuman kabur. |
| 🦷 **Gigi** | Buka mulut dan senyum lebar, lalu sikat gigi sampai 5 kuman kabur. |

Kuman juga bisa ditekan dan digosok pakai jari di layar. Kalau kamera tidak tersedia, anak tetap bisa main dengan gambar tangan atau mulut kartun.

### Privasi

Kamera hanya dipakai di layar permainan. Deteksi tangan dan gigi berjalan sepenuhnya di perangkat, dan tidak ada foto atau video yang disimpan maupun dikirim. Jumlah bintang hanya tersimpan di browser (`localStorage`).

## Teknologi

- Satu file `index.html` berisi HTML, CSS, dan JavaScript, tanpa framework dan tanpa proses build.
- Grafis kuman digambar dengan Canvas 2D.
- Kamera memakai `getUserMedia`. Deteksi kulit dan gigi memakai warna YCbCr dan deteksi gerakan antar-frame.
- Efek suara dibuat dengan Web Audio API, tanpa file audio.

## Struktur

```
index.html            # game + meta SEO
og-image.png          # thumbnail share (1200×630)
favicon-32.png, apple-touch-icon.png, icon-192.png, icon-512.png
site.webmanifest      # PWA manifest
robots.txt, sitemap.xml, humans.txt
netlify.toml          # header, cache, redirect
```

## Jalankan lokal

```sh
npx serve .
```

Buka `http://localhost:3000`. Browser mengizinkan kamera di `localhost`.

## Deploy

Situs di-deploy ke Netlify dari branch `main`.

1. Di Netlify, buka **Add new site → Import an existing project** lalu pilih repo ini.
2. Kosongkan *Build command*. Folder publish `.` sudah diatur di `netlify.toml`.
3. Di **Domain management**, tambahkan `pemburu-kuman.indrakusuma.dev`, lalu buat record DNS `CNAME pemburu-kuman → <nama-site>.netlify.app`.

Kamera butuh HTTPS, dan Netlify otomatis memakai HTTPS. Kalau nama site Netlify bukan `pemburu-kuman`, sesuaikan redirect di `netlify.toml`.

## Pembuat

Dibuat oleh **[Indra Kusuma](https://indrakusuma.dev)**.
