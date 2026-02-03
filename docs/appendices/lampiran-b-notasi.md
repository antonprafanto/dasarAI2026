# Lampiran B: Notasi dan Konvensi

---

Lampiran ini menjelaskan notasi dan konvensi yang digunakan secara konsisten di seluruh buku ini. Gunakan sebagai referensi cepat saat membaca.

---

## B.1 Notasi Umum

### B.1.1 Skalar, Vektor, dan Matriks

| Notasi                       | Tipe                           | Contoh                            |
| ---------------------------- | ------------------------------ | --------------------------------- |
| $x$, $y$, $\alpha$, $\beta$  | Skalar (huruf kecil miring)    | $x = 5$, $\alpha = 0.01$          |
| $\mathbf{x}$, $\mathbf{w}$   | Vektor (huruf kecil tebal)     | $\mathbf{x} = [1, 2, 3]^T$        |
| $A$, $W$, $X$                | Matriks (huruf kapital miring) | $W \in \mathbb{R}^{m \times n}$   |
| $\mathcal{X}$, $\mathcal{D}$ | Himpunan (huruf kaligrafi)     | $\mathcal{D} = \{x_1, x_2, ...\}$ |

### B.1.2 Subskrip dan Superskrip

| Notasi    | Arti                                   |
| --------- | -------------------------------------- |
| $x_i$     | Elemen ke-i dari vektor x              |
| $A_{ij}$  | Elemen baris i, kolom j dari matriks A |
| $x^{(t)}$ | Nilai x pada iterasi/waktu t           |
| $a^{[l]}$ | Aktivasi di layer l (neural networks)  |
| $W^{[l]}$ | Weight matrix di layer l               |
| $\hat{y}$ | Nilai prediksi (hat = prediksi)        |

### B.1.3 Operator Matematika

| Notasi           | Nama           | Arti                     |
| ---------------- | -------------- | ------------------------ |
| $\sum$           | Sigma          | Penjumlahan              |
| $\prod$          | Pi             | Perkalian                |
| $\nabla$         | Nabla/Del      | Gradient                 |
| $\partial$       | Del parsial    | Turunan parsial          |
| $\|\mathbf{x}\|$ | Norm           | Panjang vektor           |
| $\|A\|_F$        | Frobenius norm | Norm matriks             |
| $\mathbf{x}^T$   | Transpose      | Transpose vektor/matriks |
| $A^{-1}$         | Inverse        | Invers matriks           |
| $\odot$          | Hadamard       | Perkalian element-wise   |
| $\circ$          | Komposisi      | Komposisi fungsi         |

---

## B.2 Notasi Machine Learning

### B.2.1 Dataset

| Notasi             | Arti                   |
| ------------------ | ---------------------- |
| $\mathcal{D}$      | Dataset                |
| $n$                | Jumlah sampel          |
| $d$ atau $p$       | Jumlah fitur/dimensi   |
| $\mathbf{x}^{(i)}$ | Sampel ke-i            |
| $y^{(i)}$          | Label sampel ke-i      |
| $X$                | Matriks desain (n × d) |
| $\mathbf{y}$       | Vektor label           |

### B.2.2 Model dan Parameter

| Notasi                      | Arti                      |
| --------------------------- | ------------------------- |
| $\theta$                    | Parameter model (generik) |
| $\mathbf{w}$                | Vektor weight             |
| $b$                         | Bias                      |
| $\hat{y}$ atau $\hat{f}(x)$ | Prediksi model            |
| $h_\theta(x)$               | Hypothesis function       |
| $f_\theta(x)$               | Model dengan parameter θ  |

### B.2.3 Fungsi Loss dan Objektif

| Notasi                       | Arti                    |
| ---------------------------- | ----------------------- |
| $L(\theta)$ atau $J(\theta)$ | Loss/Cost function      |
| $\mathcal{L}(y, \hat{y})$    | Loss untuk satu sampel  |
| $\mathcal{R}(\theta)$        | Regularization term     |
| $\lambda$                    | Regularization strength |

### B.2.4 Hyperparameters

| Notasi               | Arti                                   | Typical Values   |
| -------------------- | -------------------------------------- | ---------------- |
| $\eta$ atau $\alpha$ | Learning rate                          | 0.001, 0.01, 0.1 |
| $k$                  | Jumlah neighbors (KNN) atau folds (CV) | 3, 5, 10         |
| $m$                  | Jumlah trees (ensemble)                | 100, 500         |
| $\epsilon$           | Epsilon (threshold kecil)              | 1e-8             |
| $\beta_1$, $\beta_2$ | Momentum parameters (Adam)             | 0.9, 0.999       |

---

## B.3 Notasi Neural Networks

### B.3.1 Arsitektur

| Notasi             | Arti                                                      |
| ------------------ | --------------------------------------------------------- |
| $L$                | Jumlah layer (tidak termasuk input)                       |
| $n^{[l]}$          | Jumlah neuron di layer l                                  |
| $W^{[l]}$          | Weight matrix layer l (shape: $n^{[l]} \times n^{[l-1]}$) |
| $\mathbf{b}^{[l]}$ | Bias vector layer l                                       |
| $\mathbf{z}^{[l]}$ | Pre-activation (linear combination)                       |
| $\mathbf{a}^{[l]}$ | Activation (output setelah non-linearity)                 |
| $g^{[l]}$          | Activation function di layer l                            |

