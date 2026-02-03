# Lampiran C: Kunci Jawaban Soal Latihan

---

Lampiran ini berisi kunci jawaban untuk soal latihan pilihan ganda di setiap bab. Untuk soal esai dan tantangan, hanya diberikan panduan atau poin-poin utama yang harus dijawab.

---

## BAB 1: Pengantar Kecerdasan Buatan

### Pilihan Ganda

1. **c) Sistem yang dapat belajar dan beradaptasi**
2. **c) Winter AI**
3. **b) Deep Blue**
4. **d) Natural Language Processing**
5. **b) Menggabungkan ML dengan reasoning**

### Panduan Esai

6. Machine Learning adalah subset AI yang fokus pada pembelajaran dari data, sementara DL adalah subset ML menggunakan neural networks dengan banyak layer.
7. AGI belum tercapai karena AI saat ini masih narrow — hanya bisa melakukan tugas spesifik, tidak generalisasi seperti manusia.
8. AI di Indonesia: e-commerce recommendation, chatbot customer service, fintech credit scoring.

---

## BAB 2: Dasar Algoritma dan Pemecahan Masalah

### Pilihan Ganda

1. **b) Memiliki langkah yang jelas dan terbatas**
2. **c) O(n log n)**
3. **a) Rekursi**
4. **b) O(n)**
5. **c) BFS**

### Panduan Esai

6. Rekursi: elegant tapi memori tinggi (call stack). Iterasi: lebih efisien memori tapi bisa lebih kompleks.
7. O(1) lebih baik saat data besar. n=10: O(n²)=100, O(1)=1. n=1000: O(n²)=1000000, O(1)=1.
8. Problem space untuk 8-puzzle: states adalah konfigurasi puzzle, actions adalah gerakan tile.

---

## BAB 3: Representasi Pengetahuan dalam AI

### Pilihan Ganda

1. **b) Propositional Logic**
2. **c) Semantic Networks**
3. **a) Ontology**
4. **c) Expert System**
5. **b) Fuzzy Logic**

### Panduan Esai

6. Frames menyimpan informasi dalam slot-value pairs dengan inheritance, mirip OOP. Contoh: Frame "Mobil" dengan slot merek, warna, tahun.
7. Certainty Factor digunakan ketika probabilitas tidak diketahui pasti atau sulit dihitung, seperti dalam diagnosis medis.
8. Forward chaining: dari fakta ke kesimpulan (data-driven). Backward chaining: dari goal ke fakta (goal-driven).

---

## BAB 4: Algoritma Pencarian

### Pilihan Ganda

1. **b) BFS**
2. **b) Admissible**
3. **c) Infinite loop**
4. **b) Lebih mungkin menerima langkah yang lebih buruk**
5. **c) Crossover**

### Panduan Esai

6. g(n) = actual cost dari start, h(n) = estimasi ke goal, f(n) = g(n) + h(n). Contoh: route finding dengan g = jarak tempuh, h = straight-line distance.
7. IDDFS menggabungkan completeness BFS dengan memory efficiency DFS. Overhead iterasi hanya ~11%.
8. Heuristic untuk 8-puzzle: Manhattan distance (jumlah gerakan horizontal+vertikal ke posisi benar). Admissible karena setiap tile minimal butuh sekian gerakan.

---

## BAB 5: Pengantar Machine Learning

### Pilihan Ganda

1. **c) Memprediksi harga saham**
2. **b) Overfitting**
3. **b) Mean = 0, Std = 1**
4. **b) Low bias, high variance**
5. **c) Reduksi dimensi**

### Panduan Esai

6. Supervised: data berlabel (spam detection). Unsupervised: tanpa label (clustering). RL: belajar dari reward (game AI).
7. Training untuk melatih, validation untuk tuning hyperparameter, test untuk evaluasi final. Tanpa split, tidak tahu generalization.
8. Data [100,200,300,400,500]: Min=100, Max=500, Mean=300, Std≈158. Normalization: [0, 0.25, 0.5, 0.75, 1]. Standardization: [-1.26, -0.63, 0, 0.63, 1.26].

---

