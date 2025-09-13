🤖 Kynay AI – Intelligent Chat Assistant

Dibuat oleh: Farhan Kertadiwangsa


---

📌 Tentang Proyek

Kynay AI adalah aplikasi AI Assistant berbasis web dengan dukungan memory percakapan, multi-session, dan UI modern.

Struktur utama:

index.html → frontend dengan TailwindCSS, GSAP, voice recognition, dark/light mode.

server.js → backend Node.js/Express dengan autentikasi JWT, session management, dan endpoint chat.


👉 🌐 Live Preview

Aplikasi ini bisa digunakan sebagai:

Asisten pribadi berbasis AI.

Bot customer service dengan riwayat percakapan.

Platform edukasi untuk belajar integrasi frontend–backend dengan AI.



---

✨ Fitur Utama

Fitur AI

🧠 Ingatan percakapan – AI melanjutkan konteks dalam setiap sesi.

📂 Multi-session chat – pengguna dapat membuat, mengganti nama, dan menghapus sesi percakapan.

📝 Auto-rename – judul sesi otomatis diambil dari pesan pertama.

🎤 Voice input – input suara via Web Speech API.

🌙 Dark/Light mode – tampilan adaptif.


Fitur Sistem

🔑 Login & Register dengan JWT – autentikasi aman dengan hashing password (bcrypt).

🔔 Toast notification – feedback interaktif dengan animasi GSAP.

🖥 Dashboard responsif – sidebar daftar sesi, area chat dengan bubble modern.

📦 Persistensi data – riwayat percakapan tersimpan di database.



---

🏗 Arsitektur Aplikasi

Frontend (index.html)

Login/Register form dengan validasi input.

Dashboard: sidebar daftar sesi + tombol New Chat.

Chat area: bubble user (kanan) dan AI (kiri).

Input form: teks + mic untuk voice recognition.

Dark/Light mode toggle disimpan di localStorage.

Toast notification dengan GSAP animation.


Backend (server.js)

Auth API: register & login user dengan JWT.

Session API: create, rename, delete, get all sessions.

Chat API: menerima pesan & mengembalikan balasan AI.

JWT middleware: validasi setiap request.

Database layer: menyimpan user, session, dan message.



---

🚀 Instalasi & Setup

Persyaratan

Node.js ≥ 16.x

NPM ≥ 8.x

Database: MongoDB/MySQL/Postgres

Browser modern


Jalankan Aplikasi Lokal

# Clone repository
git clone https://github.com/farhankerdiwangsa/Kynay-ai.git
cd Kynay-ai

# Install dependencies & jalankan backend
npm install
node server.js

Lalu buka index.html di browser (disarankan dengan Live Server).


---

📡 Dokumentasi API Singkat

Auth

POST /auth/register → register user.

POST /auth/login → login user.


Session

GET /api/session → ambil daftar sesi.

POST /api/session → buat sesi baru.

PUT /api/session/:id → rename sesi.

DELETE /api/session/:id → hapus sesi.


Chat

POST /api/chat/:sessionId/message → kirim pesan user & terima balasan AI.



---

🌐 Live Preview

👉 Coba langsung di sini
https://kynay-assistent.vercel.app

---

🗺 Roadmap

Integrasi dengan OpenAI API atau model lokal.

Mode real-time dengan WebSocket.

Export chat ke PDF/Markdown.

UI multi-bahasa.

Dukungan multimodal (teks + gambar).



---

📜 Lisensi

MIT License © 2025 Farhan Kertadiwangsa
