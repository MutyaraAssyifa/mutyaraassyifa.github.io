---
layout: post
title: "Sweet Alert"
---

Penjelasan Sweet Alert

---

## Apa itu SweetAlert?

SweetAlert adalah library JavaScript yang dirancang untuk menggantikan fungsi `alert()`, `confirm()`, dan `prompt()` bawaan browser dengan tampilan popup yang lebih menarik dan fungsional. Library ini memberikan cara mudah untuk menampilkan pesan kepada pengguna dalam bentuk modal (popup) yang cantik, responsif, dan interaktif.

## Mengapa menggunakan SweetAlert?

Alert standar browser biasanya:

- Tampilan sangat sederhana dan kaku (kurang menarik).
- Tidak dapat dikustomisasi secara visual (warna, font, ikon, tombol).
- Tidak bisa menampilkan input kompleks.
- Membuat pengalaman pengguna kurang baik karena tampilannya yang monoton.

SweetAlert mengatasi semua kekurangan ini dengan menawarkan:

- **Desain modern dan menarik:** Popup yang lebih stylish dengan animasi halus.
- **Kustomisasi lengkap:** Judul, pesan, ikon (success, error, warning, info), warna tombol, teks tombol, bahkan input seperti text field.
- **Dukungan interaksi:** Bisa pakai tombol konfirmasi, batal, dan callback untuk mengeksekusi fungsi tertentu setelah pengguna berinteraksi.
- **Mudah digunakan:** Sintaks yang sederhana untuk dipahami dan diimplementasikan.

## Fitur-Fitur SweetAlert

- Popup tipe sukses, error, warning, info, dan question dengan ikon bawaan.
- Popup konfirmasi dengan tombol OK dan Cancel.
- Popup dengan input user seperti teks, password, email, textarea, select dropdown.
- Kustomisasi tombol: mengubah teks, warna, dan gaya tombol.
- Callback fungsi setelah tombol diklik.
- Mendukung Promise untuk penanganan asinkron.
- Mendukung tema dan styling CSS untuk penyesuaian tampilan lebih lanjut.

## Cara Menggunakan SweetAlert

### 1.Mengimpor SweetAlert

```html
<script src="https://unpkg.com/sweetalert/dist/sweetalert.min.js"></script>

```
### 2. Contoh Penggunaan dasar
- Popup sederhana

javascript
```html
swal("Halo dunia!");
```

- Popup sukses dengan judul dan teks

javascript
```html
swal("Berhasil!", "Data berhasil disimpan.", "success");
```

- Popup konfirmasi dengan tombol OK dan Cancel

javascript
```html
swal({
  title: "Apakah kamu yakin?",
  text: "Data yang dihapus tidak bisa dikembalikan!",
  icon: "warning",
  buttons: true,
  dangerMode: true,
})
.then((willDelete) => {
  if (willDelete) {
    swal("Data telah dihapus!", { icon: "success" });
  } else {
    swal("Data aman!");
  }
});
```

- Popup input untuk memasukkan teks

javascript
```html
swal("Masukkan nama kamu:", {
  content: "input",
})
.then((value) => {
  if (value) {
    swal(`Halo, ${value}!`);
  } else {
    swal("Kamu belum memasukkan nama.");
  }
});
```

### Contoh Lengkap dengan Tombol Pemicu
```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Contoh SweetAlert</title>
  <script src="https://unpkg.com/sweetalert/dist/sweetalert.min.js"></script>
</head>
<body>

  <button onclick="showSuccess()">Simpan Data</button>
  <button onclick="confirmDelete()">Hapus Data</button>
  <button onclick="inputName()">Masukkan Nama</button>

  <script>
    function showSuccess() {
      swal("Berhasil!", "Data berhasil disimpan.", "success");
    }

    function confirmDelete() {
      swal({
        title: "Apakah kamu yakin?",
        text: "Data yang dihapus tidak bisa dikembalikan!",
        icon: "warning",
        buttons: true,
        dangerMode: true,
      }).then((willDelete) => {
        if (willDelete) {
          swal("Data telah dihapus!", { icon: "success" });
        } else {
          swal("Data aman!");
        }
      });
    }

    function inputName() {
      swal("Masukkan nama kamu:", {
        content: "input",
      }).then((value) => {
        if (value) {
          swal(`Halo, ${value}!`);
        } else {
          swal("Kamu belum memasukkan nama.");
        }
      });
    }
  </script>

</body>
</html>
```

### Kesimpulan
SweetAlert adalah solusi mudah dan efektif untuk meningkatkan pengalaman pengguna dengan mengganti alert browser standar menjadi popup yang lebih interaktif dan estetis. Dengan fitur lengkap dan kemudahan integrasi, SweetAlert banyak dipakai dalam pengembangan web modern.