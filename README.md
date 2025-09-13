🤖 Kynay AI – Intelligent Chat Assistant

Dibuat oleh: Farhan Kertadiwangsa


---

📑 Daftar Isi

1. Pendahuluan


2. Latar Belakang & Motivasi


3. Tentang Kynay AI


4. Fitur Utama


5. Arsitektur Aplikasi


6. Teknologi yang Digunakan


7. Instalasi & Setup


8. Dokumentasi API


9. Analisis Kode Frontend (index.html)


10. Analisis Kode Backend (index.js)


11. Fitur AI Detail


12. Keamanan


13. Deployment


14. 🌐 Live Preview


15. Roadmap


16. Kontribusi


17. Lisensi


18. Ucapan Terima Kasih




---

🔰 1. Pendahuluan

Kynay AI adalah sebuah proyek AI Assistant berbasis web yang dibangun dengan semangat open-source untuk menghadirkan pengalaman percakapan cerdas, natural, dan mudah digunakan. Tidak seperti chatbot sederhana yang hanya menerima input lalu membalas dengan respons generik, Kynay AI membawa konsep memory (ingatan) sehingga percakapan dapat berlanjut dengan konteks.

Dalam ekosistem aplikasi modern, user experience (UX) adalah faktor penentu apakah sebuah aplikasi akan dipakai terus-menerus atau ditinggalkan. Itulah sebabnya, selain logika backend yang solid, Kynay AI juga dibekali frontend modern dengan TailwindCSS untuk styling, GSAP untuk animasi, serta interaksi interaktif seperti voice recognition, dark/light mode, dan toast notification.

Proyek ini ditujukan untuk:

Developer pemula yang ingin belajar membangun aplikasi AI end-to-end.

Tim kecil yang membutuhkan fondasi untuk mengembangkan produk berbasis AI.

Individu yang menginginkan asisten virtual pribadi dengan UI elegan.


Kynay AI bukan sekadar eksperimen; ia adalah kerangka kerja nyata yang dapat dikembangkan menjadi aplikasi komersial di masa depan.


---

📖 2. Latar Belakang & Motivasi

Tantangan dalam membangun AI Assistant

Sebagian besar developer kesulitan saat membangun AI Assistant karena:

1. Kurangnya contoh implementasi nyata: kebanyakan tutorial hanya membahas frontend atau backend, jarang keduanya sekaligus.


2. Manajemen konteks yang sulit: tanpa memory, AI terasa kaku.


3. Kurangnya perhatian pada UI/UX: aplikasi AI biasanya berfokus pada fungsi, bukan tampilan.



Solusi yang ditawarkan Kynay AI

Integrasi lengkap: frontend + backend + database dalam satu proyek.

Memory system: setiap sesi percakapan disimpan, sehingga konteks tidak hilang.

UI modern: desain elegan, dark/light mode, animasi interaktif, dan voice recognition.

Open-source spirit: kode dapat dipelajari, dimodifikasi, dan digunakan kembali oleh siapa pun.


Filosofi pengembangan

Kynay AI dibangun dengan filosofi:

Sederhana dalam penggunaan.

Fleksibel untuk dikembangkan.

Aman dalam pengelolaan data user.

Terbuka untuk kontribusi dari komunitas.



---

📖 3. Tentang Kynay AI

Kynay AI terdiri dari dua lapisan utama:

1. Frontend (index.html)

Mengatur tampilan dan interaksi pengguna.

Memuat login/register, dashboard, chat interface, toast notification, voice recognition, dan dark/light mode.

Dibangun dengan HTML5, TailwindCSS, GSAP, dan JavaScript vanilla agar ringan dan cepat.



2. Backend (server.js)

Menyediakan API untuk autentikasi, manajemen sesi, dan chat.

Menggunakan Node.js dan Express.js dengan dukungan JWT untuk keamanan.

Memiliki struktur REST API yang jelas, sehingga mudah diintegrasikan dengan frontend atau bahkan aplikasi mobile.




Kedua lapisan ini berkomunikasi melalui HTTP request dengan payload JSON. JWT digunakan sebagai mekanisme validasi, memastikan hanya user yang sudah login yang bisa mengakses data percakapannya.


---

✨ 4. Fitur Utama

🔹 Fitur AI

🧠 Ingatan Percakapan (Memory)
AI mengingat konteks dalam satu sesi, sehingga percakapan terasa lebih natural.

