# Studi Kasus: Sistem Diagnostik Medis

#### Studi Kasus: Sistem Diagnostik Medis

**Forward Chaining**

**Kasus**: Pasien datang ke dokter dengan keluhan demam dan batuk.

1. **Identifikasi Fakta Awal**: Pasien memiliki demam dan batuk.
2. **Pemilihan Aturan**:
   * Aturan 1: Jika demam dan batuk, maka kemungkinan flu.
   * Aturan 2: Jika demam tetapi tidak ada batuk, maka kemungkinan infeksi.
3. **Evaluasi Aturan**: Aturan 1 sesuai dengan fakta awal.
4. **Tambahkan Kesimpulan ke Daftar Fakta**: Pasien kemungkinan mengalami flu.
5. **Iterasi**: Tidak ada aturan lain yang sesuai.
6. **Evaluasi Hasil**: Pasien kemungkinan mengalami flu dan perlu lebih lanjut diuji.

**Backward Chaining**

**Kasus**: Pasien ingin tahu apakah ia mengalami infeksi paru-paru.

1. **Identifikasi Kesimpulan yang Diinginkan**: Pasien mengalami infeksi paru-paru.
2. **Pemilihan Aturan**:
   * Aturan 1: Jika demam dan sesak napas, maka infeksi paru-paru.
   * Aturan 2: Jika batuk berdarah, maka infeksi paru-paru.
3.  **Evaluasi Aturan**:

    * Aturan 1 memerlukan demam dan sesak napas.
    * Aturan 2 memerlukan batuk berdarah.

    3.1. **Jika Ya**: Lanjut ke langkah 4.

    3.2. **Jika Tidak**: Pasien tidak memiliki batuk berdarah atau sesak napas, maka tidak bisa digunakan aturan ini.
4. **Verifikasi Fakta**: Pasien tidak memiliki gejala yang sesuai dengan aturan.
5. **Capai Kesimpulan**: Tidak dapat disimpulkan bahwa pasien mengalami infeksi paru-paru berdasarkan gejala yang ada.
6. **Evaluasi Hasil**: Lebih banyak pemeriksaan medis diperlukan untuk diagnosa yang akurat.
