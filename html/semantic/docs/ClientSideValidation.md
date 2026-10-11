# HTML Client-Side Form Validation

## Pengertian

**Client-side form validation** adalah proses memeriksa data yang dimasukkan pengguna di sisi klien, yaitu melalui browser atau perangkat pengguna, sebelum data dikirimkan untuk diproses.

Validasi bertujuan membantu memastikan bahwa data yang dimasukkan memenuhi persyaratan tertentu.

Contohnya:

- Email tidak boleh kosong.
- Email harus memiliki format yang sesuai.
- Panjang teks harus memenuhi batas minimum.
- Panjang teks tidak boleh melebihi batas maksimum.

HTML menyediakan beberapa atribut bawaan untuk membantu melakukan validasi tanpa harus menulis JavaScript terlebih dahulu.

---

## Client-Side vs. Server-Side Validation

Ada dua jenis validasi yang umum digunakan dalam aplikasi web.

### 1. Client-Side Validation

Validasi dilakukan di browser pengguna sebelum data dikirimkan ke server.

Contohnya:

```html
<input type="email" required>
```

Browser dapat memeriksa apakah kolom sudah diisi dan apakah nilai yang dimasukkan sesuai dengan format email dasar.

Keuntungan:

- Memberikan umpan balik dengan cepat.
- Membantu pengguna memperbaiki kesalahan input.
- Mengurangi pengiriman data yang jelas-jelas tidak sesuai persyaratan.

### 2. Server-Side Validation

Validasi dilakukan oleh server setelah menerima data dari pengguna.

Server memeriksa apakah data memenuhi aturan aplikasi sebelum memproses atau menyimpannya.

Client-side validation tidak dapat menggantikan server-side validation karena pemeriksaan di browser dapat dilewati atau dimanipulasi.

**Kesimpulan:** Gunakan validasi sisi klien untuk membantu pengguna dan validasi sisi server untuk memastikan data diperiksa kembali sebelum diproses.

---

## Atribut `required`

Atribut `required` digunakan untuk menentukan bahwa sebuah input wajib diisi sebelum formulir dapat dikirimkan.

Contoh:

```html
<form>
  <label for="email">Email:</label>
  <input type="email" id="email" required>

  <button type="submit">Submit Form</button>
</form>
```

Jika pengguna mencoba mengirimkan formulir ketika kolom email masih kosong, browser akan menampilkan pesan validasi.

Pesan dan tampilan peringatan dapat berbeda-beda tergantung browser.

### Cara Kerja

```text
Pengguna mengisi formulir
          |
          v
Menekan tombol Submit
          |
          v
Browser memeriksa input
          |
      +---+---+
      |       |
   Valid    Tidak valid
      |       |
      v       v
  Formulir   Pesan
  dikirim    validasi
```

Atribut `required` hanya memastikan bahwa kolom wajib diisi. Atribut tersebut tidak memastikan bahwa alamat email benar-benar dimiliki atau digunakan oleh seseorang.

---

## Validasi Email dengan `type="email"`

Atribut `type="email"` digunakan untuk membuat input yang ditujukan bagi alamat email.

Contoh:

```html
<label for="email">Email:</label>

<input
  type="email"
  id="email"
  name="email"
  required
>
```

Browser akan melakukan pemeriksaan format email dasar ketika formulir dikirimkan.

Contoh nilai yang umumnya memenuhi pemeriksaan format dasar:

```text
akbar@example.com
```

Contoh nilai yang tidak memenuhi format dasar:

```text
abc
```

Jika pengguna memasukkan `abc` lalu menekan tombol submit, browser biasanya akan menampilkan peringatan karena nilai tersebut bukan alamat email dengan format yang valid.

### Batasan Validasi Email

Validasi bawaan browser tidak membuktikan bahwa:

- Alamat email tersebut benar-benar ada.
- Email tersebut dapat menerima pesan.
- Pengguna benar-benar memiliki alamat email tersebut.

Pemeriksaan format email hanyalah validasi awal. Verifikasi kepemilikan email membutuhkan mekanisme tambahan, misalnya mengirimkan tautan verifikasi.

---

## Atribut `minlength`

Atribut `minlength` menentukan jumlah minimum karakter yang harus dimiliki oleh nilai input.

Contoh:

```html
<input
  type="email"
  id="email"
  name="email"
  minlength="5"
>
```

Pada contoh tersebut, panjang nilai input ditetapkan minimal 5 karakter.

Jika panjang input tidak memenuhi ketentuan, browser dapat menolak pengiriman formulir dan menampilkan pesan validasi.

### Contoh Penggunaan

```html
<form>
  <label for="email">Email:</label>

  <input
    type="email"
    id="email"
    name="email"
    minlength="6"
    required
  >

  <button type="submit">Submit</button>
</form>
```

Input tersebut memiliki dua ketentuan:

