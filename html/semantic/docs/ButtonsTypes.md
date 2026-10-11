# HTML Button Types

## Pengertian

Elemen `<button>` digunakan untuk membuat tombol yang dapat diaktifkan pengguna untuk menjalankan suatu tindakan.

Contoh penggunaannya:

- Mengirim formulir.
- Mengatur ulang data formulir.
- Membuka atau menutup menu.
- Menampilkan modal.
- Menjalankan fungsi JavaScript.

Contoh dasar:

```html
<button>Start Game</button>
```

Kode tersebut membuat tombol dengan teks `Start Game`.

Elemen `<button>` memiliki atribut `type` yang menentukan perilaku tombol ketika diaktifkan.

---

## Jenis-Jenis `button`

Ada tiga nilai utama atribut `type` pada elemen `<button>`:

| `type` | Fungsi |
|---|---|
| `button` | Tombol biasa yang tidak mengirim atau mereset form secara otomatis |
| `submit` | Mengirimkan formulir |
| `reset` | Mengembalikan kontrol formulir ke nilai awalnya |

---

## 1. `type="button"`

Tipe `button` digunakan untuk membuat tombol biasa yang tidak memiliki tindakan bawaan untuk mengirim atau mereset formulir.

Contoh:

```html
<button type="button">Show Alert</button>
```

Tombol tersebut tidak akan menampilkan alert atau melakukan tindakan lain secara otomatis.

Agar tombol bisa menjalankan tindakan tertentu, kita dapat menambahkan JavaScript.

Contoh penggunaan lainnya:

```html
<button type="button">Open Menu</button>
<button type="button">Close Modal</button>
```

Tombol seperti ini sering digunakan untuk menjalankan fungsi JavaScript, misalnya membuka menu navigasi atau menampilkan dialog.

**Catatan:** `type="button"` tidak melakukan tindakan secara otomatis, tetapi tetap dapat digunakan untuk menjalankan fungsi melalui JavaScript.

---

## 2. `type="submit"`

Tipe `submit` digunakan untuk mengirimkan data formulir.

Contoh:

```html
<form action="/submit" method="post">
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <button type="submit">Submit</button>
</form>
```

Ketika tombol `Submit` ditekan, browser akan mencoba mengirimkan data formulir ke alamat yang ditentukan oleh atribut `action`.

Pada contoh tersebut:

- `<form>` menjadi wadah formulir.
- `action="/submit"` menentukan tujuan pengiriman.
- `method="post"` menentukan metode pengiriman.
- `name="email"` memberikan nama data yang dikirim.
- `type="submit"` membuat tombol mengirimkan formulir.

Pengiriman data ke server hanya dapat diproses dengan benar apabila endpoint tujuan tersedia dan menangani permintaan tersebut.

### Catatan Penting

Jika elemen `<button>` berada di dalam formulir dan atribut `type` tidak ditentukan, tombol tersebut umumnya berperilaku sebagai tombol submit.

Karena itu, sebaiknya tuliskan `type` secara eksplisit agar perilakunya jelas.

---

## 3. `type="reset"`

Tipe `reset` digunakan untuk mengembalikan nilai kontrol formulir ke nilai awalnya.

Contoh:

```html
<form>
  <label for="username">Username:</label>
  <input
    type="text"
    id="username"
    name="username"
    value="Akbar"
  >

  <button type="reset">Reset</button>
</form>
```

Pada contoh tersebut, nilai awal input adalah `Akbar`.

Jika pengguna mengubahnya menjadi `Akbar123` lalu menekan tombol `Reset`, nilai input akan kembali menjadi `Akbar`.

Reset tidak selalu berarti membuat semua input kosong. Browser mengembalikan kontrol formulir ke nilai awal yang ditentukan oleh HTML.

### Kekurangan Tombol Reset

Tombol reset perlu digunakan dengan hati-hati karena pengguna bisa menekannya secara tidak sengaja dan kehilangan perubahan yang sudah dimasukkan ke dalam formulir.

Untuk formulir yang panjang, fitur reset terkadang justru mengganggu pengalaman pengguna.

---

## Menggunakan Elemen `<input>` sebagai Tombol

