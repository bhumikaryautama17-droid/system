# Bara Indah Sinergi Group - Workflow Approval Web App (GitHub DB Version)

Aplikasi workflow approval ini dirancang sebagai website mandiri yang siap di-deploy ke Vercel dengan database berbasis file JSON yang disimpan langsung di repositori GitHub Anda.

## Struktur File
- index.html: File frontend gabungan (HTML + CSS + JS) untuk di-deploy ke Vercel atau GitHub Pages.
- db/: Folder berisi file database JSON default yang wajib Anda unggah ke repositori GitHub Anda.

## Langkah-Langkah Deploy ke GitHub & Vercel

### 1. Buat Repositori GitHub Baru
1. Buat sebuah repositori baru di GitHub (bisa bertipe **Public** atau **Private**).
2. Unggah file index.html dan folder db/ beserta isinya ke root repositori Anda.

### 2. Dapatkan GitHub Personal Access Token (PAT)
Aplikasi memerlukan token untuk menulis data (commit file) ke repositori Anda secara aman.
1. Masuk ke GitHub, klik foto profil Anda di kanan atas > **Settings**.
2. Gulir ke bawah dan klik **Developer Settings** > **Personal Access Tokens** > **Tokens (classic)**.
3. Klik **Generate new token (classic)**.
4. Beri nama token (misal: "workflow-db-token").
5. Centang opsi scope **"repo"** (atau jika repositori publik, cukup berikan izin akses write).
6. Klik **Generate token** dan salin kodenya (formatnya seperti ghp_...). *Catat kode ini karena kode hanya ditampilkan sekali.*

### 3. Deploy ke Vercel
1. Masuk ke dashboard **Vercel** (ercel.com).
2. Buat proyek baru (**New Project**) dan hubungkan ke repositori GitHub yang baru saja Anda buat.
3. Klik **Deploy**. Vercel akan menyajikan aplikasi Anda sebagai website statis.
4. Buka URL web hasil deploy Vercel Anda di browser.

### 4. Hubungkan Aplikasi Vercel dengan Repositori GitHub
1. Saat pertama kali memuat halaman web Vercel Anda, popup **GitHub Database Connection** akan otomatis muncul.
2. Masukkan detail repositori Anda:
   - **GitHub Owner**: Username GitHub Anda (atau nama organisasi).
   - **GitHub Repository Name**: Nama repositori GitHub yang baru Anda buat.
   - **GitHub Branch**: Cabang repositori Anda (umumnya main).
   - **GitHub Personal Access Token (PAT)**: Token ghp_... yang telah Anda buat di Langkah 2.
3. Klik **Simpan Koneksi**.
4. Halaman akan memuat ulang, membaca data pengguna dari repositori Anda, dan aplikasi siap digunakan sepenuhnya!
5. Untuk mengubah koneksi atau token di masa mendatang, klik ikon **Settings (sliders)** di bar kanan atas halaman.
