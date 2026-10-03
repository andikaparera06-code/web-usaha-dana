# Analisis Perancangan Sistem Mitra Usaha Coffee Shop Berbasis QR Code

## 1. Latar Belakang

Perkembangan teknologi informasi memberikan kemudahan dalam berbagai aktivitas bisnis, termasuk pada usaha coffee shop. Proses pemesanan yang masih dilakukan secara manual, seperti pelanggan memanggil pelayan untuk memesan menu, dapat menyebabkan antrean, kesalahan pencatatan pesanan, serta membutuhkan waktu lebih lama.

Untuk mengatasi masalah tersebut, dirancang sebuah **sistem pemesanan pada Mitra Usaha Coffee Shop menggunakan QR Code**. Pelanggan cukup melakukan scan QR Code yang tersedia pada meja menggunakan smartphone. Setelah QR Code dipindai, pelanggan akan diarahkan ke halaman sistem yang menampilkan daftar menu. Pelanggan dapat memilih menu, menentukan jumlah pesanan, melihat total harga, kemudian mengirimkan pesanan secara langsung ke sistem.

Sistem ini diharapkan dapat membantu mempercepat proses pemesanan, mengurangi kesalahan pencatatan, dan memudahkan pihak coffee shop dalam mengelola pesanan.

---

## 2. Identifikasi Masalah

Beberapa permasalahan yang terdapat pada proses pemesanan secara manual antara lain:

1. Pelanggan harus menunggu pelayan untuk melakukan pemesanan.
2. Pencatatan pesanan masih berpotensi mengalami kesalahan.
3. Pelayan harus mencatat dan mengantarkan pesanan secara manual.
4. Pelanggan tidak dapat melihat informasi menu secara langsung melalui perangkatnya.
5. Proses pemesanan menjadi kurang efisien ketika coffee shop sedang ramai.
6. Pengelola kesulitan memantau pesanan yang sedang diproses apabila pencatatan masih dilakukan secara manual.

---

## 3. Rumusan Masalah

Berdasarkan permasalahan tersebut, rumusan masalahnya adalah:

> **Bagaimana merancang sistem pemesanan Mitra Usaha Coffee Shop berbasis QR Code yang dapat mempermudah pelanggan dalam melakukan pemesanan serta membantu pengelola dalam mengelola menu dan pesanan?**

---

## 4. Tujuan Sistem

Tujuan dari perancangan sistem ini adalah:

- Mempermudah pelanggan dalam melakukan pemesanan.
- Mengurangi waktu tunggu pelanggan.
- Mengurangi kesalahan dalam pencatatan pesanan.
- Membantu kasir atau admin mengelola pesanan.
- Menampilkan menu secara digital.
- Memudahkan pengelola dalam memperbarui informasi menu.
- Meningkatkan efisiensi proses pemesanan di coffee shop.

---

## 5. Analisis Sistem yang Berjalan

Pada sistem yang sedang berjalan, proses pemesanan dilakukan secara manual.

### Alur Sistem Lama

```text
Pelanggan datang
      ↓
Pelanggan memilih tempat
      ↓
Memanggil pelayan
      ↓
Pelayan memberikan/menjelaskan menu
      ↓
Pelanggan memilih menu
      ↓
Pelayan mencatat pesanan
      ↓
Pesanan diberikan ke bagian dapur/bar
      ↓
Pesanan dibuat
      ↓
Pesanan diberikan kepada pelanggan
      ↓
Pelanggan melakukan pembayaran
```

### Kekurangan Sistem Lama

- Membutuhkan tenaga pelayan untuk setiap pesanan.
- Terjadi antrean ketika banyak pelanggan datang.
- Risiko salah mencatat menu atau jumlah pesanan.
- Informasi menu tidak selalu diperbarui dengan cepat.
- Proses pemesanan relatif lebih lama.

---

## 6. Analisis Sistem yang Diusulkan

Sistem yang diusulkan menggunakan **QR Code pada setiap meja**. Setiap QR Code dapat mengandung identitas meja sehingga sistem dapat mengetahui dari meja mana pesanan berasal.

### Alur Sistem Baru

```text
Pelanggan datang
      ↓
Memilih meja
      ↓
Scan QR Code pada meja
      ↓
Sistem menampilkan halaman menu
      ↓
Pelanggan memilih menu
      ↓
Menentukan jumlah pesanan
      ↓
Memasukkan catatan (opsional)
      ↓
Melihat keranjang & total harga
      ↓
Konfirmasi pesanan
      ↓
Pesanan masuk ke dashboard admin/barista
      ↓
Pesanan diproses
      ↓
Status pesanan diperbarui
      ↓
Pesanan selesai
      ↓
Pelanggan menerima pesanan
      ↓
Pembayaran
```

