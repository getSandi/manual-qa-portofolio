# Regression Testing

## 1. Test Information

| Informasi | Detail |
|---|---|
| Aplikasi | SauceDemo (Swag Labs) |
| Sistem Operasi | Windows 10 |
| Browser | Google Chrome 152 |
| Testing Type | Regression Testing |
| Metode | Manual Testing |
| Pendekatan | Black Box Testing |
| Test Status | Completed |

---

## 2. Regression Testing Objective

Regression testing dilakukan untuk memastikan fungsi utama aplikasi SauceDemo tetap berjalan sesuai dengan expected result berdasarkan kondisi aplikasi saat pengujian dilakukan.

Regression testing dilakukan dengan menjalankan kembali test case yang telah dibuat pada fitur utama aplikasi.

Pada project ini, SauceDemo digunakan sebagai aplikasi demo untuk keperluan portfolio Manual QA. Tidak dilakukan proses bug fixing dan retest karena pengujian dilakukan terhadap kondisi aplikasi yang tersedia.

---

## 3. Regression Testing Scope

| Module | Regression Scope |
|---|---|
| Login | Memastikan fungsi login tetap berjalan sesuai dengan expected result. |
| Product | Memastikan daftar produk, informasi produk, detail produk, dan penambahan produk ke cart tetap berjalan. |
| Product Sorting | Memastikan seluruh opsi sorting produk tetap berjalan sesuai dengan expected result. |
| Shopping Cart | Memastikan fungsi membuka cart, menampilkan produk, menambah produk, menghapus produk, dan melanjutkan checkout tetap berjalan. |
| Checkout | Memastikan proses checkout dan validasi informasi checkout tetap berjalan. |
| Logout | Memastikan fungsi logout dan autentikasi setelah logout tetap berjalan. |

---

## 4. Regression Test Execution

## 4.1 Login

| Scenario ID | Test Case ID | Test Case | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TS-LOGIN-001 | TC-LOGIN-001 | Login dengan username dan password valid | `standard_user` / `secret_sauce` | Pengguna berhasil login dan diarahkan ke halaman Products. | Pengguna berhasil login dan diarahkan ke halaman Products. | PASS |
| TS-LOGIN-002 | TC-LOGIN-002 | Login dengan username tidak valid | `invalid_user` / `secret_sauce` | Sistem menolak login dan menampilkan pesan error. | Sistem menolak login dan menampilkan pesan error. | PASS |
| TS-LOGIN-003 | TC-LOGIN-003 | Login dengan password tidak valid | `standard_user` / `wrong_password` | Sistem menolak login dan menampilkan pesan error. | Sistem menolak login dan menampilkan pesan error. | PASS |
| TS-LOGIN-004 | TC-LOGIN-004 | Login dengan username kosong | Username kosong / `secret_sauce` | Sistem menampilkan validasi bahwa username diperlukan. | Sistem menampilkan validasi bahwa username diperlukan. | PASS |
| TS-LOGIN-005 | TC-LOGIN-005 | Login dengan password kosong | `standard_user` / Password kosong | Sistem menampilkan validasi bahwa password diperlukan. | Sistem menampilkan validasi bahwa password diperlukan. | PASS |
| TS-LOGIN-006 | TC-LOGIN-006 | Login menggunakan akun yang terkunci | `locked_out_user` / `secret_sauce` | Sistem menolak login dan menampilkan pesan bahwa pengguna terkunci. | Sistem menolak login dan menampilkan pesan bahwa pengguna terkunci. | PASS |

---

## 4.2 Product

| Scenario ID | Test Case ID | Test Case | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TS-PROD-001 | TC-PROD-001 | Menampilkan daftar produk | `standard_user` / `secret_sauce` | Daftar produk ditampilkan. | Daftar produk ditampilkan. | PASS |
| TS-PROD-002 | TC-PROD-002 | Menampilkan nama produk | - | Nama setiap produk ditampilkan. | Nama setiap produk ditampilkan. | PASS |
| TS-PROD-003 | TC-PROD-003 | Menampilkan harga produk | - | Harga setiap produk ditampilkan. | Harga setiap produk ditampilkan. | PASS |
| TS-PROD-004 | TC-PROD-004 | Menampilkan gambar produk | `problem_user` / `secret_sauce` | Setiap produk menampilkan gambar yang sesuai dengan produk tersebut. | Beberapa gambar produk tidak sesuai dengan produk ketika menggunakan `problem_user`. | FAIL |
| TS-PROD-005 | TC-PROD-005 | Membuka detail produk | Sauce Labs Backpack | Halaman detail produk yang dipilih ditampilkan. | Halaman detail produk yang dipilih ditampilkan. | PASS |
| TS-PROD-006 | TC-PROD-006 | Menambahkan produk ke shopping cart dari halaman Products | Sauce Labs Backpack | Produk ditambahkan ke shopping cart. | Produk berhasil ditambahkan ke shopping cart. | PASS |

