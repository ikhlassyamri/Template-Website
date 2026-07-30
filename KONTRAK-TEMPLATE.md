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

## Cara menambah template baru (3, 4, 5, …)

- Buat folder `template-N-namareferensi/` berisi `index.html` + `README.md` singkat.
- Bangun desain sesuai referensi, TAPI patuhi 12 aturan di atas.
- README folder cukup menunjuk ke `PANDUAN-PROMPT.md` universal (jangan bikin prompt baru).
- Uji: buka di HP & desktop, pastikan tanpa horizontal-overflow.

Selama kontrak ini dipatuhi, pembeli cukup pakai **1 prompt + 1 data brief** untuk template mana pun.
