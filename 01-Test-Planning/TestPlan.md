# Test Plan

## 1. Informasi Dokumen

| Informasi | Detail |
|---|---|
| Proyek | Pengujian Manual E-Commerce SauceDemo |
| Jenis Pengujian | Manual QA |
| Aplikasi | SauceDemo |
| Tester | getSandi | ****************
| Sistem Operasi | Windows 10 |
| Browser | Google Chrome 152 |
| Versi Dokumen | 1.0 |

---

## 2. Tujuan Pengujian

Tujuan dari pengujian ini adalah untuk memverifikasi bahwa fungsi utama pada aplikasi e-commerce SauceDemo berjalan sesuai dengan perilaku yang diharapkan.

Pengujian difokuskan pada fungsi utama yang digunakan oleh pengguna, mulai dari proses login, melihat produk, mengelola keranjang, hingga melakukan proses checkout.

Pengujian juga dilakukan untuk menemukan dan mendokumentasikan kemungkinan defect atau bug yang terdapat pada aplikasi.

---

## 3. Ruang Lingkup Pengujian

### 3.1 Fitur yang Termasuk dalam Pengujian

Fitur yang akan diuji meliputi:

- Login
- Daftar Produk
- Pengurutan Produk
- Detail Produk
- Menambahkan Produk ke Keranjang
- Menghapus Produk dari Keranjang
- Keranjang Belanja
- Checkout
- Logout

### 3.2 Fitur yang Tidak Termasuk dalam Pengujian

Pengujian berikut tidak termasuk dalam ruang lingkup proyek:

- Performance Testing
- Load Testing
- Stress Testing
- Security Penetration Testing
- API Testing
- Database Testing
- Source Code Testing

---

## 4. Pendekatan dan Jenis Pengujian

### 4.1 Manual Testing

Seluruh proses pengujian dilakukan secara manual dengan menjalankan langkah-langkah pengujian dan mencatat hasil aktual dari aplikasi.

### 4.2 Black Box Testing

Pengujian dilakukan dengan memeriksa fungsi dan perilaku aplikasi berdasarkan input dan output tanpa melihat atau mengakses source code aplikasi.

### 4.3 Functional Testing

Pengujian dilakukan untuk memastikan setiap fungsi aplikasi berjalan sesuai dengan perilaku yang diharapkan.

### 4.4 Positive Testing

Pengujian dilakukan menggunakan input dan kondisi yang valid untuk memastikan aplikasi memberikan hasil yang sesuai.

### 4.5 Negative Testing

Pengujian dilakukan menggunakan input atau kondisi yang tidak valid untuk melihat bagaimana aplikasi menangani kondisi tersebut.

### 4.6 Exploratory Testing

Pengujian dilakukan dengan mengeksplorasi aplikasi secara bebas untuk menemukan kemungkinan masalah yang belum tercakup dalam test case.

### 4.7 Regression Testing

Pengujian dilakukan kembali terhadap fungsi yang sebelumnya telah diuji untuk memastikan perubahan atau perbaikan tidak menyebabkan masalah pada fungsi lainnya.

---

## 5. Lingkungan Pengujian

| Komponen | Konfigurasi |
|---|---|
| Aplikasi | SauceDemo |
| Sistem Operasi | Windows 10 |
| Browser | Google Chrome 152 |
| Metode Pengujian | Manual Testing |

---

## 6. Pendekatan Pengujian

Pengujian akan dilakukan secara manual dengan mengikuti test scenario dan test case yang telah dibuat.

Proses pengujian dilakukan dengan tahapan berikut:

1. Menganalisis fitur yang tersedia pada aplikasi.
2. Mengidentifikasi test scenario.
3. Membuat test case berdasarkan test scenario.
4. Menjalankan test case pada aplikasi.
5. Mencatat hasil aktual dari setiap pengujian.
6. Membandingkan hasil aktual dengan hasil yang diharapkan.
7. Membuat bug report apabila ditemukan perbedaan antara hasil aktual dan hasil yang diharapkan.
8. Melakukan regression testing apabila terdapat perbaikan terhadap bug.
9. Membuat test summary report setelah seluruh pengujian selesai.

---

## 7. Kriteria Awal Pengujian

Pengujian dapat dimulai apabila:

- Aplikasi SauceDemo dapat diakses.
- Fitur utama aplikasi dapat digunakan.
- Test scenario telah dibuat.
- Test case telah disiapkan.
- Environment pengujian telah tersedia.
- Akun untuk melakukan pengujian tersedia.

---

## 8. Kriteria Selesai Pengujian

Pengujian dapat dinyatakan selesai apabila:

- Seluruh test case yang telah direncanakan sudah dijalankan.
- Hasil pengujian telah didokumentasikan.
- Bug yang ditemukan telah dibuat dalam bug report.
- Fungsi utama aplikasi telah diverifikasi.
- Test summary report telah dibuat.

---

## 9. Hasil yang Akan Didokumentasikan

Dokumen yang akan dihasilkan dari proses pengujian meliputi:

- Test Plan
- Test Scenario
- Test Case
- Test Execution
- Bug Report
- Regression Testing

---

## 10. Risiko Pengujian

Beberapa risiko yang mungkin terjadi selama proses pengujian:

- Perubahan pada aplikasi selama proses pengujian.
- Gangguan koneksi internet yang dapat memengaruhi proses pengujian.
- Perbedaan hasil pengujian berdasarkan browser atau environment.
- Waktu pengujian yang terbatas sehingga tidak semua kondisi dapat diuji.
- Perubahan pada data atau kondisi aplikasi selama proses pengujian.

---

## 11. Asumsi

Asumsi yang digunakan dalam pengujian ini:

- Aplikasi SauceDemo dapat diakses selama proses pengujian.
- Tester memiliki akun yang dapat digunakan untuk melakukan pengujian.
- Browser dan sistem operasi dapat menjalankan aplikasi dengan baik.
- Koneksi internet tersedia selama proses pengujian.
- Fitur yang akan diuji tersedia dan dapat diakses.