---

## 4.3 Product Sorting

| Scenario ID | Test Case ID | Test Case | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TS-SORT-001 | TC-SORT-001 | Sorting nama A-Z | Name (A to Z) | Produk diurutkan berdasarkan nama dari A sampai Z. | Produk diurutkan berdasarkan nama dari A sampai Z. | PASS |
| TS-SORT-002 | TC-SORT-002 | Sorting nama Z-A | Name (Z to A) | Produk diurutkan berdasarkan nama dari Z sampai A. | Produk diurutkan berdasarkan nama dari Z sampai A. | PASS |
| TS-SORT-003 | TC-SORT-003 | Sorting harga rendah ke tinggi | Price (low to high) | Produk diurutkan berdasarkan harga terendah ke tertinggi. | Produk diurutkan berdasarkan harga terendah ke tertinggi. | PASS |
| TS-SORT-004 | TC-SORT-004 | Sorting harga tinggi ke rendah | Price (high to low) | Produk diurutkan berdasarkan harga tertinggi ke terendah. | Produk diurutkan berdasarkan harga tertinggi ke terendah. | PASS |

---

## 4.4 Shopping Cart

| Scenario ID | Test Case ID | Test Case | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TS-CART-001 | TC-CART-001 | Membuka shopping cart | - | Halaman Your Cart ditampilkan. | Halaman Your Cart ditampilkan. | PASS |
| TS-CART-002 | TC-CART-002 | Memastikan produk ditampilkan di shopping cart | Sauce Labs Backpack | Produk yang dipilih ditampilkan di shopping cart. | Produk yang dipilih ditampilkan di shopping cart. | PASS |
| TS-CART-003 | TC-CART-003 | Menghapus produk dari shopping cart | Sauce Labs Backpack / `problem_user` | Produk berhasil dihapus dari shopping cart. | Button Remove tidak dapat menghapus produk pada akun `problem_user`. | FAIL |
| TS-CART-004 | TC-CART-004 | Memastikan jumlah item bertambah | Dua produk | Jumlah item pada ikon shopping cart bertambah sesuai jumlah produk. | Jumlah item bertambah sesuai jumlah produk. | PASS |
| TS-CART-005 | TC-CART-005 | Memastikan jumlah item berkurang setelah produk dihapus | Produk dalam cart | Jumlah item pada shopping cart diperbarui. | Jumlah item diperbarui setelah produk dihapus. | PASS |
| TS-CART-006 | TC-CART-006 | Melanjutkan checkout dari shopping cart | Produk dalam cart | Pengguna diarahkan ke halaman Checkout: Your Information. | Pengguna diarahkan ke halaman Checkout: Your Information. | PASS |

---

## 4.5 Checkout

| Scenario ID | Test Case ID | Test Case | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TS-CHECK-001 | TC-CHECK-001 | Membuka halaman checkout | Produk dalam cart | Halaman Checkout: Your Information ditampilkan. | Halaman Checkout: Your Information ditampilkan. | PASS |
| TS-CHECK-002 | TC-CHECK-002 | Checkout menggunakan informasi valid | First Name: Soe / Last Name: Kar / ZIP: 12345 | Pengguna diarahkan ke halaman Checkout: Overview. | Pengguna diarahkan ke halaman Checkout: Overview. | PASS |
| TS-CHECK-003 | TC-CHECK-003 | Checkout dengan First Name kosong | First Name kosong | Sistem menampilkan validasi First Name diperlukan. | Sistem menampilkan validasi First Name diperlukan. | PASS |
| TS-CHECK-004 | TC-CHECK-004 | Checkout dengan Last Name kosong | Last Name kosong | Sistem menampilkan validasi Last Name diperlukan. | Sistem menampilkan validasi Last Name diperlukan. | PASS |
| TS-CHECK-005 | TC-CHECK-005 | Checkout dengan ZIP kosong | ZIP kosong | Sistem menampilkan validasi Postal Code diperlukan. | Sistem menampilkan validasi Postal Code diperlukan. | PASS |
| TS-CHECK-006 | TC-CHECK-006 | Memastikan informasi produk ditampilkan pada Checkout Overview | Produk dalam cart | Produk dan informasi order ditampilkan pada halaman Checkout: Overview. | Produk dan informasi order ditampilkan pada halaman Checkout: Overview. | PASS |
| TS-CHECK-007 | TC-CHECK-007 | Menyelesaikan checkout | Data checkout valid | Proses checkout berhasil diselesaikan. | Proses checkout berhasil diselesaikan. | PASS |
| TS-CHECK-008 | TC-CHECK-008 | Menampilkan konfirmasi checkout | Checkout berhasil | Sistem menampilkan konfirmasi bahwa pesanan berhasil. | Sistem menampilkan konfirmasi bahwa pesanan berhasil. | PASS |

