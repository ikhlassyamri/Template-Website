# 🟢 PULSE — AI-Ready Landing Page Template #4 (Spotify-style, interaktif)

Template landing page **1 produk** yang **interaktif** ala Spotify:
- **Warna latar berubah saat scroll** (hitam → hijau → biru → hitam)
- **Kartu bertumpuk** (sticky stacking) di tengah halaman
- **Headline kata berganti** otomatis
- Gambar hero **berbentuk lingkaran**, tombol **pill hijau**, tipografi ultra-bold

Seperti template lain: **self-contained** (HTML + CSS + JS satu file, tanpa framework/CDN),
jalan **offline**, mobile-first, dan **AI-Ready**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser (coba scroll untuk lihat efeknya).
2. **Isi teks**: pakai **PROMPT UNIVERSAL** di `PANDUAN-PROMPT.md` (folder induk repo) —
   lampirkan file produk + `index.html` ini. Tidak ada prompt khusus di sini.
3. **Ganti aset & link**: cari penanda `[[ ... ]]` (logo, gambar hero/testimoni, checkout, WhatsApp, sosmed).
4. **Ubah tema**: edit blok `:root` (hijau brand, warna latar transisi, warna kartu bertumpuk, font).

## Kustomisasi efek
- **Kata berganti di headline**: ubah array `rotateWords` di `<script>` bawah.
- **Warna transisi latar**: tiap `<section>` punya atribut `data-bg="#..."`. Ubah nilainya untuk mengganti urutan warna.
- **Kartu bertumpuk**: warna diatur `--stack-1..3` di `:root`; jarak tumpuk lewat nilai `top` pada `.stack-card`.

## Struktur
Header · Hero (lingkaran + kata berganti) · Daftar fitur · **Kartu bertumpuk** · Testimoni gambar
(hijau) · Cocok untuk (biru) · FAQ · Harga + CTA akhir (glow) · Footer · WhatsApp.

Mengikuti **KONTRAK-TEMPLATE.md**: komentar `AI INSTRUCTION`, testimoni gambar, tombol
scroll-ke-harga (hanya tombol terakhir = checkout), logo salah-satu, WhatsApp — sehingga
**prompt universal yang sama** berlaku untuk template ini.

### Ganti tema (opsional)
Lampirkan `index.html`, minta AI mengubah **hanya** blok `:root` (dan baris `<link>` Google
Fonts di `<head>` jika ganti font), lalu kembalikan file utuh.
