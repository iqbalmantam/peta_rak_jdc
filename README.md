# Peta Kapasitas Rak JDC

Denah interaktif kapasitas rak gudang JDC. Data berasal dari `Master_location_JDC.xlsx` (sheet `EXISTING` dan `plan penambahan`).

Aplikasi ini satu file HTML (`index.html`). Tidak perlu server atau instalasi: buka file di browser.

## Cara membaca peta

- Tiap kotak adalah satu posisi rak. Angka di dalam kotak adalah jumlah **level** rak (7 berarti rak 7 level).
- **PP** dihitung dari jumlah level semua kotak.
- Blok rak: Row A (A01–A14), Row B (B01–B14), Row C (C01–C10), Row D (D01–D09), ditambah area Depan dan Samping.

## Mode tampilan

| Mode | Fungsi |
|---|---|
| Existing | Level rak kondisi sekarang |
| Rencana | Level rak setelah penambahan |
| Selisih | Rak baru, level naik, level turun, dan yang tidak berubah |
| Customer | Warna per customer; klik nama customer untuk memfilter, klik **Semua customer** untuk kembali |

Fitur lain: filter blok, cari kode rak (misalnya `C04`), zoom, tabel kapasitas per rak dan per customer, serta salin ringkasan sebagai CSV.

## Memakai file Excel sendiri

Klik **Muat file Excel** atau seret file `.xlsx` ke halaman. Pilih sheet Existing dan sheet Rencana kalau file punya lebih dari satu sheet.

Aplikasi membaca kode rak (A01, B01, C01, D01, dan seterusnya) di baris 11 dan 49, lalu angka level di baris 15–88. Tata letak file harus sama dengan `Master_location_JDC.xlsx`.

Mode Customer hanya tersedia untuk data contoh, karena nama customer di Excel berupa kotak teks yang tidak terbaca saat file diunggah.

## Catatan data

- Total existing 20.013 PP; total rencana 23.297 PP (termasuk kolom Samping 420 PP).
- Batas customer diambil dari posisi kotak teks di Excel, jadi kotak di tepi blok bisa tergeser satu kolom.
- Ada 328 kotak rak baru (area Depan dan bagian atas blok C dan D) yang belum punya customer.

## Menjalankan

Buka `index.html` di browser. Font dan pembaca Excel dimuat dari internet, jadi fitur unggah Excel memerlukan koneksi.

Untuk membuka lewat link: **Settings → Pages**, pilih branch `main` dan folder `/ (root)`.
