# 🤖 PANDUAN PROMPT — Cara Menyuruh AI Mengisi Landing Page

File ini berisi prompt **siap salin-tempel** untuk menyuruh AI (Claude, ChatGPT,
Gemini, dll) mengisi copywriting `index.html` Anda secara otomatis.

Alurnya: **Isi brief → tempel prompt + isi file `index.html` → terima hasil.**

---

## 🧾 LANGKAH 1 — Isi "Brief" Bisnis Anda

Lengkapi data di bawah ini dulu. Ini "bahan bakar" agar hasil AI tidak ngawur.

```
- Nama Produk/Layanan   :
- Jenis produk          : (ebook / fisik / software / kelas / jasa)
- Target market spesifik : (mis. "ibu rumah tangga sibuk", "mahasiswa IT")
- Masalah utama yang dipecahkan :
- 3–4 fitur / isi utama produk  :
- Keunggulan dibanding lain     :
- Harga jual            :
- Harga coret (opsional):
- Garansi (jika ada)    :
- Alasan beli sekarang / urgensi (jika ada) :
- Nada bahasa           : (santai / profesional / semangat / mewah)
```

> ⚠️ **Testimoni JANGAN dikarang oleh AI.** Isi sendiri dengan testimoni asli
> pelanggan Anda. Etika bisnis + rawan komplain.

---

## 📋 LANGKAH 2 — Prompt Utama (Isi Semua Copywriting)

Salin prompt di bawah, ganti bagian `[...]`, lalu tempel **beserta seluruh isi
file `index.html`**.

```text
Bertindaklah sebagai copywriter direct-response profesional berbahasa Indonesia.

Saya punya template landing page HTML "AI-Ready". Di dalamnya ada banyak komentar
penanda <!-- AI INSTRUCTION: ... -->. Tugas Anda: ISI teks tepat SETELAH setiap
komentar itu sesuai instruksinya.

ATURAN KETAT:
1. HANYA ubah teks yang ditandai AI INSTRUCTION dan teks placeholder di dekatnya.
2. JANGAN mengubah struktur HTML, tag, class Tailwind, CSS, atau JavaScript.
3. JANGAN menghapus komentar AI INSTRUCTION (biarkan agar bisa diedit ulang nanti).
4. JANGAN mengarang testimoni. Section testimoni memakai GAMBAR screenshot asli —
   cukup biarkan slot gambarnya, jangan menulis kutipan/nama palsu.
   Untuk LOGO di navbar: pakai SALAH SATU saja, logo (img) ATAU teks brand — jangan keduanya.
5. Pertahankan gaya persuasif, ringkas, dan berorientasi manfaat (benefit-driven).
6. Ikuti batasan panjang yang tertulis di tiap instruksi (mis. "maks 8 kata").
7. Kembalikan SELURUH file HTML yang sudah terisi, utuh, siap disimpan ulang.

BRIEF BISNIS SAYA:
[TEMPEL HASIL LANGKAH 1 DI SINI]

Berikut file index.html yang harus diisi:
[TEMPEL SELURUH ISI index.html DI SINI]
```

---

## 🎨 LANGKAH 3 (Opsional) — Ganti Tema Warna & Font

```text
Pada file HTML ini, ubah HANYA blok CSS variables di dalam :root (bagian
"PENGATURAN USER"). Jangan sentuh kode lain.

Permintaan tema saya:
- Warna utama / tombol : [mis. hijau emerald / biru / ungu]
- Nuansa latar         : [mis. hitam pekat / navy gelap / abu gelap]
- Karakter font        : [mis. tegas & modern / elegan / santai]
- Bentuk tombol        : [kotak tegas / agak membulat / bulat penuh]

Pilihkan kode HEX yang harmonis dan nama Google Font yang sesuai, lalu kembalikan
blok :root yang sudah diperbarui. Jika mengganti font, ingatkan saya untuk
memperbarui <link> Google Fonts di <head>.
```

---

## ✍️ LANGKAH 4 (Opsional) — Edit Satu Bagian Saja

Kalau cuma mau memperbaiki satu section (mis. FAQ), tak perlu kirim semua:

```text
Tolong tulis ulang HANYA bagian ini agar lebih persuasif untuk [produk saya].
Pertahankan struktur HTML & komentar AI INSTRUCTION, ganti teksnya saja:

[TEMPEL POTONGAN <section> YANG MAU DIEDIT]
```

---

## ✅ Setelah Menerima Hasil

1. Simpan hasil AI menimpa `index.html` (atau copy-paste bagian yang berubah).
2. Buka di browser untuk cek.
3. Ganti aset & link manual — lihat `CHECKLIST-ASET.md`.
4. Belum pas? Ulangi dengan permintaan revisi spesifik ("buat headline lebih
   berani", "tambahkan angka di value proposition", dst).

Selamat! Halaman Anda kini terasa custom tanpa harus menulis kode. 🚀
