# Test Summary Report

## 1. Test Summary

| Informasi | Detail |
|---|---|
| Aplikasi | SauceDemo (Swag Labs) |
| Sistem Operasi | Windows 10 |
| Browser | Google Chrome 152 |
| Metode | Manual Testing |
| Pendekatan | Black Box Testing |
| Test Status | Completed |

---

# 2. Test Objective

| Objective | Detail |
|---|---|
| Tujuan Pengujian | Memastikan fitur utama SauceDemo berjalan sesuai dengan expected result. |
| Testing Type | Manual Testing |
| Testing Approach | Black Box Testing |
| Fokus Pengujian | Functional Testing |
| Defect Detection | Menemukan defect yang dapat memengaruhi fungsi aplikasi dan user experience. |

---

# 3. Test Scope

| Scope | Feature |
|---|---|
| In Scope | Login |
| In Scope | Product |
| In Scope | Product Sorting |
| In Scope | Shopping Cart |
| In Scope | Checkout |
| In Scope | Logout |
| Out of Scope | Performance Testing |
| Out of Scope | Load Testing |
| Out of Scope | Security Testing |
| Out of Scope | API Testing |
| Out of Scope | Database Testing |

---

# 4. Test Execution Summary

| Result | Total | Percentage |
|---|---:|---:|
| PASS | 28 | 93.33% |
| FAIL | 2 | 6.67% |
| BLOCKED | 0 | 0% |
| **Total** | **30** | **100%** |

---

# 5. Failed Test Cases

| Scenario ID | Test Case ID | Module | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| TS-PROD-004 | TC-PROD-004 | Product | Setiap produk menampilkan gambar yang sesuai dengan produk tersebut. | Beberapa gambar produk tidak sesuai dengan produk ketika menggunakan `problem_user`. | FAIL |
| TS-CART-003 | TC-CART-003 | Shopping Cart | Produk berhasil dihapus ketika button Remove diklik. | Button Remove tidak dapat menghapus produk pada akun `problem_user`. | FAIL |

---

# 6. Bug Summary

| Bug ID | Test Case ID | Module | Title | Severity | Priority | Status |
|---|---|---|---|---|---|---|
| BUG-001 | TC-PROD-004 | Product | Gambar produk tidak sesuai dengan produk pada `problem_user` | Medium | Medium | Open |
| BUG-002 | TC-CART-003 | Shopping Cart | Button Remove tidak dapat menghapus produk pada `problem_user` | Medium | Medium | Open |

---

# 7. BUG-001 Summary

## Product Image Tidak Sesuai

| Field | Detail |
|---|---|
| Bug ID | BUG-001 |
| Test Case ID | TC-PROD-004 |
| Scenario ID | TS-PROD-004 |
| Module | Product |
| Title | Gambar produk tidak sesuai dengan produk pada `problem_user` |
| Environment | Windows 10, Google Chrome 152 |
| Test Account | `problem_user` |
| Severity | Medium |
| Priority | Medium |
| Status | Open |

### Description

| Field | Detail |
|---|---|
| Preconditions | Pengguna login menggunakan akun `problem_user`. |
| Expected Result | Setiap produk menampilkan gambar yang sesuai dengan produk tersebut. |
| Actual Result | Beberapa gambar produk tidak sesuai dengan produk yang ditampilkan. |
| Impact | User dapat mengalami kebingungan karena gambar produk tidak sesuai dengan produk sebenarnya. |

### Test Data

| Data | Value |
|---|---|
| Username | `problem_user` |
| Password | `secret_sauce` |

---

# 8. BUG-002 Summary

## Button Remove Tidak Dapat Menghapus Produk

| Field | Detail |
|---|---|
| Bug ID | BUG-002 |
| Test Case ID | TC-CART-003 |
| Scenario ID | TS-CART-003 |
| Module | Shopping Cart |
| Title | Button Remove tidak dapat menghapus produk pada `problem_user` |
| Environment | Windows 10, Google Chrome 152 |
| Test Account | `problem_user` |
| Severity | Medium |
| Priority | Medium |
| Status | Open |

### Description

| Field | Detail |
|---|---|
| Preconditions | Pengguna login menggunakan akun `problem_user` dan produk telah ditambahkan ke shopping cart. |
| Expected Result | Produk berhasil dihapus dari shopping cart ketika button Remove diklik. |
| Actual Result | Button Remove tidak dapat menghapus produk pada akun `problem_user`. |
| Impact | User tidak dapat menghapus produk dari shopping cart melalui button Remove. |

### Test Data

| Data | Value |
|---|---|
| Username | `problem_user` |
| Password | `secret_sauce` |
| Product | Sauce Labs Backpack |
| Action | Add to cart → Remove |

---

# 9. Defect Analysis

| Bug ID | Module | Severity | Priority | Impact | Status |
|---|---|---|---|---|---|
| BUG-001 | Product | Medium | Medium | Gambar produk tidak sesuai dan dapat membingungkan user. | Open |
| BUG-002 | Shopping Cart | Medium | Medium | User tidak dapat menghapus produk melalui button Remove. | Open |

---

# 10. Regression Testing

## 10.1 Regression Testing Objective

Regression testing dilakukan untuk memastikan fungsi utama aplikasi tetap berjalan dan untuk mengidentifikasi apakah terdapat perubahan perilaku pada fitur yang sebelumnya telah diuji.

