---
layout: post
title: "Instalasi Ruby dan Jekyll"
---

Penjelasan tentang Instalasi Ruby dan Jekyll

![HTML Link dan List](/assets/image/gamabar_ruby%20image.png)

---

## 1. Instalasi Untuk Windows:
Menggunakan RubyInstaller:

1. Kunjungi situs web resmi RubyInstaller di https://rubyinstaller.org/.
2. Unduh versi Ruby yang sesuai dengan sistem operasi Anda (Windows 64-bit atau 32-bit).
3. Jalankan installer dan ikuti langkah-langkahnya.
4. Pastikan untuk mencentang opsi yang mengatakan "Add Ruby to PATH" saat instalasi.
5. Setelah instalasi selesai, buka Command Prompt atau PowerShell dan periksa versi Ruby dengan:

_ruby -v_



## 2. Instalasi Jekyll
Setelah Ruby terinstal, langkah berikutnya adalah menginstal Jekyll, yang merupakan generator situs statis yang dibangun dengan Ruby.

#### a. Instalasi Jekyll menggunakan RubyGems
1. Instalasi Jekyll di macOS, Linux, atau Windows:

* Buka terminal atau command prompt dan jalankan perintah berikut untuk menginstal Jekyll dan Bundler (manajer dependensi Ruby):

_gem install jekyll bundler_


* Tunggu hingga instalasi selesai. Setelah selesai, Anda dapat memverifikasi instalasi dengan menjalankan:

_jekyll -v_


#### b. Membuat Situs Baru dengan Jekyll
Setelah menginstal Jekyll, Anda bisa membuat situs baru.

Buat Situs Baru dengan Jekyll:

1. Jalankan perintah berikut untuk membuat situs Jekyll baru:

*jekyll new nama_situs*

Gantilah nama_situs dengan nama folder yang Anda inginkan untuk situs Anda.

2. Masuk ke Direktori Situs: Setelah situs dibuat, masuk ke dalam folder situs tersebut:

*cd nama_situs*


3. Menjalankan Server Jekyll Lokal: Anda dapat menjalankan server lokal untuk melihat situs web Jekyll Anda:

*bundle exec jekyll serve*

* Setelah itu, buka browser dan kunjungi http://localhost:4000 untuk melihat situs Anda.

#### c. Instalasi pada Windows (Alternatif menggunakan WSL)
Jika Anda menggunakan Windows, Anda bisa menginstal Jekyll di lingkungan Windows Subsystem for Linux (WSL). Untuk itu, pastikan Anda menginstal WSL terlebih dahulu dan menggunakan distribusi Linux seperti Ubuntu.

Berikut adalah langkah-langkah umum:

1. Instal WSL dari Microsoft Store dan pilih Ubuntu.

2. Jalankan Ubuntu dan ikuti instruksi di atas untuk menginstal Ruby dan Jekyll di Ubuntu.


3. Memperbarui Jekyll dan Ruby
Jika suatu saat Anda perlu memperbarui Jekyll atau Ruby:

* Untuk memperbarui Jekyll, jalankan:

_gem update jekyll_

* Untuk memperbarui Ruby, gunakan Homebrew (macOS) atau apt (Linux) untuk memperbarui paketnya.

4. Masalah Umum dan Pemecahan Masalah
* Error saat instalasi Jekyll (permissoin denied): Jika Anda mengalami masalah dengan izin, Anda bisa mencoba menambahkan sudo pada perintah instalasi di macOS/Linux:

_sudo gem install jekyll bundler_

* Tidak bisa menjalankan jekyll serve: Pastikan Anda berada di dalam direktori proyek Jekyll dan menjalankan perintah bundle exec jekyll serve di terminal.

* Masalah dengan versi Ruby: Pastikan Anda menginstal versi Ruby yang kompatibel dengan Jekyll. Jika perlu, gunakan versi Ruby tertentu menggunakan RVM (Ruby Version Manager).

