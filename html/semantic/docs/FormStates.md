# HTML Form States

## Pengertian

Form state adalah kondisi suatu kontrol formulir HTML ketika digunakan atau ditampilkan pada halaman web.

Elemen formulir, seperti `<input>`, dapat berada dalam beberapa kondisi yang memengaruhi cara pengguna berinteraksi dengannya.

Empat kondisi yang dipelajari dalam materi ini adalah:

- **Default state** → kondisi awal atau normal.
- **Focused state** → kondisi ketika input sedang mendapatkan fokus.
- **Disabled state** → kondisi ketika input dinonaktifkan.
- **Readonly state** → kondisi ketika nilai input tidak dapat diedit oleh pengguna.

Memahami kondisi formulir penting untuk membuat antarmuka yang mudah digunakan dan memberikan informasi yang jelas kepada pengguna.

---

## 1. Default State

Default state merupakan kondisi awal kontrol formulir ketika tidak sedang berada dalam kondisi khusus seperti focused atau disabled.

Contoh:

```html
<label for="email">Email:</label>
<input type="email" id="email">
```

Ketika halaman pertama kali dibuka, input tersebut tampil dalam kondisi normal dan kosong.

Contoh lain:

```html
<input type="text" value="Akbar">
```

Pada contoh tersebut, input memiliki nilai awal `Akbar`.

**Catatan:** Default state tidak selalu berarti input kosong. Nilai awalnya dapat ditentukan menggunakan atribut `value`.

---

## 2. Focused State

Focused state adalah kondisi ketika suatu elemen formulir sedang mendapatkan fokus.

Fokus biasanya terjadi ketika pengguna:

- Mengeklik kolom input.
- Memilih input menggunakan tombol `Tab` pada keyboard.
- Memindahkan fokus ke input melalui interaksi lain yang didukung browser.

Contoh:

```html
<label for="username">Username:</label>
<input type="text" id="username">
```

Ketika input diklik atau dipilih menggunakan tombol `Tab`, input akan mendapatkan fokus.

Browser biasanya menampilkan indikator fokus, misalnya garis tepi berwarna biru.

Tampilan tersebut dapat berbeda tergantung browser dan pengaturan sistem.

### Mengatur Focus dengan CSS

CSS menyediakan pseudo-class `:focus` untuk memilih elemen yang sedang mendapatkan fokus.

Contoh:

```css
input:focus {
  outline: 2px solid blue;
  outline-offset: 2px;
}
```

Ketika input mendapatkan fokus, browser akan menerapkan gaya tersebut.

Contoh ini membantu menunjukkan kepada pengguna bagian halaman yang sedang aktif.

### Mengapa Focus State Penting?

Focus state sangat penting untuk aksesibilitas, terutama bagi pengguna yang bernavigasi menggunakan keyboard.

Indikator fokus membantu pengguna mengetahui elemen mana yang sedang dipilih.

Sebaiknya jangan menghilangkan indikator fokus tanpa menyediakan penggantinya yang tetap terlihat jelas.

---

## 3. Disabled State

Disabled state adalah kondisi ketika elemen formulir dinonaktifkan menggunakan atribut `disabled`.

Contoh:

```html
<label for="disabled-email">Email:</label>
<input
  type="email"
  id="disabled-email"
  value="example@email.com"
  disabled
>
```

Input tersebut memiliki nilai awal, tetapi pengguna tidak dapat mengeditnya selama atribut `disabled` tetap diterapkan.

Pada umumnya, input yang dinonaktifkan:

- Tidak dapat diedit.
- Tidak menerima fokus melalui navigasi keyboard biasa.
- Tidak dapat dioperasikan seperti input aktif.
- Tidak ikut dikirim sebagai data formulir.

Browser biasanya menampilkan elemen disabled dengan tampilan yang berbeda, misalnya teks atau latar belakang yang terlihat redup.

### Kapan Menggunakan `disabled`?

Atribut `disabled` cocok digunakan ketika suatu kontrol belum boleh digunakan atau memang tidak tersedia untuk sementara.

Contoh:

```html
<button type="submit" disabled>
  Submit
</button>
```

Tombol tersebut tidak dapat digunakan sampai atribut `disabled` dihilangkan.

### Catatan Penting

Atribut `disabled` memengaruhi interaksi pengguna dan pengiriman data formulir.

Jika suatu nilai tetap perlu dikirim bersama formulir, jangan menganggap input disabled akan ikut terkirim secara otomatis.

---

## 4. Readonly State

Readonly state adalah kondisi ketika nilai suatu input hanya dapat dibaca dan tidak dapat diubah oleh pengguna melalui interaksi normal.

Untuk menerapkannya, gunakan atribut `readonly`.

Contoh:

```html
<label for="readonly-email">Email:</label>
<input
  type="email"
  id="readonly-email"
  value="example@email.com"
  readonly
>
```

Pada contoh tersebut:

