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

# 10. Recommendation

| No | Recommendation | Status |
|---:|---|---|
| 1 | Memperbaiki BUG-001 terkait gambar produk yang tidak sesuai. | Recommended |
| 2 | Memperbaiki BUG-002 terkait button Remove. | Recommended |
| 3 | Melakukan Retest setelah bug diperbaiki. | Recommended |
| 4 | Melakukan Regression Testing pada module Product. | Recommended |
| 5 | Melakukan Regression Testing pada module Shopping Cart. | Recommended |
| 6 | Memastikan fungsi yang sebelumnya PASS tetap berjalan setelah perbaikan. | Recommended |
| 7 | Mengupdate status Bug Report setelah Retest selesai. | Recommended |

---

# 11. Conclusion

| Metric | Result |
|---|---:|
| Total Test Case | 30 |
| PASS | 28 |
| FAIL | 2 |
| BLOCKED | 0 |
| Total Bug | 2 |
| Open Bug | 2 |
| Closed Bug | 0 |
| Pass Rate | 93.33% |

Berdasarkan hasil pengujian, sebanyak **28 dari 30 test case berhasil PASS** dan **2 test case FAIL**.

| Test Case ID | Bug ID | Description |
|---|---|---|
| TC-PROD-004 | BUG-001 | Gambar produk tidak sesuai ketika menggunakan `problem_user`. |
| TC-CART-003 | BUG-002 | Button Remove tidak dapat menghapus produk pada `problem_user`. |

Aplikasi belum dapat dinyatakan **Fully Passed** karena masih terdapat 2 bug dengan status **Open**.

---

# 12. Final Test Status

| Status | Result |
|---|---|
| Test Status | **NOT FULLY PASSED** |
| Total Test Case | 30 |
| PASS | 28 |
| FAIL | 2 |
| BLOCKED | 0 |
| Total Bug | 2 |
| Open Bug | 2 |
| Closed Bug | 0 |
| Pass Rate | 93.33% |

---

# 13. QA Testing Flow

| Step | Testing Process | Status |
|---:|---|---|
| 1 | Test Plan | Completed |
| 2 | Test Scenario | Completed |
| 3 | Test Case | Completed |
| 4 | Test Execution | Completed |
| 5 | Bug Report | Completed |
| 6 | Test Summary Report | Completed |

### Final Testing Result

| Item | Result |
|---|---|
| Application | SauceDemo (Swag Labs) |
| Total Test Case | 30 |
| Passed | 28 |
| Failed | 2 |
| Blocked | 0 |
| Total Bug | 2 |
| Open Bug | 2 |
| Pass Rate | 93.33% |
| Final Status | **NOT FULLY PASSED** |
