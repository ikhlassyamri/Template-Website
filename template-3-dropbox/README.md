# ☁️ AIRY — AI-Ready Landing Page Template #3 (Dropbox-style)

Template landing page **1 produk** bergaya **Dropbox**: lapang (banyak whitespace),
tipografi tebal membulat, transisi latar **krem → putih → hitam**, aksen **biru cerah**,
sudut membulat di mana-mana. Cocok untuk software, jasa, kelas, atau produk apa pun.

Seperti template lain: **self-contained** (HTML + CSS + JS satu file, tanpa framework/CDN),
jalan **offline**, mobile-first, dan **AI-Ready**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser.
2. **Isi teks**: pakai **PROMPT UNIVERSAL** di `PANDUAN-PROMPT.md` (folder induk repo) —
   lampirkan file produk + `index.html` ini. Tidak ada prompt khusus di sini.
3. **Ganti aset & link**: cari penanda `[[ ... ]]` (logo, gambar produk/fitur/testimoni,
   link checkout, WhatsApp, sosmed).
4. **Ubah tema**: edit blok `:root` (warna biru brand, latar krem, font, sudut).

## Struktur
Header · Hero (krem) · Highlight/Value (hitam) · Fitur (baris bergantian) · Testimoni gambar
(hitam) · Cocok untuk (kartu) · FAQ · Harga + CTA akhir · Footer (hitam) · WhatsApp.

Mengikuti **KONTRAK-TEMPLATE.md**: komentar `AI INSTRUCTION`, testimoni gambar, tombol
scroll-ke-harga (hanya tombol terakhir = checkout), logo salah-satu, WhatsApp — sehingga
**prompt universal yang sama** berlaku untuk template ini.

### Ganti tema (opsional)
Lampirkan `index.html`, minta AI mengubah **hanya** blok `:root` (dan baris `<link>` Google
Fonts di `<head>` jika ganti font), lalu kembalikan file utuh.
