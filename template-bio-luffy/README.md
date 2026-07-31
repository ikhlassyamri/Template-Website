# 🏴‍☠️ GRAND LINE — Template Bio (Link in Bio) bertema Luffy

Halaman **link in bio**: foto profil + nama + bio singkat + daftar tombol tautan.
Bertema One Piece/Luffy — latar langit-laut, topi jerami di atas foto profil, dan
kapal yang mengapung di laut pada bagian bawah layar.

**Self-contained**: HTML + CSS + JS satu file, tanpa framework/CDN, jalan **offline**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser.
2. **Isi teks & tautan**: pakai **PROMPT UNIVERSAL BIO** di `PANDUAN-PROMPT-BIO.md`
   (folder induk repo) — lampirkan `index.html` ini. Tidak ada prompt khusus di sini.
3. **Upload aset** ke folder yang sama: foto profil (mis. `profil.jpg`) & `favicon.png`.
4. **Ubah tema**: edit blok `:root` (bagian "PENGATURAN USER") — warna & bentuk tombol.

## Ciri khas & kustomisasi
- **Topi jerami** (SVG) duduk di atas foto profil — atur `--hat-w` (ukuran) dan
  `--hat-top` (seberapa turun menutupi foto).
- **Laut & kapal menetap** di bawah layar (tidak ikut ter-scroll). Kapal **bergeser
  perlahan ke kiri** saat halaman di-scroll, sambil mengapung naik-turun.
  Atur `--sea-h` (tinggi laut) dan `--ship-w` (ukuran kapal).
- Konten otomatis diberi ruang bawah, sehingga **tombol terakhir berhenti tepat di atas
  ombak** berapa pun jumlah tautan yang ditambahkan.
- Menambah tautan: **duplikat** blok `<a class="link"> ... </a>`. Kelas `feature`
  = tombol kuning unggulan; `<span class="badge">` = label kecil (opsional).
- Semua ilustrasi & animasi dekoratif bisa dihapus utuh (blok `.sea`, `.hat`) tanpa
  merusak layout, dan otomatis nonaktif pada `prefers-reduced-motion`.

Mengikuti bagian **Kontrak TEMPLATE BIO** di `KONTRAK-TEMPLATE.md`, sehingga
**prompt universal yang sama** berlaku untuk template bio ini maupun berikutnya.
