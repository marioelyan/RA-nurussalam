# Website Profil RA Nurussalam — Kerangka + Draf Beranda

Status: **Tahap 3 dari spek** — palet + layout Beranda disetujui Mario pada 2026-11-03; semua 11 halaman sudah dibangun penuh di staging lokal (struktur lengkap per spek, isi masih berpenanda menunggu konten asli RA). Ini staging lokal di folder kerja Imam, bukan deploy — go-live menunggu keputusan Mario tentang domain/hosting dan persetujuan final (tahap 6 spek).

Spek: "Spesifikasi Website Profil RA Nurussalam", disetujui Mario 2026-11-03, diterima via email Juleha 2026-11-03.

## Usulan palet warna (1 palet, untuk persetujuan Mario)

- **Hijau zamrud `#0F766E`** — warna utama (header, tombol, judul). Nuansa Islami, tenang, dipercaya orang tua.
- **Kuning mentega `#F5B942`** — aksen ceria anak (penanda, sorotan), dipakai seperlunya.
- **Krem hangat `#FFF8EC`** — latar seksi selang-seling, lembut dan ramah.
- Teks: `#22312C` di atas putih/krem (kontras terbaca di HP).

Font: tumpukan font sistem (Segoe UI / system-ui / Arial) — tanpa unduhan font, loading cepat.

## Struktur

- `index.html` — Beranda (draf penuh sesuai spek bagian 3)
- `profil.html`, `legalitas.html`, `program.html`, `fasilitas.html`, `pendidik.html`, `organisasi.html`, `dokumen.html`, `galeri.html`, `ppdb.html`, `kontak.html` — kerangka halaman
- `assets/css/style.css` — gaya bersama, mobile-first, breakpoint 720px
- `assets/js/main.js` — menu mobile + tahun footer

Tanpa login, tanpa database (v1, sesuai spek bagian 4). Konten diubah lewat file.

## Hosting (keputusan Mario, 2026-11-03)

- Website akan di-host di **GitHub Pages**. Semua tautan dan aset memakai path relatif, dan ada file `.nojekyll` agar GitHub Pages menyajikan file apa adanya.
- Pengunggahan/deploy sementara menjadi urusan **Juleha**. Imam tidak deploy sendiri — Imam menyiapkan folder ini (atau ZIP-nya) sebagai paket siap unggah.
- Konten pihak RA: Mario sendiri yang mengatur penyediaannya; sampai konten tiba, halaman tetap berpenanda.

## Aturan konten (dari spek)

- Semua isi yang belum diberikan pihak RA ditandai `[MENUNGGU KONTEN RA]`.
- Tidak ada profil, angka, program, atau status legalitas yang dikarang.
- Status izin operasional ditulis apa adanya: **dalam pengajuan (pengajuan baru)** — jawaban Mario 2026-11-03. Tenggat IJOB masih lama; daftar syarat Kankemenag tidak diperlukan.
- Foto: tidak memakai foto stok di kerangka ini; semua slot foto adalah penanda menunggu foto asli RA (dengan izin).
- Dilarang tampil: ijazah, NIP/NIK, data siswa.

## Cara mengubah konten nanti

1. Cari teks `[MENUNGGU KONTEN RA ...]` di file HTML halaman terkait, ganti dengan konten asli RA.
2. Foto asli ditaruh di `assets/img/` (buat foldernya saat foto pertama masuk), lalu ganti blok `.photo-placeholder` dengan `<img>` yang menunjuk ke file itu.
3. Jalankan pengujian ulang sebelum naik staging/live.
