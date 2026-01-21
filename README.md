🍎 Fruit Ripeness Detection using CNN (Xception)
Proyek ini mengembangkan sistem deteksi tingkat kematangan buah berbasis citra digital menggunakan metode Convolutional Neural Network (CNN) dengan arsitektur Xception sebagai model utama. Klasifikasi dilakukan ke dalam tiga kelas kematangan, yaitu unripe, ripe, dan overripe. Penelitian ini juga membandingkan performa model dengan InceptionV3 dan VGG19.

🎯 Tujuan Proyek
Mendeteksi tingkat kematangan buah secara otomatis dari citra digital
Menerapkan transfer learning untuk meningkatkan performa model
Membandingkan arsitektur CNN (Xception, InceptionV3, VGG19)
Mengevaluasi model menggunakan metrik klasifikasi yang komprehensif


🛠️ Teknologi yang Digunakan
Python
TensorFlow & Keras
NumPy, Pandas
Matplotlib & Seaborn
Scikit-learn

📘 Panduan Instalasi & Menjalankan Aplikasi
1. Clone repository
    git clone https://github.com/username/fruit-ripeness-detection.git
    cd fruit-ripeness-detection

2. Buat virtual environment (opsional)
    python -m venv venv
    source venv/bin/activate   # Linux / Mac
    venv\Scripts\activate      # Windows

3. Install dependencies
    pip install -r requirements.txt
Jika belum ada requirements.txt, gunakan:
    pip install tensorflow numpy pandas matplotlib seaborn scikit-learn


Aplikasi Deteksi Kematangan Buah (Web)
Panduan ini dibuat agar aplikasi dapat dijalankan di laptop mana pun tanpa mengubah kode.

⚠️ PENTING (WAJIB DIBACA)
Gunakan Python 3.10 (64-bit)
Jangan gunakan Python 3.11 / 3.12 / 3.13 (sering error TensorFlow)
Semua library sudah dikunci versinya di requirements.txt

1️⃣ Prasyarat
Pastikan sudah terinstal:
Python 3.10 (64-bit)
Python sudah dicentang Add to PATH
Cek versi:
    python --version
2️⃣ Masuk ke Folder Project
Buka CMD / Terminal, lalu:
    cd path/ke/folder/project
3️⃣ (Disarankan) Buat Virtual Environment
Agar library tidak bentrok dengan Python lain:
    python -m venv venv
Aktifkan:
Windows
    venv\Scripts\activate
    Mac / Linux
    source venv/bin/activate
4️⃣ Instal Library
    pip install -r requirements.txt
⏳ Proses ini bisa agak lama karena TensorFlow.
5️⃣ Struktur Folder Penting
Pastikan file model ada di:
    model/
    └── xception_224_0.0001_128_30.keras
6️⃣ Menjalankan Aplikasi
    python app.py
Buka browser:
  http://127.0.0.1:5000
📌 Saat pertama dijalankan, sistem akan mengunduh bobot ImageNet (~80MB).
Pastikan koneksi internet aktif.

📁 Struktur Folder Dataset
dataset_buah/
│
├── Train/
│   ├── Unripe/
│   ├── Ripe/
│   └── Overripe/
│
└── Test/
    ├── Unripe/
    ├── Ripe/
    └── Overripe/

🧪 Preprocessing & Augmentasi Data
    Resize citra ke 224 × 224 piksel
    Normalisasi nilai piksel (rescale 1/255)
    Image augmentation:
    Rotasi
    Pergeseran horizontal & vertikal
    Zoom
    Shearing
    Horizontal flip
    Penyesuaian kecerahan

🧠 Arsitektur Model
Model utama: Xception (pretrained ImageNet)
Model pembanding: InceptionV3, VGG19
Transfer Learning:
    Base model dibekukan (freeze)
Ditambahkan:  
    Global Average Pooling   
    Dense layer
    Dropout
    Softmax (3 kelas)

🚀 Pelatihan Model
    Optimizer: Adam
    Learning Rate: 0.001
    Batch Size: 64
    Epoch: 30
    Loss Function: Categorical Crossentropy

📊 Evaluasi Model
Evaluasi dilakukan menggunakan data uji dengan metrik:
    Categorical Accuracy
    Precision
    Recall
    AUC
    Confusion Matrix
    Classification Report
Hasil evaluasi digunakan untuk membandingkan performa Xception, InceptionV3, dan VGG19.

📈 Hasil
Model Xception menunjukkan performa paling stabil dan efisien dalam mendeteksi tingkat kematangan buah dibandingkan model pembanding, terutama dalam hal generalisasi dan efisiensi parameter.

🖼️ Dataset dapat diunduh melalui:
https://www.kaggle.com/datasets/asadullahprl/fruits-ripeness-classification-dataset/data

📘 Mahasiswa Teknik Informatika Semester 5 

