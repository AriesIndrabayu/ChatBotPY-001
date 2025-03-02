# Chatbot Virtual Pintar Sederhana

Chatbot Virtual Pintar ini adalah chatbot berbasis **Python** yang memiliki **memori** untuk menyimpan percakapan dan dapat **terintegrasi dengan WhatsApp** menggunakan **Twilio API** atau **yowsup**.

## 🚀 Fitur Utama

- **Memori Percakapan**: Chatbot dapat mengingat konteks percakapan sebelumnya.
- **Pembelajaran Mesin**: Menggunakan **TensorFlow & LSTM** untuk memahami pertanyaan.
- **Dukungan JSON Dataset**: Intent chatbot didefinisikan dalam file JSON.
- **Integrasi WhatsApp**: Chatbot bisa digunakan langsung melalui WhatsApp.
- **API RESTful**: Dibangun dengan **Flask** untuk integrasi dengan aplikasi lain.

## 📂 Struktur Proyek

```
Chatbot-Virtual-Pintar/
│-- dataset.json            # Dataset intents untuk chatbot
│-- 1_setup_environment.sh  # Setup environment dan install library
│-- 2_data_preparation.py   # Menyiapkan dan membersihkan data
│-- 3_train_model.py        # Melatih model chatbot menggunakan TensorFlow
│-- 4_chatbot_response.py   # Mengelola respons chatbot
│-- 5_api_server.py         # Menyediakan API REST untuk chatbot
│-- 6_main.py               # File utama untuk menjalankan chatbot
│-- 7_whatsapp_bot.py       # Integrasi chatbot dengan WhatsApp
│-- models/chatbot_model.h5 # Model yang sudah dilatih
```

## 🔧 Instalasi dan Konfigurasi

### 1️⃣ Persiapan Lingkungan

Jalankan script setup untuk menginstall dependensi:

```sh
bash 1_setup_environment.sh
```

Atau secara manual:

```sh
pip install tensorflow flask twilio numpy pandas nltk
```

### 2️⃣ Latih Model Chatbot

Jalankan script untuk melatih model chatbot:

```sh
python 3_train_model.py
```

### 3️⃣ Jalankan Chatbot

Untuk mengaktifkan chatbot lokal:

```sh
python 6_main.py
```

Chatbot sekarang dapat menerima input dari terminal.

### 4️⃣ Jalankan API untuk Integrasi

```sh
python 5_api_server.py
```

API berjalan di `http://localhost:5000`.

### 5️⃣ Integrasi WhatsApp

#### 🔹 Dengan Twilio API

1. Daftar akun di [Twilio](https://www.twilio.com/whatsapp).
2. Buat file `.env` dengan kredensial Twilio:
   ```sh
   TWILIO_ACCOUNT_SID=your_account_sid
   TWILIO_AUTH_TOKEN=your_auth_token
   TWILIO_PHONE_NUMBER=whatsapp:+your_twilio_number
   ```
3. Jalankan bot WhatsApp:
   ```sh
   python 7_whatsapp_bot.py
   ```

#### 🔹 Dengan Yowsup (Alternatif)

1. Install `yowsup`:
   ```sh
   pip install yowsup2
   ```
2. Konfigurasi akun WhatsApp.
3. Jalankan bot dengan Yowsup:
   ```sh
   python 7_whatsapp_bot.py
   ```

## 📌 API Endpoint

| Endpoint | Method | Deskripsi                   |
| -------- | ------ | --------------------------- |
| `/chat`  | POST   | Mengirim pesan ke chatbot   |
| `/train` | GET    | Melatih ulang model chatbot |

## 📜 Lisensi

Proyek ini menggunakan lisensi **MIT**. Silakan digunakan dan dikembangkan lebih lanjut.

---

🎯 **Dikembangkan oleh Aries Indrabayu**
