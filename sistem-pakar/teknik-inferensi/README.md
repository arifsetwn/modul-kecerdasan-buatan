# Teknik Inferensi

**Algoritma Berbasis Aturan (Rule-Based Algorithm)**

Algoritma Berbasis Aturan adalah jenis algoritma sistem pakar yang paling awal dan paling umum digunakan. Dalam sistem ini, pengetahuan direpresentasikan dalam bentuk aturan "IF-THEN" yang menghubungkan premis dengan kesimpulan. Misalnya, dalam sistem pakar medis, aturan mungkin berbentuk: "JIKA pasien memiliki demam DAN batuk, MAKA kemungkinan pasien mengidap flu." Algoritma ini memanfaatkan mesin inferensi untuk mengevaluasi aturan ini dan menghasilkan kesimpulan atau rekomendasi.

Algoritma Berbasis Aturan (Rule-Based Algorithms) adalah algoritma yang menggunakan seperangkat aturan atau hukum untuk membuat keputusan atau inferensi. Berikut adalah beberapa algoritma dan teknik yang termasuk dalam kategori ini:

1. **Decision Trees**: Seperti ID3, C4.5, dan CART, yang menggunakan struktur pohon untuk merepresentasikan aturan.
2. **Decision Table**: Tabel keputusan yang mencakup semua kemungkinan situasi dan tindakan yang sesuai.
3. **Production Rules**: Aturan produksi dalam bentuk IF-THEN yang digunakan dalam sistem pakar.
4. **Association Rule Learning Algorithms**: Seperti Apriori dan FP-Growth, yang digunakan untuk menemukan aturan asosiasi dalam dataset.
5. **Inference Engines**: Mesin inferensi yang menggunakan aturan untuk menarik kesimpulan, biasanya digunakan dalam sistem pakar.
6. **Rule-Based Classifiers**: Klasifikasi berdasarkan aturan yang telah ditentukan.
7. **Zeroth**: Algoritma pembelajaran aturan yang mencoba meminimalkan jumlah aturan dan kondisi.

**Algoritma Berbasis Kasus** (Case-Based Reasoning)

Algoritma Berbasis Kasus (Case-Based Reasoning) adalah pendekatan yang memanfaatkan basis data dari kasus-kasus sebelumnya untuk menyelesaikan masalah baru. Sistem ini mencari kesamaan antara masalah baru dan kasus yang ada dalam basis data. Setelah menemukan kasus yang paling serupa, sistem akan menyesuaikan solusi dari kasus sebelumnya untuk menyelesaikan masalah baru. Ini sangat efektif dalam situasi di mana masalah yang dihadapi adalah variasi dari masalah yang sudah ada.

Algoritma Case-Based Reasoning (CBR) tidak terbatas pada satu algoritma spesifik, tetapi lebih merupakan paradigma yang melibatkan beberapa langkah umum: Retrieve, Reuse, Revise, dan Retain (4R). Namun, ada beberapa algoritma dan teknik yang sering digunakan dalam implementasi CBR, antara lain:

1. **k-Nearest Neighbors (k-NN)**: Digunakan dalam tahap Retrieve untuk menemukan kasus-kasus terdekat dari kasus baru.
2. **Cosine Similarity**: Metode lain untuk mengukur kedekatan antara kasus baru dan kasus dalam basis pengetahuan.
3. **Weighted Features**: Beberapa fitur mungkin lebih penting daripada yang lain dalam menentukan kesamaan antara kasus.
4. **Local and Global Similarity Measures**: Menggunakan kombinasi dari metrik kesamaan lokal dan global untuk menemukan kasus terbaik untuk digunakan sebagai solusi.
5. **Bayesian Networks**: Dalam beberapa implementasi, jaringan Bayesian digunakan untuk memodelkan basis pengetahuan dan membuat inferensi.
6. **Decision Trees**: Dapat digunakan dalam tahap Reuse untuk memodifikasi solusi dari kasus terdahulu agar sesuai dengan kasus baru.
7. **Genetic Algorithms**: Dalam kasus-kasus tertentu, algoritma genetika digunakan untuk menyesuaikan atau memodifikasi solusi dari kasus terdahulu.

**Algoritma Berbasis Probabilitas**

Algoritma Berbasis Probabilitas memanfaatkan teori probabilitas dan statistik untuk mengevaluasi kemungkinan dari berbagai hasil berdasarkan data yang ada. Salah satu implementasi populer dari pendekatan ini adalah Jaringan Bayesian. Dalam konteks sistem pakar, algoritma ini biasanya digunakan dalam aplikasi yang memerlukan analisis risiko atau diagnostik medis.