## BAB 6: Algoritma Klasifikasi Dasar

### Pilihan Ganda

1. **b) Probabilitas antara 0 dan 1**
2. **b) Underfitting**
3. **b) Fitur independent satu sama lain**
4. **b) Menggabungkan banyak trees dengan randomization**
5. **c) Recall**

### Panduan Esai

6. KNN: jarak sensitif terhadap skala, perlu scaling. Decision Tree: berbasis perbandingan, skala tidak berpengaruh.
7. Dari confusion matrix: Accuracy = (80+70)/200 = 75%, Precision = 80/110 = 72.7%, Recall = 80/100 = 80%, F1 = 2×0.727×0.8/(0.727+0.8) = 76.2%.
8. Logistic Regression: asumsi linearity, interpretable, butuh scaling. Naive Bayes: asumsi independence, cepat, bagus untuk text.

---

## BAB 7: Algoritma Klastering

### Pilihan Ganda

1. **b) Within-cluster sum of squares**
2. **c) Cluster dengan density berbeda**
3. **c) Data mungkin salah cluster**
4. **c) Menentukan jumlah cluster**
5. **b) Minimum points untuk membentuk core point**

### Panduan Esai

6. K-Means mengasumsikan cluster spherical. Cluster bulan sabit tidak bisa dipisahkan dengan centroid. DBSCAN lebih cocok.
7. Data [1,2,8,9,10,25], k=2, C1=1, C2=25. Iterasi 1: Cluster {1,2,8,9,10} dan {25}. Update centroids. Iterasi 2: Cluster {1,2} dan {8,9,10,25}.
8. Gunakan k-distance graph: hitung jarak ke k-th nearest neighbor, plot ascending, cari elbow.

---

## BAB 8: Dasar Jaringan Saraf Tiruan

### Pilihan Ganda

1. **b) Masalah tidak linearly separable**
2. **c) Sigmoid dan Tanh**
3. **c) ReLU**
4. **b) Momentum dan RMSprop**
5. **b) Random mematikan neurons saat training**

### Panduan Esai

6. ReLU tidak saturate untuk nilai positif (gradient tetap 1), menghindari vanishing gradient. Sigmoid saturate di kedua ujung.
7. Vanishing gradient: gradient menjadi sangat kecil saat propagate mundur. Solusi: ReLU, batch normalization, skip connections.
8. Batch GD: stabil, lambat, memory tinggi. Mini-batch: balance, paling umum. Stochastic: noisy, cepat, bisa escape local minima.

---

## BAB 9: Evaluasi dan Optimasi Algoritma AI

### Pilihan Ganda

1. **a) 1 kali**
2. **b) Tidak semua hyperparameter penting**
3. **b) Variance**
4. **b) Boosting**
5. **c) Model interpretability**

### Panduan Esai

6. Bagging: parallel, reduce variance (Random Forest). Boosting: sequential, reduce bias (XGBoost).
7. Bayesian Optimization membangun model dari hasil sebelumnya dan memilih next point secara cerdas, tidak random.
8. Gap besar antara training dan validation score = overfitting. Jika berkurang dengan lebih banyak data, butuh data lebih.

---

## BAB 10: Etika dan Tantangan Algoritma AI

### Pilihan Ganda

1. **b) Keputusan bias menjadi data training baru**
2. **c) Proporsi prediksi positif sama**
3. **c) High risk**
4. **b) Menambah noise untuk proteksi individual**
5. **b) Input yang dirancang untuk menipu model**

### Panduan Esai

6. Impossibility theorem: tidak bisa memenuhi demographic parity, equal opportunity, dan calibration bersamaan (kecuali kasus khusus).
7. EU AI Act: Unacceptable (banned), High (regulated ketat), Limited (transparency), Minimal (bebas). High risk butuh human oversight.
8. Langkah: audit bias, check fairness metrics, ensure explainability, human-in-the-loop, regular monitoring, provide recourse.

---

_← [Lampiran B: Notasi dan Konvensi](./Lampiran-B-Notasi-dan-Konvensi.md) | [Daftar Pustaka](./Daftar-Pustaka.md) →_
