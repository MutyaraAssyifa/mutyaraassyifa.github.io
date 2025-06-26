---
layout: post
title: "Bootstrap"

---

Penjelasan Bootstrap

---

## Apa itu Bootstrap?

**Bootstrap** adalah framework open-source yang digunakan untuk membuat antarmuka web yang responsif dan menarik dengan cepat. Dikembangkan pertama kali oleh Twitter.

Bootstrap menyediakan:
- Grid system (layout)
- Komponen UI siap pakai
- Utilitas CSS
- Responsivitas mobile-first

---

## Versi Terbaru

Versi saat ini: **Bootstrap 5.x**  
Link dokumentasi resmi:  
🔗 [https://getbootstrap.com](https://getbootstrap.com)

---

## Cara Menggunakan Bootstrap

### 1. Melalui CDN
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

### 2. Mengunduh File
Unduh dari [getbootstrap.com](https://getbootstrap.com), lalu tambahkan file `bootstrap.min.css` dan `bootstrap.bundle.min.js` ke dalam proyekmu.

---

## Struktur Grid Bootstrap

Bootstrap menggunakan sistem grid 12 kolom. Contoh:
```html
<div class="container">
  <div class="row">
    <div class="col-6">Kolom 1</div>
    <div class="col-6">Kolom 2</div>
  </div>
</div>
```

**Breakpoints Responsif:**
- `col-sm-*` (≥576px)
- `col-md-*` (≥768px)
- `col-lg-*` (≥992px)
- `col-xl-*` (≥1200px)

---

## Komponen Bootstrap

### 1. Button
```html
<button class="btn btn-primary">Klik Saya</button>
```

### 2. Alert
```html
<div class="alert alert-success">Berhasil disimpan!</div>
```

### 3. Card
```html
<div class="card" style="width: 18rem;">
  <img src="image.jpg" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Judul</h5>
    <p class="card-text">Isi konten singkat.</p>
    <a href="#" class="btn btn-primary">Aksi</a>
  </div>
</div>
```

### 4. Navbar
```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">Logo</a>
  <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
      <li class="nav-item"><a class="nav-link" href="#">Tentang</a></li>
    </ul>
  </div>
</nav>
```

---

## Utilitas Kelas CSS

- **Spacing:** `m-3`, `p-2`, `mt-4`, `pb-1`
- **Text Align:** `text-center`, `text-end`
- **Text Color:** `text-primary`, `text-danger`
- **Background:** `bg-light`, `bg-warning`
- **Display:** `d-flex`, `d-none`, `d-block`

---

## Membuat Form dengan Bootstrap
```html
<form>
  <div class="mb-3">
    <label for="email" class="form-label">Email address</label>
    <input type="email" class="form-control" id="email">
  </div>
  <div class="mb-3">
    <label for="password" class="form-label">Password</label>
    <input type="password" class="form-control" id="password">
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

---

## Tips Penggunaan

- Gunakan `container` atau `container-fluid` sebagai pembungkus utama layout.
- Gunakan utilitas Bootstrap daripada membuat CSS manual jika memungkinkan.
- Jangan lupa menambahkan JavaScript Bootstrap untuk komponen interaktif seperti modal atau dropdown.

---
