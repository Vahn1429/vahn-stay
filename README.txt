# Keuangan Vahn Cell

Aplikasi pembukuan harian UMKM berbasis HTML, CSS, dan JavaScript.

## Isi folder
- `index.html` — aplikasi utama
- `manifest.webmanifest` — identitas aplikasi untuk Android/PWA
- `sw.js` — cache agar aplikasi dapat dibuka offline setelah pertama kali dimuat melalui HTTPS
- `assets/` — ikon aplikasi PNG

## Menjalankan di Android
1. Ekstrak ZIP ini terlebih dahulu (jangan membuka file HTML dari dalam ZIP). Pastikan folder `Vahn-Cell-Keuangan` berisi `index.html`, `manifest.webmanifest`, `sw.js`, dan folder `assets`.
2. Untuk melihat tampilan awal, buka `index.html` di Acode.
3. Untuk pemasangan sebagai aplikasi dan fitur offline PWA, unggah SEMUA isi folder ini ke repository GitHub (bukan hanya `index.html`), lalu aktifkan GitHub Pages.
4. Buka alamat HTTPS GitHub Pages di Chrome Android. Pilih Pasang Aplikasi atau menu Chrome > Tambahkan ke layar utama.
5. Buka aplikasi sekali saat online agar service worker menyimpan file aplikasi. Setelah itu aplikasi dapat dibuka offline.

## Catatan data
- Catatan disimpan otomatis di localStorage browser/perangkat.
- Gunakan tombol `Backup Data` secara berkala untuk mengunduh cadangan JSON.
- `Simpan & Kunci` mengunci catatan tanggal tersebut. Tombol `Buka Kunci` tersedia jika perlu koreksi.
- `Salin Kemarin` hanya menyalin nama daftar dari kemarin ke tanggal aktif; semua nominal diatur kembali menjadi Rp0 dan alasan dikosongkan. Isi tanggal aktif diganti setelah konfirmasi.
- Kolom 1 dan 2 masing-masing memiliki daftar awal bank BRI, Mandiri, BCA, BNI, BSI, Seabank, dan Superbank. Keduanya dapat ditambah atau dihapus secara terpisah.
- Data browser tidak otomatis berpindah ke HP lain. Simpan backup secara berkala.

## Rumus
Total Modal = Total Hari Ini - Tabungan Terpakai - Titipan Terpakai.
Selisih = Total Modal hari ini - Total Modal tanggal sebelumnya.

- Jika kolom Penyebab Selisih tidak bisa diketik, periksa apakah tanggal tersebut terkunci. Tekan tombol `Buka Kunci` atau `Buka Kunci untuk Mengisi` pada kolom alasan.

Pembaruan: nominal pada kolom rincian otomatis memakai titik pemisah ribuan (contoh 100.000). Kalender membatasi pilihan sampai tanggal hari ini; tanggal mendatang tidak dapat dipilih. Navigasi tombol hari sebelumnya/berikutnya telah dihapus.
