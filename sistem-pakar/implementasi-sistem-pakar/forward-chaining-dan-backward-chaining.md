# Forward chaining dan backward chaining

Berikut adalah implementasi sederhana dari studi kasus diagnostik medis menggunakan forward chaining dan backward chaining dalam bahasa pemrograman Python.

```python
# Forward Chaining
def forward_chaining(symptoms):
    diagnosis = "Tidak diketahui"
    if "demam" in symptoms and "batuk" in symptoms:
        diagnosis = "Flu"
    elif "demam" in symptoms and "batuk" not in symptoms:
        diagnosis = "Infeksi"
    return diagnosis

# Backward Chaining
def backward_chaining(goal):
    diagnosis = "Tidak dapat disimpulkan"
    if goal == "Infeksi Paru-paru":
        required_symptoms = ["demam", "sesak napas"]
        other_required_symptoms = ["batuk berdarah"]
        
        if all(symptom in symptoms for symptom in required_symptoms):
            diagnosis = "Infeksi Paru-paru"
        elif all(symptom in symptoms for symptom in other_required_symptoms):
            diagnosis = "Infeksi Paru-paru"
    return diagnosis

# Forward Chaining Example
symptoms = ["demam", "batuk"]
result_forward = forward_chaining(symptoms)
print(f"Hasil Diagnosa (Forward Chaining): {result_forward}")

# Backward Chaining Example
goal = "Infeksi Paru-paru"
symptoms = ["demam", "sesak napas"]
result_backward = backward_chaining(goal)
print(f"Hasil Diagnosa (Backward Chaining): {result_backward}")
```

Dalam contoh ini, fungsi `forward_chaining` menerima daftar gejala sebagai argumen dan mengembalikan diagnosa berdasarkan aturan yang telah ditentukan. Fungsi `backward_chaining` menerima tujuan diagnosa yang ingin dicapai dan mengembalikan diagnosa berdasarkan gejala yang diperlukan.

#### Forward Chaining

Dalam forward chaining, kita memulai dari fakta yang kita miliki (dalam hal ini, gejala) dan bergerak maju untuk menarik kesimpulan (diagnosa). Fungsi `forward_chaining` menerima daftar `symptoms` dan memeriksa setiap kondisi untuk menentukan diagnosa. Jika pasien memiliki "demam" dan "batuk", maka diagnosa adalah "Flu". Jika hanya "demam", maka diagnosa adalah "Infeksi".

#### Backward Chaining

Sebaliknya, dalam backward chaining, kita memulai dari tujuan (diagnosa yang ingin dicapai) dan bekerja mundur untuk menemukan fakta yang mendukung tujuan tersebut. Fungsi `backward_chaining` menerima `goal` sebagai argumen dan memeriksa apakah semua `required_symptoms` atau `other_required_symptoms` ada dalam daftar `symptoms`. Jika ya, maka diagnosa yang diinginkan (dalam hal ini, "Infeksi Paru-paru") dikonfirmasi.

#### Penerapan dalam Python

Kode Python di atas menunjukkan implementasi dasar dari kedua metode ini. Fungsi `forward_chaining` dan `backward_chaining` masing-masing mengimplementasikan logika dari forward chaining dan backward chaining. Kedua fungsi ini kemudian diuji dengan contoh gejala dan tujuan untuk memverifikasi keakuratannya.

Dengan demikian, forward chaining dan backward chaining menawarkan dua pendekatan berbeda untuk menyelesaikan masalah yang sama, yaitu diagnostik medis dalam contoh ini. Keduanya memiliki kegunaan dan keterbatasan masing-masing, dan pilihan antara keduanya seringkali bergantung pada konteks dan kebutuhan spesifik dari aplikasi yang dihadapi.