📂 Multi-Session Chat
User dapat membuat beberapa sesi berbeda, misalnya “Belajar”, “Kerja”, “Santai”.

📝 Auto-Rename Session
Judul sesi otomatis diambil dari pesan pertama agar lebih relevan.

🎤 Voice Input
Dengan Web Speech API, user bisa bicara langsung dan teks muncul otomatis.

🌙 Dark/Light Mode
Tampilan menyesuaikan preferensi user.

🔎 Search Chat
User bisa mencari riwayat percakapan lama dengan cepat.


🔹 Fitur Sistem

🔑 Login & Register dengan JWT
User data aman dengan password hash.

🔔 Toast Notification
Memberikan feedback real-time dengan animasi GSAP.

🖥 Dashboard Responsif
Sidebar dinamis dengan daftar sesi.

📦 Persistensi Data
Semua percakapan disimpan di database, tidak hilang saat reload.

🎨 Animasi UI Modern
Efek ripple, shine, dan transisi halus membuat aplikasi enak dipakai.

🏗 5. Arsitektur Aplikasi

Gambaran Umum

Arsitektur Kynay AI dirancang dengan pendekatan client-server yang sederhana namun fleksibel. Frontend menangani interaksi visual dan input user, sedangkan backend mengelola logika bisnis, autentikasi, dan penyimpanan data.

Diagram alur data :

[User Browser]
      |
      v
 [Frontend: indexhtml]
      |
  (HTTP Request/Response)
      |
      v
 [Backend: backen.js] ----> [Database]

Frontend (index.html)

Login & Register: validasi input → request ke backend.

Dashboard: render daftar sesi dari API /api/session.

Chat Area: menampilkan bubble user & AI.

Voice Recognition: API browser menangkap suara.

Dark/Light Mode: toggle UI, disimpan di localStorage.


Backend (server.js)

Auth API: login & register user dengan JWT.

Session API: CRUD sesi percakapan.

Chat API: menerima pesan, mengembalikan balasan AI.

JWT Middleware: validasi akses setiap request.

Database Layer: menyimpan user, sesi, dan chat.


Database

Tabel/collection utama:

users → id, username, passwordHash.

sessions → id, userId, title.

messages → id, sessionId, role, content, timestamp.



---

🛠 6. Teknologi yang Digunakan

Frontend

HTML5: struktur halaman.

TailwindCSS: styling cepat dan konsisten.

GSAP: animasi interaktif.

FontAwesome: ikon siap pakai.

Web Speech API: voice recognition.


Backend

Node.js: runtime JavaScript.

Express.js: framework HTTP.

JWT (jsonwebtoken): autentikasi token.

bcrypt: hash password.

CORS: mengizinkan request dari frontend.

body-parser: parsing JSON request.


Database

MongoDB (opsi default, cocok untuk JSON)

Bisa juga MySQL/Postgres untuk relational schema.



---

🔧 7. Instalasi & Setup

Persyaratan Sistem

Node.js ≥ 16.x

NPM ≥ 8.x

MongoDB Atlas atau MySQL server

Browser modern (Chrome/Edge/Firefox terbaru)


Langkah Instalasi

Clone Repository

git clone https://github.com/Farhankerdiwangsa/Kynay-ai.git
cd Kynay-ai

Menjalankan Frontend

Buka file index.html dengan Live Server (VSCode extension).

Atau deploy ke Netlify/Vercel untuk akses publik.


Menjalankan Backend

cd server
npm install
node server.js

Konfigurasi Environment

Buat file .env:

JWT_SECRET=your_secret_key
DB_URI=mongodb://localhost:27017/kynay
PORT=2009


---

📡 8. Dokumentasi API

🔑 Auth

Register

POST /auth/register
Request:

{ "username": "farhan", "password": "123456" }

Response:

{
  "ok": true,
  "token": "jwt_token",
  "user": { "id": 1, "username": "farhan" }
}

Login

POST /auth/login
Request:

{ "username": "farhan", "password": "123456" }

Response:

{
  "ok": true,
  "token": "jwt_token",
  "user": { "id": 1, "username": "farhan" }
}


---

📂 Session

Create Session

POST /api/session

{ "title": "Belajar JavaScript" }

Get All Sessions

GET /api/session

Rename Session

PUT /api/session/:id

{ "title": "Sesi Belajar AI" }

