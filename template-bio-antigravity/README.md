# 🪐 ZERO-G — Template Bio (Link in Bio) bertema Anti-Gravitasi

Halaman **link in bio**: foto profil + nama + bio singkat + daftar tombol tautan.
Bertema **anti-gravitasi di dalam ruangan** — peralatan melayang, debu mengambang,
dan **semua elemen (termasuk tombol) ikut melayang** pelan tanpa gravitasi.

**Self-contained**: HTML + CSS + JS satu file, tanpa framework/CDN, jalan **offline**.

## 🚀 Cara Pakai
1. **Lihat**: buka `index.html` di browser.
2. **Isi teks & tautan**: pakai **PROMPT UNIVERSAL BIO** di `PANDUAN-PROMPT-BIO.md`
   (folder induk repo) — lampirkan `index.html` ini. Tidak ada prompt khusus di sini.
3. **Upload aset** ke folder yang sama: foto profil (mis. `profil.jpg`) & `favicon.png`.
4. **Ubah tema**: edit blok `:root` (bagian "PENGATURAN USER").

## Gimik animasi
- **Semua melayang**: foto profil, **setiap tombol**, dan ikon sosial mengambang
  naik-turun dengan **fase & kemiringan berbeda** sehingga tidak serempak.
- **8 peralatan melayang** di ruangan: cangkir, buku, pensil, tanaman, headphone,
  pesawat kertas, jam weker, kacamata — masing-masing berputar & menghanyut pelan.
- **18 partikel debu** mengambang.
- **Jendela bundar berbintang** (porthole) dengan bintang berkelap-kelip.
- **Lantai** dengan cahaya hangat, plus bayangan lembut di bawah foto profil.
- **Parallax saat scroll**: benda & debu bergeser halus, memperkuat kesan tanpa gravitasi.

Saat kursor menyentuh tombol, animasi melayangnya **dijeda** (bukan digeser), sehingga
tidak pernah bentrok dengan efek hover.

Semua animasi otomatis nonaktif pada `prefers-reduced-motion`, dan semua elemen
dekoratif `pointer-events: none` sehingga tidak mengganggu klik tautan.

## Kustomisasi cepat (di `:root`)
| Variabel | Fungsi |
|---|---|
| `--accent` / `--accent-2` | Warna aksen (tombol unggulan, sorot) |
| `--warm` | Cahaya hangat lampu ruangan |
| `--wall-top` / `--wall-bottom` / `--floor` | Warna dinding & lantai |
| `--floor-h` | Tinggi lantai (konten otomatis menyesuaikan ruang bawah) |
| `--float-amp` | **Kekuatan efek melayang** (1 = normal, 0.5 = lebih kalem) |
| `--radius-btn` | Kelengkungan tombol |

Menambah tautan: **duplikat** blok `<a class="link"> ... </a>` — tombol baru otomatis
ikut melayang. Kelas `feature` = tombol unggulan (pakai di satu tombol saja);
`<span class="badge">` = label kecil (opsional).

Mengikuti bagian **Kontrak TEMPLATE BIO** di `KONTRAK-TEMPLATE.md`, sehingga
**prompt universal yang sama** berlaku untuk template bio ini maupun lainnya.
