# 🦁 Animals Image Classification

## 📘 Pengertian Proyek
Proyek ini berfokus pada **klasifikasi citra hewan** menggunakan model *Convolutional Neural Network (CNN)* dan *EfficientNetB0*. Tujuannya adalah untuk membangun sistem yang mampu mengenali jenis hewan dari gambar secara otomatis dengan akurasi tinggi melalui pemrosesan citra, augmentasi data, dan teknik *deep learning* modern.

---

## 🧾 Deskripsi Proyek
Proyek ini mengimplementasikan pipeline lengkap untuk *image classification*, mulai dari eksplorasi data, analisis kualitas gambar, preprocessing, augmentasi, hingga pelatihan dan evaluasi model.  
Eksperimen dilakukan dengan dua pendekatan:
- **EfficientNetB0 (Transfer Learning)** — menggunakan bobot pra-latih dari *ImageNet* untuk efisiensi dan akurasi tinggi.  
- **Custom CNN** — dibangun dari awal untuk membandingkan performa dengan model pra-latih.

Model terbaik dipilih berdasarkan akurasi validasi tertinggi dan performa pengujian terhadap dataset uji.

---

## 📂 Dataset
Dataset terdiri dari **4 kelas hewan**:
- 🐃 **Buffalo**
- 🐘 **Elephant**
- 🦏 **Rhino**
- 🦓 **Zebra**


Jumlah total gambar: ±4.000 citra  
Data dibagi menjadi 80% untuk pelatihan dan 20% untuk pengujian.

---

## 🧰 Tools dan Teknologi
Proyek ini menggunakan beberapa pustaka dan framework berikut:
- **Python** 🐍  
- **TensorFlow / Keras** — untuk membangun dan melatih model deep learning  
- **Scikit-learn** — untuk evaluasi performa model  
- **Matplotlib & Seaborn** — untuk visualisasi data  
- **Pillow & Scikit-image** — untuk analisis kualitas gambar  
- **NumPy & Pandas** — untuk manipulasi data  
- **Grad-CAM** — untuk interpretasi visual area yang diperhatikan model

---

## 🧪 Tahapan Analisis

### 1️⃣ Load Data & Exploratory Data Analysis (EDA)
- Menampilkan distribusi label dan contoh citra dari setiap kelas.
- Analisis kualitas gambar: **Brightness, Contrast, Sharpness, dan Entropy**.
- Visualisasi distribusi fitur kualitas gambar untuk memahami variasi dataset.

### 2️⃣ Error Level Analysis (ELA)
- Digunakan untuk memeriksa tingkat kompresi gambar dan potensi anomali.
- Mengidentifikasi perbedaan tingkat kesalahan piksel untuk setiap tingkat kualitas JPEG.

### 3️⃣ Data Preprocessing & Augmentation
- Pembagian dataset menjadi *training*, *validation*, dan *testing set*.
- Penerapan augmentasi:
  - Rotasi acak, flipping, zooming, dan cropping.
  - Perubahan kontras, kecerahan, dan normalisasi.
- Meningkatkan generalisasi model terhadap berbagai variasi gambar.

### 4️⃣ Model Training & Hyperparameter Tuning
- Dua model utama:
  - **EfficientNetB0 (Transfer Learning)**
  - **Custom CNN**
- Hyperparameter yang diuji:
  - Learning Rate: `0.001`, `0.0001`
  - Dense Units: `128`, `256`
  - Dropout Rate: `0.5`
- Callback:
  - *EarlyStopping*, *ModelCheckpoint*, dan *ReduceLROnPlateau*
- Model terbaik: **EfficientNetB0**
  - Validation Accuracy: **99.38%**
  - Test Accuracy: **98.88%**

### 5️⃣ Model Evaluation
- Evaluasi dilakukan menggunakan **Confusion Matrix** dan **Classification Report**.
- Hasil menunjukkan performa stabil dengan nilai:
  - Precision: ~0.99  
  - Recall: ~0.99  
  - F1-score: ~0.99  

### 6️⃣ Prediction Result
- Visualisasi hasil prediksi terhadap gambar acak dari dataset uji.
- Warna **hijau** menunjukkan prediksi benar, **merah** menunjukkan prediksi salah.
- Contoh hasil prediksi: ['rhino', 'elephant', 'zebra', 'elephant', 'elephant']

---


### 7️⃣ Grad-CAM Visualization
- Visualisasi area fokus model pada gambar menggunakan *Gradient-weighted Class Activation Mapping (Grad-CAM)*.
- Membantu memahami bagian citra yang paling berpengaruh terhadap keputusan model.

---

## 📊 Hasil Akhir Analisis
- Model terbaik: **EfficientNetB0**
- Akurasi Pengujian: **98.88%**
- Kinerja tinggi dan stabil di semua kelas dengan distribusi seimbang.
- Penerapan transfer learning terbukti mempercepat pelatihan dan meningkatkan performa.

---

## 💡 Insight dan Manfaat
- Augmentasi data secara signifikan meningkatkan kemampuan generalisasi model.  
- Analisis kualitas citra membantu memahami karakteristik dataset dan potensi perbaikan.  
- Transfer learning dengan EfficientNetB0 sangat efisien untuk dataset berukuran sedang.  
- Model ini dapat digunakan sebagai dasar untuk sistem pengenalan hewan otomatis di bidang konservasi, zoologi, atau aplikasi edukatif berbasis citra.

---

## 🧭 Kesimpulan Akhir
Proyek **Animals Image Classification** berhasil menunjukkan implementasi lengkap pipeline *deep learning* untuk klasifikasi citra hewan dengan akurasi tinggi.  
Dengan kombinasi *data augmentation*, *transfer learning*, dan analisis mendalam, proyek ini memberikan bukti kuat akan efektivitas **EfficientNetB0** sebagai model modern dalam tugas *image recognition*.

---

## 👩‍💻 Author
**Rehana Putri**  
📍 Institut Teknologi Sepuluh Nopember (ITS)  
💼 Bidang: Machine Learning & Computer Vision