Selain elemen `<button>`, HTML juga menyediakan elemen `<input>` untuk membuat tombol.

Beberapa nilai `type` yang dapat digunakan adalah:

- `button`
- `submit`
- `reset`

Contoh:

```html
<input type="button" value="Click Me">
<input type="submit" value="Submit Form">
<input type="reset" value="Reset Form">
```

Atribut `value` digunakan untuk menentukan teks yang ditampilkan pada tombol.

Pada contoh tersebut:

- `type="button"` menghasilkan tombol biasa.
- `type="submit"` menghasilkan tombol submit.
- `type="reset"` menghasilkan tombol reset.

Perlu diperhatikan bahwa tombol dari `<input>` juga membutuhkan JavaScript jika ingin menjalankan tindakan khusus yang bukan perilaku bawaan tombol.

---

## Perbedaan `<button>` dan `<input>` sebagai Tombol

Keduanya dapat digunakan untuk membuat tombol, tetapi memiliki perbedaan dalam struktur HTML.

### Elemen `<button>`

Elemen `<button>` memiliki tag pembuka dan penutup. Kontennya dapat berupa teks, gambar, ikon, atau kombinasi elemen HTML yang sesuai.

Contoh:

```html
<button type="button">
  <strong>Start</strong>
</button>
```

### Elemen `<input>`

Elemen `<input>` merupakan void element sehingga tidak memiliki tag penutup dan tidak dapat menampung elemen anak.

Teks tombol ditentukan melalui atribut `value`.

Contoh:

```html
<input type="button" value="Start">
```

Perbandingan:

| Fitur | `<button>` | `<input>` |
|---|---|---|
| Tag penutup | Ada | Tidak ada |
| Teks tombol | Konten di dalam elemen | Atribut `value` |
| Dapat memiliki elemen anak | Ya, untuk konten yang sesuai | Tidak |
| Mendukung `button`, `submit`, dan `reset` | Ya | Ya |

---

## Contoh Form dengan Berbagai Tombol

```html
<form action="/submit" method="get">
  <label for="name">Nama:</label>

  <input
    type="text"
    id="name"
    name="name"
    value="Akbar"
  >

  <button type="button">Tombol Biasa</button>
  <button type="reset">Reset</button>
  <button type="submit">Kirim</button>
</form>
```

Pada contoh tersebut terdapat tiga tombol dengan perilaku yang berbeda:

1. **Tombol Biasa:** tidak mengirim atau mereset formulir secara otomatis.
2. **Reset:** mengembalikan input ke nilai awal, yaitu `Akbar`.
3. **Kirim:** mengirimkan formulir sesuai atribut `action` dan `method`.

---

## Best Practice

Beberapa hal yang perlu diperhatikan ketika menggunakan tombol HTML:

- Gunakan `type="button"` untuk tombol yang menjalankan tindakan khusus melalui JavaScript.
- Gunakan `type="submit"` untuk mengirim formulir.
- Gunakan `type="reset"` hanya jika memang dibutuhkan pengguna.
- Tuliskan atribut `type` secara eksplisit agar perilaku tombol mudah dipahami.
- Gunakan elemen `<button>` ketika membutuhkan konten tombol yang lebih fleksibel.
- Berikan teks tombol yang menjelaskan tindakan yang akan dilakukan.

---

## Ringkasan

### `type="button"`

Membuat tombol biasa yang tidak mengirim atau mereset formulir secara otomatis.

```html
<button type="button">Click Me</button>
```

### `type="submit"`

Mengirimkan formulir.

```html
<button type="submit">Submit</button>
```

### `type="reset"`

Mengembalikan kontrol formulir ke nilai awalnya.

```html
<button type="reset">Reset</button>
```

### Elemen `<input>` sebagai tombol

Elemen `<input>` juga dapat menghasilkan tombol menggunakan atribut `type`.

```html
<input type="button" value="Click Me">
```

**Kesimpulan:** Gunakan jenis tombol berdasarkan tindakan yang dibutuhkan. Pemilihan `type` yang tepat membuat perilaku formulir lebih jelas dan mengurangi kesalahan ketika pengguna berinteraksi dengan halaman web.