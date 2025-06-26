---
layout: post
title: "Xampp dan PHP"
---

Penjelasan Xampp dan PHP

---


## Apa itu XAMPP?

XAMPP adalah paket perangkat lunak yang dikembangkan oleh **Apache Friends**. Digunakan untuk membuat server lokal guna menjalankan aplikasi berbasis web (PHP + MySQL) di komputer pribadi.

Installer XAMPP dapat diunduh melalui situs resminya:  
🔗 [https://www.apachefriends.org](https://www.apachefriends.org)

---

## Isi Paket XAMPP

- **Apache**  
  Web server default.

- **MySQL / MariaDB**  
  Sistem manajemen database.

- **PHP**  
  Bahasa pemrograman server-side.

- **phpMyAdmin**  
  Tools untuk mengelola database melalui web.

- **FileZilla FTP Server**  
  Untuk transfer file.

- **Tomcat**  
  Server Java.

- **XAMPP Control Panel**  
  Untuk mengatur semua komponen XAMPP.

---

## Komponen XAMPP (Versi DTS 2021)

| Komponen         | Versi       | Keterangan                                        |
|------------------|-------------|---------------------------------------------------|
| Apache           | 2.4.39      | Web server                                        |
| MariaDB          | 10.1.38     | DBMS pengganti MySQL                              |
| PHP              | 7.3.4       | Bahasa pemrograman server-side                    |
| phpMyAdmin       | 4.8.5       | Manajemen MySQL berbasis web                      |
| OpenSSL          | 1.1.0g      | Protokol keamanan SSL/TSL                         |
| XAMPP Control    | 3.2.3       | Antarmuka GUI untuk semua komponen                |

---

## Konfigurasi XAMPP

Jika terjadi konflik port (biasanya dengan Skype atau IIS), ubah port Apache dari 80 ke 8080 pada file:
```
C:\xampp\apache\conf\httpd.conf
```

---

## Peletakan Source Code

Semua file aplikasi web disimpan di dalam folder:

```
C:\xampp\htdocs\
```

Contoh:  
`C:\xampp\htdocs\Latihan\index.php`

---

## Menjalankan Apache

1. Buka **XAMPP Control Panel**.
2. Klik **Start** pada bagian Apache.
3. Buka browser, akses: `http://localhost/`

---

## Perbandingan Skema HTML vs PHP

### Skema HTML:
```html
<!DOCTYPE html>
<html>
<head>
  <title>belajar web</title>
</head>
<body>
  <h1>Selamat Datang</h1>
  <p>Selamat belajar pemrograman web</p>
</body>
</html>
```

### Skema PHP (embedded di HTML):
```php
<!DOCTYPE html>
<html>
<head><title>Contoh</title></head>
<body>
  Selamat Belajar PHP. <br>
  <?php
    printf("Tgl. Sekarang : %s", date("d F Y"));
  ?>
</body>
</html>
```

---

## Tag Dasar PHP

- **Tag pembuka:** `<?php`
- **Tag penutup:** `?>`

Semua kode PHP harus ditulis di antara kedua tag ini.

---

## Cara Penulisan Sintaks PHP

1. **Full Tag (Direkomendasikan)**  
   ```php
   <?php echo "Hello World!"; ?>
   ```

2. **Short Tag (SGML Style)**  
   ```php
   <? echo "Hello"; ?>
   ```

   ⚠ Tidak disarankan karena tidak selalu didukung semua server.

---

## PHP Case Sensitivity

- **Case Sensitive**: Nama variabel (`$nama`, `$Nama`) dianggap berbeda.
- **Case Insensitive**: Nama fungsi dan keyword (`echo`, `Echo`) tidak sensitif terhadap huruf besar/kecil.

---

## Cara Membuka File PHP

1. Masuk ke folder `C:\xampp\htdocs\`
2. Buat folder baru, contoh: `DigiTalent`
3. Buat file baru: `index.php`
4. Buka file dengan Sublime Text, Notepad, atau VS Code
5. Jalankan melalui browser:  
   `http://localhost/DigiTalent/index.php`

---

## Eksekusi File PHP

- Pastikan Apache sudah dijalankan dari XAMPP.
- Ketik URL lokal di browser seperti:  
  `localhost/Latihan/belajarweb.html`  
  atau  
  `localhost/DigiTalent/juniorwebprogrammer.php`

---

## Membuat Form Validasi PHP

### File: kominfo.php
```php
<html>
<head>
  <title>Membuat Form Validasi </title>
</head>
<body>
  <h1>Membuat Form Validasi Dengan PHP</h1>
  <?php
    if(isset($_GET['nama'])){
      if($_GET['nama'] == "kosong"){
        echo "<h4 style='color:red'>Nama Belum Di Masukkan!</h4>";
      }
    }
  ?>
</body>
</html>
```

---