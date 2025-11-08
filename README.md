# Gemini Chatbot API

Aplikasi chatbot berbasis web yang menggunakan Google Gemini API untuk menghasilkan respons percakapan yang cerdas dan interaktif.

## 📋 Deskripsi

Gemini Chatbot API adalah aplikasi web yang memungkinkan pengguna untuk berinteraksi dengan model AI Google Gemini melalui antarmuka yang user-friendly. Aplikasi ini dibangun menggunakan Node.js sebagai backend dan terintegrasi dengan Google Generative AI API.

## ✨ Fitur

- 💬 Chat interaktif dengan AI Gemini
- 🚀 Respon real-time
- 📝 Riwayat percakapan
- 🎨 Antarmuka yang responsif dan modern
- 🔒 Keamanan API key
- ⚡ Performa tinggi

## 🛠️ Teknologi yang Digunakan

- **Backend**: Node.js
- **AI Model**: Google Gemini API
- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Dependencies**: 
  - @google/generative-ai
  - express (jika menggunakan Express.js)
  - dotenv (untuk environment variables)

## 📦 Instalasi

### Prasyarat

- Node.js 14.x atau lebih tinggi
- npm (Node Package Manager)
- Google Gemini API Key

### Langkah-langkah Instalasi

1. **Clone repository**
   ```bash
   git clone https://github.com/akhmadsudaisi31-code/gemini_chatbot_API.git
   cd gemini_chatbot_API
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Konfigurasi API Key**
   
   Buat file `.env` di root directory dan tambahkan API key Anda:
   ```
   GEMINI_API_KEY=your_api_key_here
   ```
   
   Atau edit langsung di file `index.js`:
   ```javascript
   const API_KEY = "your_api_key_here";
   ```

4. **Dapatkan API Key**
   
   Dapatkan API key gratis dari [Google AI Studio](https://makersuite.google.com/app/apikey)

## 🚀 Cara Menjalankan

1. **Jalankan aplikasi**
   ```bash
   node index.js
   ```
   
   Atau jika menggunakan npm script:
   ```bash
   npm start
   ```

2. **Akses aplikasi**
   
   Buka browser dan kunjungi:
   ```
   http://localhost:3000
   ```
   
   Atau sesuai port yang dikonfigurasi di `index.js`

## 📖 Penggunaan

1. Buka aplikasi di browser
2. Ketik pesan Anda di kolom input
3. Tekan Enter atau klik tombol Send
4. AI akan merespons pertanyaan atau pesan Anda
5. Percakapan akan tersimpan dalam session

## ⚙️ Konfigurasi

### Model Configuration

Anda dapat menyesuaikan parameter model di file `index.js`:

```javascript
const generationConfig = {
  temperature: 0.9,
  topP: 1,
  topK: 1,
  maxOutputTokens: 2048,
};
```

### Safety Settings

Atur tingkat keamanan untuk filter konten berbahaya:

```javascript
const safetySettings = [
  {
    category: HarmCategory.HARM_CATEGORY_HARASSMENT,
    threshold: HarmBlockThreshold.BLOCK_MEDIUM_AND_ABOVE,
  },
  // ... konfigurasi safety lainnya
];
```

### Rate Limiting

⚠️ **Penting**: Gemini API memiliki batasan 60 query per menit untuk akun gratis.

## 📁 Struktur Project

```
gemini_chatbot_API/
│
├── public/               # Folder untuk file publik (frontend)
│   ├── index.html        # Halaman utama chatbot
│   ├── script.js         # JavaScript untuk interaksi dengan API
│   └── style.css         # Styling untuk tampilan web
│
├── index.js              # File utama aplikasi (Backend Node.js)
├── package.json          # Dependencies dan konfigurasi Node.js
├── package-lock.json     # Lock file untuk dependencies
└── README.md             # Dokumentasi project (file ini)
```

**Penjelasan File Penting:**
- `index.js`: Backend Node.js yang menangani routing dan integrasi dengan Gemini API
- `package.json`: Daftar library Node.js dan script yang dibutuhkan
- `public/index.html`: Interface chatbot tempat user berinteraksi
- `public/script.js`: Handling input user, fetch API, dan menampilkan response
- `public/style.css`: Styling untuk membuat UI chatbot menarik dan responsif

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan ikuti langkah berikut:

1. Fork repository ini
2. Buat branch fitur baru (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan Anda (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

## 📝 Catatan Penting

- **API Key**: Jangan pernah commit API key ke repository publik
- **Rate Limit**: Perhatikan batasan penggunaan API
- **Error Handling**: Implementasikan error handling yang baik untuk production
- **Security**: Gunakan environment variables untuk kredensial sensitif
- **CORS**: Pastikan CORS dikonfigurasi dengan benar jika backend dan frontend terpisah

## 🐛 Troubleshooting

### Error: "API Key tidak valid"
- Pastikan API key Anda benar
- Verifikasi API key di Google AI Studio
- Periksa apakah API sudah diaktifkan

### Error: "Module not found"
- Jalankan `npm install`
- Hapus folder `node_modules` dan `package-lock.json`, lalu install ulang
- Periksa versi Node.js Anda dengan `node --version`

### Error: "Port already in use"
- Ubah port di file `index.js`
- Atau hentikan proses yang menggunakan port tersebut:
  ```bash
  # Windows
  netstat -ano | findstr :3000
  taskkill /PID <PID> /F
  
  # Linux/Mac
  lsof -i :3000
  kill -9 <PID>
  ```

### Error: "CORS Policy"
- Pastikan CORS sudah dikonfigurasi dengan benar di backend
- Tambahkan header yang sesuai untuk mengizinkan request dari frontend

### Error: "Failed to fetch"
- Periksa koneksi internet Anda
- Pastikan backend server sudah berjalan
- Cek console browser untuk error detail

## 💡 Tips Pengembangan

- Gunakan `nodemon` untuk auto-restart saat development:
  ```bash
  npm install -g nodemon
  nodemon index.js
  ```
- Tambahkan logging untuk debugging
- Implementasikan rate limiting di backend
- Gunakan environment variables untuk semua konfigurasi sensitif

## 📄 Lisensi

[MIT License](LICENSE)

## 👨‍💻 Author

**Akhmad Sudaisi**

- GitHub: [@akhmadsudaisi31-code](https://github.com/akhmadsudaisi31-code)

## 🙏 Acknowledgments

- Google Gemini API Team
- Node.js Community
- Komunitas Open Source

## 📧 Kontak

Jika Anda memiliki pertanyaan atau saran, silakan buat issue di repository ini.

---

⭐ Jika project ini membantu Anda, berikan star pada repository ini!
