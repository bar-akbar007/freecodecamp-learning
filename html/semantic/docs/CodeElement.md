# HTML `<code>` dan `<pre>` Element

## Pengertian

HTML menyediakan elemen `<code>` dan `<pre>` untuk menampilkan **kode komputer** pada halaman web.

Keduanya sering digunakan pada:

- Dokumentasi pemrograman.
- Artikel teknis.
- Tutorial coding.
- Dokumentasi API.
- Website pembelajaran pemrograman.

Perbedaan utamanya adalah:

- `<code>` → untuk **cuplikan kode pendek atau inline**.
- `<pre>` + `<code>` → untuk **kode yang terdiri dari beberapa baris**.

---

## Elemen `<code>`

Elemen `<code>` digunakan untuk merepresentasikan **cuplikan kode pendek di dalam teks**.

Contoh:

```html
<p>
  Gunakan <code>color: blue;</code> untuk mengubah warna teks.
</p>
```

Pada contoh tersebut, `color: blue;` merupakan potongan kode yang berada di dalam kalimat.

Browser biasanya memberikan gaya default berupa **font monospace** pada teks yang berada di dalam `<code>`.

---

## Font Monospace

Font monospace adalah font yang setiap karakternya memiliki **lebar yang sama**.

Contohnya:

```text
WWWW
iiii
```

Dalam font monospace, setiap karakter memiliki lebar yang sama sehingga kode lebih mudah dibaca dan disejajarkan.

Karena alasan tersebut, browser biasanya menampilkan elemen `<code>` menggunakan font monospace secara default.

---

## Contoh `<code>` Inline

```html
<p>
  Untuk membuat paragraf, gunakan elemen <code>&lt;p&gt;</code>.
</p>
```

Contoh lainnya:

```html
<p>
  Jalankan perintah <code>npm install</code> di terminal.
</p>
```

Pada contoh tersebut, `<code>` hanya digunakan untuk bagian kode yang pendek.

---

## Elemen `<pre>`

Elemen `<pre>` digunakan untuk merepresentasikan **teks yang telah diformat sebelumnya**.

Berbeda dengan elemen HTML biasa, spasi dan baris baru di dalam `<pre>` akan dipertahankan oleh browser.

Contoh:

```html
<pre>
Hello
World
</pre>
```

Spasi dan baris baru yang terdapat di dalam `<pre>` akan tetap dipertahankan ketika ditampilkan.

---

## `<pre>` dan Spasi

Perhatikan contoh berikut:

```html
<pre>
    Hello
        World
</pre>
```

Spasi sebelum `Hello` dan `World` akan tetap ditampilkan.

Artinya, ketika menggunakan `<pre>`, **indentasi di dalam kode HTML akan memengaruhi tampilan pada browser**.

Karena itu, penulisan `<pre>` harus diperhatikan agar tidak menghasilkan indentasi yang tidak diinginkan.

---

## Menggabungkan `<pre>` dan `<code>`

Untuk menampilkan **kode program yang panjang atau terdiri dari beberapa baris**, gunakan `<code>` di dalam `<pre>`.

Contoh:

```html
<pre><code>
const name = "Akbar";

console.log(name);
</code></pre>
```

Strukturnya:

```text
<pre>
  └── <code>
        └── kode program
```

`<pre>` mempertahankan format dan spasi kode, sedangkan `<code>` memberikan makna bahwa isi tersebut merupakan **kode komputer**.

---

## Contoh Kode CSS

```html
<pre><code>
body {
  background-color: white;
  color: black;
}
</code></pre>
```

Contoh tersebut cocok digunakan dalam dokumentasi CSS karena kode memiliki beberapa baris dan membutuhkan indentasi yang tetap.

---

## Perbedaan `<code>` dan `<pre>`

| Elemen | Fungsi | Contoh penggunaan |
|---|---|---|
| `<code>` | Menampilkan cuplikan kode pendek | `npm install` |
| `<pre>` | Mempertahankan format teks dan spasi | Teks atau kode multi-baris |
| `<pre><code>` | Menampilkan kode multi-baris | CSS, JavaScript, PHP |

---

## Kapan Menggunakan `<code>`?

Gunakan `<code>` ketika ingin menampilkan kode yang pendek dan berada di dalam sebuah kalimat.

Contoh:

```html
<p>
  Gunakan <code>console.log()</code> untuk menampilkan data di JavaScript.
</p>
```

---

## Kapan Menggunakan `<pre><code>`?

Gunakan kombinasi `<pre>` dan `<code>` ketika ingin menampilkan kode yang:

- terdiri dari beberapa baris,
- memiliki indentasi,
- memiliki spasi atau baris baru yang harus dipertahankan,
- atau digunakan sebagai contoh program lengkap.

Contoh:

```html
<pre><code>
function greet(name) {
  return "Hello " + name;
}

console.log(greet("Akbar"));
</code></pre>
```

---

## Catatan Penting

Elemen `<pre>` tidak hanya digunakan untuk kode program. Elemen ini dapat digunakan untuk **teks apa pun yang membutuhkan format asli tetap dipertahankan**.

Namun, ketika tujuannya memang menampilkan kode komputer, penggunaan:

```html
<pre><code>
  ...
</code></pre>
```

lebih tepat karena memberikan makna semantik yang jelas bahwa isi tersebut adalah kode.

---

## Contoh Lengkap

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8">
    <title>Code Element</title>
  </head>

  <body>
    <h1>Contoh Kode dalam HTML</h1>

    <p>
      Gunakan <code>console.log()</code>
      untuk menampilkan data di JavaScript.
    </p>

    <h2>Contoh Kode Multi-baris</h2>

    <pre><code>
function greet(name) {
  return "Hello " + name;
}

console.log(greet("Akbar"));
    </code></pre>
  </body>
</html>
```

---

## Ringkasan

### `<code>`

Digunakan untuk **cuplikan kode pendek atau inline**.

```html
<code>console.log()</code>
```

### `<pre>`

Digunakan untuk menampilkan **teks yang formatnya dipertahankan**, termasuk spasi dan baris baru.

```html
<pre>
Hello
World
</pre>
```

### `<pre><code>`

Digunakan untuk menampilkan **kode komputer yang lebih panjang dan memiliki beberapa baris**.

```html
<pre><code>
const name = "Akbar";
console.log(name);
</code></pre>
```

Jadi, pola sederhananya:

```text
Kode pendek  → <code>
Kode panjang → <pre><code>
```