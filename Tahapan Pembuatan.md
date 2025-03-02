### 🔹 **Langkah 1: Setup Environment**

Kita akan membuat environment baru dan menginstall library yang dibutuhkan.

1️⃣ **Buat Virtual Environment**  
Jalankan perintah berikut di terminal:

```sh
python -m venv chatbot-env
```

Lalu aktifkan environment:

- **Bash:**
  ```bash
  source chatbot-env/Scripts/activate
  ```
- **Windows:**
  ```sh
  chatbot-env\Scripts\activate
  ```
- **Mac/Linux:**
  ```sh
  source chatbot-env/bin/activate
  ```

2️⃣ **Install Library yang Diperlukan**

```sh
pip install tensorflow flask twilio numpy pandas nltk
```

3️⃣ **Cek Apakah Semua Terinstal**

```sh
pip list
```

---

## 🔹 **Langkah 2: Persiapan Data**

Kita akan membuat dataset chatbot dalam format JSON, lalu mempersiapkan data untuk pelatihan model.

### 1️⃣ **Buat File dataset.json**

Buat file **dataset.json** dan masukkan contoh berikut:

```json
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": ["Halo", "Hai", "Apa kabar?", "Selamat pagi"],
      "responses": [
        "Halo!",
        "Hai, ada yang bisa saya bantu?",
        "Halo, bagaimana kabarmu?"
      ]
    },
    {
      "tag": "goodbye",
      "patterns": ["Sampai jumpa", "Dadah", "Selamat tinggal"],
      "responses": [
        "Sampai jumpa!",
        "Dadah, semoga harimu menyenangkan!",
        "Selamat tinggal, sampai ketemu lagi!"
      ]
    },
    {
      "tag": "thanks",
      "patterns": ["Terima kasih", "Makasih", "Thanks"],
      "responses": ["Sama-sama!", "Senang bisa membantu!", "Kapan saja!"]
    }
  ]
}
```

Dataset ini berisi **intents**, yaitu kategori percakapan dengan pola (patterns) dan respons yang mungkin diberikan oleh chatbot.

---

### 2️⃣ **Buat File 2_data_preparation.py**

Sekarang kita buat file **2_data_preparation.py** untuk membaca dan membersihkan dataset.

---

### 3️⃣ **Jalankan Script untuk Menyiapkan Data**

Jalankan perintah berikut di terminal:

```sh
python 2_data_preparation.py
```

Jika berhasil, kamu akan melihat output:  
✅ **"Data berhasil diproses dan disimpan!"**