- `required` → kolom wajib diisi.
- `minlength="6"` → panjang nilai minimal 6 karakter.

Meskipun panjangnya sudah memenuhi batas minimum, nilai tersebut tetap harus memenuhi validasi format email.

---

## Atribut `maxlength`

Atribut `maxlength` menentukan jumlah maksimum karakter yang diperbolehkan dalam nilai input.

Contoh:

```html
<input
  type="email"
  id="email"
  name="email"
  maxlength="50"
>
```

Pada contoh tersebut, panjang nilai input dibatasi maksimal 50 karakter.

Ketika pengguna mengetik, browser umumnya membatasi jumlah karakter yang dapat dimasukkan hingga batas tersebut.

### Contoh Penggunaan

```html
<form>
  <label for="email">Email:</label>

  <input
    type="email"
    id="email"
    name="email"
    maxlength="50"
    required
  >

  <button type="submit">Submit</button>
</form>
```

Input tersebut wajib diisi dan memiliki panjang maksimum 50 karakter.

---

## Menggabungkan `minlength` dan `maxlength`

Kedua atribut tersebut dapat digunakan secara bersamaan untuk menetapkan rentang panjang input.

Contoh:

```html
<input
  type="email"
  id="email"
  name="email"
  minlength="6"
  maxlength="50"
  required
>
```

Ketentuan input tersebut:

| Atribut | Fungsi |
|---|---|
| `type="email"` | Memeriksa format email dasar |
| `minlength="6"` | Menentukan panjang minimum 6 karakter |
| `maxlength="50"` | Menentukan panjang maksimum 50 karakter |
| `required` | Mewajibkan kolom diisi |

Pengguna harus memasukkan nilai yang tidak kosong, memenuhi batas panjang, dan sesuai dengan format email.

Perlu diingat bahwa aturan panjang dan format merupakan pemeriksaan yang berbeda. Memenuhi satu aturan tidak berarti otomatis memenuhi aturan lainnya.

---

## Contoh Formulir dengan Validasi

```html
<form action="#" method="get">
  <label for="email">Email:</label>

  <input
    type="email"
    id="email"
    name="email"
    placeholder="example@email.com"
    minlength="6"
    maxlength="50"
    required
  >

  <button type="submit">Submit Form</button>
</form>
```

Pada contoh tersebut:

1. `type="email"` memeriksa format email dasar.
2. `minlength="6"` menetapkan panjang minimum.
3. `maxlength="50"` menetapkan panjang maksimum.
4. `required` mewajibkan pengguna mengisi kolom.
5. Tombol `submit` mencoba mengirim formulir setelah validasi berhasil.

Contoh ini hanya untuk mempelajari validasi browser. Karena belum terhubung dengan backend, formulir tersebut tidak menyimpan data ke database.

---

## Perbedaan `minlength` dan `maxlength`

| Atribut | Fungsi | Contoh |
|---|---|---|
| `minlength` | Mengatur panjang minimum karakter | `minlength="6"` |
| `maxlength` | Mengatur panjang maksimum karakter | `maxlength="50"` |

Contoh:

```html
<input type="text" minlength="3" maxlength="10">
```

Input tersebut memiliki batas panjang minimal 3 karakter dan maksimal 10 karakter.

Kedua atribut ini mengatur **jumlah karakter**, bukan lebar visual kolom input.

Jika ingin mengatur lebar tampilan kolom, gunakan CSS atau atribut HTML yang sesuai dengan kebutuhan tampilan.

---

## Catatan Keamanan

Validasi HTML sangat membantu untuk meningkatkan pengalaman pengguna, tetapi tidak cukup untuk melindungi aplikasi.

Pengguna dapat memanipulasi permintaan atau mengirimkan data tanpa melalui validasi browser.

Karena itu, backend tetap harus memvalidasi data yang diterima sebelum melakukan proses penting, seperti:

- Menyimpan data ke database.
- Membuat akun pengguna.
- Memproses transaksi.
- Memperbarui informasi akun.

**Jangan menganggap data aman hanya karena formulir lolos validasi di browser.**

---

## Ringkasan

### `required`

Mewajibkan input diisi.

```html
<input type="email" required>
```

### `type="email"`

Memberikan validasi format email dasar.

```html
<input type="email">
```

### `minlength`

Menentukan jumlah minimum karakter.

```html
<input type="text" minlength="3">
```

### `maxlength`

Menentukan jumlah maksimum karakter.

```html
<input type="text" maxlength="20">
```

### Kesimpulan

Client-side validation membantu pengguna memasukkan data yang sesuai sebelum formulir dikirimkan.

HTML menyediakan atribut bawaan seperti `required`, `type="email"`, `minlength`, dan `maxlength` untuk melakukan pemeriksaan tersebut.

Untuk aplikasi nyata, **client-side validation harus dilengkapi server-side validation** agar data tetap diperiksa sebelum diproses oleh backend.