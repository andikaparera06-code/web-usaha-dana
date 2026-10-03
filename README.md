# Mitra Usaha Coffee

Aplikasi pemesanan coffee shop berbasis QR Code dengan Next.js, Laravel 12, dan MySQL XAMPP. Laravel 12 dipilih agar cocok dengan PHP 8.2 pada XAMPP di mesin pengembangan ini.

## Persiapan database

1. Buka XAMPP Control Panel lalu jalankan **MySQL**.
2. Buat database bernama `mitra_usaha` di phpMyAdmin, dengan collation `utf8mb4_unicode_ci`.
3. Pastikan `backend/.env` memakai koneksi MySQL XAMPP. Konfigurasi bawaan memakai `127.0.0.1:3306`, user `root`, dan password kosong.

## Menjalankan aplikasi

Jalankan setiap perintah dari terminal terpisah.

Terminal backend:

```powershell
cd backend
php artisan migrate --seed
php artisan serve --host 127.0.0.1 --port 8000
```

Terminal frontend:

```powershell
cd frontend
npm.cmd run dev
```

Buka `http://localhost:3000`. URL meja mengikuti pola `http://localhost:3000/?meja=05`.

## Fitur

- Menu dari MySQL dengan kategori, pencarian, harga, dan ketersediaan.
- Keranjang per meja, catatan pelanggan, total tervalidasi server, dan pemesanan.
- Antrean barista dengan status menunggu, diproses, siap diambil, dan selesai.
- Pengelolaan menu, QR untuk meja, konfirmasi pembayaran, laporan, dan ekspor CSV.
- Migration dan seeder untuk 12 meja serta menu contoh.

Data menu dan transaksi tersimpan di MySQL. Gambar menu dan gambar QR dihasilkan melalui layanan eksternal sehingga perlu koneksi internet. Endpoint admin saat ini belum memakai autentikasi; tambahkan login/otorisasi sebelum aplikasi dipakai di jaringan publik.
