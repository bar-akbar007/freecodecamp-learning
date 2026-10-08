# HTML `<form>`, `<label>`, dan `<input>` Elements

## Pengertian

Form dalam HTML digunakan untuk **mengumpulkan informasi dari pengguna**.

Contohnya:

- Nama pengguna.
- Alamat email.
- Nomor telepon.
- Password.
- Pilihan atau data lainnya.

Form biasanya digunakan pada halaman:

- Login.
- Registrasi.
- Kontak.
- Pencarian.
- Checkout.
- Pengisian data.

Elemen utama yang digunakan untuk membuat form adalah `<form>`, `<label>`, dan `<input>`.

---

## Elemen `<form>`

Elemen `<form>` digunakan sebagai **wadah untuk mengelompokkan input yang akan dikirimkan oleh pengguna**.

Sintaks dasar:

```html
<form action="url-goes-here">
  <!-- input elements go here -->
</form>
```

Contoh:

```html
<form action="/submit">
  <input type="text">
</form>
```

Semua elemen input yang berkaitan dengan suatu formulir biasanya ditempatkan di dalam `<form>`.

---

## Atribut `action`

Atribut `action` menentukan **tujuan tempat data form akan dikirim ketika form dikirimkan (submit)**.

Contoh:

```html
<form action="/submit">
  ...
</form>
```

Pada contoh tersebut, data form akan dikirim ke:

```text
/submit
```

Nilai `action` biasanya mengarah ke URL atau endpoint yang menangani data form.

Contoh pada aplikasi web:

```html
<form action="/login">
  ...
</form>
```

Form tersebut dapat digunakan untuk mengirim data ke endpoint `/login`.

> Catatan: `action` hanya menentukan tujuan pengiriman data. Metode pengiriman seperti `GET` atau `POST` biasanya ditentukan menggunakan atribut `method`.

---

## Elemen `<input>`

Elemen `<input>` digunakan untuk **menerima data dari pengguna**.

Contoh:

```html
<input type="text">
```

`<input>` merupakan **void element**, sehingga tidak memiliki closing tag.

Benar:

```html
<input type="text">
```

Tidak perlu:

```html
<input type="text"></input>
```

---

## Atribut `type`

Atribut `type` menentukan **jenis data atau kontrol input** yang digunakan.

Contoh input teks:

```html
<input type="text">
```

Input email:

```html
<input type="email">
```

Input angka:

```html
<input type="number">
```

Input password:

```html
<input type="password">
```

Beberapa jenis `type` yang umum:

| `type` | Fungsi |
|---|---|
| `text` | Input teks biasa |
| `email` | Input alamat email |
| `number` | Input angka |
| `password` | Input password |
| `date` | Input tanggal |
| `checkbox` | Pilihan yang dapat dicentang |
| `radio` | Memilih salah satu pilihan |

---

## Elemen `<label>`

Elemen `<label>` digunakan untuk memberikan **keterangan atau nama pada input**.

Contoh:

```html
<label>Full Name:</label>
<input type="text">
```

Dengan adanya label, pengguna dapat mengetahui informasi apa yang harus dimasukkan ke dalam input.

---

## Hubungan `<label>` dengan `<input>`

Ada dua cara utama untuk menghubungkan `<label>` dengan `<input>`:

1. **Implicit association**
2. **Explicit association**

---

## Implicit Association

Implicit association terjadi ketika elemen `<input>` ditempatkan **di dalam `<label>`**.

Contoh:

```html
<label>
  Full Name:
  <input type="text">
</label>
```

Karena input berada di dalam label, browser dapat memahami bahwa keduanya saling berhubungan.

Keuntungan lainnya adalah ketika pengguna mengeklik teks label, input yang berada di dalamnya dapat menjadi fokus.

---

## Explicit Association

Explicit association dilakukan dengan menggunakan atribut `for` pada `<label>` dan atribut `id` pada `<input>`.

Contoh:

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

Perhatikan bahwa:

```text
for="email"
```

dan:

```text
id="email"
```

memiliki **nilai yang sama**.

Hubungannya:

```text
label for="email"
        ↓
input id="email"
```

Dengan cara tersebut, browser mengetahui bahwa label tersebut ditujukan untuk input tertentu.

---

## Atribut `for`

Atribut `for` pada `<label>` digunakan untuk **secara eksplisit menghubungkan label dengan elemen input**.

Contoh:

```html
<label for="username">Username:</label>
<input type="text" id="username">
```

Nilai `for` harus sama dengan nilai `id` dari input yang ingin dihubungkan.

Contoh yang benar:

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

Contoh yang tidak terhubung dengan benar:

```html
<label for="email">Email:</label>
<input type="email" id="user-email">
```

Karena:

```text
for="email"
```

berbeda dengan:

```text
id="user-email"
```

---

## Atribut `id`

Atribut `id` memberikan **identitas unik** pada elemen HTML.

Pada form, `id` sering digunakan bersama `for` untuk menghubungkan `<label>` dengan `<input>`.

Contoh:

