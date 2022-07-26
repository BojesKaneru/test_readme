###### Nama : Irdiansyah Nur R.
###### Kelas : XII RPL 1
###### No. Absen : 29

# Modul 1

## Soal No. 1 dan 2

Lakukan proses instalasi framework laravel kedalam folder dengan nama masing-masing dan Buatlah projek pertama laravel dengan nama projek “penjualan” dan tampilkan dalam browser.

![image](https://user-images.githubusercontent.com/109930784/180925516-8478c4a0-0dc9-4977-a07c-be065b8820b7.png)

composer create-project laravel/laravel penjualan


# Modul 2

## Soal No. 1

Buatlah migration tabel kategori dengan menggunakan teknik yang telah di pelajari dalam modul ini.

### Langkah Pertama

Buatlah Tabel Kategori Terlebih dahulu
...
php artisan make:migration create_kategori_table
...

### Langkah Kedua

Isikan code dibawah ini kedalam File yang sudah dibuat

![image](https://user-images.githubusercontent.com/109930784/180926116-33081a79-f60a-4f22-9d52-0ed6eb14824e.png)

Pastikan Kodenya Berjalan saat dijalankan di terminal menggunakan
...
php artisan migrate
...
Setelah bisa berjalan mari kita buat model kategori.

### Langkah Ketiga

ketik code ini didalam terminal untuk membuat model
...
php artisan make:model kategori
...

Hasil dari perintah di atas, akan ada satu file baru pada folder penjualan/app/models dengan nama kategori.php. hasil dari perintah artisan di atas dapat dilihat pada gambar dibawah.

![image](https://user-images.githubusercontent.com/109930784/180926378-4e48e10c-d6b7-4fe5-a5fa-a7f6d6f6517c.png)

jika nama file model disini adalah kategori maka nama tabel yang ada di dalam database adalah kategoris. Namun hal tersebut dapat dikonfigurasi dengan cara membuka file model kategori.php yang baru saja dibuat dan tambahkan script berikut:

![image](https://user-images.githubusercontent.com/109930784/180926571-edc6c871-5dca-4829-85dc-febd23995ad2.png)

value dari variabel ini akan dianggap sebagai nama tabel yang diwakili oleh model ini.

## Soal No. 2

Berikan data dengan menggunakan seeder yang telah anda pelajari pada modul ini.

### Langkah Pertama

Untuk Membuat Seeder, gunakan perintah artisan pada **CMD** seperti berikut:

![image](https://user-images.githubusercontent.com/109930784/180927100-fcca521c-0ad0-433f-be7b-7bf43c587de4.png)
...
php artisan make:seeder kategoriTableSeeder
...

Perintah tersebut akan menghasilkan satu file baru pada folder database/seeders dengan nama kategoriTableSeeder.php atau yang diketikan pada perintah. Hasil dari perintah artisan diatas dapat dilihat pada gambar dibawah:

![image](https://user-images.githubusercontent.com/109930784/180927171-8145bbdc-9cf7-4584-8e40-7ce6191db86f.png)

### Langkah Kedua

Buka file kategoriTableSeeder yang telah dibuat dan tambakan kode sehingga menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/109930784/180927411-a16b9500-463e-418a-a425-a86820bc46a3.png)

### Langkah Ketiga 

Buka file DatabaseSeeder.php yang ada pada folder database/seeds dan panggil seeder yang baru dibuat pada method run dengan menambahkan, berikut ini:

![image](https://user-images.githubusercontent.com/109930784/180927764-ad5982ea-b9e5-484b-8c69-ce767bb7967e.png)

setelah itu jalankan perintah artisan pada **CMD** untuk mengeksekusi seeder yang telah dibuat dengan perintah seperti berikut ini:
...
php artisan db:seed
...