---

## 7. Aktor Sistem

Sistem dapat memiliki beberapa aktor utama:

| Aktor | Peran |
|---|---|
| **Pelanggan** | Melihat menu dan melakukan pemesanan melalui QR Code |
| **Admin** | Mengelola menu, kategori, harga, dan data pesanan |
| **Kasir** | Mengelola pembayaran dan status transaksi |
| **Barista/Kitchen** | Melihat dan memproses pesanan |
| **Pemilik** | Melihat data dan laporan penjualan |

---

## 8. Fitur Sistem

### A. Fitur Pelanggan

Pelanggan dapat:

1. Scan QR Code.
2. Melihat menu.
3. Melihat kategori makanan/minuman.
4. Melihat foto dan harga menu.
5. Memilih menu.
6. Menentukan jumlah pesanan.
7. Menambahkan catatan pesanan.
8. Memasukkan pesanan ke keranjang.
9. Melihat total harga.
10. Mengirim pesanan.
11. Melihat status pesanan.

### Status Pesanan

```text
Pesanan diterima
      ↓
Sedang diproses
      ↓
Sedang dibuat
      ↓
Siap diambil/diantar
      ↓
Selesai
```

### B. Fitur Admin

Admin dapat:

- Login.
- Menambahkan menu.
- Mengubah menu.
- Menghapus menu.
- Mengatur harga.
- Menambahkan foto menu.
- Mengatur kategori menu.
- Melihat pesanan masuk.
- Mengubah status pesanan.
- Mengelola data meja.
- Membuat atau mencetak QR Code meja.

### C. Fitur Kasir

Kasir dapat:

- Melihat pesanan.
- Melihat total pembayaran.
- Mengonfirmasi pembayaran.
- Mengubah status pembayaran.
- Melihat riwayat transaksi.
- Membuat laporan transaksi.

### D. Fitur Barista/Kitchen

Barista dapat melihat:

```text
No. Pesanan : #001
Meja        : 05

Pesanan:
- Es Kopi Susu × 2
- Americano × 1
- Kentang Goreng × 1

Catatan:
- Es batu sedikit
```

Status pesanan dapat diubah menjadi:

**Menunggu → Diproses → Selesai**

---

## 9. Analisis Kebutuhan Fungsional

Kebutuhan fungsional adalah fungsi yang harus tersedia dalam sistem.

| No | Kebutuhan |
|---|---|
| 1 | Sistem dapat menampilkan menu |
| 2 | Sistem dapat membaca identitas meja dari QR Code |
| 3 | Pelanggan dapat memilih menu |
| 4 | Pelanggan dapat menentukan jumlah menu |
| 5 | Pelanggan dapat memasukkan catatan |
| 6 | Sistem dapat menghitung total harga |
| 7 | Pelanggan dapat melakukan konfirmasi pesanan |
| 8 | Admin dapat mengelola menu |
| 9 | Admin dapat mengelola meja |
| 10 | Admin dapat melihat pesanan |
| 11 | Barista dapat melihat pesanan |
| 12 | Sistem dapat mengubah status pesanan |
| 13 | Kasir dapat mengelola pembayaran |
| 14 | Sistem dapat menyimpan riwayat transaksi |
| 15 | Sistem dapat menghasilkan laporan penjualan |

---

## 10. Kebutuhan Non-Fungsional

| Kebutuhan | Penjelasan |
|---|---|
| **Keamanan** | Data admin harus dilindungi dengan login |
| **Kemudahan** | Sistem mudah digunakan oleh pelanggan |
| **Kecepatan** | Halaman menu dan pesanan dapat diakses dengan cepat |
| **Responsif** | Tampilan dapat digunakan melalui smartphone |
| **Ketersediaan** | Sistem dapat digunakan selama operasional coffee shop |
| **Keandalan** | Pesanan yang dikirim harus tersimpan dengan benar |
| **Usability** | Navigasi sederhana dan mudah dipahami |

---

## 11. Rancangan Database

Database dapat terdiri dari beberapa tabel utama.

### Tabel `users`

| Field | Keterangan |
|---|---|
| `id_user` | ID pengguna |
| `nama` | Nama pengguna |
| `username` | Username |
| `password` | Password |
| `role` | Admin/Kasir/Barista |

### Tabel `meja`

