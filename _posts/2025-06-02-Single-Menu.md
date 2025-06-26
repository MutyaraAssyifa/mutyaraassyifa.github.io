---
layout: post
title: "Single Menu"

---

Penjelasan Single Menu

---

## Apa itu Single Menu?

**Single Menu** adalah tipe menu navigasi tunggal yang biasanya digunakan pada aplikasi atau halaman web sederhana. Menu ini menampilkan satu baris atau satu kolom menu yang berisi tautan ke halaman-halaman tertentu.

Cocok digunakan untuk:
- Aplikasi CRUD sederhana
- Website landing page
- Halaman profil atau portofolio

---

## Contoh Struktur Single Menu

### Menggunakan HTML dan CSS Sederhana
```html
<!DOCTYPE html>
<html>
<head>
  <title>Single Menu</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    .menu {
      background-color: #333;
      overflow: hidden;
    }
    .menu a {
      float: left;
      display: block;
      color: white;
      text-align: center;
      padding: 14px 16px;
      text-decoration: none;
    }
    .menu a:hover {
      background-color: #575757;
    }
  </style>
</head>
<body>

<div class="menu">
  <a href="index.php">Beranda</a>
  <a href="form-daftar.php">Daftar</a>
  <a href="list-siswa.php">List Data</a>
</div>

<h2>Selamat Datang di Aplikasi</h2>
<p>Silakan pilih menu di atas untuk memulai.</p>

</body>
</html>
```

---

## Contoh Single Menu dengan Bootstrap

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Aplikasi</a>
    <div class="collapse navbar-collapse">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" href="index.php">Beranda</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="form-daftar.php">Daftar</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="list-siswa.php">List Data</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

---

## Variasi Tampilan Single Menu

### 1. Single Menu Horizontal
Menu horizontal cocok untuk tampilan header.

```html
<div class="menu">
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Contact</a>
</div>
```

### 2. Single Menu Vertikal
Menu vertikal cocok untuk sidebar atau layout dashboard.

```html
<div class="vertical-menu">
  <a href="#">Home</a>
  <a href="#">Profile</a>
  <a href="#">Logout</a>
</div>
```

```css
.vertical-menu {
  width: 200px;
  background-color: #f1f1f1;
  padding: 10px;
}
.vertical-menu a {
  display: block;
  color: #000;
  padding: 8px;
  text-decoration: none;
}
.vertical-menu a:hover {
  background-color: #ccc;
}
```

---

## Tips Penerapan Single Menu

- Pastikan link menu sesuai dengan struktur file projek.
- Tambahkan class `active` pada halaman yang sedang dibuka.
- Gunakan desain responsif jika ingin tampilan optimal di semua perangkat.
- Untuk Bootstrap, jangan lupa menyertakan file JS dan CSS dari CDN.

---

## Manfaat Single Menu

- Sederhana dan mudah dibuat
- Mempermudah navigasi pengguna
- Cocok untuk aplikasi skala kecil-menengah

---