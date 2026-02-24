# Memahami Data

## Pengertian Data

Data adalah sekumpulan fakta atau informasi mentah yang dapat diolah menjadi informasi yang lebih bermakna. Dalam data mining, memahami jenis dan karakteristik data sangat penting sebelum melakukan analisis.

Artinya, sebelum melakukan pemodelan atau perhitungan, kita harus mengetahui bentuk dan tipe data yang digunakan agar metode yang dipilih sesuai dan tidak menghasilkan kesalahan analisis.

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

Jenis data ini paling mudah dianalisis karena sudah memiliki format yang jelas dan konsisten.

Contoh:
- Data nilai mahasiswa
- Data pelanggan
- Data transaksi penjualan

Setiap kolom disebut **atribut** atau **variabel**.  
Setiap baris biasanya merepresentasikan satu objek atau satu entitas data.

#### Jenis Atribut pada Data Terstruktur

**1. Nominal**  
Kategori tanpa urutan.  
Contoh: jenis kelamin, warna, jurusan.  

Data nominal hanya berfungsi sebagai label dan tidak bisa dihitung secara matematis.

**2. Biner**  
Hanya memiliki dua nilai.  
Contoh: Ya/Tidak, 0/1, Lulus/Tidak.  

Sering digunakan dalam klasifikasi dua kelas.

**3. Ordinal**  
Memiliki urutan tetapi jarak antar nilai tidak pasti.  
Contoh: kecil – sedang – besar.  

Walaupun berurutan, selisih antar kategori tidak bisa diukur secara numerik.

**4. Numerik**  
Berupa angka dan bisa dihitung.  
Contoh: umur, tinggi badan, nilai ujian.

Numerik dibagi menjadi:
- Interval (tidak memiliki nol mutlak, contoh: suhu °C)
- Rasio (memiliki nol mutlak, contoh: berat badan)

Pada skala rasio, nilai nol berarti tidak ada sama sekali.

---

### Data Tidak Terstruktur

Data yang tidak memiliki format tetap dan tidak tersusun dalam tabel.

Contoh:
- Email
- Artikel
- Chat
- Dokumen teks

Biasanya perlu diproses terlebih dahulu sebelum dianalisis karena tidak langsung bisa dihitung.

---

### Data Bahasa Alami

Data berupa bahasa manusia.

Contoh:
- Komentar media sosial
- Review produk
- Berita

Biasanya diolah menggunakan teknik **Natural Language Processing (NLP)** karena teks perlu diubah menjadi representasi numerik.

---

### Data yang Dibuat oleh Mesin

Data yang dihasilkan otomatis oleh mesin atau sensor.

Contoh:
- Log server
- Sensor Internet of Things (IoT)

Data ini biasanya berukuran besar dan bisa berbentuk real-time.

---

### Data Berbasis Graph

Data yang menunjukkan hubungan antar objek.

Contoh:
- Jaringan pertemanan media sosial
- Relasi antar pengguna

Biasanya terdiri dari node (objek) dan edge (hubungan).

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

Biasanya diproses langsung tanpa menunggu semua data terkumpul.

---

## Distribusi Data

Distribusi data menunjukkan bagaimana data tersebar. Distribusi yang paling umum adalah distribusi normal yang berbentuk kurva lonceng.

Distribusi membantu memahami apakah data terkonsentrasi di sekitar rata-rata atau menyebar jauh.

### Rumus Distribusi Normal

$$
f(x)=\frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

Rumus ini adalah fungsi kepadatan probabilitas distribusi normal.  
Nilai $\mu$ menentukan pusat distribusi, sedangkan $\sigma$ menentukan tingkat penyebaran data.  
Semakin besar $\sigma$, kurva semakin melebar.

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

Statistik ini hanya menjelaskan kondisi data, bukan membuat prediksi.

### Ukuran Pusat

#### Mean (Rata-rata)

$$
\bar{x} = \frac{\sum x_i}{n}
$$

Mean diperoleh dengan menjumlahkan seluruh nilai lalu dibagi jumlah data.  
Mean sensitif terhadap outlier sehingga bisa berubah signifikan jika ada nilai ekstrem.

Keterangan:
- $\bar{x}$ = rata-rata
- $x_i$ = nilai ke-i
- $n$ = jumlah data

---

#### Median

Jika jumlah data ganjil:

$$
Me = x_{\frac{n+1}{2}}
$$

Jika jumlah data genap:

$$
Me = \frac{x_{\frac{n}{2}} + x_{\frac{n}{2}+1}}{2}
$$

Median adalah nilai tengah setelah data diurutkan.  
Median lebih stabil dibanding mean ketika terdapat outlier.

---

#### Modus

Nilai yang paling sering muncul.  
Modus berguna untuk melihat nilai atau kategori yang dominan.

---

### Ukuran Penyebaran

#### Range (Rentang)

$$
Range = X_{max} - X_{min}
$$

Range menunjukkan selisih antara nilai terbesar dan terkecil.  
Namun range hanya melihat dua nilai ekstrem.

---

#### Variansi

Populasi:

$$
\sigma^2 = \frac{\sum (x_i - \mu)^2}{n}
$$

Sampel:

$$
s^2 = \frac{\sum (x_i - \bar{x})^2}{n-1}
$$

Variansi mengukur rata-rata kuadrat jarak data terhadap rata-rata.  
Semakin besar variansi, semakin besar penyebaran data.

---

#### Standar Deviasi

Populasi:

$$
\sigma = \sqrt{\sigma^2}
$$

Sampel:

$$
s = \sqrt{s^2}
$$

Standar deviasi adalah akar dari variansi dan memiliki satuan yang sama dengan data asli sehingga lebih mudah diinterpretasikan.

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

Rumus ini mengukur tingkat kemencengan distribusi secara matematis.  
Jika nilai $Sk$ semakin besar (positif atau negatif), distribusi semakin tidak simetris.

Jika:
- $Sk > 0$ → miring ke kanan
- $Sk < 0$ → miring ke kiri
- $Sk = 0$ → simetris

---

## Pengukuran Jarak (Distance Measurement)

Digunakan dalam clustering dan klasifikasi untuk mengukur tingkat kemiripan antar data.

### Euclidean Distance

$$
d = \sqrt{\sum_{i=1}^{n}(x_i - y_i)^2}
$$

Mengukur jarak lurus antara dua titik dalam ruang multidimensi.

---

### Manhattan Distance

$$
d = \sum_{i=1}^{n}|x_i - y_i|
$$

Mengukur jarak berdasarkan jumlah selisih absolut tiap dimensi.

---

### Minkowski Distance

$$
d = \left(\sum_{i=1}^{n}|x_i - y_i|^m \right)^{1/m}
$$

Merupakan bentuk umum dari Euclidean dan Manhattan.  
Jika $m=1$ maka menjadi Manhattan, jika $m=2$ maka menjadi Euclidean.

---

### Cosine Similarity

$$
Cosine(x,y)=\frac{\sum x_i y_i}{||x|| \; ||y||}
$$

Mengukur kemiripan berdasarkan sudut antar vektor, bukan jarak absolut.

---

### Mahalanobis Distance

$$
d = \sqrt{(x-y)S^{-1}(x-y)^T}
$$

Mempertimbangkan korelasi antar variabel melalui matriks kovarians $S$.

---

### Jaccard Similarity

$$
sim(i,j)=\frac{q}{q+r+s}
$$

Mengukur kemiripan berdasarkan jumlah elemen yang sama dibanding total elemen unik.