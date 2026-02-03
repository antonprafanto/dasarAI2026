# Lampiran A: Prasyarat Matematika

---

Lampiran ini menyediakan review singkat tentang konsep matematika yang digunakan dalam buku ini. Jika Anda merasa perlu memperkuat fondasi ini, kami sarankan untuk mempelajari lebih lanjut dari sumber-sumber yang dicantumkan di akhir lampiran.

---

## A.1 Aljabar Linear

### A.1.1 Vektor

**Vektor** adalah array 1-dimensi dari bilangan.

**Notasi:**
$$\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$$

**Operasi dasar:**

- **Penjumlahan**: $\mathbf{x} + \mathbf{y} = [x_1+y_1, x_2+y_2, ...]$
- **Perkalian skalar**: $c\mathbf{x} = [cx_1, cx_2, ...]$
- **Dot product**: $\mathbf{x} \cdot \mathbf{y} = \sum_{i} x_i y_i$
- **Norm (panjang)**: $\|\mathbf{x}\| = \sqrt{\sum_{i} x_i^2}$

### A.1.2 Matriks

**Matriks** adalah array 2-dimensi dari bilangan.

**Notasi:**
$$A = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \cdots & a_{mn} \end{bmatrix}$$

**Operasi dasar:**

- **Perkalian matriks-vektor**: $A\mathbf{x}$ menghasilkan vektor
- **Perkalian matriks-matriks**: $AB$ (kolom A = baris B)
- **Transpose**: $A^T$ (baris ↔ kolom)

### A.1.3 Eigenvalues dan Eigenvectors

Untuk matriks A, jika:
$$A\mathbf{v} = \lambda\mathbf{v}$$

Maka λ adalah **eigenvalue** dan **v** adalah **eigenvector**.

**Aplikasi dalam AI**: PCA, stability analysis

---

## A.2 Kalkulus

### A.2.1 Turunan (Derivative)

Turunan mengukur **laju perubahan** fungsi.

$$f'(x) = \frac{df}{dx} = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

**Aturan dasar:**
| Fungsi | Turunan |
|--------|---------|
| $x^n$ | $nx^{n-1}$ |
| $e^x$ | $e^x$ |
| $\ln(x)$ | $1/x$ |
| $f(g(x))$ | $f'(g(x)) \cdot g'(x)$ (Chain rule) |

### A.2.2 Turunan Parsial

Untuk fungsi multi-variabel $f(x, y)$:

$$\frac{\partial f}{\partial x} = \lim_{h \to 0} \frac{f(x+h, y) - f(x, y)}{h}$$

**Contoh**: $f(x,y) = x^2 + 3xy$

- $\frac{\partial f}{\partial x} = 2x + 3y$
- $\frac{\partial f}{\partial y} = 3x$

### A.2.3 Gradient

**Gradient** adalah vektor dari semua turunan parsial:

$$\nabla f = \begin{bmatrix} \frac{\partial f}{\partial x_1} \\ \frac{\partial f}{\partial x_2} \\ \vdots \end{bmatrix}$$

Gradient menunjukkan **arah kenaikan tercepat** dari fungsi.

### A.2.4 Chain Rule untuk Backpropagation

Jika $y = f(g(x))$:

$$\frac{dy}{dx} = \frac{dy}{dg} \cdot \frac{dg}{dx}$$

Ini adalah dasar dari backpropagation dalam neural networks.

---

## A.3 Probabilitas dan Statistik

### A.3.1 Dasar Probabilitas

**Aksioma Probabilitas:**

1. $0 \leq P(A) \leq 1$
2. $P(\Omega) = 1$ (sample space)
3. $P(A \cup B) = P(A) + P(B)$ untuk A, B mutually exclusive

### A.3.2 Probabilitas Kondisional

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

### A.3.3 Teorema Bayes

$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

**Aplikasi**: Naive Bayes classifier, Bayesian inference

### A.3.4 Distribusi Probabilitas

**Discrete:**

- Bernoulli: Binary outcome (sukses/gagal)
- Binomial: n percobaan Bernoulli

**Continuous:**

- **Normal (Gaussian)**: $f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$
- Uniform: Semua nilai sama mungkin

### A.3.5 Ukuran Statistik

