# Implementasi Sistem Pakar

#### Pembuatan Sistem Pakar Diagnostik Medis Covid-19 Menggunakan Python

**Pendahuluan**

Sistem Pakar Diagnostik Medis untuk Covid-19 adalah aplikasi berbasis Python yang dirancang untuk membantu dalam mendiagnosis Covid-19. Sistem ini memungkinkan pengguna untuk memasukkan nama dan gejala yang mereka alami, dan selanjutnya sistem akan memberikan diagnosa serta solusi yang sesuai.

**Komponen Utama**

1.  **Basis Pengetahuan**: Ini adalah database yang berisi informasi tentang gejala Covid-19 dan hubungannya dengan diagnosis yang mungkin.

    ```python
    knowledge_base = {
        'COVID-19': {'gejala': ['demam', 'batuk kering', 'kehilangan indera perasa dan penciuman'], 'solusi': 'Segera lakukan tes PCR dan isolasi diri'},
        'Flu': {'gejala': ['demam', 'batuk', 'sakit tenggorokan'], 'solusi': 'Istirahat cukup dan konsumsi obat flu'},
        'Common Cold': {'gejala': ['batuk', 'pilek', 'sakit tenggorokan'], 'solusi': 'Istirahat dan minum obat pereda batuk'}
    }
    ```
2.  **Mesin Inferensi**: Ini adalah algoritma yang digunakan untuk mengevaluasi gejala dan mencapai diagnosis.

    ```python
    def diagnose(name, symptoms, knowledge_base):
        for disease, attributes in knowledge_base.items():
            matching_symptoms = [s for s in symptoms if s in attributes['gejala']]
            if len(matching_symptoms) / len(attributes['gejala']) >= 0.3:  # At least 30% match
                return f"{name}, diagnosis Anda adalah {disease}. {attributes['solusi']}"
        return f"{name}, diagnosis tidak ditemukan. Silakan konsultasi dengan dokter."

    ```

**Implementasi**

1.  **Pengumpulan Data**: Sistem akan meminta pengguna untuk memasukkan nama dan gejala yang dialami.

    ```python
    name = input("Masukkan nama Anda: ")
    symptoms = input("Masukkan gejala yang dialami, dipisahkan oleh koma: ").split(',')
    ```
2.  **Diagnosis dan Solusi**: Mesin inferensi akan memproses gejala untuk memberikan diagnosis dan solusi.

    ```python
    result = diagnose(name, symptoms, knowledge_base)
    print(result)
    ```

**Kesimpulan**

Sistem Pakar Diagnostik Medis untuk Covid-19 dalam Python menawarkan solusi yang efisien dan efektif untuk diagnosis awal. Meskipun memiliki beberapa keterbatasan, sistem ini berfungsi sebagai alat pendukung dalam proses diagnostik dan dapat ditingkatkan lebih lanjut dengan data dan algoritma yang lebih canggih
