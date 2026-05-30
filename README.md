# 🎓 Student Performance Analytics: Key Drivers of Academic Success

[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)](https://public.tableau.com/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=Jupyter&logoColor=white)](https://jupyter.org/)

**Author:** Nelil Amaani (2306227835)  
**Course:** Business Intelligence (BI) - Class A  

## 📝 Project Overview
Proyek ini berfokus pada pembedahan data performa akademik (+6.600 baris data) untuk menyaring elemen spekulatif dan mengisolasi faktor-faktor yang memiliki pengaruh paling signifikan terhadap skor ujian siswa (*Exam Score*). 

Melalui proses analisis korelasi dan visualisasi interaktif di Tableau, proyek ini memetakan pola kontribusi utama dari variabel aktivitas belajar dan lingkungan, memberikan gambaran yang jelas bagi institusi pendidikan untuk mengambil tindakan intervensi yang efektif.

## 🛠️ Tech Stack & Tools
* **Data Pre-processing & EDA:** Python (Pandas, Seaborn, Matplotlib), Jupyter Notebook
* **Data Visualization & Dashboarding:** Tableau Desktop
* **Data Source:** `DatasetPerformaSiswa (2).csv`

## ⚙️ Data Pre-processing & Cleaning
Proses *pre-processing* dilakukan menggunakan Python untuk memastikan validitas hasil analisis sebelum ditransformasikan ke dalam grafik:
1. **Handling Missing Values:** Mengisi baris kosong (*null*) pada komponen kategoris kunci seperti kualitas guru (`Teacher_Quality`) dan tingkat pendidikan orang tua (`Parental_Education_Level`) menggunakan nilai modus.
2. **Outlier Capping:** Menyelaraskan anomali data pada kolom skor ujian (`Exam_Score`) dengan membatasi nilai logis maksimal di angka 100.
3. **Deduplication:** Menghapus data duplikat untuk menjaga keaslian sebaran sampel data.

*Langkah-langkah pembersihan data secara detail terdokumentasi pada file `Lab Tableau_BI_A_2306227835_Nelil_Amaani.ipynb`.*

## 📊 Core Factors & Key Insights
Berdasarkan hasil pemfilteran korelasi, analisis visual dipusatkan pada faktor-faktor utama yang paling menentukan pencapaian akademis:

1. **Tingkat Kehadiran (*Attendance*)**
   Variabel dengan korelasi linear positif terkuat. Tren data menunjukkan bahwa siswa yang menjaga tingkat kehadiran di atas 90% secara konsisten mendominasi pencapaian skor ujian tertinggi. Kehadiran menjadi fondasi utama sebelum faktor lain dapat bekerja.
2. **Durasi Belajar Mandiri (*Hours Studied*)**
   Menunjukkan dampak positif yang signifikan. Terdapat peningkatan nilai yang stabil seiring dengan bertambahnya alokasi waktu belajar mandiri yang dihabiskan siswa setiap minggunya.
3. **Performa Akademik Historis (*Previous Scores*)**
   Bertindak sebagai prediktor baseline yang kuat. Siswa dengan rekam jejak nilai masa lalu yang baik memiliki kecenderungan besar untuk mempertahankan konsistensi performanya.
4. **Keterlibatan Orang Tua (*Parental Involvement*)**
   Faktor eksternal yang krusial. Sebaran data menunjukkan bahwa dukungan dan keterlibatan aktif dari orang tua di rumah memberikan batas bawah nilai yang lebih aman bagi stabilitas belajar anak.

## 💡 Actionable Recommendations
* **Early Warning System:** Menerapkan sistem peringatan otomatis berbasis kehadiran apabila absensi siswa mulai menyentuh batas kritis (di bawah 85%).
* **Workshop Manajemen Waktu:** Membantu siswa menyusun jadwal belajar mandiri mingguan yang optimal tanpa mengorbankan waktu istirahat.
* **Sinergi Sekolah & Keluarga:** Membuka saluran komunikasi berkala untuk memastikan pendampingan belajar di rumah berjalan selaras dengan target di sekolah.

## 📂 Repository Structure
* `DatasetPerformaSiswa (2).csv` - Dataset utama yang digunakan dalam analisis.
* `Lab Tableau_BI_A_2306227835_Nelil_Amaani.ipynb` - Jupyter Notebook yang memuat skrip Python untuk pembersihan dan eksplorasi data.
* `Lab Tableau - BI A - 2306227835 - Nelil Amaani.twb` - File *workbook* Tableau berisi seluruh perancangan lembar kerja grafik dan dashboard interaktif.

## 🚀 How to Run
1. Salin repositori ini ke komputer lokal:  
   `git clone https://github.com/nelilamaani21/Student-Performance-Analytics.git`
2. Jalankan file `.ipynb` melalui Jupyter Notebook untuk meninjau tahapan *data engineering*.
3. Buka file `.twb` menggunakan Tableau Desktop untuk mengeksplorasi dashboard secara interaktif (pastikan file dataset `.csv` berada dalam satu direktori yang sama agar pemanggilan data otomatis berjalan lancar).
