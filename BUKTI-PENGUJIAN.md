# Bukti Pengujian — Kerangka + Draf Beranda RA Nurussalam

Tanggal: 2026-11-03 (jam kerja)
Penguji: Imam
Perintah uji: `python3 test_site.py` (skrip pengujian otomatis di folder kerja Imam)

## Hasil pengujian otomatis: 79/79 lolos, 0 gagal

Kelompok pengujian:

1. **Kelengkapan halaman (11/11)** — index, profil, legalitas, program, fasilitas, pendidik, organisasi, dokumen, galeri, ppdb, kontak: semua ada.
2. **Struktur & SEO dasar (per halaman)** — doctype + `lang="id"`, meta viewport untuk mobile, judul + meta description, struktur tag HTML seimbang (parser): lolos di semua halaman.
3. **Penanda konten** — setiap halaman memuat penanda `[MENUNGGU KONTEN RA]`: lolos. Tidak ada lorem ipsum, tidak ada foto stok (Unsplash/Pexels/Picsum), dan belum ada tag `<img>` sebelum foto asli RA masuk.
4. **Tautan** — semua tautan internal antarhalaman valid (target file ada).
5. **Fitur wajib v1 (yang dapat dicek pada kerangka)** — Beranda memuat tombol WhatsApp + tombol Cara Mendaftar, 3 keunggulan, dan cuplikan kegiatan; tombol WhatsApp ada di semua halaman (header + tombol melayang); halaman Legalitas menulis status "dalam pengajuan" apa adanya; halaman Dokumen mencantumkan larangan ijazah/NIP/NIK/data siswa; halaman Pendidik menegaskan tanpa data pribadi.
6. **CSS/JS** — variabel palet sesuai usulan (hijau `#0F766E`, kuning `#F5B942`, krem `#FFF8EC`); breakpoint responsif `@media (max-width: 720px)` ada; JS menu mobile terpasang.

## Uji asap HTTP (server statis lokal)

- `GET /` → 200
- `GET /legalitas.html` → 200
- `GET /assets/css/style.css` → 200

## Pengujian Tahap 3 (2026-11-03, setelah persetujuan palet + layout Beranda)

- Mario menyetujui palet + layout draf Beranda pada 2026-11-03.
- Semua halaman dibangun penuh di staging lokal dengan struktur lengkap per spek (Profil: sejarah/visi/misi/nilai/pengelola; Program: program unggulan, harian/mingguan, ekstrakurikuler, kurikulum, tabel jadwal; Pendidik & Legalitas: tabel data; PPDB: syarat + alur langkah; Kontak: kartu kontak + penanda peta; Galeri: 6 penanda foto).
- Pengujian otomatis diperbarui dengan 17 cek tahap 3 (jumlah section per halaman, tabel, alur PPDB, penanda peta, jumlah penanda foto galeri).
- **Hasil: 96/96 pengujian lolos, 0 gagal.**
- Uji asap HTTP server statis lokal: kesebelas halaman (`/`, profil, legalitas, program, fasilitas, pendidik, organisasi, dokumen, galeri, ppdb, kontak) semuanya balas **200**.

## Kesiapan GitHub Pages (2026-11-03, keputusan Mario)

- Mario memutuskan hosting di GitHub Pages, pengunggahan sementara diurus Juleha; konten RA diatur Mario sendiri.
- Ditambahkan file `.nojekyll`; ditambah 2 cek otomatis: `.nojekyll` ada, dan tidak ada path absolut pada href/src (semua relatif agar aman di subpath GitHub Pages).
- **Hasil pengujian terbaru: 98/98 lolos, 0 gagal.** Paket ZIP diperbarui (file preview satu-file tidak disertakan dalam paket unggah).

## Belum diuji (menunggu tahap berikutnya)

- Tampilan visual final di HP/laptop dengan konten & foto asli RA (saat ini masih penanda).
- Fungsi tombol WhatsApp ke nomor asli (nomor resmi RA belum diberikan).
- Peta Google Maps (alamat resmi RA belum diberikan).
- Verifikasi silang data dengan berkas IJOB (checkpoint tahap 5 spek) — menunggu konten dan berkas.