Delete Session

DELETE /api/session/:id


---

💬 Chat

Send Message

POST /api/chat/:sessionId/message
Request:

{ "message": "Halo AI, apa kabar?" }

Response:

{
  "ok": true,
  "message": {
    "role": "assistant",
    "content": "Halo Farhan, saya baik-baik saja!",
    "ts": 1699987200
  }
}

📂 9. Analisis Kode Frontend (index.html)

Struktur Umum

File index.html adalah jantung frontend Kynay AI. Ia memuat seluruh tampilan aplikasi, termasuk login/register, dashboard, chat area, serta berbagai elemen interaktif.

Struktur besar:

<head> → meta, CSS (Tailwind), ikon (FontAwesome), GSAP.

<body> → 3 container utama: Auth Container, Dashboard, Toast Notification.

<script> → seluruh logika UI (animasi, request API, state UI).


Login & Register Form

Elemen form terdiri dari input username, password, dan tombol submit.

Validasi dilakukan di sisi frontend: jika input kosong, munculkan toast error.

Jika valid, frontend mengirim request ke endpoint /auth/login atau /auth/register dengan payload JSON.

Jika sukses, backend mengembalikan JWT yang disimpan di localStorage.

Setelah login, container auth disembunyikan dengan animasi fade-out, lalu dashboard dimunculkan.


Catatan teknis: penggunaan GSAP untuk transisi container membuat pengalaman user lebih halus dibanding sekadar display: none;.

Dashboard

Terdiri dari dua bagian utama: sidebar dan chat area.

Sidebar menampilkan daftar sesi percakapan. Ada tombol “+ New Chat” untuk membuat sesi baru. Setiap sesi ditampilkan sebagai item list dengan opsi rename/delete.

Chat Area berisi percakapan antara user dan AI. Pesan user muncul di sisi kanan (warna biru), sedangkan pesan AI muncul di sisi kiri (warna abu-abu).


Chat Input & Voice Recognition

Di bawah chat area ada form input teks + tombol mic.

Jika user mengetik lalu enter → pesan dikirim ke backend.

Jika user menekan tombol mic → Web Speech API diaktifkan.

API ini mendengarkan suara.

Hasil transkripsi dimasukkan ke input text secara real-time.

Setelah selesai, transkrip bisa langsung dikirim.



Catatan teknis: fallback diperlukan untuk browser yang tidak mendukung window.SpeechRecognition.

Dark/Light Mode

Toggle tersedia di dashboard.

Ketika user menekan tombol, class Tailwind seperti dark:bg-gray-900 ditambahkan/dihapus.

Preferensi user disimpan di localStorage, sehingga mode bertahan setelah reload.


Toast Notification

Implementasi sederhana dengan container di pojok kanan atas.

Setiap kali ada error/sukses, elemen toast ditambahkan lalu dianimasikan dengan GSAP (fade in → stay → fade out).

Contoh penggunaan: saat login gagal, atau saat session berhasil dibuat.


Animasi & UX

GSAP digunakan untuk animasi masuk/keluar container.

Efek ripple pada tombol memberi kesan modern.

Perubahan state (misalnya dark → light) diberi transisi agar smooth.



---

⚙️ 10. Analisis Kode Backend (server.js)

Struktur Dasar

Import dependency:

const express = require('express');
const bodyParser = require('body-parser');
const jwt = require('jsonwebtoken');
const bcrypt = require('bcrypt');
const cors = require('cors');

Inisialisasi server Express, port default 2009.

Middleware: app.use(cors()), app.use(bodyParser.json()).


Middleware JWT

Fungsi middleware memeriksa header Authorization.

Jika token valid → req.user diisi data user.

Jika tidak ada/invalid → kembalikan error 401.


Auth Routes

Register:

Menerima username & password.

Password di-hash dengan bcrypt.hash.

User baru disimpan di DB.

JWT dibuat dan dikirim ke client.


Login:

Ambil user berdasarkan username.

Cocokkan password dengan bcrypt.compare.

Jika cocok → buat JWT dan kirim ke client.



Session Routes

Create Session: user membuat sesi baru dengan judul default.

Get Sessions: kembalikan semua sesi milik user.

Rename Session: update judul sesi.

Delete Session: hapus sesi dan seluruh message di dalamnya.


Chat Routes

POST /api/chat/:sessionId/message

