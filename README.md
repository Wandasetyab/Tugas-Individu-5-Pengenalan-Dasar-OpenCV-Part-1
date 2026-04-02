# Tugas Individu 5 : Pengenalan Dasar OpenCV (Part 1)

**Mata Kuliah:** Praktikum Machine Learning (Computer Vision)  
**Dosen Pengampu:** Herfandi, Ph.D. — Informatika — Universitas Teknologi Sumbawa (UTS)

---

## 👤 Profil Mahasiswa
* **Nama:** Wanda Setya Budi
* **NIM:** 231001008
* **Kelas:** Informatika — [C]

---

## 📝 Deskripsi Proyek
Repositori ini memuat dokumentasi teknis dan skrip dari praktik mandiri mengenai dasar-dasar **OpenCV** (Open Source Computer Vision Library). Praktikum ini merupakan gerbang awal untuk memahami bagaimana mesin dan komputer memproses data visual. Sebelum masuk ke pengenalan objek atau kecerdasan buatan, kita harus memahami terlebih dahulu cara melakukan ekstraksi, manipulasi, dan manajemen *Input/Output* dari sebuah citra digital maupun video.

Materi pada repositori ini difokuskan pada operasi fundamental pemrosesan gambar dan integrasi *hardware* (kamera).

---

## ⚙️ Lingkungan Pengembangan (Environment)
Skrip dan pengujian di dalam repositori ini berjalan pada spesifikasi sistem berikut:
* **Kode Editor:** VS Code / Jupyter Notebook
* **Interpreter:** Python 3.8+
* **Library Utama:** OpenCV (`cv2`), NumPy, Matplotlib
* **Metode Eksekusi:** *Interactive execution* berbasis *cell*

---

## 🛠️ Cakupan Praktikum
Langkah-langkah praktikum yang diimplementasikan meliputi:
1.  **Arsitektur Citra Digital:** Membedah gambar untuk melihat resolusi (tinggi & lebar) serta ukuran memori (*bytes*) menggunakan struktur matriks *array* NumPy.
2.  **Operasi I/O Gambar:** Menggunakan `cv2.imread()` untuk memuat gambar ke memori RAM, `cv2.imshow()` untuk me-*render* antarmuka GUI, dan `cv2.imwrite()` untuk menyimpan perubahan ke dalam *disk*.
3.  **Matplotlib & Manipulasi Channel:** Mengatasi perbedaan pembacaan format warna (*default* OpenCV adalah **BGR**, sedangkan Matplotlib adalah **RGB**) melalui teknik *slicing array* `::-1` maupun fungsi konversi.
4.  **Pemrosesan Video:** Menggunakan `cv2.VideoCapture` untuk mengekstrak dan menampilkan rentetan *frame* dari sebuah *file* video `.mp4` menggunakan fungsi perulangan.
5.  **Akses Perangkat Eksternal (Webcam):** Melakukan inisialisasi koneksi ke periferal kamera (*port* 0 atau 1) guna menangkap foto serta merekam video menggunakan *codec* dan modul `VideoWriter`.

---

## 🔍 Analisis & Kesimpulan Teknis
Berdasarkan hasil uji coba dan bedah kode yang telah dilakukan, berikut adalah ringkasan analisis saya:

1.  **Gambar adalah Susunan Matriks:** Secara komputasi, komputer tidak melihat gambar sebagai sebuah entitas visual, melainkan sebagai tumpukan matriks angka berskala 0 hingga 255. Oleh karena itu, kemampuan kita memotong (*slicing*) *array* di NumPy secara langsung berdampak pada kemampuan kita memanipulasi piksel gambar di OpenCV.
2.  **Efisiensi Format Warna:** Menyadari bahwa OpenCV membaca gambar dari belakang (Blue, Green, Red) adalah hal yang krusial. Kelalaian dalam mengonversi matriks ini ke format standar (RGB) saat disambungkan ke *library* lain (seperti Matplotlib) akan merusak visualisasi data.
3.  **Video Hanyalah Ilusi Frame:** Pemrosesan video tidak membutuhkan perintah khusus yang rumit, karena video pada hakikatnya hanyalah gambar tak beraturan yang ditangkap berulang-ulang dengan kecepatan tinggi (*FPS*). Selama kita menguasai teknik pemrosesan gambar statis, pemrosesan video hanyalah masalah *looping* belaka.
4.  **Kesimpulan:** Manipulasi media menggunakan OpenCV berjalan dengan sangat ringan dan cepat karena arsitekturnya berjalan di atas NumPy. Menguasai manajemen memori dan penanganan *error* pada tahap *Input/Output* ini adalah syarat mutlak sebelum melatih model *Machine Learning* untuk mendeteksi wajah atau objek lainnya.

---

## 📽️ Presentasi Video
Penjelasan komprehensif terkait setiap baris kode, arsitektur matriks gambar, serta demonstrasi pembacaan *webcam* dapat disaksikan pada video berikut:

👉 [**https://youtu.be/kpOIfMVtGbw**]

---
