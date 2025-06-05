---
layout: post
title: "Formspree"
---

Penjelasan Formspree

---
## Apa itu Formspree?

Formspree adalah layanan **backend form submission** yang memungkinkan kamu untuk menghubungkan form HTML di website langsung ke email atau layanan lain tanpa perlu membuat backend sendiri. Dengan Formspree, kamu cukup mengatur URL endpoint form dan data akan otomatis dikirim ke email atau integrasi yang kamu pilih.

Formspree sangat membantu bagi developer atau pemilik website yang ingin menerima data form seperti kontak, pendaftaran, atau feedback tanpa harus membuat server dan menangani pengiriman email sendiri.



## Keunggulan Formspree

- **Tanpa perlu backend:** Tidak perlu setup server, cukup form HTML biasa.
- **Mudah digunakan:** Hanya perlu ubah atribut `action` pada form.
- **Gratis paket dasar:** Cukup untuk kebutuhan form sederhana dan website kecil.
- **Keamanan:** Fitur anti-spam seperti reCAPTCHA, honeypot.
- **Dukungan berbagai metode:** Mendukung metode HTTP POST dan GET.
- **Fleksibel:** Bisa integrasi dengan Zapier, Google Sheets, dan layanan lainnya.
- **Pengaturan lanjutan:** Redirect custom, custom headers, dan pengaturan email.



## Cara Kerja Formspree

1. **Buat Form HTML**  
   Buat form seperti biasa dengan method POST, dan arahkan atribut `action` ke URL Formspree.

2. **Submit Form**  
   Saat user submit, data form dikirim ke server Formspree.

3. **Formspree Proses Data**  
   Formspree akan memproses data dan meneruskannya ke email kamu, atau layanan lain jika diintegrasikan.

4. **Email Penerima**  
   Kamu akan menerima email berisi data yang dikirim oleh user.

5. **Feedback untuk User**  
   Bisa dikonfigurasi redirect halaman atau pesan sukses setelah submit.



## Contoh Implementasi Form dengan Formspree

```html
<form action="https://formspree.io/f/your-form-id" method="POST">
  <label for="name">Nama Lengkap:</label>
  <input type="text" id="name" name="name" required />

  <label for="email">Email:</label>
  <input type="email" id="email" name="_replyto" required />

  <label for="message">Pesan:</label>
  <textarea id="message" name="message" required></textarea>

  <button type="submit">Kirim</button>
</form>
```

## Cara Mendapatkan Endpoint Formspree
- Daftar akun di https://formspree.io

- Buat form baru di dashboard.

- Salin URL endpoint yang disediakan.

- Tempel URL tersebut di atribut action form HTML kamu.

## Fitur Lanjutan Formspree
- Validasi Otomatis
  Field yang wajib (required) akan divalidasi oleh Formspree.

- Proteksi Spam
  Integrasi Google reCAPTCHA, honeypot untuk mencegah spam bot.

- Redirect Custom
  Setelah submit berhasil, user bisa diarahkan ke halaman tertentu.

- Multiple Recipients
  Kirim email ke lebih dari satu alamat.

- Integrasi Layanan Pihak Ketiga
  Zapier, Slack, Google Sheets, Mailchimp, dan lainnya.

- Webhook dan API
  Bisa dihubungkan ke sistem backend kamu lewat webhook.
 
- Analytics
  Laporan jumlah submission dan aktivitas form.

### Contoh Form dengan Redirect Setelah Submit
```html
<form action="https://formspree.io/f/your-form-id" method="POST">
  <input type="hidden" name="_next" value="https://yourdomain.com/thank-you.html" />

  <label for="email">Email:</label>
  <input type="email" name="_replyto" required />

  <label for="message">Pesan:</label>
  <textarea name="message" required></textarea>

  <button type="submit">Kirim</button>
</form>
```
Penjelasan:
Atribut name="_next" dengan value URL adalah halaman yang akan dituju user setelah submit form sukses.

### Contoh Form dengan Proteksi reCAPTCHA
```html
<form action="https://formspree.io/f/your-form-id" method="POST">
  <label>Email:</label>
  <input type="email" name="_replyto" required />

  <label>Pesan:</label>
  <textarea name="message" required></textarea>

  <!-- reCAPTCHA v2 widget -->
  <div class="g-recaptcha" data-sitekey="your-site-key"></div>

  <button type="submit">Kirim</button>
</form>

<script src="https://www.google.com/recaptcha/api.js" async defer></script>
```
Catatan:
Untuk proteksi reCAPTCHA kamu perlu mendaftar dan dapatkan site-key dari Google reCAPTCHA.

### Kelebihan Formspree dibanding Membuat Backend Sendiri

| Aspek        | Formspree                     | Backend Sendiri               |
|--------------|------------------------------|------------------------------|
| Setup        | Cepat, tanpa coding backend  | Membutuhkan waktu dan skill  |
| Maintenance  | Formspree yang kelola         | Kamu yang harus kelola server|
| Skalabilitas | Cocok untuk website kecil sampai menengah  |  Bisa disesuaikan untuk apapun |
| Keamanan     | Ada proteksi anti-spam built-in | Perlu konfigurasi sendiri    |
| Biaya        | Ada paket gratis dan berbayar | Biaya server dan pengembangan|


### Kesimpulan
Formspree adalah solusi praktis dan cepat untuk mengaktifkan form di website tanpa ribet bikin backend. Cocok untuk developer pemula maupun profesional yang ingin fokus frontend. Dengan berbagai fitur proteksi, validasi, dan integrasi, Formspree bisa diandalkan untuk banyak kebutuhan form online.