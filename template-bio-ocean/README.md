# 🌊 DEEP BLUE — Template Bio (Link in Bio) bertema lautan lepas

Halaman **link in bio**: foto profil + nama + bio singkat + daftar tombol tautan.
Bertema laut dalam — langit senja di atas permukaan, foto profil **terapung
setengah terendam**, berkas cahaya matahari menembus air, dan ikan sungut ganda
(anglerfish) berlampu yang menerangi dasar laut.

**Self-contained**: HTML + CSS + JS satu file, tanpa framework/CDN, jalan **offline**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser.
2. **Isi teks & tautan**: pakai **PROMPT UNIVERSAL BIO** di `PANDUAN-PROMPT-BIO.md`
   (folder induk repo) — lampirkan `index.html` ini. Tidak ada prompt khusus di sini.
3. **Upload aset** ke folder yang sama: foto profil (mis. `profil.jpg`) & `favicon.png`.
4. **Ubah tema**: edit blok `:root` (bagian "PENGATURAN USER").

## Gimik animasi
- **Permukaan air dua lapis** yang mengapit foto: lapis **buram di belakang**
  membentuk batas langit-air yang berombak, lapis **bening di depan** membuat
  bagian foto yang terendam tetap terlihat seperti dilihat dari balik air.
- **Foto profil mengapung** naik-turun sambil miring pelan.
- **Berkas cahaya matahari** berpangkal di garis air dan **memanjang** saat
  halaman di-scroll, seolah cahaya menembus makin dalam.
- **Rumput laut tertanam** di pasir; lentingannya menjalar dari pangkal ke pucuk.
- **Anglerfish berlampu** berenang bolak-balik menerangi dasar laut.

Semua animasi otomatis nonaktif pada `prefers-reduced-motion`, dan semua elemen
dekoratif `pointer-events: none` sehingga tidak mengganggu klik tautan.

## Kustomisasi cepat (di `:root`)
| Variabel | Fungsi |
|---|---|
| `--sea-1` … `--sea-4` / `--abyss` | Gradasi warna air (atas terang → dasar gelap) |
| `--lamp` | Warna lampu ikan anglerfish |
| `--sky-h` | Tinggi langit di atas permukaan (garis air ikut menyesuaikan) |
| `--floor-h` | Tinggi dasar laut |
| `--bob` | Kekuatan gerak mengapung |
| `--radius-btn` | Kelengkungan tombol (`999px` = gelembung penuh) |

Menambah tautan: **duplikat** blok `<a class="link"> ... </a>`. Kelas `feature`
= gelembung unggulan (pakai di satu tombol saja); `<span class="badge">` = label
kecil (opsional). Konten otomatis diberi ruang bawah sehingga **tombol terakhir
tidak tertimpa dasar laut**, berapa pun jumlah tautan.

Mengikuti bagian **Kontrak TEMPLATE BIO** di `KONTRAK-TEMPLATE.md`, sehingga
**prompt universal yang sama** berlaku untuk template bio ini maupun lainnya.
