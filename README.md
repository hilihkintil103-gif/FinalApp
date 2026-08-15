# 🛒 KasiGR-atis POS - Kasir Digital & Manajemen Usaha F&B / Ritel

![Android](https://img.shields.io/badge/Platform-Android-green.svg?logo=android)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-purple.svg?logo=kotlin)
![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4.svg?logo=jetpackcompose)
![Architecture](https://img.shields.io/badge/Architecture-MVVM-orange.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

**KasiGR-atis POS** adalah aplikasi Kasir Digital (Point of Sale) modern berbasis Android yang dirancang khusus untuk membantu UMKM, bisnis F&B (makanan & minuman), serta toko ritel dalam mengelola transaksi, stok bahan baku, kalkulasi HPP, hingga analisis keuangan secara akurat dan efisien.

---

## ✨ Fitur Unggulan

### 1. 💳 Kasir Digital & POS
- **Katalog Produk Visual**: Pencarian produk cepat dengan filter kategori.
- **Multi-Metode Pembayaran**: Mendukung pembayaran Tunai (dengan kalkulator kembalian otomatis) dan QRIS.
- **Manajemen Meja & Pelanggan**: Pencatatan nama pelanggan atau nomor meja transaksi.
- **Struk Digital & Cetak**: Riwayat struk belanja yang rapi dan siap dicetak/dibagikan.

### 2. 🧮 Kalkulator HPP & Resep BOM (Bill of Materials) V6.7
- **Perhitungan HPP Bahan Baku**: Menghitung biaya modal per porsi berdasarkan takaran pakai, isi total kulakan, dan persentase *waste* (bahan terbuang).
- **Rincian Biaya Overhead & Operasional**:
  - 👷 **Tenaga Kerja**: `Gaji Harian / Target Porsi per Hari`
  - 📦 **Kemasan**: Akumulasi biaya wadah/sendok/plastik sekali pakai.
  - 🔥 **Gas, Listrik & Air**: `Tagihan Bulanan / Total Porsi Terjual`
- **Simulasi Food Cost & Margin**: Menyarankan harga jual ideal berdasarkan target % Food Cost atau % Margin Keuntungan yang diinginkan.
- **Panduan Rumus Interaktif**: Dilengkapi kartu rumus lipat (*collapsible*) dan contoh kalkulasi riil di dalam aplikasi.

### 3. 📦 Manajemen Stok & Bahan Baku
- **Pemotongan Stok Otomatis**: Stok bahan baku dan produk berkurang otomatis saat terjadi transaksi kasir.
- **Peringatan Stok Sedikit**: Indikator visual ketika stok mencapai ambang batas minimum.

### 4. 📝 Pencatatan Kasbon / Piutang
- Pelacakan utang/kasbon pelanggan dengan riwayat pembayaran bertahap.
- Filter pencarian nama pelanggan dan status pelunasan yang responsif.

### 5. 📊 Laporan Penjualan & Evaluasi Bisnis
- **Ringkasan Keuangan**: Ringkasan omzet, laba kotor, laba bersih, dan jumlah transaksi.
- **Analisis Produk Terlaris**: Mengetahui item mana yang paling diminati pembeli.
- **Ekspor & Evaluasi Laporan**: Fitur rangkuman evaluasi penjualan yang siap dibagikan.

### 6. 🔐 Akses Multi-Role & Keamanan
- **Role Pemilik (Owner)**: Akses penuh ke Laporan, Pengaturan Harga, Kelola User, dan Reset Data.
- **Role Kasir**: Akses terbatas yang difokuskan untuk kecepatan transaksi POS.
- **Konfirmasi Otorisasi Owner**: Proteksi kata sandi untuk aksi sensitif seperti *Restore* dan *Reset Data*.

### 7. 💾 Cadangan Data (Backup & Restore)
- Ekspor dan impor seluruh data toko/transaksi dalam format file **JSON** lokal untuk keamanan ekstra tanpa bergantung pada koneksi internet.

### 8. 📖 Buku Panduan Operasional Built-in
- Panduan langkah demi langkah penggunaan aplikasi yang disesuaikan untuk Kasir maupun Owner.

---

## 🛠️ Stack Teknologi & Arsitektur

- **Bahasa Pemrograman**: Kotlin 100%
- **UI Framework**: Jetpack Compose (Material Design 3)
- **Arsitektur**: MVVM (Model-View-ViewModel) dengan Unidirectional Data Flow (UDF)
- **State Management**: StateFlow & SharedFlow dengan Coroutines
- **Penyimpanan Lokal**: Room Database (SQLite) / Local JSON Persistence
- **Navigation**: Jetpack Compose Navigation

---

## 📐 Rumus Perhitungan HPP yang Digunakan

1. **HPP Bahan Baku** = (Harga Kulakan / Total Isi) × Takaran × (1 + Waste %)
2. **Total HPP Batch** = Total HPP Bahan + Tenaga Kerja + Kemasan + Gas & Listrik
3. **HPP Bersih Unit** = Total HPP Batch / Jumlah Porsi Hasil (Yield)
4. **Harga Jual Ideal** = HPP Bersih Unit / (Target Food Cost % / 100)
5. **Margin (%)** = ((Harga Jual - HPP Unit) / Harga Jual) × 100%

---

## 🚀 Cara Menjalankan Proyek di Android Studio

1. **Clone Repositori ini**:
   ```bash
   git clone https://github.com/USERNAME_ANDA/kasigr-atis-pos.git