Algoritma Berbasis Probabilitas adalah algoritma yang menggunakan prinsip-prinsip probabilitas untuk membuat keputusan atau inferensi. Berikut adalah beberapa algoritma dan teknik yang termasuk dalam kategori ini:

1. **Naive Bayes Classifier**: Algoritma klasifikasi yang berdasarkan pada teorema Bayes.
2. **Hidden Markov Models (HMMs)**: Digunakan dalam pemrosesan bahasa alami dan pengenalan pola.
3. **Gaussian Mixture Models (GMMs)**: Digunakan dalam klustering dan klasifikasi.
4. **Bayesian Networks**: Model grafik probabilitas yang merepresentasikan ketergantungan antar variabel acak.
5. **Monte Carlo Methods**: Teknik simulasi untuk memahami dampak ketidakpastian dalam prediksi dan perkiraan.
6. **Markov Chain Monte Carlo (MCMC)**: Digunakan untuk mendekati distribusi posterior dalam statistik Bayes.
7. **Expectation-Maximization (EM)**: Digunakan untuk menemukan parameter maksimum likelihood dalam model statistik.
8. **Particle Filters**: Digunakan dalam sistem pelacakan dan navigasi.
9. **Conditional Random Fields (CRFs)**: Digunakan dalam pemrosesan bahasa alami untuk tugas seperti tagging dan segmentasi.
10. **Probabilistic Graphical Models**: Termasuk Bayesian Networks dan Markov Random Fields.
11. **Logistic Regression**: Meskipun merupakan model regresi, ia digunakan untuk estimasi probabilitas.
12. **Random Forests**: Meskipun berbasis pohon keputusan, ia menggunakan voting berbasis probabilitas untuk klasifikasi.
13. **Q-Learning**: Sebuah algoritma pembelajaran penguatan yang estimasinya berdasarkan pada probabilitas.



**Teknik Inferensi dalam Jenis-jenis Algoritma**

1. **Forward Chaining**: Digunakan terutama dalam algoritma berbasis aturan. Sistem memulai dari fakta yang diketahui dan bergerak maju melalui aturan hingga mencapai kesimpulan.
2. **Backward Chaining**: Umumnya digunakan dalam sistem diagnostik. Sistem memulai dari kesimpulan yang diinginkan dan bergerak mundur untuk menemukan fakta yang mendukung kesimpulan tersebut.
3. **Hybrid Chaining**: Kombinasi dari forward chaining dan backward chaining. Ini biasanya digunakan dalam sistem yang kompleks dan memerlukan jenis inferensi yang lebih fleksibel.

**Langkah-Langkah Forward Chaining**

1. **Identifikasi Fakta Awal**: Tentukan fakta awal yang diketahui. Fakta ini akan menjadi titik awal dalam proses inferensi.
2. **Pemilihan Aturan**: Pilih semua aturan yang memiliki premis yang sesuai dengan fakta awal.
3. **Evaluasi Aturan**: Evaluasi aturan yang dipilih satu per satu. Jika semua kondisi dalam premis aturan terpenuhi, maka lakukan aksi yang ditentukan dalam bagian kesimpulan aturan.
4. **Tambahkan Kesimpulan ke Daftar Fakta**: Hasil dari evaluasi aturan ditambahkan ke daftar fakta yang diketahui.
5. **Iterasi**: Ulangi langkah 2-4 sampai tidak ada aturan lagi yang dapat dievaluasi atau sampai mencapai kesimpulan yang diinginkan.
6. **Evaluasi Hasil**: Periksa apakah kesimpulan yang diinginkan telah dicapai atau apakah semua aturan telah dievaluasi.

**Langkah-Langkah Backward Chaining**

1. **Identifikasi Kesimpulan yang Diinginkan**: Tentukan kesimpulan atau tujuan yang ingin dicapai.
2. **Pemilihan Aturan**: Pilih semua aturan yang memiliki kesimpulan yang sesuai dengan tujuan atau sub-tujuan yang ingin dicapai.
3.  **Evaluasi Aturan**: Untuk setiap aturan yang dipilih, periksa apakah semua premis dalam aturan tersebut terpenuhi.

    3.1. **Jika Ya**: Lanjutkan ke langkah berikutnya.

    3.2. **Jika Tidak**: Ubah premis yang tidak terpenuhi menjadi sub-tujuan baru dan kembali ke langkah 2.
4. **Verifikasi Fakta**: Jika semua premis terpenuhi, verifikasi fakta ini dengan basis pengetahuan atau data yang ada.
5. **Capai Kesimpulan**: Jika verifikasi berhasil, kesimpulan yang diinginkan telah dicapai.
6. **Evaluasi Hasil**: Periksa apakah kesimpulan yang diinginkan telah dicapai atau apakah lebih banyak inferensi diperlukan
