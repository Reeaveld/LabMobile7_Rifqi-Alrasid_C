# Screenshot

![Screenshot (1617)](https://github.com/user-attachments/assets/81b6486d-2aab-4dfc-b682-a8985a5f29cf)
![Screenshot (1618)](https://github.com/user-attachments/assets/ed956136-73d8-49bc-8985-0866bb4fcd9e)
![Screenshot 2024-11-05 193644 (1)](https://github.com/user-attachments/assets/3b52070f-3c89-4429-b025-7f81ff411dd3)
![Screenshot (1619)](https://github.com/user-attachments/assets/aed3a298-6b30-49f9-9e7e-67ffd7961226)

# Penjelasan
Database dan API: Database MySQL dibuat dengan tabel user untuk menyimpan `username` dan `password` (dalam hash MD5). API PHP dibuat untuk mengakses database, dengan `login.php` yang memverifikasi pengguna berdasarkan data yang diinputkan.

Autentikasi di Ionic: Di aplikasi Ionic, `authentication.service.ts` mengelola login. Data pengguna (token dan nama) disimpan menggunakan `@capacitor/preferences`, dan kondisi login diperiksa melalui `isAuthenticated`.

Auth Guards: `authGuard` dan `autoLoginGuard` memastikan pengguna yang belum login diarahkan ke halaman login, sedangkan pengguna yang sudah login langsung ke halaman utama (home).

Halaman Login: `login.page.ts` menangani input login, memvalidasi dengan API, menyimpan data pengguna, dan memberi notifikasi jika login gagal.

Halaman Home: Menampilkan sambutan dan tombol logout, yang menghapus data login dari Preferences dan mengarahkan kembali ke login.
