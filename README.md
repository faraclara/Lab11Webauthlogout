# Lab11Web 
Login, Auth dan logout.

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

#### 1. Membuat Tabel: User Login

![](img/1%20satu1.jpg)

#### 2. Membuat Model User

Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada 
direktori app/Models dengan nama UserModel.php

![](img/2%20models.jpg)

#### 3. Membuat Controller User

Buat Controller baru dengan nama User.php pada direktori app/Controllers.
Kemudian tambahkan method index() untuk menampilkan daftar user, dan method 
login() untuk proses login.

![](img/3%20controllers.jpg)

![](img/3a%20controllers.jpg)

#### 4. Membuat View Login

Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file 
baru dengan nama login.php. 

![](img/4%20views.jpg)


#### 5. Membuat Database Seeder

Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul 
login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat 
database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:


![](img/db%20seeder.jpg)

Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori 
/app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut:

![](img/5%20userseed.jpg)


Selanjutnya buka kembali CLI dan ketik perintah berikut:

![](img/db%20seeder2.jpg)


![](img/db%20seeder3.jpg)

#### 6. Uji Coba Login

Selanjutnya buka url http://localhost:8080/user/login seperti berikut:

![](img/login%20pagebener.jpg)

#### 7. Menambahkan Auth Filter

Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php
pada direktori app/Filters. 

![](img/filter%20page.jpg)

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:

![](img/filter%20page2.jpg)

![](img/filter%20page3.jpg)

Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.


#### Percobaan Akses Menu Admin

Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut 
diakses maka, akan dimuculkan halaman login

![](img/login%20pagebener.jpg)

#### Fungsi Logout

Tambahkan method logout pada Controller User seperti berikut

![](img/logout%20control.jpg)

![](img/akhir%20img.jpg)


## Pertanyaan dan Tugas

Selesaikan programnya sesuai Langkah-langkah yang ada. Anda boleh melakukan 
improvisasi.

## Laporan Praktikum

1. Melanjutkan praktikum sebelumnya pada repository dengan nama Lab11Web.
2. Kerjakan semua latihan yang diberikan sesuai urutannya.
3. Screenshot setiap perubahannya.
4. Update file README.md dan tuliskan penjelasan dari setiap langkah praktikum 
beserta screenshotnya.
5. Commit hasilnya pada repository masing-masing.
6. Kirim URL repository pada e-learning ecampus

