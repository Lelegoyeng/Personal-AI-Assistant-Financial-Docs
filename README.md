## 🚀 Personal AI Assistant Financial Report

Laporan keuangan pribadi yang dihasilkan oleh asisten AI untuk membantu pengguna memantau, menganalisis, dan merencanakan keuangan secara lebih cerdas dan efisien.

### ✨ Fitur

- **Integrasi WhatsApp**: Berinteraksi dengan asisten AI langsung dari WhatsApp.
- **Kecerdasan Buatan**: Didukung oleh model bahasa canggih untuk memproses permintaan Anda.
- **Pencatatan Google Sheets**: Semua interaksi dan data keuangan dicatat secara otomatis di Google Sheets.
- **Deployment Mudah**: Didesain untuk dideploy dengan mudah di Vercel.

###  prerequisites

Sebelum memulai, pastikan Anda memiliki:

- [Node.js](https://nodejs.org/en/) (v18 atau lebih tinggi)
- [pnpm](https://pnpm.io/)
- Akun [Google Cloud Platform](https://cloud.google.com/) dengan Google Sheets API diaktifkan
- Akun [Vercel](https://vercel.com/)

### ⚙️ Instalasi

1.  **Install dependensi:**

    ```bash
    pnpm install
    ```

2.  **Siapkan kredensial Google Sheets:**

    - Ikuti panduan [ini](https://docs.sheetjs.com/docs/getting-started/installation/nodejs#service-account) untuk membuat akun layanan dan mengunduh file kredensial JSON.
    - Ganti nama file JSON menjadi `credentials.json` dan letakkan di direktori `src`.

3.  **Konfigurasi variabel lingkungan:**

    - Salin `.env.example.js` menjadi `.env`.
    - Isi variabel yang diperlukan, seperti `OPENAI_API_KEY` dan `SPREADSHEET_ID`.

### ▶️ Menjalankan Bot Secara Lokal

1.  **Jalankan aplikasi dalam mode pengembangan:**

    ```bash
    pnpm run start:dev
    ```

2.  **Pindai Kode QR:**

    - Saat pertama kali dijalankan, kode QR akan muncul di terminal.
    - Buka WhatsApp di ponsel Anda, buka **Pengaturan** > **Perangkat Tertaut** > **Tautkan Perangkat**, lalu pindai kode QR.
    - Sesi akan disimpan di direktori `wa.session`, jadi Anda tidak perlu memindai ulang setiap kali memulai ulang.

### 🚀 Deployment ke Vercel

1.  **Hubungkan repositori Anda ke Vercel.**
2.  **Konfigurasikan variabel lingkungan di pengaturan proyek Vercel.**
3.  **Deploy!** Vercel akan secara otomatis membangun dan men-deploy bot Anda.

### 💬 Cara Menggunakan

Setelah bot berjalan dan terhubung ke WhatsApp Anda, gunakan format berikut untuk mencatat keuangan secara akurat.

#### 📝 Mencatat Pemasukan

Gunakan kata kunci seperti `pemasukan`, `gaji`, `terima uang`, diikuti dengan jumlah dan sumbernya.

**Contoh:**
- `"Pemasukan 5.000.000 dari gaji bulanan"`
- `"Dapat bonus 1.500.000"`
- `"Terima uang 250.000 dari project freelance"`

#### 💸 Mencatat Pengeluaran

Sebutkan jumlah, barang/jasa yang dibeli, dan kategorinya untuk pencatatan yang lebih rapi.

**Format:** `[jumlah] [deskripsi] [kategori]`

**Contoh:**
- `"Beli kopi 25.000 kategori makanan & minuman"`
- `"Bayar tagihan listrik 350.000 kategori tagihan"`
- `"Transportasi ke kantor 50.000 kategori transportasi"`
- `"15.000 untuk parkir kategori lain-lain"`

#### 📊 Menanyakan Informasi Keuangan

Anda bisa bertanya tentang ringkasan keuangan Anda.

**Contoh:**
- `"Berapa total pengeluaran saya bulan ini?"`
- `"Tampilkan semua pemasukan di bulan Juni"`
- `"Berapa sisa saldo saya?"`
- `"Laporan keuangan kuartal ini"`

