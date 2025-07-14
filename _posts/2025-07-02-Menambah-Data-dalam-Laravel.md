---
layout: post
title: "Laravel"

---

Langkah-langkah Menambah Data Laravel

---


## 1. Membuat Model dan Migration

Jalankan perintah berikut:

```bash
php artisan make:model Siswa -cm
```

### Penjelasan:
- `make:model Siswa` → Membuat model `Siswa` di folder `app/Models`.
- `-c` → Membuat controller `SiswaController`.
- `-m` → Membuat file migrasi `create_siswas_table` di folder `database/migrations`.

**Fungsi:** Menghasilkan model, controller, dan file migrasi untuk entitas `Siswa`.

---

## 2. Mengatur Struktur Tabel

Edit file migration di folder `database/migrations` dan sesuaikan strukturnya menjadi:

```php
public function up(): void
{
    Schema::create('siswas', function (Blueprint $table) {
        $table->id();
        $table->string('nama', 100);
        $table->text('alamat');
        $table->boolean('jenis_kelamin');
        $table->string('agama');
        $table->string('sekolah_asal');
        $table->timestamps();
    });
}
```

**Fungsi:** Menentukan struktur tabel `siswas` di dalam database.

---

## 3. Menjalankan Migrasi

```bash
php artisan migrate
```

**Fungsi:** Menjalankan file migrasi dan membentuk tabel-tabel pada database.

---

## 4. Instalasi Laravel Breeze

```bash
composer require laravel/breeze --dev
```

**Fungsi:** Menginstal starter kit autentikasi (login, register, dll.) berbasis Blade dan Tailwind CSS.

---

## 5. Mengatur Breeze

```bash
php artisan breeze:install
```

**Fungsi:** Mengaktifkan sistem autentikasi dasar pada Laravel.

---

## 6. Instalasi Frontend

```bash
npm install
```

**Fungsi:** Mengunduh dependensi frontend seperti Tailwind CSS dan Vite.

---

## 7. Menjalankan Build Assets

```bash
npm run dev
```

**Fungsi:** Mengompilasi file CSS dan JS ke dalam folder `public/build/` menggunakan Vite.

---

## 8. Model: `app/Models/Siswa.php`

```php
class Siswa extends Model
{
    protected $fillable = [
        'nama', 'alamat', 'agama', 'jenis_kelamin', 'sekolah_asal'
    ];
}
```

**Fungsi:** Mendefinisikan kolom yang dapat diisi secara massal dalam model.

---

## 9. Controller: `app/Http/Controllers/SiswaController.php`

```php
class SiswaController extends Controller
{
    public function index() {
        $siswas = Siswa::all();
        return view('siswa.index', compact('siswas'));
    }

    public function create() {
        return view('siswa.create');
    }

    public function store(Request $request) {
        $data = $request->validate([
            'nama' => 'required',
            'alamat' => 'required',
            'agama' => 'required',
            'jenis_kelamin' => 'required|boolean',
            'sekolah_asal' => 'required',
        ]);
        Siswa::create($data);
        return redirect()->route('siswa.index');
    }

    public function edit(Siswa $siswa) {
        return view('siswa.edit', compact('siswa'));
    }

    public function update(Request $request, Siswa $siswa) {
        $data = $request->validate([
            'nama' => 'required',
            'alamat' => 'required',
            'agama' => 'required',
            'jenis_kelamin' => 'required|boolean',
            'sekolah_asal' => 'required',
        ]);
        $siswa->update($data);
        return redirect()->route('siswa.index')->with('success', 'Data berhasil diperbarui');
    }

    public function destroy(Siswa $siswa) {
        $siswa->delete();
        return redirect()->route('siswa.index')->with('success', 'Data berhasil dihapus');
    }
}
```

**Fungsi:** Mengelola data siswa mulai dari menampilkan, menambahkan, mengedit, hingga menghapus.

---

## 10. Routing: `routes/web.php`

```php
use App\Http\Controllers\SiswaController;

Route::get('/', function () {
    return redirect()->route('siswa.index');
});

Route::middleware(['auth'])->group(function () {
    Route::resource('/siswa', SiswaController::class);
});
```

**Fungsi:** Mendefinisikan rute untuk akses halaman utama dan semua aksi CRUD siswa dengan proteksi autentikasi.

---

## 11. Link Navigasi: `resources/views/navigation.blade.php`

```php
<x-nav-link :href="route('siswa.index')" :active="request()->routeIs('siswa.*')">
    Data Siswa
</x-nav-link>
```

**Fungsi:** Menambahkan menu navigasi ke halaman data siswa.

---

## 12. Validasi dan Route pada Formulir

- Pastikan `action` menggunakan route yang benar, contoh:

```php

<form action="{{ route('siswa.store') }}" method="POST">

```

- Gunakan `old()` pada create dan `$siswa->field` pada edit untuk menjaga input.

```php

<input type="text" name="nama" value="{{ old('nama') }}" />
<input type="text" name="nama" value="{{ $siswa->nama }}" />

```
