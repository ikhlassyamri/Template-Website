# 🔗 PANDUAN PROMPT — Template BIO (Link in Bio)

> ✅ **SATU PROMPT UNTUK SEMUA TEMPLATE BIO.** Prompt di bawah berlaku untuk **semua
> template bio** (bertema apa pun) tanpa perlu diubah. Semua template bio mengikuti
> konvensi yang sama, jadi tema/ilustrasinya boleh beda-beda — prompt tetap sama.

Ini **berbeda** dari `PANDUAN-PROMPT.md` (itu untuk landing page **jualan produk**).
Halaman bio = foto profil + nama + bio singkat + daftar tombol tautan.

---

## 🧾 LANGKAH 1 — Siapkan data Anda

```
[HALAMAN]
- Judul halaman (tab browser) :
- Deskripsi singkat (1 kalimat, untuk hasil pencarian) :

[PROFIL]
- Nama tampilan : (bebas — "@username" ATAU nama biasa, boleh emoji)
- Bio singkat   : (1-2 kalimat, boleh emoji)

[ASET — file yang Anda upload sendiri ke folder yang sama]
- Nama file foto profil : (mis. profil.jpg)
- Nama file favicon     : (mis. favicon.png — opsional)

[TAUTAN — tambah sebanyak yang diinginkan]
- Tautan 1 : judul | keterangan singkat | URL | teks badge (opsional)
- Tautan 2 : judul | keterangan singkat | URL
- Tautan 3 : judul | keterangan singkat | URL
- Tautan 4 : …

[SOSIAL MEDIA] (tulis "hapus" bila tak dipakai)
- Instagram :
- TikTok    :
- YouTube   :
```

---

## 📋 LANGKAH 2 — MEGA-PROMPT (lampirkan `index.html`, lalu tempel ini)

```text
Kamu adalah editor HTML profesional. Saya melampirkan file index.html — sebuah halaman
"link in bio" yang berisi ilustrasi SVG dan animasi buatan tangan.

TUGASMU: isi teks, tautan, dan nama file aset sesuai DATA SAYA di bawah. Selain itu,
jangan ubah apa pun.

ATURAN EMAS (WAJIB DIPATUHI):
1. HANYA ubah teks yang didahului komentar <!-- AI INSTRUCTION: ... --> dan atribut
   src="" / href="" yang ditandai <!-- [[ ... ]] -->. Patuhi batas panjang yang tertulis.
2. DILARANG KERAS menyentuh: seluruh isi <style>, seluruh isi <script>, semua elemen
   <svg> beserta <path>/<clipPath>/<defs>/koordinatnya, serta semua class, id, dan
   struktur HTML. Ini mencakup SEMUA ilustrasi dekoratif dan animasinya, apa pun temanya.
   Jangan "merapikan", "menyederhanakan", "memperbaiki", atau menulis ulang kode —
   termasuk bila menurutmu ada yang bisa dioptimalkan.
3. JANGAN HAPUS SATU BARIS PUN di dalam blok :root maupun blok html "JARING PENGAMAN".
   Salin keduanya PERSIS seperti aslinya, baris demi baris, termasuk baris yang tampak
   tidak terpakai. Menghapus satu variabel warna saja bisa membuat seluruh teks hilang.
4. JANGAN menambah framework, CDN, library, font, atau file eksternal apa pun.
5. MENAMBAH TAUTAN: duplikat seluruh blok tombol tautan yang sudah ada, lalu ganti
   teksnya saja. Jangan mengubah nama class. MENGHAPUS TAUTAN: hapus satu blok tombol
   secara utuh. Jika ada kelas penanda "tombol unggulan", biarkan hanya pada satu tombol.
6. JIKA ADA badge/label kecil pada tombol: ganti teksnya, atau hapus elemen badge itu
   secara utuh bila tidak dipakai.
7. JIKA ADA ikon sosial media: hanya ganti href-nya. Untuk yang tidak dipakai, hapus
   seluruh elemen <a> ikon tersebut — JANGAN mengubah isi <svg> ikonnya.
8. Isi nama file foto profil dan favicon sesuai data saya (file-nya saya upload sendiri).
9. Kembalikan SELURUH isi file index.html yang sudah terisi, utuh dan siap disimpan.

DATA SAYA:
[TEMPEL HASIL LANGKAH 1 DI SINI]
```

---

## 🎨 (Opsional) Ganti tema warna & font — MINTA TERPISAH

Jangan digabung dengan prompt di atas. Lampirkan `index.html`, lalu:

```text
Ubah tema visual index.html ini. Kamu HANYA boleh menyentuh:
(a) blok CSS variables di dalam :root (bagian "PENGATURAN USER"), dan
(b) baris <link> Google Fonts di <head> JIKA saya mengganti font.
Jangan ubah kode lain — termasuk semua <svg>, animasi, dan struktur HTML.

Tema saya:
- Warna utama/aksen :
- Nuansa latar      :
- Karakter font     :

Kembalikan SELURUH isi file index.html yang sudah diperbarui, utuh & siap disimpan.
```

---

## ✅ Setelah menerima hasil

1. Simpan hasil AI menimpa `index.html`.
2. Upload aset (foto profil, favicon) ke folder yang sama.
3. Buka di HP & desktop — pastikan ilustrasi & animasi masih utuh.
4. Klik semua tombol tautan, pastikan mengarah ke URL yang benar.

> ⚠️ **Aturan No. 2 paling krusial.** AI sering "berinisiatif" merapikan kode SVG dan
> justru merusak ilustrasi/animasinya. Jangan hapus aturan itu dari prompt.
