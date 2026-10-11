# FIRZA JAYA TEKNIK - Catatan Sewa Alat

Aplikasi PWA (Progressive Web App) untuk pencatatan sewa alat.

## ✨ Fitur

- 📱 **Install sebagai App** - Bisa diinstall di HP seperti aplikasi native
- 💾 **Offline Support** - Tetap bisa digunakan tanpa internet
- 📊 **Pencatatan Sewa** - Catat penyewaan alat dengan mudah
- 💰 **Ringkasan Keuangan** - Pemasukan, pembayaran, dan piutang
- 📈 **Grafik Performa** - Lihat performa bisnis dalam grafik
- 📄 **Invoice** - Generate invoice untuk pelanggan
- 📥 **Export Excel/CSV** - Download data dalam format Excel atau CSV

## 🚀 Deploy ke Vercel

### Opsi 1: Via GitHub (Recommended)

1. **Push ke GitHub**
   ```bash
   cd rental-deploy
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/USERNAME/rental-deploy.git
   git push -u origin main
   ```

2. **Connect ke Vercel**
   - Buka [vercel.com](https://vercel.com)
   - Login dengan GitHub
   - Klik "New Project"
   - Pilih repository `rental-deploy`
   - Klik "Deploy"

### Opsi 2: Via Vercel CLI

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Deploy**
   ```bash
   cd rental-deploy
   vercel --prod
   ```

## 📲 Install di HP

Setelah di-deploy:

1. Buka URL aplikasi di browser HP (Chrome/Safari)
2. **Android (Chrome)**:
   - Ketuk menu (⋮) di kanan atas
   - Pilih "Tambah ke layar utama"
3. **iPhone (Safari)**:
   - Ketuk ikon Share (□↑)
   - Scroll ke bawah, pilih "Tambah ke Layar Utama"

## 📁 Struktur File

```
rental-deploy/
├── index.html        # Aplikasi utama
├── manifest.json     # Konfigurasi PWA
├── sw.js            # Service Worker (offline support)
├── icon-192.png     # Icon untuk home screen
├── icon-512.png     # Icon besar untuk install
├── vercel.json      # Konfigurasi deployment
└── .gitignore       # File yang diabaikan git
```

## 🔧 Konfigurasi

### Mengubah Nama App
Edit `manifest.json`:
```json
{
  "name": "NAMA APP ANDA",
  "short_name": "SHORT NAME"
}
```

### Mengubah Warna Tema
Edit `manifest.json`:
```json
{
  "theme_color": "#WARNAMU",
  "background_color": "#WARNA_BG"
}
```

### Mengubah Icon
Ganti file `icon-192.png` dan `icon-512.png` dengan gambar Anda
(disarankan: 192x192 dan 512x512 pixel, format PNG)

## ⚠️ Catatan Penting

- **Data tersimpan di browser** - Setiap perangkat menyimpan datanya sendiri
- **Backup rutin** - Download Excel/CSV secara berkala
- **Berbeda perangkat = beda data** - Jika butuh sinkronisasi, perlu backend server

## 🛠️ Tech Stack

- HTML5 + CSS3 + Vanilla JavaScript
- Service Worker (Offline support)
- Vercel (Hosting)
- LocalStorage (Data storage)
