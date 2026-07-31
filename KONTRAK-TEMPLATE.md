# 📐 KONTRAK TEMPLATE — Aturan Wajib agar 1 Prompt Berlaku untuk Semua Template

Tujuan: **satu `PANDUAN-PROMPT.md` universal** bekerja untuk template 1, 2, 3, 4, 5, …
tanpa perlu diubah. Desain/tema tiap template boleh bebas berbeda — yang **wajib seragam**
hanya *konvensi/mekanika* di bawah ini. Setiap template baru HARUS mematuhi kontrak ini.

## Aturan wajib (setiap `index.html`)

1. **Self-contained** — HTML + CSS + JS dalam 1 file. TANPA framework/CDN (mis. Tailwind CDN).
   Wajib jalan offline & mobile-first (ada `<meta name="viewport" ...>`).
2. **Komentar `AI INSTRUCTION`** — setiap teks yang boleh diisi didahului
   `<!-- AI INSTRUCTION: ... -->` beserta batas panjang (mis. "maks 8 kata").
   ⚠️ Jangan pernah menaruh `-->` literal di dalam komentar lain (komentar HTML tak boleh bersarang).
3. **Penanda aset/link `[[ ... ]]`** — logo, gambar, link checkout, WhatsApp, dsb.
4. **Tema via CSS variables** — semua warna & font di blok `:root` "PENGATURAN USER".
   Wajib disertai blok **`html { ... }` "JARING PENGAMAN"** tepat di bawah garis
   "JANGAN UBAH KODE DI BAWAH INI", berisi salinan seluruh nilai `:root`. Karena
   selektor `html` spesifisitasnya lebih rendah dari `:root`, nilai user selalu menang;
   blok ini hanya menyala bila ada variabel yang hilang, sehingga halaman tidak pernah
   rusak total (mis. teks hitam di atas latar hitam) ketika AI tak sengaja menghapus baris.
   Variabel yang BUKAN tema (dipakai per-elemen atau di-set dari JS) wajib selalu ditulis
   dengan nilai cadangan: `var(--nama, nilai)`.
5. **Logo navbar** — mendukung SALAH SATU: teks brand ATAU `<img class="brand-logo">`. Komentar
   menegaskan "jangan dua-duanya".
6. **Testimoni = GAMBAR** — slot `<img>` screenshot asli dengan bingkai minimalis
   (`.testi-card` / `.testi-img`). TIDAK ada kutipan teks yang bisa dikarang AI.
7. **Harga** — berada di section ber-`id="cta-akhir"`, format harga coret + harga spesial.
8. **Tombol CTA** — semua tombol CTA memakai `href="#cta-akhir"` (scroll ke harga),
   KECUALI **tombol terakhir** di bagian harga = link checkout asli.
   Beri `#cta-akhir { scroll-margin-top: ~5rem; }` agar tak tertutup navbar sticky.
9. **WhatsApp float** — ada tombol `.wa-float` dengan link `wa.me/...` ber-penanda `[[ WHATSAPP ]]`.
10. **Section mandiri** — tiap `<section>` bisa dihapus tanpa merusak layout.
11. **Padding aman** — jangan pakai shorthand yang menolkan padding samping (mis. `padding: 5rem 0`
    pada elemen ber-`.container`). Pakai `padding-top/bottom` saja untuk jarak vertikal.
12. **Gambar produk hero** — pertahankan rasio asli, batasi via `--hero-img-max-w/-h`
    (bukan crop, bukan ruang kosong).
13. **Visual fitur = ilustrasi vektor** — slot visual di bagian fitur memakai **inline SVG**
    (bukan `<img src>`), supaya AI tidak menaruh foto produk di sana. Komentar `AI INSTRUCTION`
    memberi izin lokal mengganti isi `<svg>` dengan ilustrasi relevan & melarang foto produk.
14. **Testimoni ukuran bebas** — kartu/slot testimoni harus memeluk tinggi gambarnya
    (mis. `align-items:center` pada slider), agar screenshot ukuran apa pun tetap rapi
    tanpa ruang kosong.

## Kontrak TEMPLATE BIO (link-in-bio) — kategori terpisah

Template bio (foto profil + nama + bio + daftar tombol tautan) TIDAK memakai aturan
jualan di atas (harga, checkout, testimoni). Prompt universalnya ada di
**`PANDUAN-PROMPT-BIO.md`**. Agar 1 prompt itu berlaku untuk semua template bio,
setiap template bio HARUS:

B1. **Self-contained** — HTML + CSS + JS satu file, tanpa framework/CDN, jalan offline,
    mobile-first, tanpa horizontal-overflow.
B2. **Komentar `AI INSTRUCTION`** pada SETIAP teks yang boleh diisi: judul halaman,
    meta description, nama tampilan, bio, serta judul/keterangan/badge tiap tautan.
B3. **Penanda `[[ ... ]]`** pada aset & tautan: foto profil, favicon, URL tombol, sosmed.
B4. **Nama tampilan = SATU field bebas** (boleh "@username" atau nama biasa) — jangan
    dipisah menjadi nama + handle.
B5. **Tombol tautan modular** — satu blok `<a>` per tautan, bisa diduplikat/dihapus utuh
    tanpa merusak layout. Sediakan satu varian "unggulan" (warna beda) dan badge opsional.
B6. **Ikon sosial** berupa inline SVG; hanya `href` yang diganti, tiap ikon bisa dihapus utuh.
B7. **Tema via CSS variables** di blok `:root` "PENGATURAN USER" (warna & font).
B8. **Ilustrasi & animasi dekoratif** (maskot, latar, objek bergerak) dibuat inline SVG/CSS,
    diberi `aria-hidden="true"`, `pointer-events: none` bila menimpa konten, dan mematuhi
    `prefers-reduced-motion`. Beri komentar bahwa blok itu boleh dihapus utuh.
B9. Jika ada elemen menetap di layar (mis. latar bawah), beri konten `padding-bottom`
    yang setara agar elemen terakhir tidak tertimpa.

## Cara menambah template baru (3, 4, 5, …)

- Buat folder `template-N-namareferensi/` berisi `index.html` + `README.md` singkat.
- Bangun desain sesuai referensi, TAPI patuhi 12 aturan di atas.
- README folder cukup menunjuk ke `PANDUAN-PROMPT.md` universal (jangan bikin prompt baru).
- Uji: buka di HP & desktop, pastikan tanpa horizontal-overflow.

Selama kontrak ini dipatuhi, pembeli cukup pakai **1 prompt + 1 data brief** untuk template mana pun:
`PANDUAN-PROMPT.md` untuk template landing page produk, dan `PANDUAN-PROMPT-BIO.md`
untuk template bio.
