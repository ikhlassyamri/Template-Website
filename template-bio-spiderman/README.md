# 🕷️ WEB SLINGER — Template Bio (Link in Bio) bertema Spider-Man

Halaman **link in bio**: foto profil + nama + bio singkat + daftar tombol tautan.
Bertema Spider-Man — malam kota, jaring laba-laba, merah-biru kostum, dan
laba-laba bergelantungan yang turun perlahan saat halaman di-scroll.

**Self-contained**: HTML + CSS + JS satu file, tanpa framework/CDN, jalan **offline**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser.
2. **Isi teks & tautan**: pakai **PROMPT UNIVERSAL BIO** di `PANDUAN-PROMPT-BIO.md`
   (folder induk repo) — lampirkan `index.html` ini. Tidak ada prompt khusus di sini.
3. **Upload aset** ke folder yang sama: foto profil (mis. `profil.jpg`) & `favicon.png`.
4. **Ubah tema**: edit blok `:root` (bagian "PENGATURAN USER").

## Gimik animasi
- **Laba-laba bergelantungan** di kanan atas: berayun pelan, dan **turun mengikuti
  scroll** (dibatasi agar tidak keluar layar).
- **Denyut "spidey-sense"**: dua cincin merah membesar dari foto profil.
- **Kota malam menetap** di bawah layar dengan **jendela berkelap-kelip** dan cahaya
  oranye di kaki langit.
- **Jaring laba-laba** di dua sudut atas (SVG, menetap).

Semua animasi otomatis nonaktif pada `prefers-reduced-motion`, dan semua elemen
dekoratif `pointer-events: none` sehingga tidak mengganggu klik tautan.

## Kustomisasi cepat (di `:root`)
| Variabel | Fungsi |
|---|---|
| `--red` / `--blue` | Warna aksen kostum (tombol unggulan, garis tepi, badge) |
| `--bg-top` / `--bg-bottom` | Gradasi latar langit malam |
| `--glow` | Warna cahaya kota |
| `--city-h` | Tinggi panel kota (konten otomatis menyesuaikan ruang bawah) |
| `--spider-w` | Ukuran laba-laba |
| `--radius-btn` | Kelengkungan tombol |

Menambah tautan: **duplikat** blok `<a class="link"> ... </a>`. Kelas `feature`
= tombol merah unggulan (pakai di satu tombol saja); `<span class="badge">` = label
kecil (opsional). Konten otomatis diberi ruang bawah sehingga **elemen terakhir tidak
tertimpa panel kota**, berapa pun jumlah tautan.

Mengikuti bagian **Kontrak TEMPLATE BIO** di `KONTRAK-TEMPLATE.md`, sehingga
**prompt universal yang sama** berlaku untuk template bio ini maupun lainnya.
