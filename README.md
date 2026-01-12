# Analisis Sentimen, Hate Speech, dan Chatbot Puisi Transformer
## Klasifikasi Ujaran Kebencian dan Analisis Sentimen Menggunakan Arsitektur RNN dan Transformer

---

## 📋 Daftar Isi
- [Anggota Kelompok](#anggota-kelompok)
- [Pendahuluan](#pendahuluan)
- [Deskripsi Project](#deskripsi-project)
- [Struktur Folder](#struktur-folder)
- [Dataset](#dataset)
- [Setup dan Instalasi](#setup-dan-instalasi)
- [Cara Menggunakan](#cara-menggunakan)
- [Model dan Hasil](#model-dan-hasil)
- [Referensi](#referensi)

---

## 👥 Anggota Kelompok

| No | Nama | NIM |
|----|------|-----|
| 1 | Zakiyah Hasanah | 2305274 |
| 2 | Putra Hadiyanto Nugroho | 2308163 |
| 3 | Hafsah Hamidah | 2311474 |
| 4 | Natasha Adinda Cantika | 2312120 |

**Universitas:** Universitas Pendidikan Indonesia (UPI)  
**Mata Kuliah:** Deep Learning - Semester 5  
**Tahun Akademik:** 2024/2025

---

## 🎯 Pendahuluan

Fenomena **ujaran kebencian (*Hate Speech*)** di media sosial, khususnya Twitter, telah menjadi tantangan serius dalam menjaga ruang publik yang sehat di Indonesia. Ujaran kebencian merupakan salah satu bentuk **sentimen negatif ekstrem** yang perlu dideteksi dan diklasifikasikan secara otomatis.

Project ini bertujuan untuk:
1. Mengimplementasikan dan membandingkan kinerja berbagai arsitektur *Deep Learning* dalam klasifikasi ujaran kebencian
2. Memahami perbedaan antara arsitektur RNN tradisional (SimpleRNN, LSTM, Bidirectional LSTM) dengan arsitektur Transformer
3. Membangun chatbot yang mampu menganalisis sentimen puisi menggunakan Transformer

---

## 📝 Deskripsi Project

Project ini terdiri dari tiga komponen utama:

### 1. **Klasifikasi Ujaran Kebencian dengan RNN dan LSTM**
   - **File:** `Tugas 2 - Klasifikasi Sentimen (RNN dan LSTM) revisi pakai dataset baru.ipynb`
   - **Tujuan:** Membandingkan performa SimpleRNN, LSTM, dan Bidirectional LSTM
   - **Fitur:**
     - Preprocessing mendalam (case folding, normalisasi alay, pembersihan noise)
     - Visualisasi dan eksplorasi data (Word Cloud, distribusi kelas)
     - Training dan evaluasi model RNN
     - Perbandingan metrik akurasi, precision, recall, dan F1-Score

### 2. **Klasifikasi Sentimen dengan Arsitektur Transformer**
   - **File:** `Tugas 3 - Klasifikasi Sentimen Transformer.ipynb`
   - **Tujuan:** Mengimplementasikan Transformer Encoder untuk klasifikasi hate speech
   - **Fitur:**
     - Implementasi Attention Mechanism
     - Perbandingan Transformer dengan arsitektur RNN
     - Analisis performa pada ketergantungan konteks jarak jauh
     - Evaluasi model dengan metrik komprehensif

### 3. **Chatbot Analisis Sentimen Puisi**
   - **File:** `Tugas 3 - Chatbot Puisi Transformer.ipynb`
   - **Tujuan:** Membangun chatbot yang menganalisis sentimen pada puisi menggunakan Transformer
   - **Fitur:**
     - Text generation menggunakan Transformer
     - Analisis sentimen pada puisi Indonesia
     - Interactive chatbot interface
     - Pemahaman konteks puisi yang mendalam

---

## 📁 Struktur Folder

```
Analisis-Sentimen-Sentiment-Analysis-dan-Chatbot/
├── README.md                                              # File dokumentasi ini
├── data_hate_speech.csv                                   # Dataset ujaran kebencian
├── new_kamusalay.csv                                      # Kamus normalisasi kata alay
├── puisi.csv                                              # Dataset puisi untuk chatbot
├── Tugas 2 - Klasifikasi Sentimen (RNN dan LSTM)...ipynb # Implementasi RNN/LSTM
├── Tugas 3 - Klasifikasi Sentimen Transformer.ipynb      # Implementasi Transformer
└── Tugas 3 - Chatbot Puisi Transformer.ipynb             # Chatbot puisi
```

---

## 📊 Dataset

### Dataset Hate Speech
**Sumber:** [Kaggle - Indonesian Abusive and Hate Speech Twitter Text](https://www.kaggle.com/datasets/ilhamfp31/indonesian-abusive-and-hate-speech-twitter-text)

**Deskripsi:**
- Dataset tweet berbahasa Indonesia dengan label hate speech dan abusive language
- Format: Multi-label classification
- Label utama:
  - **HS (Hate Speech):** 1 = Hate Speech, 0 = Non-Hate Speech
  - **Abusive:** 1 = Abusive Language, 0 = Non-Abusive
  - **HS_Individual, HS_Group, HS_Religion, dll.:** Label spesifik tipe hate speech

**Kamus Normalisasi (`new_kamusalay.csv`):**
- Mapping dari kata tidak baku/alay ke kata baku
- Digunakan untuk normalisasi teks selama preprocessing

**Dataset Puisi (`puisi.csv`):**
- Koleksi puisi berbahasa Indonesia
- Digunakan untuk training chatbot analisis sentimen puisi

### Sitasi Akademik
```
Muhammad Okky Ibrohim and Indra Budi. 2019. 
"Multi-label Hate Speech and Abusive Language Detection in Indonesian Twitter." 
In ALW3: 3rd Workshop on Abusive Language Online, 46-57.
```

---

## 🔧 Setup dan Instalasi

### Prasyarat
- Python 3.7 atau lebih tinggi
- Jupyter Notebook atau JupyterLab
- pip (Python package manager)

### Instalasi Library
```bash
# Install dependencies utama
pip install pandas numpy matplotlib seaborn
pip install nltk wordcloud Pillow tqdm
pip install tensorflow scikit-learn
pip install jupyterlab

# Download NLTK data (punkt tokenizer)
python -c "import nltk; nltk.download('punkt')"
```

### Instalasi Lengkap (Recommended)
```bash
# Buat virtual environment (opsional)
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

# Install semua dependencies
pip install -r requirements.txt  # jika ada file requirements.txt
# atau
pip install pandas numpy matplotlib seaborn nltk wordcloud Pillow tqdm tensorflow scikit-learn
```

---

## 🚀 Cara Menggunakan

### 1. Menjalankan Notebook Klasifikasi RNN/LSTM
```bash
jupyter notebook "Tugas 2 - Klasifikasi Sentimen (RNN dan LSTM) revisi pakai dataset baru.ipynb"
```

**Langkah-langkah:**
1. Jalankan sel-sel secara berurutan untuk loading dataset
2. Ikuti preprocessing text
3. Training model SimpleRNN, LSTM, dan Bidirectional LSTM
4. Evaluasi dan bandingkan hasil

### 2. Menjalankan Notebook Transformer
```bash
jupyter notebook "Tugas 3 - Klasifikasi Sentimen Transformer.ipynb"
```

**Langkah-langkah:**
1. Load dataset hate speech
2. Implement Transformer Encoder architecture
3. Train dan evaluate model
4. Bandingkan dengan RNN models

### 3. Menjalankan Chatbot Puisi
```bash
jupyter notebook "Tugas 3 - Chatbot Puisi Transformer.ipynb"
```

**Langkah-langkah:**
1. Load dataset puisi
2. Training Transformer untuk text generation
3. Implementasi chatbot interface
4. Test dengan input puisi custom

---

## 📈 Model dan Hasil

### Arsitektur Model

#### RNN/LSTM Models
| Model | Tipe | Keunggulan | Kelemahan |
|-------|------|-----------|----------|
| SimpleRNN | Basic RNN | Sederhana, cepat training | Sulit menangkap long-term dependencies |
| LSTM | RNN variant | Mengatasi vanishing gradient | Lebih complex |
| Bidirectional LSTM | 2-way LSTM | Konteks dua arah | Lebih lambat, lebih parameters |

#### Transformer Model
| Model | Tipe | Keunggulan | Kelemahan |
|-------|------|-----------|----------|
| Transformer Encoder | Attention-based | Excellent untuk long-range dependencies, parallelizable | Lebih complex, butuh lebih banyak data |

### Metrik Evaluasi
- **Accuracy:** Persentase prediksi yang benar
- **Precision:** Dari yang diprediksi positif, berapa yang benar-benar positif
- **Recall:** Dari yang sebenarnya positif, berapa yang terdeteksi
- **F1-Score:** Harmonic mean dari precision dan recall

### Expected Results
Model Transformer umumnya menghasilkan performa lebih baik dalam:
- Menangkap konteks jarak jauh dalam teks
- Memahami nuansa bahasa Indonesia yang kompleks
- Generalizing ke data yang belum pernah dilihat

---

## 🛠️ Tech Stack

### Data Processing & Analysis
- **pandas:** Data manipulation
- **numpy:** Numerical computing
- **scikit-learn:** Machine learning utilities

### NLP & Text Processing
- **NLTK:** Natural Language Processing
- **WordCloud:** Visualisasi kata-kata dominan

### Deep Learning
- **TensorFlow/Keras:** Deep learning framework
- **Custom Transformer Implementation:** Attention mechanism

### Visualization
- **matplotlib:** Plotting dan visualisasi
- **seaborn:** Statistical data visualization

---

## 📚 Referensi

### Paper dan Publikasi
1. Ibrohim, M. O., & Budi, I. (2019). Multi-label Hate Speech and Abusive Language Detection in Indonesian Twitter. In ALW3: 3rd Workshop on Abusive Language Online (pp. 46-57).

2. Vaswani, A., et al. (2017). Attention Is All You Need. NeurIPS 2017.
   - Landmark paper untuk Transformer architecture

### Dataset Reference
- Kaggle Dataset: [Indonesian Abusive and Hate Speech Twitter Text](https://www.kaggle.com/datasets/ilhamfp31/indonesian-abusive-and-hate-speech-twitter-text)

### Dokumentasi Penting
- [TensorFlow Documentation](https://www.tensorflow.org/api_docs)
- [Keras Documentation](https://keras.io/)
- [NLTK Documentation](https://www.nltk.org/)

---

## 💡 Tips dan Best Practices

1. **Memory Management:** Jika mengalami out of memory, kurangi batch size atau gunakan GPU
2. **Data Augmentation:** Pertimbangkan augmentasi data untuk meningkatkan generalisasi
3. **Early Stopping:** Gunakan untuk mencegah overfitting
4. **Model Checkpointing:** Simpan model terbaik selama training

---

## 🤝 Kontribusi dan Feedback

Untuk pertanyaan atau saran perbaikan, silakan hubungi anggota kelompok:
- Zakiyah Hasanah
- Putra Hadiyanto Nugroho
- Hafsah Hamidah
- Natasha Adinda Cantika

---

## 📄 Lisensi

Project ini dibuat untuk keperluan akademik Universitas Pendidikan Indonesia.

---

**Last Updated:** Januari 2025  
**Status:** Completed

