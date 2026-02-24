# Memahami Data

## Pengertian Data

Data adalah sekumpulan fakta atau informasi mentah yang dapat diolah menjadi informasi yang lebih bermakna. Dalam data mining, memahami jenis dan karakteristik data sangat penting sebelum melakukan analisis.

Data dapat berasal dari berbagai sumber seperti:
- Manusia
- Mesin
- Sensor
- Media sosial
- Transaksi online
- dan lain-lain

---

## Jenis-Jenis Data

### Data Terstruktur

Data terstruktur adalah data yang tersusun rapi dalam bentuk tabel (baris dan kolom), seperti di Excel atau database.

Contoh:
- Data nilai mahasiswa
- Data pelanggan
- Data transaksi penjualan

Setiap kolom disebut **atribut** atau **variabel**.

#### Jenis Atribut pada Data Terstruktur

**1. Nominal**  
Kategori tanpa urutan.  
Contoh: jenis kelamin, warna, jurusan.

**2. Biner**  
Hanya memiliki dua nilai.  
Contoh: Ya/Tidak, 0/1, Lulus/Tidak.

**3. Ordinal**  
Memiliki urutan tetapi jarak antar nilai tidak pasti.  
Contoh: kecil – sedang – besar.

**4. Numerik**  
Berupa angka dan bisa dihitung.  
Contoh: umur, tinggi badan, nilai ujian.

Numerik dibagi menjadi:
- Interval (tidak memiliki nol mutlak, contoh: suhu °C)
- Rasio (memiliki nol mutlak, contoh: berat badan)

---

### Data Tidak Terstruktur

Data yang tidak memiliki format tetap dan tidak tersusun dalam tabel.

Contoh:
- Email
- Artikel
- Chat
- Dokumen teks

Biasanya perlu diproses terlebih dahulu sebelum dianalisis.

---

### Data Bahasa Alami

Data berupa bahasa manusia.

Contoh:
- Komentar media sosial
- Review produk
- Berita

Biasanya diolah menggunakan teknik **Natural Language Processing (NLP)**.

---

### Data yang Dibuat oleh Mesin

Data yang dihasilkan otomatis oleh mesin atau sensor.

Contoh:
- Log server
- Sensor Internet of Things (IoT)

---

### Data Berbasis Graph

Data yang menunjukkan hubungan antar objek.

Contoh:
- Jaringan pertemanan media sosial
- Relasi antar pengguna

---

### Data Multimedia

Data berupa audio, video, dan gambar yang memerlukan teknik khusus untuk diproses.

---

### Data Streaming

Data yang terus mengalir secara real-time.

Contoh:
- Data sensor per detik
- Transaksi online
- Aktivitas media sosial

---

## Distribusi Data

Distribusi data menunjukkan bagaimana data tersebar. Distribusi yang paling umum adalah distribusi normal yang berbentuk kurva lonceng.

### Rumus Distribusi Normal

$$
f(x)=\frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

Keterangan:
- $\mu$ = mean (rata-rata)
- $\sigma$ = standar deviasi
- $\sigma^2$ = variansi
- $\pi$ = 3.14159
- $e$ = 2.718

Distribusi membantu mengetahui:
- Apakah data seimbang
- Apakah data miring
- Apakah ada nilai ekstrem (outlier)

---

## Statistik Deskriptif

Statistik deskriptif digunakan untuk merangkum data numerik.

### Ukuran Pusat

#### Mean (Rata-rata)

$$
\bar{x} = \frac{\sum x_i}{n}
$$

Keterangan:
- $\bar{x}$ = rata-rata
- $x_i$ = nilai ke-i
- $n$ = jumlah data

#### Median

Jika jumlah data ganjil:

$$
Me = x_{\frac{n+1}{2}}
$$

Jika jumlah data genap:

$$
Me = \frac{x_{\frac{n}{2}} + x_{\frac{n}{2}+1}}{2}
$$

#### Modus

Nilai yang paling sering muncul.

---

### Ukuran Penyebaran

#### Range (Rentang)

$$
Range = X_{max} - X_{min}
$$

#### Variansi

Populasi:

$$
\sigma^2 = \frac{\sum (x_i - \mu)^2}{n}
$$

Sampel:

$$
s^2 = \frac{\sum (x_i - \bar{x})^2}{n-1}
$$

#### Standar Deviasi

Populasi:

$$
\sigma = \sqrt{\sigma^2}
$$

Sampel:

$$
s = \sqrt{s^2}
$$

Semakin besar standar deviasi → semakin menyebar data.

---

## Skewness (Kemencengan)

Skewness menunjukkan arah kemiringan distribusi data.

### Skewness Positif
- Ekor lebih panjang di kanan
- Mean > Median

### Skewness Negatif
- Ekor lebih panjang di kiri
- Mean < Median

### Distribusi Simetris
- Kiri dan kanan sama
- Mean ≈ Median

### Rumus Skewness

$$
Sk = \frac{\sum (x_i - \mu)^3}{n \sigma^3}
$$

Jika:
- $Sk > 0$ → miring ke kanan
- $Sk < 0$ → miring ke kiri
- $Sk = 0$ → simetris

---

## Pengukuran Jarak (Distance Measurement)

Digunakan dalam clustering dan klasifikasi.

### Euclidean Distance

$$
d = \sqrt{\sum_{i=1}^{n}(x_i - y_i)^2}
$$

### Manhattan Distance

$$
d = \sum_{i=1}^{n}|x_i - y_i|
$$

### Minkowski Distance

$$
d = \left(\sum_{i=1}^{n}|x_i - y_i|^m \right)^{1/m}
$$

### Cosine Similarity

$$
Cosine(x,y)=\frac{\sum x_i y_i}{||x|| \; ||y||}
$$

### Mahalanobis Distance

$$
d = \sqrt{(x-y)S^{-1}(x-y)^T}
$$

### Jaccard Similarity

$$
sim(i,j)=\frac{q}{q+r+s}
$$