| Field | Keterangan |
|---|---|
| `id_meja` | ID meja |
| `nomor_meja` | Nomor meja |
| `qr_code` | Data QR Code |
| `status` | Tersedia/Digunakan |

### Tabel `menu`

| Field | Keterangan |
|---|---|
| `id_menu` | ID menu |
| `nama_menu` | Nama menu |
| `kategori` | Kategori menu |
| `harga` | Harga |
| `gambar` | Foto menu |
| `stok` | Jumlah stok |
| `status` | Tersedia/Habis |

### Tabel `pesanan`

| Field | Keterangan |
|---|---|
| `id_pesanan` | ID pesanan |
| `id_meja` | Meja pelanggan |
| `tanggal` | Waktu pemesanan |
| `total` | Total harga |
| `status` | Status pesanan |

### Tabel `detail_pesanan`

| Field | Keterangan |
|---|---|
| `id_detail` | ID detail |
| `id_pesanan` | ID pesanan |
| `id_menu` | Menu yang dipesan |
| `jumlah` | Jumlah |
| `harga` | Harga |
| `catatan` | Catatan pelanggan |
| `subtotal` | Total per menu |

### Tabel `pembayaran`

| Field | Keterangan |
|---|---|
| `id_pembayaran` | ID pembayaran |
| `id_pesanan` | ID pesanan |
| `total_bayar` | Jumlah pembayaran |
| `metode` | Cash/QRIS/dll |
| `status` | Belum/Lunas |
| `waktu_bayar` | Waktu pembayaran |

---

## 12. Relasi Database

Secara sederhana hubungan tabelnya:

```text
USERS
  │
  │ mengelola
  ↓
MENU

MEJA
  │
  │ memiliki
  ↓
PESANAN
  │
  │ memiliki
  ↓
DETAIL_PESANAN
  │
  │ mengambil data
  ↓
MENU

PESANAN
  │
  │ memiliki
  ↓
PEMBAYARAN
```

---

## 13. Use Case Sederhana

```text
                  SISTEM COFFEE SHOP

Pelanggan ────────┐
                  │
                  ├── Scan QR Code
                  ├── Lihat Menu
                  ├── Pilih Menu
                  ├── Buat Pesanan
                  ├── Konfirmasi Pesanan
                  └── Lihat Status Pesanan


Admin ────────────┐
                  ├── Login
                  ├── Kelola Menu
                  ├── Kelola Meja
                  ├── Kelola QR Code
                  └── Kelola Pesanan


Kasir ────────────┐
                  ├── Lihat Pesanan
                  ├── Konfirmasi Pembayaran
                  └── Lihat Transaksi


Barista ──────────┐
                  ├── Lihat Pesanan
                  ├── Proses Pesanan
                  └── Ubah Status Pesanan
```

---

## 14. Teknologi yang Dapat Digunakan

### Frontend

- HTML
- CSS
- JavaScript
- Bootstrap atau Tailwind CSS

### Backend

- PHP/Laravel, atau
- Node.js/Express

### Database

- MySQL

### QR Code

- QR Code Generator/Library QR Code

### Server

- XAMPP untuk pengembangan lokal
- Hosting/cloud server untuk sistem online

---

## 15. Contoh Rancangan Tampilan Sistem

### Halaman Pelanggan

```text
┌──────────────────────────────┐
│     MITRA USAHA COFFEE       │
│          Meja 05             │
├──────────────────────────────┤
│ 🔎 Cari menu...              │
├──────────────────────────────┤
│ [Kopi] [Non-Kopi] [Makanan]  │
├──────────────────────────────┤
│ ☕ Es Kopi Susu               │
│ Rp18.000                     │
│              [-] 1 [+]       │
├──────────────────────────────┤
│ ☕ Americano                  │
│ Rp15.000                     │
│              [-] 1 [+]       │
├──────────────────────────────┤
│ 🛒 Keranjang (2)             │
│ Total: Rp33.000              │
│                              │
│       [ PESAN SEKARANG ]     │
└──────────────────────────────┘
```

---

## 16. Kesimpulan

Sistem **Mitra Usaha Coffee Shop berbasis QR Code** dirancang untuk menggantikan proses pemesanan manual menjadi proses digital. Pelanggan cukup melakukan scan QR Code pada meja untuk mengakses menu dan melakukan pemesanan melalui smartphone.

Sistem ini mencakup **pengelolaan menu, QR Code meja, pemesanan, pengelolaan pesanan, pembayaran, dan laporan transaksi**. Dengan sistem tersebut, proses pemesanan dapat dilakukan secara lebih terstruktur dan data pesanan dapat langsung diteruskan kepada pihak coffee shop.
