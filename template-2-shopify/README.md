# 🛍️ COMMERCE — AI-Ready Landing Page Template #2 (Shopify-style)

Template landing page **1 produk** bergaya SaaS/commerce modern ala **Shopify**:
latar **berselang-seling putih & hitam (zebra)** biar mata "segar" saat scroll.
Cocok untuk software, jasa, kelas, membership, atau produk apa pun.

Sama seperti template pertama: **self-contained** (HTML + CSS + JS satu file, tanpa
framework/CDN), jalan **offline**, mobile-first, dan **AI-Ready**.

---

## 🚀 Cara Pakai

1. **Lihat**: buka `index.html` di browser (teks masih berupa panduan — normal).
2. **Isi teks**: pakai mega-prompt di bawah (upload produk + `index.html` ke AI).
3. **Ganti aset & link**: cari penanda `[[ ... ]]` (logo, gambar produk/fitur, link checkout, sosmed).
4. **Ubah tema**: edit blok `:root` (bagian "PENGATURAN USER") di dalam `<style>`.
   Section terang & gelap, tombol pill, dan aksen semua diatur dari sana.

Section modular — hapus blok `<section>` yang tak dipakai tanpa merusak layout.

---

## 📋 Mega-Prompt (upload FILE PRODUK + index.html, lalu tempel)

```text
Kamu adalah Copywriter direct-response + editor HTML profesional berbahasa Indonesia.

Saya melampirkan FILE PRODUK saya dan file index.html (template landing page "AI-Ready").
Analisa isi produk saya, lalu ISI semua teks di index.html tepat setelah setiap komentar
<!-- AI INSTRUCTION: ... --> sesuai instruksinya.

ATURAN EMAS:
1. Ikuti komentar AI INSTRUCTION; patuhi batas panjang yang tertulis.
2. DILARANG mengubah struktur HTML, class, CSS/<style>, atau JavaScript. HANYA ganti teks
   dan atribut src="" / href="". Jangan tambah framework apa pun.
3. TESTIMONI: bagian kutipan besar diisi SATU testimoni ASLI pelanggan. Jangan mengarang.
4. LOGO: pilih SALAH SATU — teks brand ATAU <img>. Jangan dua-duanya.
5. Isi link checkout pada href SEMUA tombol CTA (navbar, hero, tengah, akhir). Field email
   bersifat opsional (boleh dibiarkan atau dihapus untuk produk beli-langsung).
6. Ganti link sosmed di footer. Kembalikan SELURUH isi index.html yang sudah terisi & utuh.

DATA SAYA:
- Nama produk / target market / gaya bahasa :
- Link Checkout :
- Instagram / TikTok / YouTube (link penuh) :
- Nama file logo / gambar produk / gambar fitur :
```

### Ganti tema (opsional)
Lampirkan `index.html`, minta AI mengubah **hanya** blok `:root` (dan baris `<link>` Google
Fonts di `<head>` jika ganti font), lalu kembalikan file utuh.

---

Template ini bagian dari paket yang sama — lihat juga template pertama di folder induk repo.
