# 🎬 SPOTLIGHT — AI-Ready Landing Page Template

Template landing page **1 produk** bertema gelap (dark mode) yang terinspirasi
desain Netflix. Cocok untuk menjual **apa saja**: ebook, produk fisik,
software/SaaS, kelas online, atau jasa.

Dibuat dengan konsep **AI-Ready**: Anda tidak perlu jago ngoding. Cukup buka
file, minta bantuan AI (Claude, ChatGPT, Gemini, dll) untuk mengisi teksnya,
ganti beberapa gambar & link, lalu **online**.

---

## 📦 Isi Paket

| File | Fungsi |
|------|--------|
| `index.html` | Halaman landing page lengkap (HTML + CSS + JS jadi satu file). |
| `README.md` | Panduan yang sedang Anda baca. |
| `PANDUAN-PROMPT.md` | Kumpulan prompt siap-pakai untuk menyuruh AI mengisi copywriting. |
| `CHECKLIST-ASET.md` | Daftar bahan (logo, gambar, link) yang perlu Anda siapkan. |

---

## 🚀 Cara Pakai (3 Langkah)

### 1. Lihat dulu tampilannya
Klik dua kali `index.html` — akan terbuka di browser. Semua teks masih berupa
panduan (mis. *"Tulis Janji Terbesar Produk Anda di Sini"*). Itu normal.

### 2. Isi teks dengan bantuan AI
Buka `PANDUAN-PROMPT.md`, salin prompt di sana, tempel ke AI bersama isi file
`index.html`, dan isi **brief bisnis** Anda. AI akan mengembalikan `index.html`
yang sudah terisi copywriting — **tanpa merusak desain**.

> Kenapa aman? Setiap teks diberi komentar `<!-- AI INSTRUCTION: ... -->`
> sebagai rambu untuk AI, jadi AI tahu persis bagian mana yang boleh diubah.

### 3. Ganti aset & link
Cari penanda `[[ ... ]]` di dalam `index.html` untuk mengganti:
- **Logo** (`[[ LOGO ]]`)
- **Gambar/mockup produk** (`[[ GAMBAR PRODUK ]]`)
- **Link Checkout / Order** (`[[ LINK CHECKOUT ]]`) — ganti semua `href="#"` pada tombol CTA
- **Nomor WhatsApp** (`[[ WHATSAPP ]]`)
- **Link sosial media & legal** (`[[ LINK SOSIAL... ]]`)

Lihat daftar lengkap di `CHECKLIST-ASET.md`.

---

## 🎨 Mengganti Warna & Font (Tanpa Ngoding)

Semua pengaturan tampilan ada di **satu tempat**: blok `:root` di bagian atas
`<style>` dalam `index.html`. Anda cukup ubah nilainya.

```css
:root {
  --color-primary:  #E50914;   /* Warna tombol (default merah)  */
  --color-bg:       #000000;   /* Latar utama                   */
  --color-text:     #ffffff;   /* Warna teks                    */
  --font-heading:   'Inter', sans-serif;   /* Font judul        */
  --radius-button:  10px;      /* 999px = tombol bulat penuh    */
}
```

**Malas cari-cari?** Kirim blok itu ke AI:
> *"Ubah warna utama jadi hijau emerald, latar jadi navy gelap, dan font judul
> yang cocok untuk brand kopi."*

Seluruh website otomatis berubah tema — **layout tetap utuh**.

---

## 🧩 Struktur Section (Modular — Bongkar Pasang)

Urutan section sudah disusun mengikuti anatomi copywriting *high-converting*:

1. **Hero** — Judul, pengantar, CTA
2. **Value Proposition** — momen "aha!"
3. **Features** — 3–4 kartu keunggulan
4. **CTA tengah**
5. **Testimonial** — bukti sosial (isi data **asli**)
6. **Cocok untuk siapa** — checklist
7. **FAQ** — accordion
8. **CTA akhir + N.B** — urgensi & penutup

Tiap `<section>` **mandiri**. Tidak butuh testimoni karena produk baru rilis?
Hapus saja blok `<!-- 4. TESTIMONIAL -->` — layout tidak akan rusak. Ingin
tukar urutan? Pindahkan blok `<section>` nya.

---

## ⚠️ Yang Sebaiknya TIDAK Diubah (bila tak paham koding)

Agar konversi tetap terjaga, hindari mengubah:
- Posisi grid / flexbox antar elemen
- Jarak (margin & padding) bawaan
- Class Tailwind pada layout

Ubah **warna, font, teks, gambar, dan link** — itu sudah lebih dari cukup untuk
membuat halaman ini terasa custom milik Anda sendiri.

---

## 🛠️ Teknologi

- **HTML5** + **Tailwind CSS** (via CDN — tanpa proses build)
- **Vanilla JavaScript** (accordion FAQ + animasi)
- **CSS Variables** untuk tema
- 100% statis — bisa di-hosting gratis di GitHub Pages, Netlify, Vercel, atau
  hosting biasa. Cukup upload `index.html`.

Butuh internet aktif saat halaman dibuka (untuk memuat Tailwind & font dari CDN).

---

Selamat berjualan! 🚀