---

## 4.6 Logout

| Scenario ID | Test Case ID | Test Case | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TS-LOGOUT-001 | TC-LOGOUT-001 | Logout dari aplikasi | `standard_user` | Pengguna berhasil logout. | Pengguna berhasil logout. | PASS |
| TS-LOGOUT-002 | TC-LOGOUT-002 | Memastikan pengguna diarahkan ke halaman Login setelah logout | - | Pengguna diarahkan ke halaman Login. | Pengguna diarahkan ke halaman Login. | PASS |
| TS-LOGOUT-003 | TC-LOGOUT-003 | Memastikan fitur membutuhkan autentikasi setelah logout | User sudah logout | Pengguna tidak dapat mengakses fitur yang membutuhkan autentikasi. | Pengguna tidak dapat mengakses fitur yang membutuhkan autentikasi. | PASS |

---

## 5. Regression Test Result

| Result | Total | Percentage |
|---|---:|---:|
| PASS | 32 | 94.12% |
| FAIL | 2 | 5.88% |
| BLOCKED | 0 | 0% |
| **Total** | **34** | **100%** |

---

## 6. Regression Pass Rate

```text
Pass Rate = (PASS / Total Test Case) × 100%

Pass Rate = (32 / 34) × 100%

Pass Rate = 94.12%
```
---
## 7. Failed Regression Test Cases

| Scenario ID | Test Case ID | Bug ID | Module | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TS-PROD-004 | TC-PROD-004 | BUG-001 | Product | Setiap produk menampilkan gambar yang sesuai dengan produk tersebut. | Beberapa gambar produk tidak sesuai dengan produk ketika menggunakan `problem_user`. | FAIL |
| TS-CART-003 | TC-CART-003 | BUG-002 | Shopping Cart | Produk berhasil dihapus ketika button Remove diklik. | Button Remove tidak dapat menghapus produk pada akun `problem_user`. | FAIL |

---

## 8. Bug Summary

| Bug ID | Test Case ID | Module | Title | Severity | Priority | Status |
|---|---|---|---|---|---|---|
| BUG-001 | TC-PROD-004 | Product | Gambar produk tidak sesuai dengan produk pada `problem_user` | Medium | Medium | Open |
| BUG-002 | TC-CART-003 | Shopping Cart | Button Remove tidak dapat menghapus produk pada `problem_user` | Medium | Medium | Open |

---

## 9. Bug Status Definition

| Status | Keterangan |
|---|---|
| PASS | Actual Result sesuai dengan Expected Result. |
| FAIL | Actual Result tidak sesuai dengan Expected Result dan terdapat defect. |
| BLOCKED | Test case tidak dapat dijalankan karena terdapat kondisi yang menghambat pengujian. |
| OPEN | Defect telah ditemukan dan didokumentasikan, tetapi belum diperbaiki atau diverifikasi melalui retest. |

---

## 10. Regression Testing Conclusion

Berdasarkan hasil regression testing terhadap **33 test case**, sebanyak **31 test case PASS** dan **2 test case FAIL**.

Regression testing menghasilkan **Pass Rate sebesar 93.94%**.

Dua test case yang FAIL adalah:

| Test Case ID | Bug ID | Module | Description |
|---|---|---|---|
| TC-PROD-004 | BUG-001 | Product | Beberapa gambar produk tidak sesuai dengan produk ketika menggunakan `problem_user`. |
| TC-CART-003 | BUG-002 | Shopping Cart | Button Remove tidak dapat menghapus produk pada akun `problem_user`. |

Kedua defect telah didokumentasikan pada Bug Report dengan status **Open**.

Status **Open** digunakan karena defect telah ditemukan dan didokumentasikan, tetapi belum terdapat proses perbaikan dan retest dalam project ini.

SauceDemo digunakan sebagai aplikasi demo untuk keperluan portfolio Manual QA. Oleh karena itu, regression testing dilakukan berdasarkan kondisi aplikasi yang tersedia pada saat pengujian.

---

## 11. Retest Status

| Item | Status |
|---|---|
| BUG-001 Retest | Not Performed |
| BUG-002 Retest | Not Performed |
| Bug Fix Verification | Not Performed |
| Reason | Tidak terdapat proses bug fixing dalam project portfolio ini. |

---

## 12. Regression Testing Final Status

| Item | Result |
|---|---|
| Application | SauceDemo (Swag Labs) |
| Testing Type | Regression Testing |
| Testing Method | Manual Testing |
| Testing Approach | Black Box Testing |
| Total Test Case | 33 |
| PASS | 31 |
| FAIL | 2 |
| BLOCKED | 0 |
| Pass Rate | 93.94% |
| Total Bug | 2 |
| Open Bug | 2 |
| Closed Bug | 0 |
| Retest | Not Performed |
| Final Regression Status | **NOT FULLY PASSED** |
