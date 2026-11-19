# Warung Nasi Bersama — Web POS & Executive Dashboard

Aplikasi web *Transaction Processing System* (TPS) dan *dashboard* pemantauan berbasis peran (*Role-Based Access Control*) untuk mendukung operasional **Warung Nasi Bersama** di Medan. Dirancang ringan sebagai aplikasi *standalone* menggunakan **HTML5**, **Tailwind CSS**, dan **Vanilla JavaScript** dengan penyimpanan `localStorage` tanpa memerlukan *backend server* atau database eksternal.

## Fitur Utama

### 1. Pemisahan Peran & Hak Akses (*Staff* vs. *Owner*)
- **Halaman Kasir (*Staff View*)**: Fokus pada pencatatan pesanan cepat, pengelolaan antrean aktif, dan proses pembayaran. Staf tidak memiliki akses ke halaman pemantauan pemilik.
- **Halaman Pemantauan (*Owner Executive Dashboard*)**: Khusus untuk pemilik memantau metrik bisnis, mengelola daftar menu dan stok, serta mengunduh rekap laporan.

### 2. Alur Operasional Kasir
- **Pesanan Paralel & Bayar di Akhir (*Multi-Active Orders*)**: Mendukung pembuatan banyak pesanan secara bersamaan dengan *Order ID* otomatis (misalnya `WN-00125`), sehingga pelanggan dapat membayar secara acak saat selesai makan tanpa harus menunggu pesanan lain selesai.
- **Tab Khusus Pesanan Aktif (*Unpaid Orders*)**: Memudahkan staf melihat daftar pesanan yang belum lunas, mengubah rincian item/jumlah sebelum pembayaran (*Edit Unpaid Order*), dan melunasi transaksi.
- **Sidebar *Collapsible***: Tombol sembunyikan/tampilkan *sidebar* untuk memperluas area kerja kasir.

### 3. Manajemen Menu, Stok & Pemantauan Pemilik
- **Kartu *Dashboard* Interaktif (*Drill-Down Cards*)**: Ringkasan **Pendapatan Harian**, **Total Transaksi**, **Porsi Terjual**, dan **Status Stok** yang dapat diklik untuk membuka rincian atau mengarah langsung ke halaman/bagian terkait (termasuk pintasan ke *Menu & Stok* saat stok menipis).
- **Kelola Menu & Harga**: Menambah, mengedit (nama, kategori, harga, foto, status ketersediaan), dan menghapus menu dengan format pemisah titik ribuan otomatis pada input harga.
- **Pengelolaan Stok Fleksibel**: Mendukung perubahan stok menggunakan tombol `+` / `-` maupun ketik manual langsung (*numeric keyboard*).
- **Ekspor Laporan**: Mengunduh rekap data transaksi/pendapatan dalam format **CSV/Excel** dan **PDF** (atau cetak laporan).

### 4. Desain Responsif Adaptif
- Tata letak menyesuaikan tampilan di **HP (Mobile)**, **Tablet**, dan **Laptop/Desktop**.

## Teknologi yang Digunakan
- **HTML5**
- **Tailwind CSS** (via CDN)
- **Vanilla JavaScript**
- **Browser `localStorage`** (penyimpanan data lokal & sinkronisasi antar tampilan)

## Cara Menjalankan Proyek
1. Unduh atau *clone* berkas proyek ke komputer Anda.
2. Pastikan seluruh referensi file/aset (gambar, CSS/JS, atau tautan eksternal) berada pada *path* yang sesuai agar tidak terjadi kendala `404 Not Found`.
3. Buka berkas utama (`index.html`) langsung di *browser* modern (seperti Google Chrome).

## Catatan Penggunaan
- Karena data disimpan di `localStorage` pada *browser* perangkat yang digunakan, riwayat transaksi, menu, dan stok akan bertahan saat halaman di-*refresh* pada *browser* yang sama, namun tidak tersinkronisasi lintas perangkat secara otomatis tanpa *backend* atau database terpusat.
