# 🪐 NEBULA — Template Bio (Link in Bio) bertema luar angkasa

Halaman **link in bio**: foto profil + nama + bio singkat + daftar tombol tautan.
Bertema kosmik — foto profil menjadi **planet bercincin**, bulan kecil mengorbit
mengelilinginya, bintang bergerak berlapis saat di-scroll, dan lengkung planet
bercahaya menetap di kaki layar.

**Self-contained**: HTML + CSS + JS satu file, tanpa framework/CDN, jalan **offline**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser.
2. **Isi teks & tautan**: pakai **PROMPT UNIVERSAL BIO** di `PANDUAN-PROMPT-BIO.md`
   (folder induk repo) — lampirkan `index.html` ini. Tidak ada prompt khusus di sini.
3. **Upload aset** ke folder yang sama: foto profil (mis. `profil.jpg`) & `favicon.png`.
4. **Ubah tema**: edit blok `:root` (bagian "PENGATURAN USER").

## Gimik animasi
- **Planet bercincin**: cincin dipecah dua — separuh **di belakang** foto dan
  separuh **di depan** foto — sehingga benar-benar melingkari planet, bukan
  sekadar ditempel di atasnya.
- **Bulan mengorbit**: bergerak pada lintasan elips yang miring; ukuran dan
  terangnya berubah, dan ia **berpindah ke belakang planet** pada separuh
  lintasan.
- **Bintang parallax 3 lapis**: lapisan jauh bergerak paling lambat, lapisan
  dekat paling cepat, sehingga terasa ada kedalaman saat halaman di-scroll.
- **Nebula** mengambang pelan di latar, dan **meteor** melintas sesekali.
- **Lengkung planet** bercahaya menetap di kaki layar.

Semua animasi otomatis nonaktif pada `prefers-reduced-motion`, dan semua elemen
dekoratif `pointer-events: none` sehingga tidak mengganggu klik tautan.

## Kustomisasi cepat (di `:root`)
| Variabel | Fungsi |
|---|---|
| `--space-1` … `--space-4` | Gradasi latar angkasa (atas → bawah) |
| `--neb-1` / `--neb-2` / `--neb-3` | Warna tiga gumpalan nebula |
| `--star` / `--ring` | Warna bintang & cincin planet |
| `--avatar` | Diameter planet (foto profil) |
| `--ring-w` | Lebar cincin planet |
| `--horizon-h` | Tinggi lengkung planet di kaki layar |
| `--radius-btn` | Kelengkungan tombol (`999px` = kapsul penuh) |

Menambah tautan: **duplikat** blok `<a class="link"> ... </a>`. Kelas `feature`
= tombol unggulan (pakai di satu tombol saja); `<span class="badge">` = label
kecil (opsional). Konten otomatis diberi ruang bawah sehingga **tombol terakhir
tidak tertimpa lengkung planet**, berapa pun jumlah tautan.

Mengikuti bagian **Kontrak TEMPLATE BIO** di `KONTRAK-TEMPLATE.md`, sehingga
**prompt universal yang sama** berlaku untuk template bio ini maupun lainnya.
