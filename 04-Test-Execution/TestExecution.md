
# Test Execution

## Informasi Pengujian

| Informasi | Detail |
|---|---|
| Aplikasi | SauceDemo (Swag Labs) |
| Sistem Operasi | Windows 10 |
| Browser | Google Chrome 152 |
| Metode | Manual Testing |
| Pendekatan | Black Box Testing |

---

# 1. Login

| Scenario ID | Test Case ID | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TS-LOGIN-001 | TC-LOGIN-001 | Pengguna berhasil login dan diarahkan ke halaman Products. | Pengguna berhasil login menggunakan `standard_user` dan diarahkan ke halaman Products. | PASS |
| TS-LOGIN-002 | TC-LOGIN-002 | Sistem menolak login dan menampilkan pesan error. | Sistem menolak login menggunakan username tidak valid dan menampilkan pesan error. | PASS |
| TS-LOGIN-003 | TC-LOGIN-003 | Sistem menolak login dan menampilkan pesan error. | Sistem menolak login menggunakan password tidak valid dan menampilkan pesan error. | PASS |
| TS-LOGIN-004 | TC-LOGIN-004 | Sistem menampilkan validasi bahwa username diperlukan. | Sistem menampilkan pesan bahwa username diperlukan. | PASS |
| TS-LOGIN-005 | TC-LOGIN-005 | Sistem menampilkan validasi bahwa password diperlukan. | Sistem menampilkan pesan bahwa password diperlukan. | PASS |
| TS-LOGIN-006 | TC-LOGIN-006 | Sistem menolak login dan menampilkan pesan bahwa pengguna terkunci. | Login menggunakan `locked_out_user` ditolak dan sistem menampilkan pesan bahwa pengguna terkunci. | PASS |

---

# 2. Product

| Scenario ID | Test Case ID | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TS-PROD-001 | TC-PROD-001 | Daftar produk ditampilkan. | Daftar produk berhasil ditampilkan setelah login. | PASS |
| TS-PROD-002 | TC-PROD-002 | Nama setiap produk ditampilkan. | Nama produk ditampilkan pada setiap product card. | PASS |
| TS-PROD-003 | TC-PROD-003 | Harga setiap produk ditampilkan. | Harga produk ditampilkan pada setiap product card. | PASS |
| TS-PROD-004 | TC-PROD-004 | Setiap produk menampilkan gambar yang sesuai dengan produk tersebut. | Setelah login menggunakan `problem_user`, beberapa gambar produk tidak sesuai dengan produk yang ditampilkan. | FAIL |
| TS-PROD-005 | TC-PROD-005 | Halaman detail produk yang dipilih ditampilkan. | Halaman detail produk berhasil dibuka. | PASS |
| TS-PROD-006 | TC-PROD-006 | Produk berhasil ditambahkan ke shopping cart. | Produk berhasil ditambahkan ke shopping cart. | PASS |

---

# 3. Product Sorting

| Scenario ID | Test Case ID | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TS-SORT-001 | TC-SORT-001 | Produk diurutkan berdasarkan nama dari A sampai Z. | Produk berhasil diurutkan berdasarkan nama dari A sampai Z. | PASS |
| TS-SORT-002 | TC-SORT-002 | Produk diurutkan berdasarkan nama dari Z sampai A. | Produk berhasil diurutkan berdasarkan nama dari Z sampai A. | PASS |
| TS-SORT-003 | TC-SORT-003 | Produk diurutkan berdasarkan harga terendah ke tertinggi. | Produk berhasil diurutkan berdasarkan harga dari terendah ke tertinggi. | PASS |
| TS-SORT-004 | TC-SORT-004 | Produk diurutkan berdasarkan harga tertinggi ke terendah. | Produk berhasil diurutkan berdasarkan harga dari tertinggi ke terendah. | PASS |

---

# 4. Shopping Cart

