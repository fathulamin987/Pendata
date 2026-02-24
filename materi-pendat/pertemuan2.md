# Memahami Data

### 1. Jenis Data

Dalam data mining, data dibagi menjadi beberapa jenis:

- **Data Terstruktur**  
  Data yang tersusun dalam bentuk tabel (baris dan kolom), seperti data di Excel atau database.

- **Data Tidak Terstruktur**  
  Data yang tidak memiliki format tetap, seperti email, dokumen, atau teks bebas.

- **Data Bahasa Alami**  
  Data berupa bahasa manusia (contoh: Bahasa Indonesia, Inggris) yang biasanya diproses dengan NLP.

- **Data Machine-Generated**  
  Data yang dihasilkan oleh mesin atau sensor, seperti log server dan data IoT.

- **Data Multimedia (Audio, Video, Citra)**  
  Data berupa gambar, suara, atau video.

- **Data Streaming**  
  Data yang terus mengalir secara real-time, seperti transaksi online atau media sosial.

- **Data Graph**  
  Data yang berbentuk hubungan atau jaringan, seperti relasi pertemanan di media sosial.

---

### 2. Jenis Atribut (Fitur)

Atribut adalah karakteristik atau ciri dari suatu data.

- **Nominal**  
  Data kategori tanpa urutan.  
  Contoh: warna rambut, jenis kelamin.

- **Biner**  
  Data dengan dua kemungkinan nilai (0 dan 1).  
  Contoh: Ya/Tidak, Lulus/Tidak.

- **Ordinal**  
  Data yang memiliki urutan, tetapi jarak antar nilai tidak pasti.  
  Contoh: kecil, sedang, besar.

- **Numerik**  
  Data berupa angka yang bisa dihitung.
  - Interval (tidak memiliki nol mutlak, contoh: suhu °C)
  - Rasio (memiliki nol mutlak, contoh: berat badan)

---

### 3. Statistik Deskriptif

Statistik deskriptif digunakan untuk memahami isi data.

#### A. Ukuran Pemusatan

**Mean (Rata-rata)**  
Digunakan untuk mengetahui nilai rata-rata suatu data.

$$
\bar{x} = \frac{\sum_{i=1}^{N} x_i}{N}
$$

**Median**  
Nilai tengah setelah data diurutkan.

**Modus**  
Nilai yang paling sering muncul.

---

#### B. Ukuran Penyebaran

Digunakan untuk mengetahui seberapa menyebar data.

**Variansi**

$$
\sigma^2 = \frac{1}{N}\sum_{i=1}^{N}(x_i - \bar{x})^2
$$

**Standar Deviasi**

$$
\sigma = \sqrt{\sigma^2}
$$

Semakin besar standar deviasi, semakin menyebar data tersebut.

---

#### C. Distribusi Normal

Distribusi normal berbentuk seperti lonceng dan simetris.

$$
f(x)=\frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

Keterangan:
- μ = rata-rata
- σ = standar deviasi

---

### 4. Pengukuran Jarak (Distance Measurement)

Digunakan untuk menghitung jarak atau kemiripan antar data, terutama dalam clustering.

#### Euclidean Distance
Jarak paling umum digunakan.

$$
d = \sqrt{\sum_{i=1}^{n}(x_i - y_i)^2}
$$

---

#### Manhattan Distance

$$
d = \sum_{i=1}^{n}|x_i - y_i|
$$

---

#### Minkowski Distance

$$
d = \left(\sum_{i=1}^{n}|x_i - y_i|^m \right)^{1/m}
$$

---

#### Cosine Similarity
Digunakan untuk mengukur kemiripan dokumen.

$$
Cosine(x,y)=\frac{\sum x_i y_i}{||x|| \; ||y||}
$$

---

#### Mahalanobis Distance

$$
d = \sqrt{(x-y)S^{-1}(x-y)^T}
$$

---

#### Jaccard Similarity
Digunakan untuk data biner.

$$
sim(i,j)=\frac{q}{q+r+s}
$$

---
