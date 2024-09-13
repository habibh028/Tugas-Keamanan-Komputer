Ini tugas 2

# Panduan Penggunaan Sublist3r

Panduan ini menjelaskan cara menggunakan Sublist3r untuk mencari sub-domain dan memeriksa port yang terbuka pada domain target.

1. Mencari Sub-Domain dengan Opsi `-d`

Anda dapat menggunakan opsi `-d` di Sublist3r untuk mencari sub-domain dari sebuah domain. Sebagai contoh, untuk mencari sub-domain dari `facebook.com`, gunakan perintah berikut:

sublist3r -d facebook.com
Perintah ini akan menampilkan daftar sub-domain yang terkait dengan facebook.com (misalnya, mail.facebook.com, developers.facebook.com, dll.).

![3](https://github.com/user-attachments/assets/2923f2ac-3118-44f9-acdb-866358581bb7)


2. Kombinasi dengan Opsi -t untuk Menentukan Jumlah Threads

Opsi -t memungkinkan Anda menentukan jumlah threads yang digunakan dalam proses pencarian. Semakin banyak threads yang digunakan, semakin cepat proses pencarian, terutama untuk domain yang besar. Berikut contohnya:

bash
Salin kode
sublist3r -d facebook.com -t 5
Dalam perintah ini:

-t 5 menunjukkan bahwa 5 threads akan digunakan untuk menemukan sub-domain, sehingga mempercepat proses pencarian dengan menjalankan proses secara paralel.

![2](https://github.com/user-attachments/assets/f280e0b6-b665-477d-833c-50bf9591183d)


3. Memeriksa Port yang Terbuka dengan Opsi -p

Sublist3r juga memungkinkan Anda memeriksa port yang terbuka pada sub-domain yang ditemukan dengan opsi -p. Anda bisa menentukan port mana yang ingin diperiksa, misalnya port 443 (HTTPS) dan port 80 (HTTP):

bash
Salin kode
sublist3r -d facebook.com -p 443,80
Dalam perintah ini:
-p 443,80 akan memeriksa apakah port 443 dan 80 terbuka pada sub-domain yang ditemukan.

![1](https://github.com/user-attachments/assets/5fcdbf7a-6962-4712-8e4a-099537cbed8c)


