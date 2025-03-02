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