- Nilai awal input adalah `example@email.com`.
- Pengguna tidak dapat mengubah nilai tersebut melalui input.
- Input masih dapat menerima fokus.
- Nilainya tetap dapat disertakan dalam pengiriman formulir.

Browser biasanya menampilkan input readonly dengan tampilan yang dapat berbeda dari input biasa.

### Kapan Menggunakan `readonly`?

Atribut `readonly` cocok ketika suatu nilai perlu ditampilkan kepada pengguna, tetapi tidak boleh diubah melalui kolom tersebut.

Contoh:

```html
<label for="order-id">Order ID:</label>
<input
  type="text"
  id="order-id"
  name="order_id"
  value="ORD-1024"
  readonly
>
```

Contoh tersebut menampilkan ID pesanan yang tidak dapat diedit melalui input.

### Catatan Penting

Atribut `readonly` hanya berlaku pada jenis input tertentu, seperti `text` dan `email`, serta pada elemen `<textarea>`.

Atribut ini tidak digunakan untuk semua jenis input.

Selain itu, readonly bukan pengganti validasi atau keamanan di server. Nilai yang dikirim oleh browser tetap harus diperiksa oleh backend apabila digunakan dalam proses penting.

---

## Perbedaan `disabled` dan `readonly`

Walaupun keduanya membuat nilai input tidak dapat diedit oleh pengguna, perilakunya berbeda.

| Perilaku | `disabled` | `readonly` |
|---|---|---|
| Nilai bisa diedit | Tidak | Tidak |
| Dapat menerima fokus | Umumnya tidak | Ya |
| Nilai ikut dikirim melalui form | Tidak | Ya |
| Bisa digunakan untuk semua tipe input | Tidak semua kontrol | Hanya tipe tertentu |
| Contoh penggunaan | Input belum tersedia | Data yang hanya perlu dibaca |

Contoh `disabled`:

```html
<input
  type="text"
  value="Akbar"
  disabled
>
```

Contoh `readonly`:

```html
<input
  type="text"
  value="Akbar"
  readonly
>
```

Keduanya menampilkan nilai `Akbar`, tetapi perilakunya berbeda.

Pada input pertama, kontrol dinonaktifkan dan nilainya tidak disertakan dalam pengiriman formulir.

Pada input kedua, pengguna tidak dapat mengedit nilainya melalui input, tetapi nilainya tetap dapat dikirimkan bersama formulir.

---

## Menguji Focus State dengan Keyboard

Kamu dapat menguji focus state tanpa menggunakan mouse.

Contoh:

```html
<form>
  <label for="name">Nama:</label>
  <input type="text" id="name">

  <label for="email">Email:</label>
  <input type="email" id="email">
</form>
```

Langkah pengujian:

1. Buka halaman HTML di browser.
2. Klik area kosong pada halaman.
3. Tekan tombol `Tab`.
4. Perhatikan input yang mendapatkan fokus.
5. Tekan `Tab` lagi untuk berpindah ke elemen berikutnya.

Indikator fokus akan membantu kamu melihat elemen yang sedang aktif.

Input yang disabled umumnya dilewati dalam navigasi keyboard tersebut, sedangkan input readonly masih dapat menerima fokus.

---

## Contoh Lengkap

```html
<form>
  <div>
    <label for="default-email">Default State:</label>
    <input
      type="email"
      id="default-email"
      placeholder="Masukkan email"
    >
  </div>

  <div>
    <label for="readonly-email">Readonly State:</label>
    <input
      type="email"
      id="readonly-email"
      value="example@email.com"
      readonly
    >
  </div>

  <div>
    <label for="disabled-email">Disabled State:</label>
    <input
      type="email"
      id="disabled-email"
      value="disabled@example.com"
      disabled
    >
  </div>
</form>
```

Pada contoh tersebut:

- Input pertama berada dalam kondisi normal.
- Input kedua tidak dapat diedit, tetapi masih dapat menerima fokus.
- Input ketiga dinonaktifkan dan tidak dapat berinteraksi seperti input biasa.

Focused state dapat diuji dengan mengeklik input pertama atau memilihnya menggunakan tombol `Tab`.

---

## Ringkasan

### Default State

Kondisi awal atau normal suatu kontrol formulir.

```html
<input type="text">
```

### Focused State

Kondisi ketika suatu elemen mendapatkan fokus.

```css
input:focus {
  outline: 2px solid blue;
}
```

### Disabled State

Menonaktifkan kontrol formulir.

```html
<input type="text" disabled>
```

### Readonly State

Membuat nilai input tidak dapat diedit melalui interaksi normal pengguna.

```html
<input type="text" value="Akbar" readonly>
```

### Kesimpulan

Form states menentukan bagaimana kontrol formulir berperilaku dan bagaimana pengguna berinteraksi dengannya.

Perbedaan terpenting yang perlu diingat adalah **disabled menonaktifkan kontrol, sedangkan readonly membuat nilainya tidak dapat diedit tetapi kontrolnya masih dapat menerima fokus**.