| Scenario ID | Test Case ID | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TS-CART-001 | TC-CART-001 | Halaman Your Cart ditampilkan. | Halaman Your Cart berhasil ditampilkan. | PASS |
| TS-CART-002 | TC-CART-002 | Produk yang dipilih ditampilkan di shopping cart. | Produk yang dipilih ditampilkan di shopping cart. | PASS |
| TS-CART-003 | TC-CART-003 | Produk berhasil dihapus dari shopping cart. | Button Remove tidak dapat menghapus produk pada akun `problem_user` | FAIL |
| TS-CART-004 | TC-CART-004 | Jumlah item pada shopping cart bertambah sesuai jumlah produk. | Jumlah item bertambah sesuai jumlah produk yang ditambahkan. | PASS |
| TS-CART-005 | TC-CART-005 | Jumlah item pada shopping cart diperbarui setelah produk dihapus. | Jumlah item diperbarui setelah produk dihapus. | PASS |
| TS-CART-006 | TC-CART-006 | Pengguna diarahkan ke halaman Checkout: Your Information. | Pengguna berhasil diarahkan ke halaman Checkout: Your Information. | PASS |

---

# 5. Checkout

| Scenario ID | Test Case ID | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TS-CHECK-001 | TC-CHECK-001 | Halaman Checkout: Your Information ditampilkan. | Halaman Checkout: Your Information berhasil ditampilkan. | PASS |
| TS-CHECK-002 | TC-CHECK-002 | Pengguna diarahkan ke Checkout: Overview. | Pengguna berhasil diarahkan ke Checkout: Overview. | PASS |
| TS-CHECK-003 | TC-CHECK-003 | Validasi First Name ditampilkan. | Validasi First Name ditampilkan ketika field dikosongkan. | PASS |
| TS-CHECK-004 | TC-CHECK-004 | Validasi Last Name ditampilkan. | Validasi Last Name ditampilkan ketika field dikosongkan. | PASS |
| TS-CHECK-005 | TC-CHECK-005 | Validasi Postal Code ditampilkan. | Validasi Postal Code ditampilkan ketika field dikosongkan. | PASS |
| TS-CHECK-006 | TC-CHECK-006 | Informasi produk dan order ditampilkan pada Checkout: Overview. | Informasi produk dan order ditampilkan. | PASS |
| TS-CHECK-007 | TC-CHECK-007 | Proses checkout berhasil diselesaikan. | Checkout berhasil diselesaikan. | PASS |
| TS-CHECK-008 | TC-CHECK-008 | Sistem menampilkan konfirmasi bahwa pesanan berhasil. | Halaman konfirmasi pesanan ditampilkan. | PASS |

---

# 6. Logout

| Scenario ID | Test Case ID | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TS-LOGOUT-001 | TC-LOGOUT-001 | Pengguna berhasil logout. | Pengguna berhasil logout. | PASS |
| TS-LOGOUT-002 | TC-LOGOUT-002 | Pengguna diarahkan ke halaman Login. | Pengguna diarahkan ke halaman Login. | PASS |
| TS-LOGOUT-003 | TC-LOGOUT-003 | Pengguna tidak dapat mengakses fitur yang membutuhkan autentikasi. | Setelah logout, pengguna tidak dapat menggunakan fitur yang membutuhkan autentikasi. | PASS |

---

# Test Execution Summary

| Total Test Case | PASS | FAIL | BLOCKED |
|---:|---:|---:|---:|
| 30 | 28 | 2 | 0 |

## Failed Test Cases

| Test Case ID | Defect | Severity | Priority |
|---|---|---|---|
| TC-PROD-004 | Gambar produk tidak sesuai ketika menggunakan `problem_user` | Medium | Medium |
| TC-CART-003 | Button Remove tidak dapat menghapus produk pada akun `problem_user` | Medium | Medium |

## Kesimpulan

Dari 30 test case yang dieksekusi, terdapat 28 test case PASS dan 2 test case FAIL.

Kedua test case FAIL kemudian akan dianalisis lebih lanjut dan dibuatkan Bug Report.
