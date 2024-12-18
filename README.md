# Proyek Akhir: Menyelesaikan Permasalahan Institusi Pendidikan

## Business Understanding
Jaya Jaya Institut adalah institusi pendidikan perguruan tinggi yang telah berdiri sejak tahun 2000. Meskipun memiliki reputasi baik dalam menghasilkan lulusan berkualitas, institusi ini menghadapi tantangan signifikan terkait tingginya angka dropout mahasiswa. Tingkat dropout yang tinggi dapat berdampak negatif pada:
- Kualitas pendidikan institusi
- Efisiensi sumber daya pendidikan
- Reputasi institusi
- Pendapatan dan keberlanjutan institusi

### Permasalahan Bisnis
1. Tingginya angka dropout mahasiswa yang belum teridentifikasi secara dini
2. Kurangnya intervensi proaktif untuk mencegah mahasiswa potensial dropout
3. Tidak tersedianya sistem prediktif untuk mendeteksi mahasiswa berisiko tinggi dropout
4. Kerugian finansial akibat mahasiswa yang tidak menyelesaikan pendidikan

### Cakupan Proyek
1. Analisis data mahasiswa untuk mengidentifikasi faktor-faktor yang mempengaruhi dropout
2. Pengembangan model machine learning untuk memprediksi risiko dropout
3. Identifikasi fitur-fitur yang berpengaruh terhadap status dropout
4. Pembuatan prototipe sistem prediksi dropout
### Persiapan

Sumber data: https://github.com/dicodingacademy/dicoding_dataset/blob/main/students_performance/data.csv

Setup environment:
Bahasa pemrograman: Python
Library: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Flask/Streamlit untuk dashboard
Infrastruktur: Jupyter Notebook, Google Colab, atau server lokal
```
python -m venv DropoutPrediction
pip install -r requirements.txt
```

## Business Dashboard
link dashboard: https://public.tableau.com/views/DashboardPermasalahanInstitusiPendidikan/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link 

1. Overview Data Mahasiswa:
- Terdapat 3 status mahasiswa: Dropout (1,421), Enrolled (794), dan Graduate (2,209).
- Rata-rata nilai admission grade mahasiswa adalah 127.0.
- Rata-rata usia saat enrollment adalah 23.3 tahun.
- Rata-rata tingkat inflasi adalah 1.2.
2. Analisis Berdasarkan Gender:
- Mayoritas mahasiswa berjenis kelamin perempuan (3,167) dibandingkan laki-laki (1,257).
- Secara umum, mahasiswa perempuan memiliki tingkat kelulusan yang lebih tinggi dibandingkan laki-laki.
- Namun, terdapat perbedaan yang cukup signifikan dalam jumlah mahasiswa dropout antara perempuan dan laki-laki.
3. Analisis Berdasarkan Status Debitur:
- Mayoritas mahasiswa memiliki status debitur (yes).
- Status debitur memiliki korelasi yang kuat dengan status dropout mahasiswa.
- Mahasiswa dengan status debitur memiliki jumlah dropout yang jauh lebih tinggi dibandingkan yang tidak memiliki status debitur.
- Sebaliknya, mahasiswa non-debitur memiliki jumlah kelulusan yang jauh lebih tinggi.

## Menjalankan Sistem Machine Learning
Untuk menjalankan prototipe sistem machine learning, ikuti langkah-langkah berikut untuk menganalisis data siswa dan memprediksi tingkat drop-out.

Langkah-langkah:
1. install modul (library)
- buka terminal atau command prompt dan jalankan perintah berikut:
```
pip install -r requirements.txt
```
2. Download Script 
-Unduh script dari repository GitHub berikut:
```
git clone https://github.com/aidakusuma/blank-app.git
```
3. buka script di editor code
- Gunakan editor kode favorit seperti:
    - Visual Studio Code (VSCode)
    - PyCharm
    - Jupyter Notebook
- Pastikan dataset yang digunakan sudah sesuai dengan path yang ditentukan di dalam script. Jika path dataset berbeda, sesuaikan dengan lokasi file dataset di komputer.

4. Jalankan Script
- Untuk menjalankan aplikasi, buka terminal di direktori tempat script berada, lalu jalankan:

```
streamlit run streamlit_app.py
```

Mengakses Aplikasi Prediksi Dropout:

link prototype: 

```
https://blank-app-urrvl0g3tpe.streamlit.app/
```

## Conclusion
- Student yang tidak menjadi pemegang beasiswa (Scholarship_holder = 0) memiliki korelasi positif dengan tingkat dropout. Hal ini terlihat dari korelasi negatif -0.245 antara status scholarship holder dengan dropout, menunjukkan pentingnya dukungan finansial dalam memotivasi mahasiswa untuk menyelesaikan pendidikan.
- Pembayaran biaya kuliah yang teratur (Tuition_fees_up_to_date) memiliki korelasi kuat dengan keberhasilan akademik. Terdapat korelasi negatif sebesar -0.429 dengan status dropout, mengindikasikan bahwa manajemen keuangan yang baik berkaitan erat dengan keberhasilan akademik.
- Usia saat pendaftaran (Age_at_enrollment) memiliki korelasi positif 0.254 dengan dropout, menandakan bahwa mahasiswa yang mendaftar pada usia lebih tua (di atas rata-rata) cenderung memiliki risiko dropout yang lebih tinggi.
- Variabel Gender memiliki korelasi 0.204 dengan dropout, menunjukkan adanya perbedaan signifikan dalam tingkat keberhasilan akademik berdasarkan jenis kelamin.
Mode aplikasi (Application_mode) dengan korelasi 0.198 mengindikasikan bahwa cara mahasiswa mendaftar mempengaruhi probabilitas dropout.
- Status debitur (Debtor) memiliki korelasi 0.229 dengan dropout, menandakan bahwa mahasiswa dengan status debitur lebih rentan untuk tidak menyelesaikan pendidikan.
- Fitur-fitur akademis seperti jumlah unit kurikuler yang disetujui dan nilai semester menunjukkan korelasi kuat dengan kelulusan, dengan korelasi positif tertinggi mencapai 0.577 untuk unit kurikuler semester kedua yang disetujui.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- Kembangkan program beasiswa atau bantuan finansial yang lebih komprehensif untuk mahasiswa berisiko tinggi dropout
- Sediakan layanan konseling dan pendampingan khusus untuk mahasiswa yang mendaftar pada usia lebih tua
- Buat program intervensi dini untuk mahasiswa dengan status debitur
- Kembangkan program mentoring berbasis gender untuk mendukung mahasiswa yang memiliki risiko dropout tinggi
- Optimalkan proses penerimaan mahasiswa dengan mempertimbangkan mode aplikasi yang berbeda
- Berikan dukungan tambahan untuk manajemen keuangan dan pembayaran biaya kuliah
- Kembangkan sistem peringatan dini berdasarkan indikator akademik seperti unit kurikuler dan nilai semester
- Sediakan program akselerasi atau fleksibilitas akademik untuk mahasiswa dengan karakteristik berisiko tinggi