Ambil session berdasarkan ID dan userId.

Simpan pesan user di DB.

Generate balasan AI (saat ini stub → bisa integrasi model NLP).

Simpan balasan AI di DB.

Kirim balasan ke frontend.



Struktur Data di DB

User: { id, username, passwordHash }

Session: { id, userId, title }

Message: { id, sessionId, role, content, timestamp }



---

🔎 Catatan Teknis Penting

1. Security:

Password tidak pernah disimpan plain text.

JWT memiliki expiry time agar token tidak berlaku selamanya.



2. Scalability:

Backend bisa diperluas untuk multi-user dengan load balancer.

DB bisa dipindah ke MongoDB Atlas agar lebih scalable.



3. Extensibility:

Endpoint chat bisa dihubungkan ke API eksternal (misalnya OpenAI).

Bisa dibuat WebSocket untuk real-time streaming response.

🤖 11. Fitur AI Detail

Ingatan (Memory)

Kynay AI memiliki dua level ingatan:

Jangka pendek (short-term memory) → percakapan dalam satu sesi, sehingga AI bisa memahami konteks pesan sebelumnya.

Jangka panjang (long-term memory) → percakapan disimpan di database, bisa dipanggil ulang ketika user membuka sesi lama.


Multi-Session Context

Setiap sesi memiliki konteksnya sendiri. Jika user membuka sesi baru, AI tidak lagi mengingat percakapan lama. Hal ini meniru cara aplikasi chat modern bekerja.

Auto-Rename Session

Judul sesi otomatis diambil dari pesan pertama. Contoh: jika user mengetik “Belajar Node.js”, sesi otomatis diberi nama Belajar Node.js.

Voice Recognition

Dibangun dengan Web Speech API:

Mendukung bahasa Indonesia (id-ID).

Input suara langsung diubah menjadi teks di input form.

Memberi pengalaman hands-free bagi user.


Dark/Light Mode

User bisa mengganti mode sesuai preferensi.

Class Tailwind berubah otomatis.

Preferensi disimpan di localStorage.


Toast Notification

Memberikan feedback visual untuk aksi user.

Animasinya dibuat dengan GSAP → fade in, hold, fade out.



---

🔒 12. Keamanan

Password Hashing: semua password disimpan menggunakan bcrypt.

JWT Authentication: token dikirim setiap request untuk memastikan user valid.

Input Validation: semua data user divalidasi di frontend & backend.

HTTPS: wajib saat di production untuk melindungi komunikasi.

Rate Limiting: mencegah brute-force login.

Helmet.js: menambah header keamanan pada backend.



---

🚀 13. Deployment

Deployment adalah tahap membuat aplikasi bisa diakses publik. Untuk Kynay AI:

Frontend

Bisa di-host di GitHub Pages, Netlify, atau Vercel.

File utama: index.html + asset (CSS, JS).


Backend

Bisa di-deploy ke Heroku, Render, Railway, atau VPS.

Pastikan port, JWT secret, dan DB URI diatur di .env.


Database

Disarankan pakai MongoDB Atlas (cloud), atau MySQL hosted.


CI/CD

Hubungkan repo ke Netlify/Vercel/Render.

Setiap commit → auto-deploy.



---

🌐 14. Live Preview

Kamu bisa mencoba langsung aplikasi Kynay AI melalui link berikut:

👉 Live Demo Project https://kynay-assistent.vercel.app
---

🗺 15. Roadmap

Rencana pengembangan Kynay AI:

1. Integrasi dengan OpenAI API atau model lokal.


2. Realtime response dengan WebSocket.


3. Multimodal support (teks + gambar).


4. Export chat ke PDF/Markdown.


5. Multi-bahasa UI.


6. Implementasi RAG (Retrieval-Augmented Generation).




---

🤝 16. Kontribusi

Cara berkontribusi ke proyek ini:

1. Fork repo di GitHub.


2. Buat branch baru: feature/nama-fitur.


3. Commit perubahan dengan pesan jelas.


4. Push ke branch.


5. Buat Pull Request.




---

📜 17. Lisensi

MIT License © 2025 Farhan Kertadiwangsa


---

💙 18. Ucapan Terima Kasih

Komunitas open-source.

TailwindCSS untuk styling cepat.

GSAP untuk animasi halus.

Node.js & Express untuk backend.

Semua developer yang membantu berbagi ilmu.