### B.3.2 Forward/Backward Propagation

| Notasi                                | Arti                           |
| ------------------------------------- | ------------------------------ |
| $\delta^{[l]}$                        | Error term di layer l          |
| $\frac{\partial L}{\partial W^{[l]}}$ | Gradient loss terhadap weights |
| $\nabla_W L$                          | Gradient (vektor)              |

---

## B.4 Notasi Probabilitas

| Notasi                       | Arti                        |
| ---------------------------- | --------------------------- |
| $P(A)$                       | Probabilitas event A        |
| $P(A\|B)$                    | Probabilitas A given B      |
| $P(A \cap B)$                | Probabilitas A dan B        |
| $P(A \cup B)$                | Probabilitas A atau B       |
| $\mathbb{E}[X]$              | Expected value (ekspektasi) |
| $\text{Var}(X)$              | Variance                    |
| $\sigma$                     | Standard deviation          |
| $\mathcal{N}(\mu, \sigma^2)$ | Distribusi normal           |
| $X \sim P$                   | X mengikuti distribusi P    |

---

## B.5 Konvensi Penulisan

### B.5.1 Pseudocode

**Struktur dasar:**

```
FUNGSI NamaFungsi(parameter1, parameter2):
    // Komentar
    variabel ← nilai

    JIKA kondisi:
        aksi
    LAINNYA:
        aksi_lain

    SELAMA kondisi:
        aksi

    UNTUK i DARI 1 SAMPAI n:
        aksi

    KEMBALIKAN hasil
```

**Kata kunci:**
| Bahasa Indonesia | Bahasa Inggris |
|------------------|----------------|
| FUNGSI | FUNCTION |
| JIKA | IF |
| LAINNYA | ELSE |
| SELAMA | WHILE |
| UNTUK | FOR |
| KEMBALIKAN | RETURN |
| DAN | AND |
| ATAU | OR |
| TIDAK | NOT |

### B.5.2 Kompleksitas Waktu (Big-O)

| Notasi     | Nama         | Contoh                  |
| ---------- | ------------ | ----------------------- |
| O(1)       | Constant     | Array access            |
| O(log n)   | Logarithmic  | Binary search           |
| O(n)       | Linear       | Linear search           |
| O(n log n) | Linearithmic | Merge sort              |
| O(n²)      | Quadratic    | Bubble sort             |
| O(2^n)     | Exponential  | Brute force subset      |
| O(n!)      | Factorial    | Brute force permutation |

### B.5.3 Diagram dan Visualisasi

**Simbol dalam diagram:**
| Simbol | Arti |
|--------|------|
| ○ | Node/Neuron |
| ● | Filled node (different class) |
| → | Connection/Edge |
| ═══ | Strong connection |
| - - - | Dashed (optional/conditional) |
| [ ] | Box (step/process) |
| ◇ | Decision point |

---

## B.6 Akronim dan Singkatan

| Singkatan   | Kepanjangan                           |
| ----------- | ------------------------------------- |
| AI          | Artificial Intelligence               |
| ML          | Machine Learning                      |
| DL          | Deep Learning                         |
| NN          | Neural Network                        |
| ANN         | Artificial Neural Network             |
| MLP         | Multi-Layer Perceptron                |
| CNN         | Convolutional Neural Network          |
| RNN         | Recurrent Neural Network              |
| SGD         | Stochastic Gradient Descent           |
| KNN         | K-Nearest Neighbors                   |
| SVM         | Support Vector Machine                |
| PCA         | Principal Component Analysis          |
| NLP         | Natural Language Processing           |
| CV          | Cross-Validation atau Computer Vision |
| TP/TN/FP/FN | True/False Positive/Negative          |
| MSE         | Mean Squared Error                    |
| BCE         | Binary Cross-Entropy                  |
| ReLU        | Rectified Linear Unit                 |
| GPU         | Graphics Processing Unit              |
| API         | Application Programming Interface     |

---

## B.7 Daftar Simbol Yunani

| Huruf       | Nama    | Penggunaan Umum                   |
| ----------- | ------- | --------------------------------- |
| α (alpha)   | alfa    | Learning rate                     |
| β (beta)    | beta    | Momentum parameter                |
| γ (gamma)   | gamma   | Discount factor, kernel parameter |
| δ (delta)   | delta   | Error term, small difference      |
| ε (epsilon) | epsilon | Small number, neighborhood radius |
| η (eta)     | eta     | Learning rate                     |
| θ (theta)   | theta   | Model parameters                  |
| λ (lambda)  | lambda  | Regularization, eigenvalue        |
| μ (mu)      | mu      | Mean                              |
| σ (sigma)   | sigma   | Standard deviation, sigmoid       |
| τ (tau)     | tau     | Temperature                       |
| φ (phi)     | phi     | Activation function, feature map  |
| ω (omega)   | omega   | Angular frequency                 |
| Σ (Sigma)   | Sigma   | Summation                         |
| Π (Pi)      | Pi      | Product                           |
| ∇ (nabla)   | nabla   | Gradient                          |

---

_← [Lampiran A: Prasyarat Matematika](./Lampiran-A-Prasyarat-Matematika.md) | [Lampiran C: Kunci Jawaban Soal Latihan](./Lampiran-C-Kunci-Jawaban-Soal-Latihan.md) →_
