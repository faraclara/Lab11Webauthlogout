# Lab11Web 
Auth dan logout

###### Nama : Fara Deviana
###### NIM : 312010407
###### Kelas : TI.A.2

## Instruksi Praktikum

1. Persiapkan text editor misalnya VSCode.
2. Buka kembali folder dengan nama lab11_php_ci pada docroot webserver (htdocs)
3. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya.

## Langkah-langkah Praktikum

Persiapan.
Untuk memulai membuat modul Login, yang perlu disiapkan adalah database server 
menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui 
XAMPP.

#### Membuat Tabel: User Login

Gambar 1 DB
![](img/1%20satu.jpg)

#### Membuat Tabel User

Gambar 2 Table

#### Membuat Model User

Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada 
direktori app/Models dengan nama UserModel.php

Gambar 3 Model vsc


#### Membuat Controller User

Buat Controller baru dengan nama User.php pada direktori app/Controllers.
Kemudian tambahkan method index() untuk menampilkan daftar user, dan method 
login() untuk proses login.

Gambar 4 Controller vsc

#### Membuat View Login

Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file 
baru dengan nama login.php. 


#### Membuat Database Seeder


Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul 
login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat 
database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:

Gambar 5 CLI DB seeder

Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori 
/app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut:


Gambar 6 Seeder DB

Selanjutnya buka kembali CLI dan ketik perintah berikut:

Gambar 7 use seeder DB

Uji Coba Login
Selanjutnya buka url http://localhost:8080/user/login seperti berikut:

Gambar 8 Login page

#### Menambahkan Auth Filter

Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php
pada direktori app/Filters. 

Gambar 9 tambah Auth

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:

Gambar 10 app/Config/Filters.php

Gambar 11 isi vsc app/Config/Filters.php

Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.

Gambar 12 Routes

#### Percobaan Akses Menu Admin

Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut 
diakses maka, akan dimuculkan halaman login

#### Fungsi Logout

Tambahkan method logout pada Controller User seperti berikut

Gambar 13 logout
