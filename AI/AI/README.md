---
title: Nutrify AI API
emoji: 🥗
colorFrom: green
colorTo: blue
sdk: docker
app_port: 7860
---

# 🍽️ Nutrify AI — Indonesian Food Recognition & Nutrition API

## 📌 Deskripsi Proyek
**Nutrify AI API** adalah layanan **FastAPI** yang mengenali makanan tradisional Indonesia dari gambar menggunakan model **CNN (TensorFlow / Keras)**, lalu memberikan informasi nutrisi beserta rekomendasi berbasis **Gemini LLM**. Project ini merupakan bagian dari **Capstone Project tim AI Engineer (CC26-PSU017)** — DBS Coding Camp 2026.

---

## 🧠 Fitur Utama
- 🔍 **Food Recognition** — klasifikasi gambar makanan Indonesia dengan model CNN
- 🥗 **Nutrition Lookup** — info nutrisi dari database TKPI (Kemenkes)
- 🤖 **Chat & Recommendation** — chatbot & rekomendasi makanan berbasis Gemini LLM
- ⚡ **REST API** — endpoint cepat berbasis FastAPI, siap dikonsumsi frontend (React/Express)

---

## 🗂️ Struktur Proyek
```
nutrify-ai-api/
├── app/
│   ├── core/           # config (pydantic-settings)
│   ├── routers/        # definisi endpoint
│   ├── services/       # cnn_services, gemini, dependencies
│   ├── schemas/        # request/response models
│   └── main.py         # entry point FastAPI
├── nutrify_model.keras # model CNN (Git LFS)
├── class_names.json    # daftar label kelas makanan
├── indonesian_food_clean.csv  # database nutrisi (TKPI)
├── requirements.txt
├── Dockerfile
├── .env.example
└── README.md
```

---

## 📊 Sumber Data
Database nutrisi: `indonesian_food_clean.csv` — bersumber dari **TKPI (Tabel Komposisi Pangan Indonesia, Kemenkes)**.

| Kolom | Deskripsi |
|-------|-----------|
| `food_name` | Nama makanan |
| `calories` | Energi per 100 g (kkal) |
| `protein` | Protein per 100 g (g) |
| `fat` | Lemak per 100 g (g) |
| `carbohydrates` | Karbohidrat per 100 g (g) |

---

## 🔌 Endpoint API

### System
| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| `GET` | `/` | Root / info API |
| `GET` | `/health-check` | Cek status service |

### Food Data
| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| `GET` | `/search-food` | Cari makanan di database nutrisi |
| `GET` | `/units` | Daftar satuan (units) |
| `GET` | `/disease` | Daftar penyakit untuk rekomendasi |

### Predictions
| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| `POST` | `/predict` | Prediksi makanan dari gambar (upload file) |

### Chat
| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| `POST` | `/chat/` | Kirim pesan chat & rekomendasi (Gemini) |
| `GET` | `/chat/history/{conversation_id}` | Ambil riwayat percakapan |

> 📖 Dokumentasi interaktif lengkap tersedia di `/docs` (Swagger UI).

**Contoh request `/predict`:**
```bash
curl -X POST https://damassdev-nutrify-ai-api.hf.space/predict \
  -F "file=@nasi_goreng.jpg"
```


## 🚀 Cara Menjalankan

### 1. Clone Repository
```bash
git clone https://github.com/coding-camp-project/AI.git
cd AI
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Jalankan (lokal)
```bash
uvicorn app.main:app --host 0.0.0.0 --port 7860 --reload
```
> Sesuaikan `app.main:app` dengan entry point di Dockerfile kamu.

### 4. Atau pakai Docker
```bash
docker build -t nutrify-ai-api .
docker run -p 7860:7860 nutrify-ai-api
```

### 5. Buka di Browser
```
http://localhost:7860/docs
```
> FastAPI otomatis menyediakan dokumentasi interaktif di `/docs` (Swagger UI).
```

