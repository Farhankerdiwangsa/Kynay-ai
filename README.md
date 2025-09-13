
📘 README – Kynay Assistant

Dibuat oleh Farhan Kertadiwangsa


---

📑 Daftar Isi

1. Pendahuluan


2. Tentang Proyek


3. Fitur Utama

Fitur AI

Fitur Sistem



4. Arsitektur Aplikasi

Frontend (review.html)

Backend (backenjs)

Alur Data



5. Teknologi yang Digunakan


6. Instalasi & Setup

Persyaratan Sistem

Menjalankan Frontend

Menjalankan Backend



7. Dokumentasi API

Auth

Session

Chat



8. Fitur AI Detail

Ingatan (Memory)

Konteks Multi-Session

Auto-Rename Chat

Voice Recognition

Dark/Light Mode Adaptif



9. Keamanan


10. Pengembangan Lanjutan & Roadmap


11. Kontribusi


12. Lisensi


13. Ucapan Terima Kasih




---

🔰 Pendahuluan

Kynay Assistant adalah sebuah platform AI Assistant berbasis web yang dibangun dengan fokus pada user experience, keamanan, dan fleksibilitas pengembangan. Aplikasi ini memungkinkan pengguna untuk:

Melakukan login & registrasi.

Mengelola chat session secara interaktif.

Berkomunikasi dengan AI melalui teks maupun suara.

Menyimpan riwayat percakapan dengan sistem memory.

Mengubah tampilan antarmuka ke mode gelap/terang sesuai preferensi.


Proyek ini dirancang sebagai kerangka dasar yang bisa dikembangkan lebih lanjut, baik untuk kebutuhan personal AI assistant, customer service chatbot, maupun sistem AI berbasis SaaS.


---

📖 Tentang Proyek

Proyek ini terdiri dari dua komponen utama:

1. Frontend (review.html)

Dibangun menggunakan HTML, TailwindCSS, GSAP untuk tampilan interaktif.

Fitur login, register, dashboard, chat bubble, toast notification, sidebar session, dark/light mode, voice recognition.



2. Backend (backen.js)

Menggunakan Node.js + Express.js.

Menyediakan API untuk autentikasi, manajemen session, dan chat AI.

Autentikasi berbasis JWT, penyimpanan user & session di database.





---

✨ Fitur Utama

Fitur AI

🧠 Ingatan (Memory AI) → setiap sesi percakapan menyimpan riwayat sehingga AI bisa melanjutkan konteks.

📂 Multi-Session → pengguna bisa membuat beberapa sesi, berpindah antar sesi, mengganti nama, atau menghapusnya.

📝 Auto-Rename Chat → judul chat otomatis diganti berdasarkan pesan pertama.

🎤 Voice Input → pengguna dapat mengirim pesan melalui suara dengan SpeechRecognition API.

🔎 Search Chat → cari sesi lama berdasarkan nama.

🌙 Dark/Light Mode → UI otomatis menyesuaikan preferensi pengguna.


Fitur Sistem

🔑 Autentikasi: login & register dengan JWT.

🔔 Toast Notification: feedback real-time dengan animasi GSAP.

🖥 Dashboard Responsif: sidebar dinamis, chat bubble elegan.

📦 Persistensi Data: chat tersimpan di database.

🎨 UI Modern: ripple, shine effect, animasi halus.



---

🏗 Arsitektur Aplikasi

Frontend (review.html)

Berisi komponen:

Login/Register → form dengan validasi.

Dashboard → sidebar, chat area, message input.

Chat Bubble → desain berbeda untuk user & AI.

Modals → rename & delete chat.

Voice Recognition → integrasi mic input.


Backend (backen.js)

Terdiri dari:

Auth API (/auth/login, /auth/register).

Session API (/api/session).

Chat API (/api/chat/:sessionId/message).

Middleware JWT → autentikasi token.

Database Layer → menyimpan user, session, dan message.


Alur Data

1. User login → token JWT tersimpan.


2. User kirim pesan → frontend → backend /chat → AI response → frontend render bubble.


3. Setiap pesan disimpan di DB untuk memory.


4. Jika user ganti sesi, konteks chat di-load kembali.




---

🛠 Teknologi yang Digunakan

Frontend: HTML5, TailwindCSS, GSAP, FontAwesome, SpeechRecognition API.

Backend: Node.js, Express.js, JWT, bcrypt, Database (MongoDB/MySQL/Postgres).

Deployment: Vercel/Netlify (frontend), Render/Heroku/VPS (backend).



---

🔧 Instalasi & Setup

Persyaratan Sistem

Node.js ≥ 16.x

NPM ≥ 8.x

Database (MongoDB/MySQL/Postgres)

Browser modern


Menjalankan Frontend

git clone https://github.com/farhankertadiwangsa/kynay-assistant.git
cd kynay-assistant
# buka review.html dengan live server

Menjalankan Backend

cd backend
npm install
node backen.js

API tersedia di: http://localhost:2009


---

📡 Dokumentasi API

Auth

Register

POST /auth/register

{
  "username": "farhan",
  "password": "123456"
}

Respon:

{
  "ok": true,
  "token": "...",
  "user": { "id": 1, "username": "farhan" }
}

Login

POST /auth/login

{
  "username": "farhan",
  "password": "123456"
}


---

Session

Create Session

POST /api/session

{
  "title": "New Chat"
}

Get All Sessions

GET /api/session


---

Chat

Send Message

POST /api/chat/:sessionId/message

{
  "message": "Halo, apa kabar?"
}

Respon:

{
  "ok": true,
  "message": {
    "role": "assistant",
    "content": "Halo Farhan, saya baik. Bagaimana denganmu?",
    "ts": 1699987200
  }
}


---

🤖 Fitur AI Detail

Ingatan (Memory)

Short-term memory → chat dalam satu sesi.

Long-term memory → chat tersimpan di DB, bisa di-load ulang.


Konteks Multi-Session

User bisa membuat banyak sesi dengan konteks berbeda.

AI tetap mengingat isi percakapan hanya dalam satu sesi.


Auto-Rename Chat

Judul sesi otomatis berubah menjadi potongan dari pesan pertama.


Voice Recognition

Menggunakan SpeechRecognition API.

Bahasa default: id-ID.


Dark/Light Mode Adaptif

Toggle manual.

Preferensi tersimpan di localStorage.



---

🔒 Keamanan

Password hash dengan bcrypt.

JWT token untuk autentikasi API.

Validasi input (username/password).

Disarankan menambah:

Rate limiting.

HTTPS.

Helmet middleware.




---

🚀 Pengembangan Lanjutan & Roadmap

🔮 Integrasi dengan OpenAI/LLaMA API.

📄 Export chat ke PDF/Markdown.

🖼 Dukungan multimodal (gambar + teks).

🔔 Push notifikasi real-time (WebSocket).

🌍 Multi-bahasa untuk UI & AI.

📚 Retrieval-Augmented Generation (RAG) untuk akses knowledge base.



---

🤝 Kontribusi

1. Fork repo.


2. Buat branch (feature/namafitur).


3. Commit & push.


4. Pull request.




---

📜 Lisensi

MIT License © 2025 Farhan Kertadiwangsa


---

💙 Ucapan Terima Kasih

Terima kasih kepada:

TailwindCSS Team

GSAP Creators

Node.js & Express Community

Semua kontributor open-source