Pada project ini, SauceDemo digunakan sebagai aplikasi demo untuk keperluan testing. Oleh karena itu, regression testing dilakukan sebagai **baseline regression testing** berdasarkan kondisi aplikasi saat pengujian dilakukan.

Regression testing ini bukan merupakan retest setelah bug diperbaiki karena BUG-001 dan BUG-002 masih berstatus **Pending**.

---

## 10.2 Regression Testing Scope

| Module | Regression Scope |
|---|---|
| Login | Memastikan pengguna dapat login menggunakan akun valid. |
| Product | Memastikan daftar dan detail produk dapat ditampilkan. |
| Product Sorting | Memastikan fungsi sorting produk dapat digunakan. |
| Shopping Cart | Memastikan produk dapat ditambahkan, ditampilkan, dan dihapus dari cart. |
| Checkout | Memastikan proses checkout dapat dilakukan. |
| Logout | Memastikan pengguna dapat logout dari aplikasi. |

---

## 10.3 Regression Test Result

| Module | Test Case | Result |
|---|---:|---|
| Login | 6 | PASS |
| Product | 6 | FAIL |
| Product Sorting | 4 | PASS |
| Shopping Cart | 6 | FAIL |
| Checkout | 8 | PASS |
| Logout | 3 | PASS |
| **Total** | **33** | **-** |

> Catatan: Jumlah test case pada tabel regression di atas mengikuti test case yang tersedia pada dokumen Test Case. Hasil regression harus dicatat berdasarkan test case yang benar-benar dieksekusi.

---

## 10.4 Regression Testing Status

| Item | Status |
|---|---|
| Regression Testing | Completed |
| Regression After Bug Fix | Not Performed |
| BUG-001 | Pending |
| BUG-002 | Pending |

### Regression Testing Conclusion

Hasil regression testing menunjukkan bahwa fungsi utama aplikasi tetap dapat diuji berdasarkan kondisi aplikasi saat testing dilakukan.

BUG-001 pada module Product dan BUG-002 pada module Shopping Cart masih berstatus **Pending** karena SauceDemo digunakan sebagai aplikasi demo dan tidak terdapat proses perbaikan defect dalam project ini.

Regression testing setelah bug fix tidak dilakukan karena tidak terdapat perubahan atau perbaikan bug yang perlu diverifikasi.

---

# 11. Recommendation

| No | Recommendation | Status |
|---:|---|---|
| 1 | Mendokumentasikan BUG-001 terkait gambar produk yang tidak sesuai. | Completed |
| 2 | Mendokumentasikan BUG-002 terkait button Remove. | Completed |
| 3 | Mempertahankan status BUG-001 dan BUG-002 sebagai Pending. | Completed |
| 4 | Melakukan regression testing terhadap fungsi utama aplikasi. | Completed |
| 5 | Melakukan retest apabila terdapat perbaikan terhadap defect pada environment yang sama. | Pending |
| 6 | Melakukan regression testing kembali apabila terdapat perubahan pada aplikasi. | Recommended |

---

# 12. Conclusion

| Metric | Result |
|---|---:|
| Total Test Case | 30 |
| PASS | 28 |
| FAIL | 2 |
| BLOCKED | 0 |
| Total Bug | 2 |
| Pending Bug | 2 |
| Closed Bug | 0 |
| Pass Rate | 93.33% |

Berdasarkan hasil pengujian, sebanyak **28 dari 30 test case berhasil PASS** dan **2 test case FAIL**.

| Test Case ID | Bug ID | Description |
|---|---|---|
| TC-PROD-004 | BUG-001 | Gambar produk tidak sesuai ketika menggunakan `problem_user`. |
| TC-CART-003 | BUG-002 | Button Remove tidak dapat menghapus produk pada `problem_user`. |

Kedua defect telah didokumentasikan dalam Bug Report dan memiliki status **Pending**.

Regression testing dilakukan untuk memastikan fungsi utama aplikasi tetap dapat diuji berdasarkan kondisi aplikasi saat testing dilakukan.

Karena SauceDemo digunakan sebagai aplikasi demo dan tidak terdapat proses bug fixing dalam project ini, **retest setelah bug fix tidak dilakukan**.

---

# 13. Final Test Status

| Status | Result |
|---|---|
| Test Status | **NOT FULLY PASSED** |
| Total Test Case | 30 |
| PASS | 28 |
| FAIL | 2 |
| BLOCKED | 0 |
| Total Bug | 2 |
| Pending Bug | 2 |
| Closed Bug | 0 |
| Pass Rate | 93.33% |
| Regression Testing | Completed |
| Retest After Bug Fix | Not Performed |
| Final Status | **NOT FULLY PASSED** |

---

# 14. QA Testing Flow

| Step | Testing Process | Status |
|---:|---|---|
| 1 | Test Plan | Completed |
| 2 | Test Scenario | Completed |
| 3 | Test Case | Completed |
| 4 | Test Execution | Completed |
| 5 | Bug Report | Completed |
| 6 | Regression Testing | Completed |
| 7 | Test Summary Report | Completed |

### Final Testing Result

| Item | Result |
|---|---|
| Application | SauceDemo (Swag Labs) |
| Total Test Case | 30 |
| Passed | 28 |
| Failed | 2 |
| Blocked | 0 |
| Total Bug | 2 |
| Pending Bug | 2 |
| Pass Rate | 93.33% |
| Regression Testing | Completed |
| Retest After Bug Fix | Not Performed |
| Final Status | **NOT FULLY PASSED** |
