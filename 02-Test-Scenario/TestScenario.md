# Test Scenario

## Informasi Pengujian

| Informasi       | Detail                |
| --------------- | --------------------- |
| Aplikasi        | SauceDemo (Swag Labs) |
| Jenis Pengujian | Manual QA             |
| Pendekatan      | Black Box Testing     |
| Sistem Operasi  | Windows 10            |
| Browser         | Google Chrome 152     |

---

# 1. Login

| ID           | Test Scenario                                                                |
| ------------ | ---------------------------------------------------------------------------- |
| TS-LOGIN-001 | Memastikan pengguna dapat login menggunakan username dan password yang valid |
| TS-LOGIN-002 | Memastikan sistem menolak login menggunakan username yang tidak valid        |
| TS-LOGIN-003 | Memastikan sistem menolak login menggunakan password yang tidak valid        |
| TS-LOGIN-004 | Memastikan sistem memberikan validasi ketika username kosong                 |
| TS-LOGIN-005 | Memastikan sistem memberikan validasi ketika password kosong                 |
| TS-LOGIN-006 | Memastikan sistem dapat menangani akun pengguna yang terkunci                |

---

# 2. Product

| ID          | Test Scenario                                                              |
| ----------- | -------------------------------------------------------------------------- |
| TS-PROD-001 | Memastikan daftar produk dapat ditampilkan setelah pengguna berhasil login |
| TS-PROD-002 | Memastikan nama produk ditampilkan dengan benar                            |
| TS-PROD-003 | Memastikan harga produk ditampilkan dengan benar                           |
| TS-PROD-004 | Memastikan gambar produk ditampilkan dengan benar                          |
| TS-PROD-005 | Memastikan pengguna dapat membuka detail produk                            |
| TS-PROD-006 | Memastikan pengguna dapat menambahkan produk ke shopping cart              |

---

# 3. Product Sorting

| ID          | Test Scenario                                                                        |
| ----------- | ------------------------------------------------------------------------------------ |
| TS-SORT-001 | Memastikan pengguna dapat mengurutkan produk berdasarkan nama dari A sampai Z        |
| TS-SORT-002 | Memastikan pengguna dapat mengurutkan produk berdasarkan nama dari Z sampai A        |
| TS-SORT-003 | Memastikan pengguna dapat mengurutkan produk berdasarkan harga terendah ke tertinggi |
| TS-SORT-004 | Memastikan pengguna dapat mengurutkan produk berdasarkan harga tertinggi ke terendah |

---

# 4. Shopping Cart

| ID          | Test Scenario                                                                   |
| ----------- | ------------------------------------------------------------------------------- |
| TS-CART-001 | Memastikan pengguna dapat membuka shopping cart                                 |
| TS-CART-002 | Memastikan produk yang dipilih ditampilkan di shopping cart                     |
| TS-CART-003 | Memastikan pengguna dapat menghapus produk dari shopping cart                   |
| TS-CART-004 | Memastikan jumlah item pada shopping cart diperbarui setelah produk ditambahkan |
| TS-CART-005 | Memastikan jumlah item pada shopping cart diperbarui setelah produk dihapus     |
| TS-CART-006 | Memastikan pengguna dapat melanjutkan proses checkout dari shopping cart        |

---

# 5. Checkout

| ID           | Test Scenario                                                                   |
| ------------ | ------------------------------------------------------------------------------- |
| TS-CHECK-001 | Memastikan pengguna dapat membuka halaman checkout                              |
| TS-CHECK-002 | Memastikan pengguna dapat melanjutkan checkout menggunakan informasi yang valid |
| TS-CHECK-003 | Memastikan sistem memberikan validasi ketika First Name kosong                  |
| TS-CHECK-004 | Memastikan sistem memberikan validasi ketika Last Name kosong                   |
| TS-CHECK-005 | Memastikan sistem memberikan validasi ketika ZIP/Postal Code kosong             |
| TS-CHECK-006 | Memastikan informasi produk ditampilkan pada halaman Checkout Overview          |
| TS-CHECK-007 | Memastikan pengguna dapat menyelesaikan proses checkout                         |
| TS-CHECK-008 | Memastikan sistem menampilkan konfirmasi setelah checkout berhasil              |

---

# 6. Logout

| ID            | Test Scenario                                                                               |
| ------------- | ------------------------------------------------------------------------------------------- |
| TS-LOGOUT-001 | Memastikan pengguna dapat logout dari aplikasi                                              |
| TS-LOGOUT-002 | Memastikan pengguna diarahkan ke halaman Login setelah logout                               |
| TS-LOGOUT-003 | Memastikan pengguna tidak dapat mengakses fitur yang membutuhkan autentikasi setelah logout |