| Ukuran                 | Formula                                   | Arti                  |
| ---------------------- | ----------------------------------------- | --------------------- |
| **Mean**               | $\mu = \frac{1}{n}\sum x_i$               | Rata-rata             |
| **Variance**           | $\sigma^2 = \frac{1}{n}\sum(x_i - \mu)^2$ | Sebaran data          |
| **Standard Deviation** | $\sigma = \sqrt{\sigma^2}$                | Akar variance         |
| **Covariance**         | $\text{Cov}(X,Y) = E[(X-\mu_X)(Y-\mu_Y)]$ | Hubungan dua variabel |

### A.3.6 Maximum Likelihood Estimation

Temukan parameter θ yang memaksimalkan:
$$\hat{\theta} = \arg\max_{\theta} L(\theta) = \arg\max_{\theta} \prod_i P(x_i|\theta)$$

Biasanya dioptimasi dalam bentuk log-likelihood.

---

## A.4 Fungsi Khusus

### A.4.1 Sigmoid

$$\sigma(x) = \frac{1}{1 + e^{-x}}$$

- Range: (0, 1)
- Turunan: $\sigma'(x) = \sigma(x)(1 - \sigma(x))$

### A.4.2 Softmax

$$\text{softmax}(x_i) = \frac{e^{x_i}}{\sum_j e^{x_j}}$$

- Konversi ke distribusi probabilitas
- Semua output positif dan jumlah = 1

### A.4.3 Logaritma

**Sifat penting:**

- $\log(ab) = \log(a) + \log(b)$
- $\log(a/b) = \log(a) - \log(b)$
- $\log(a^n) = n\log(a)$

**Natural log** (ln) menggunakan basis e ≈ 2.718.

---

## A.5 Teori Informasi Dasar

### A.5.1 Entropy

Entropy mengukur **ketidakpastian** dalam distribusi probabilitas:

$$H(X) = -\sum_i P(x_i) \log_2 P(x_i)$$

- High entropy = lebih uncertain
- Entropy = 0 jika satu outcome pasti

### A.5.2 Cross-Entropy

$$H(p, q) = -\sum_i p(x_i) \log q(x_i)$$

- Mengukur perbedaan antara dua distribusi
- Digunakan sebagai loss function dalam classification

### A.5.3 Information Gain

$$IG = H(\text{parent}) - \sum_{\text{children}} \frac{n_{\text{child}}}{n_{\text{parent}}} H(\text{child})$$

- Digunakan dalam Decision Trees untuk memilih fitur terbaik

---

## A.6 Optimasi

### A.6.1 Gradient Descent

Update rule:
$$\theta_{t+1} = \theta_t - \eta \nabla L(\theta_t)$$

Di mana η adalah learning rate.

### A.6.2 Convexity

Fungsi **convex** memiliki satu minimum global. Gradient descent akan konvergen ke minimum global untuk fungsi convex.

### A.6.3 Regularization

**L2 (Ridge):** $L + \lambda\|\mathbf{w}\|^2$
**L1 (Lasso):** $L + \lambda\|\mathbf{w}\|$

- L2 mengecilkan weights
- L1 bisa membuat weights = 0 (sparse)

---

## A.7 Notasi Ilmiah

| Notasi                | Arti                            |
| --------------------- | ------------------------------- |
| $\sum_{i=1}^{n} x_i$  | Penjumlahan dari i=1 sampai n   |
| $\prod_{i=1}^{n} x_i$ | Perkalian dari i=1 sampai n     |
| $\forall$             | Untuk semua                     |
| $\exists$             | Terdapat                        |
| $\in$                 | Anggota dari                    |
| $\subseteq$           | Subset dari                     |
| $\mathbb{R}$          | Himpunan bilangan real          |
| $\mathbb{R}^n$        | Ruang n-dimensi                 |
| $\arg\max_x f(x)$     | Nilai x yang memaksimalkan f(x) |
| $\arg\min_x f(x)$     | Nilai x yang meminimalkan f(x)  |

---

## Sumber Belajar Lebih Lanjut

1. **Linear Algebra**: Gilbert Strang - _Linear Algebra and Its Applications_
2. **Calculus**: James Stewart - _Calculus: Early Transcendentals_
3. **Probability & Statistics**: Sheldon Ross - _A First Course in Probability_
4. **Information Theory**: Thomas Cover - _Elements of Information Theory_
5. **Video**: 3Blue1Brown - _Essence of Linear Algebra_ (YouTube)

---

_← [BAB 10: Etika dan Tantangan Algoritma AI](./BAB-10-Etika-dan-Tantangan-Algoritma-AI.md) | [Lampiran B: Notasi dan Konvensi](./Lampiran-B-Notasi-dan-Konvensi.md) →_
