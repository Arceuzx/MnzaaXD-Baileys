# MnzaaXD-Baileys 🚀

<div align="center">

![NodeJS](https://img.shields.io/badge/Node.js-v18%2B-green?style=flat-square&logo=node.js)
![Baileys](https://img.shields.io/badge/Baileys-Interactive%20Edition-blue?style=flat-square&logo=whatsapp)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

*Base Bot WhatsApp canggih berbasis Node.js menggunakan library Baileys dengan dukungan penuh untuk fitur pesan interaktif (Buttons, List, & Cards).*

</div>

---

## 📋 Daftar Isi
- [Fitur Utama](#-fitur-utama)
- [Prasyarat Sistem](#-prasyarat-sistem)
- [Cara Instalasi](#-cara-instalasi)
  - [1. Instalasi di Termux (Android)](#1-instalasi-di-termux-android)
  - [2. Instalasi di PC / Laptop (Node.js & GitHub)](#2-instalasi-di-pc--laptop-nodejs--github)
- [Konfigurasi Penting (`package.json` & Lainnya)](#-konfigurasi-penting-packagejson--lainnya)
- [Cara Menjalankan Bot](#-cara-menjalankan-bot)
- [Catatan Penting](#-catatan-penting)
- [Kredit & Kontribusi](#-kredit--kontribusi)

---

## ✨ Fitur Utama
* 🟢 **Pairing Code Support:** Login mudah menggunakan nomor WhatsApp tanpa QR Code yang ribet.
* 🔘 **Interactive Buttons & Lists:** Mendukung tombol interaktif dan menu *list*.
* 📥 **All-in-One Downloader:** Fitur unduh media dari berbagai platform populer.
* 🎨 **Maker Tools:** Pembuat stiker, *brat*, dan manipulasi media lainnya.
* 🎮 **Mini Games:** Fitur permainan interaktif di dalam bot.

---

## ⚙️ Prasyarat Sistem
Sebelum menginstal bot ini, pastikan perangkat Anda telah terpasang:
* **Node.js** (Versi LTS v18 atau v20 direkomendasikan).
* **Git** (Untuk *cloning* repositori).
* **FFmpeg** (Wajib untuk pemrosesan media, stiker, dan audio).

---

## 📦 Cara Instalasi

### 1. Instalasi di Termux (Android)
Buka aplikasi Termux Anda, kemudian jalankan perintah di bawah ini secara berurutan:
```bash
# Perbarui dan upgrade paket Termux
pkg update && pkg upgrade -y

# Instal Git, Node.js, dan FFmpeg
pkg install git nodejs ffmpeg -y

# Kloning repositori bot Anda
git clone https://github.com/Arceuzx/MnzaaXD-Baileys.git

# Masuk ke direktori bot
cd MnzaaXD-Baileys

# Instal semua dependensi
npm install
```

### 2. Instalasi di PC / Laptop (Node.js & GitHub)
Buka Command Prompt (CMD), PowerShell, atau Terminal di komputer Anda, lalu jalankan perintah berikut secara berurutan:
```bash
# Kloning repositori ke komputer lokal
git clone https://github.com/Arceuzx/MnzaaXD-Baileys.git

# Masuk ke folder proyek
cd MnzaaXD-Baileys

# Instal bersih semua dependensi
npm install
```

---

## 🛠️ Konfigurasi Penting (`package.json` & Lainnya)

Agar bot dapat berjalan sesuai keinginan Anda, ada beberapa file penting yang perlu dan bisa diubah (baik secara penting maupun opsional):

### A. Mengubah `package.json` (Penting)
Buka file `package.json` di *root folder* bot. Bagian ini penting untuk mendefinisikan informasi bot dan sumber *library* Anda:

```json
{
   "name": "mnzaaxd-bot",
   "version": "1.0.0",
   "description": "Bot WhatsApp interaktif",
   "main": "index.js",
   "type": "module",
   "author": "Nama Anda",
   "dependencies": {
      "@whiskeysockets/baileys": "github:Arceuzx/MnzaaXD-Baileys",
      "@napi-rs/image": "^1.12.0",
      "file-type": "21.3.4",
      "qrcode": "~1.5.4",
      "yt-search": "^2.13.1"
   }
}
```
* **Yang perlu diubah:**
  * `"name"`: Ganti dengan nama proyek bot Anda.
  * `"author"`: Ganti dengan nama Anda sebagai pembuat.
  * `"@whiskeysockets/baileys"`: Pastikan mengarah ke repositori GitHub Anda sendiri (`github:USERNAME/REPOSITORY`) jika ingin menjadikannya sumber privat atau publik Anda.

### B. Konfigurasi Utama (`settings.js` / `index.js`) — Opsional & Penting
Cari file konfigurasi utama bot Anda (such as `settings.js`), beberapa hal yang bisa diubah meliputi:
* **Nomor Owner / Developer:** Masukkan nomor WhatsApp Anda agar mendapatkan akses *owner commands*.
* **Nama Bot (`botName`):** Ubah nama panggilan bot sesuai selera.
* **Pairing Code:** Pastikan `global.pairingCode = true` jika ingin menggunakan metode login nomor telepon.

---

## 🚀 Cara Menjalankan Bot

Setelah proses instalasi (`npm install`) selesai dan konfigurasi di atas disesuaikan, jalankan bot dengan perintah berikut:

```bash
npm start
```

* Jika ini pertama kali dijalankan dan menggunakan *Pairing Code*, masukkan nomor WhatsApp Anda (contoh: `628xxxxxxxxxx`) saat diminta di terminal.
* Salin dan masukkan *pairing code* yang muncul ke aplikasi WhatsApp Anda (masuk ke ikon titik tiga di kanan atas > **Perangkat Tertaut** > **Tautkan dengan nomor telepon**).

---

## ⚠️ Catatan Penting
1. **Struktur Media:** Pastikan folder `media/Image/` memiliki file `thumbnail.jpg` agar fitur menu tidak mengalami error `ENOENT`.
2. **Koneksi Internet:** Pastikan koneksi stabil saat menjalankan `npm install` pertama kali.

---

## 📜 Kredit & Kontribusi
* **WhiskeySockets** — Base pengembang *library* Baileys asli.
* **Arceuzx** — Pemelihara dan pengembang repositori ini.
