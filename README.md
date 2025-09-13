# 🤖 Kynay AI – Intelligent Chat Assistant
**Dibuat oleh: Farhan Kertadiwangsa**  

---

## 📑 Daftar Isi
1. Pendahuluan
2. Tentang Kynay AI
3. Fitur Utama
   - Fitur AI
   - Fitur Sistem
4. Arsitektur Aplikasi
   - Frontend (review.html)
   - Backend (backen.js)
   - Alur Data dan Memory
5. Teknologi yang Digunakan
6. Instalasi & Setup
   - Persyaratan Sistem
   - Menjalankan Frontend
   - Menjalankan Backend
   - Konfigurasi Database
7. Dokumentasi API
   - Autentikasi (Login & Register)
   - Session Management
   - Chat Endpoint
8. Penjelasan Kode
   - review.html
   - backen.js
9. Fitur AI Detail
   - Ingatan (Memory)
   - Multi-Session Context
   - Auto-Rename Chat
   - Voice Recognition
   - Dark/Light Mode Adaptif
10. Keamanan
11. Deployment
12. Roadmap & Pengembangan Lanjutan
13. Kontribusi
14. Lisensi
15. Ucapan Terima Kasih

---

## 🔰 Pendahuluan
Kynay AI adalah aplikasi **AI Assistant berbasis web** yang menggabungkan **frontend modern** dengan **backend Node.js** untuk menyediakan pengalaman chatting interaktif, aman, dan kaya fitur.  
[...]

## 📖 Tentang Kynay AI
Proyek ini dirancang sebagai **kerangka dasar** AI Assistant dengan UI modern, sistem autentikasi, multi-session, dan memory. Aplikasi ini dapat digunakan sebagai:  
- AI pribadi.  
- Customer service bot.  
- Platform edukasi.  
- Dasar pengembangan SaaS berbasis AI.  

[...]

## ✨ Fitur Utama
### Fitur AI
- 🧠 **Ingatan (Memory AI)** – setiap percakapan disimpan, AI bisa melanjutkan konteks.  
- 📂 **Multi-Session** – pengguna bisa membuat banyak sesi chat berbeda.  
- 📝 **Auto-Rename Chat** – judul chat otomatis diubah berdasarkan pesan pertama.  
- 🎤 **Voice Input** – integrasi SpeechRecognition API.  
- 🔎 **Search Chat** – mencari riwayat.  
- 🌙 **Dark/Light Mode** – preferensi UI.  

### Fitur Sistem
- 🔑 Autentikasi JWT.  
- 🔔 Toast Notifications dengan animasi GSAP.  
- 🖥 Dashboard responsif.  
- 📦 Persistensi data di database.  

[...]

## 🏗 Arsitektur Aplikasi
### Frontend (review.html)
[...]

### Backend (backen.js)
[...]

### Alur Data dan Memory
[...]

## 🛠 Teknologi yang Digunakan
- Frontend: HTML5, TailwindCSS, GSAP, FontAwesome.  
- Backend: Node.js, Express.js, JWT, bcrypt.  
- Database: MongoDB/MySQL.  
- Deployment: Vercel, Netlify, Heroku, VPS.  

[...]

## 🔧 Instalasi & Setup
### Persyaratan Sistem
[...]

### Menjalankan Frontend
```bash
git clone https://github.com/Farhankerdiwangsa/Kynay-ai.git
cd Kynay-ai
# buka review.html dengan live server
```

### Menjalankan Backend
```bash
cd backend
npm install
node backen.js
```

[...]

## 📡 Dokumentasi API
### Auth
#### Register
`POST /auth/register`

Request:
```json
{ "username": "farhan", "password": "123456" }
```

Response:
```json
{ "ok": true, "token": "...", "user": { "id": 1, "username": "farhan" } }
```

[...]

## 🤖 Fitur AI Detail
### Ingatan (Memory)
[...]

### Multi-Session Context
[...]

### Auto-Rename Chat
[...]

### Voice Recognition
[...]

### Dark/Light Mode
[...]

## 🔒 Keamanan
[...]

## 🚀 Deployment
[...]

## 🗺 Roadmap & Pengembangan Lanjutan
[...]

## 🤝 Kontribusi
1. Fork repo.  
2. Buat branch baru.  
3. Commit perubahan.  
4. Pull request.  

## 📜 Lisensi
MIT License © 2025 Farhan Kertadiwangsa  

## 💙 Ucapan Terima Kasih
Terima kasih kepada komunitas open-source, TailwindCSS, GSAP, Node.js, dan semua kontributor.  

---
