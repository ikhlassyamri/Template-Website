# 🤖 PANDUAN PROMPT — Isi Landing Page Otomatis dengan AI

Konsep template ini: **Produk + `index.html` = Copywriting relevan otomatis.**

Anda tidak perlu menyusun copywriting sendiri. Cukup **upload file produk** (mis.
ebook PDF) + **`index.html`**, lalu AI (Claude/ChatGPT/Gemini) akan:
1. Membaca produk Anda untuk paham isi & manfaatnya.
2. Membaca petunjuk `<!-- AI INSTRUCTION -->` di dalam `index.html`.
3. Mengisi semua teks sesuai struktur high-converting template — tanpa merusak desain.

---

## 🧾 LANGKAH 1 — Siapkan "Brief" (hal yang AI tidak bisa tebak dari file)

AI bisa baca isi produk, tapi **tidak tahu** harga, link, dan aset Anda. Isi ini dulu:

```
- Nama produk            :
- Target market spesifik : (mis. "mahasiswa yang ingin cuan tambahan")
- Gaya bahasa            : (santai / semi-formal / formal — panggilan "saya–kamu" / "saya–Anda")
- Harga normal (coret)   : Rp
- Harga spesial          : Rp
- Garansi (jika ada)     :
- Urgensi/alasan beli sekarang (jika ada) :

[LINK]
- Link Checkout (semua tombol CTA) :
- Instagram / TikTok / YouTube     :

[WHATSAPP]
- Nomor (format 62...)   :
- Pesan awal chat        : (mis. "Halo, saya mau beli [produk]")

[NAMA FILE ASET yang akan Anda upload ke repo]
- Logo/profil            : logo.png   (kosongkan jika mau pakai teks brand saja)
- Gambar produk          : produk.png
- Screenshot testimoni   : testi1.jpg, testi2.jpg, testi3.jpg
```

---

## 📋 LANGKAH 2 — MEGA-PROMPT (upload produk + index.html, lalu tempel ini)

> Lampirkan **file produk** (ebook/PDF/dll) **dan** file **`index.html`**, lalu tempel prompt di bawah.

```text
Kamu adalah Copywriter direct-response + editor HTML profesional berbahasa Indonesia.

Saya melampirkan DUA hal:
1. FILE PRODUK saya (untuk kamu pahami isinya).
2. File index.html — template landing page "AI-Ready".

TUGASMU:
Analisa file produk saya, lalu ISI semua teks di index.html tepat SETELAH setiap
komentar <!-- AI INSTRUCTION: ... --> sesuai instruksinya, agar menjadi landing page
yang menjual untuk produk saya.

ATURAN EMAS (WAJIB PATUHI):
1. IKUTI KOMENTAR: sumber kebenaran struktur ada di komentar AI INSTRUCTION di dalam
   index.html. Hormati batas panjang yang tertulis (mis. "maks 8 kata").
2. JANGAN UBAH DESAIN: dilarang mengubah struktur HTML, tag, class, CSS/<style>, atau
   JavaScript. Hanya ganti teks dan atribut (src="", href=""). Jangan tambah framework.
3. TESTIMONI = GAMBAR: bagian testimoni memakai screenshot asli. Cukup ganti src gambar
   dengan nama file testimoni saya. DILARANG KERAS menulis/mengarang kutipan & nama.
4. LOGO PILIH SATU: untuk logo di navbar, pilih SALAH SATU — ganti teks brand ATAU
   aktifkan <img>. JANGAN dua-duanya (biar tidak dobel/ikon rusak).
5. DATA NYATA SAJA: bagian angka statistik (mis. jumlah pembeli/rating) HANYA diisi bila
   saya beri data nyata di brief. Jika tidak ada, HAPUS blok grid statistik itu.
6. LINK CTA: HANYA tombol CTA TERAKHIR (di bagian harga) yang diisi link checkout asli
   pada href. Tombol CTA lain (navbar, hero, tengah) sudah di-set href="#cta-akhir" agar
   scroll ke harga — JANGAN diubah jadi link checkout. Ganti juga src gambar produk, link
   sosmed, dan link WhatsApp (format wa.me/62...?text=... dengan pesan ter-encode).
7. Kembalikan SELURUH file index.html yang sudah terisi, utuh & siap simpan.

BRIEF SAYA:
[TEMPEL HASIL LANGKAH 1 DI SINI]
```

Selesai — simpan hasilnya sebagai `index.html`, lalu upload beserta aset (logo, gambar
produk, screenshot testimoni) ke repo/hosting Anda.

---

## 🎨 (Opsional) Ganti Tema Warna & Font

```text
Pada index.html ini, ubah HANYA blok CSS variables di dalam :root (bagian "PENGATURAN
USER"). Jangan sentuh kode lain.

Tema saya:
- Warna utama/tombol : [mis. hijau emerald]
- Nuansa latar       : [mis. hitam pekat / navy gelap]
- Karakter font      : [mis. tegas modern / elegan / santai]
- Bentuk tombol      : [kotak / agak membulat / bulat penuh]

Pilihkan kode HEX harmonis + nama Google Font yang cocok, kembalikan blok :root yang
sudah diperbarui. Jika ganti font, ingatkan saya memperbarui <link> Google Fonts di <head>.
```

---

## ✍️ (Opsional) Revisi Satu Bagian Saja

```text
Tolong tulis ulang HANYA bagian ini agar lebih persuasif untuk [produk saya].
Pertahankan struktur HTML & komentar AI INSTRUCTION, ganti teksnya saja:

[TEMPEL POTONGAN <section> YANG MAU DIEDIT]
```

---

## ✅ Setelah Menerima Hasil

1. Simpan hasil AI menimpa `index.html`.
2. Upload aset (logo, produk, screenshot testimoni) ke folder yang sama.
3. Buka di browser (HP & desktop) untuk cek.
4. Klik semua tombol CTA & WhatsApp — pastikan link benar.
5. Belum pas? Minta revisi spesifik ("headline lebih berani", dst).

Lihat juga `CHECKLIST-ASET.md` untuk daftar bahan yang perlu disiapkan. 🚀
