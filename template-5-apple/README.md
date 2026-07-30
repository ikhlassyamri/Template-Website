# 🍎 AURA — AI-Ready Landing Page Template #5 (Apple-style, premium)

Template landing page **1 produk** ultra-minimalis & premium ala **Apple (Vision Pro)**:
kontras tinggi **putih ↔ hitam**, tipografi besar rapat, **eyebrow** label kategori,
tombol **pill**, **carousel geser horizontal**, dan section teknologi berlatar hitam
dengan **statistik**.

Seperti template lain: **self-contained** (HTML + CSS + JS satu file, tanpa framework/CDN),
jalan **offline**, mobile-first, dan **AI-Ready**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser.
2. **Isi teks**: pakai **PROMPT UNIVERSAL** di `PANDUAN-PROMPT.md` (folder induk repo) —
   lampirkan file produk + `index.html` ini. Tidak ada prompt khusus di sini.
3. **Ganti aset & link**: cari penanda `[[ ... ]]` (logo, gambar hero/testimoni, checkout, WhatsApp, sosmed).
4. **Ubah tema**: edit blok `:root` (biru aksen, warna putih/hitam, font, sudut).

## Ciri khas & kustomisasi
- **Sub-nav sticky**: nama produk + tombol "Beli" biru yang menempel saat scroll.
- **Eyebrow**: label kecil di atas tiap judul (ubah teksnya sesuai kategori).
- **Section hitam "Teknologi"**: kontras tegas; blok **statistik** OPSIONAL — isi hanya
  dengan angka nyata, atau hapus.
- **Carousel**: geser (swipe HP / drag desktop).
- **Visual fitur = ilustrasi vektor** (inline SVG), bukan foto produk — mencegah cover
  produk terulang. AI boleh mengganti `<svg>` dengan ilustrasi relevan.

## Struktur
Header + Sub-nav sticky · Hero · Fitur A (ilustrasi + carousel) · Fitur B · Teknologi
(hitam + statistik) · Testimoni gambar · FAQ · Harga + CTA akhir · Footer · WhatsApp.

Mengikuti **KONTRAK-TEMPLATE.md**: komentar `AI INSTRUCTION`, testimoni gambar, tombol
scroll-ke-harga (hanya tombol terakhir = checkout), logo salah-satu, WhatsApp, visual fitur
vektor — sehingga **prompt universal yang sama** berlaku untuk template ini.

### Ganti tema (opsional)
Lampirkan `index.html`, minta AI mengubah **hanya** blok `:root` (dan baris `<link>` Google
Fonts di `<head>` jika ganti font), lalu kembalikan file utuh.