```html
<label for="full-name">Full Name:</label>
<input type="text" id="full-name">
```

Hubungannya:

```text
for="full-name"
       ↕
id="full-name"
```

---

## Atribut `placeholder`

Atribut `placeholder` digunakan untuk memberikan **petunjuk atau contoh singkat** mengenai data yang diharapkan dari pengguna.

Contoh:

```html
<input
  type="email"
  placeholder="example@email.com"
>
```

Sebelum pengguna mengetik, browser akan menampilkan:

```text
example@email.com
```

Setelah pengguna mulai mengetik, teks placeholder akan hilang.

---

## Placeholder Bukan Pengganti Label

`placeholder` sebaiknya digunakan sebagai **petunjuk tambahan**, bukan sebagai pengganti `<label>`.

Contoh yang lebih baik:

```html
<label for="email">Email:</label>
<input
  type="email"
  id="email"
  placeholder="example@email.com"
>
```

Dalam contoh tersebut:

- `<label>` → menjelaskan apa yang harus diisi.
- `placeholder` → memberikan contoh format data.

Jadi keduanya memiliki fungsi yang berbeda.

---

## Input dengan `type="text"`

Digunakan untuk menerima teks biasa.

```html
<label for="name">Full Name:</label>
<input type="text" id="name">
```

Contoh penggunaannya:

```text
Full Name: [________________]
```

---

## Input dengan `type="email"`

Digunakan untuk menerima alamat email.

```html
<label for="email">Email:</label>
<input
  type="email"
  id="email"
  placeholder="example@email.com"
>
```

`type="email"` memberikan validasi dasar agar input mengikuti format alamat email yang sesuai.

Contoh:

```text
user@example.com
```

---

## Contoh Form Sederhana

```html
<form action="/submit">
  <label for="name">Full Name:</label>
  <input type="text" id="name">

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="example@email.com"
  >
</form>
```

Strukturnya:

```text
<form>
├── <label>
├── <input>
├── <label>
└── <input>
```

---

## Contoh Form dengan Implicit Association

```html
<form action="/submit">
  <label>
    Full Name:
    <input type="text">
  </label>

  <label>
    Email:
    <input type="email">
  </label>
</form>
```

Pada contoh ini, input berada di dalam masing-masing `<label>`, sehingga hubungan antara label dan input dibuat secara implicit.

---

## Contoh Form dengan Explicit Association

```html
<form action="/submit">
  <label for="name">Full Name:</label>
  <input type="text" id="name">

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="example@email.com"
  >
</form>
```

Pada contoh ini, hubungan dibuat secara explicit menggunakan:

```text
<label for="...">
        ↕
<input id="...">
```

Nilai `for` dan `id` harus cocok.

---

## Contoh Lengkap

```html
<form action="/submit">
  <div>
    <label for="name">Full Name:</label>
    <input
      type="text"
      id="name"
      placeholder="John Doe"
    >
  </div>

  <div>
    <label for="email">Email:</label>
    <input
      type="email"
      id="email"
      placeholder="example@email.com"
    >
  </div>

  <div>
    <label for="age">Age:</label>
    <input
      type="number"
      id="age"
      placeholder="18"
    >
  </div>
</form>
```

Form tersebut memiliki tiga input:

```text
Full Name → text
Email     → email
Age       → number
```

---

## Kesalahan yang Sering Terjadi

### 1. Menggunakan `for` dan `id` yang berbeda

Salah:

```html
<label for="email">Email:</label>
<input type="email" id="user-email">
```

Benar:

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

---

### 2. Menggunakan `placeholder` sebagai label

Kurang baik:

```html
<input
  type="email"
  placeholder="Email"
>
```

Lebih baik:

```html
<label for="email">Email:</label>

<input
  type="email"
  id="email"
  placeholder="example@email.com"
>
```

---

### 3. Memberikan closing tag pada `<input>`

Salah:

```html
<input type="text"></input>
```

Benar:

```html
<input type="text">
```

Karena `<input>` merupakan void element.

---

## Ringkasan

### `<form>`

Digunakan sebagai wadah untuk mengumpulkan data pengguna.

```html
<form action="/submit">
  ...
</form>
```

### `<input>`

Digunakan untuk menerima data dari pengguna.

```html
<input type="text">
```

### `<label>`

Digunakan untuk memberikan keterangan pada input.

```html
<label for="name">Full Name:</label>
```

### `for` dan `id`

Digunakan untuk membuat hubungan explicit antara label dan input.

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

Nilai `for` dan `id` harus sama.

### `placeholder`

Digunakan untuk memberikan **petunjuk atau contoh data** di dalam input.

```html
<input
  type="email"
  placeholder="example@email.com"
>
```

---

## Pola Dasar Form

```html
<form action="/submit">

  <label for="name">Full Name:</label>
  <input type="text" id="name">

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="example@email.com"
  >

</form>
```

Pola sederhananya:

```text
<form>
    ↓
  <label> + <input>
          ↓
      for ↔ id
          ↓
    placeholder
```