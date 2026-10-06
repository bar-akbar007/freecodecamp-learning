# HTML Semantic Review

## Pengertian

HTML semantik adalah penggunaan elemen HTML yang memiliki **makna dan fungsi yang jelas** terhadap struktur maupun isi halaman web.

Contohnya adalah:

```html
<header>
<nav>
<main>
<section>
<article>
<figure>
<address>
```

Berbeda dengan elemen presentasi yang lebih berfokus pada tampilan.

---

## Pentingnya HTML Semantik

Penggunaan HTML semantik membantu membuat struktur halaman menjadi lebih jelas dan logis.

HTML semantik juga penting untuk:

- Struktur dokumen.
- Aksesibilitas.
- Pembaca layar.
- Pemahaman struktur halaman oleh browser dan sistem lainnya.

---

## Hirarki Heading

Heading digunakan untuk membuat hierarki struktur dokumen.

Terdapat enam tingkat heading:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

`<h1>` adalah tingkat heading tertinggi, sedangkan `<h6>` adalah tingkat terendah.

Heading sebaiknya digunakan secara terstruktur dan tidak melompati tingkatan secara sembarangan karena dapat mengganggu hierarki logis dokumen dan aksesibilitas.

---

## Elemen Semantik Utama

### `<header>`

Digunakan untuk mendefinisikan bagian header dari dokumen atau suatu bagian halaman.

```html
<header>
  <h1>Website Akbar</h1>
</header>
```

---

### `<main>`

Digunakan untuk memuat **konten utama** halaman web.

```html
<main>
  <h1>Artikel Utama</h1>
  <p>Isi utama halaman.</p>
</main>
```

---

### `<section>`

Digunakan untuk membagi konten menjadi **bagian-bagian yang lebih kecil**.

```html
<section>
  <h2>Tentang Kami</h2>
  <p>Informasi tentang perusahaan.</p>
</section>
```

---

### `<nav>`

Digunakan untuk mewakili bagian yang berisi **link navigasi**.

```html
<nav>
  <a href="#home">Home</a>
  <a href="#about">About</a>
  <a href="#contact">Contact</a>
</nav>
```

---

### `<article>`

Digunakan untuk mewakili konten yang **mandiri dan independen**, seperti artikel berita atau posting blog.

```html
<article>
  <h2>Belajar HTML Semantic</h2>
  <p>Artikel tentang HTML semantik.</p>
</article>
```

---

### `<figure>`

Digunakan untuk memuat ilustrasi, diagram, atau konten visual yang berhubungan dengan isi halaman.

```html
<figure>
  <img src="diagram.png" alt="Diagram HTML">
</figure>
```

---

# Elemen Teks Semantik

## `<em>`

Digunakan untuk memberikan **penekanan atau stress** pada teks.

```html
<p>
  Ini adalah <em>bagian penting</em> dari kalimat.
</p>
```

`<em>` memiliki makna semantik, bukan hanya untuk membuat teks miring.

Jika hanya ingin mengubah tampilan menjadi miring, gunakan CSS.

---

## `<i>`

Digunakan untuk menunjukkan teks yang memiliki konteks berbeda dari teks sekitarnya, misalnya:

- Istilah teknis.
- Istilah dari bahasa lain.
- Istilah idiomatik.
- Suara atau suasana tertentu.
- Pemikiran.

Contoh:

```html
<p>
  Kata <i>bonjour</i> berasal dari bahasa Prancis.
</p>
```

Atribut `lang` dapat digunakan untuk menunjukkan bahasa teks.

```html
<i lang="fr">bonjour</i>
```

`<i>` tidak menunjukkan bahwa teks tersebut penting.

---

## `<strong>`

Digunakan untuk menunjukkan **kepentingan yang kuat**.

```html
<p>
  <strong>Peringatan:</strong> Data akan dihapus.
</p>
```

`<strong>` memiliki makna semantik bahwa teks tersebut sangat penting.

---

## `<b>`

Digunakan untuk **menarik perhatian** pada teks yang tidak memiliki kepentingan semantik yang kuat.

Salah satu penggunaannya adalah untuk menyoroti keyword atau nama produk.

```html
<p>
  Produk <b>Super Laptop</b> sedang tersedia.
</p>
```

`<b>` berbeda dengan `<strong>` karena `<b>` tidak menunjukkan tingkat kepentingan yang kuat.

---

# Description List

## `<dl>`

Digunakan untuk membuat kumpulan **istilah dan deskripsi**.

## `<dt>`

Digunakan untuk mendefinisikan **istilah**.

## `<dd>`

Digunakan untuk memberikan **deskripsi dari istilah**.

Contoh:

```html
<dl>
  <dt>HTML</dt>
  <dd>Bahasa markup untuk struktur halaman web.</dd>

  <dt>CSS</dt>
  <dd>Bahasa stylesheet untuk mengatur tampilan.</dd>
</dl>
```

Strukturnya:

```text
<dl>
├── <dt> → istilah
└── <dd> → deskripsi
```

---

# Elemen Kutipan

## `<blockquote>`

Digunakan untuk mewakili bagian yang merupakan **kutipan dari sumber lain**.

Atribut `cite` dapat digunakan untuk memberikan URL sumber.

```html
<blockquote cite="https://example.com">
  Belajar adalah proses yang terus berlangsung.
</blockquote>
```

---

## `<cite>`

Digunakan untuk menandai **judul karya atau sumber yang dirujuk**.

Contoh:

```html
<p>
  Saya sedang membaca <cite>Belajar HTML</cite>.
</p>
```

`<cite>` berbeda dengan atribut `cite` pada `<blockquote>`.

---

## `<q>`

Digunakan untuk **kutipan pendek atau inline**.

```html
<p>
  Dia berkata, <q>Belajar coding setiap hari.</q>
</p>
```

Gunakan `<q>` untuk kutipan pendek dan `<blockquote>` untuk kutipan yang lebih panjang.

---

# Abbreviation

## `<abbr>`

Digunakan untuk menandai sebuah **singkatan**.

Atribut `title` dapat digunakan untuk memberikan bentuk lengkap atau deskripsi yang mudah dipahami.

```html
<p>
  Saya sedang belajar
  <abbr title="HyperText Markup Language">HTML</abbr>.
</p>
```

---

# Informasi Kontak

## `<address>`

Digunakan untuk mewakili **informasi kontak**.

```html
<address>
  Muhammad Akbar<br>
  Yogyakarta, Indonesia<br>
  <a href="mailto:example@email.com">
    example@email.com
  </a>
</address>
```

---

## `<br>`

Digunakan untuk membuat **baris baru**.

Biasanya berguna pada alamat atau teks yang memang membutuhkan pemisahan baris.

```html
<address>
  Jalan Merdeka No. 10<br>
  Yogyakarta<br>
  Indonesia
</address>
```

---

# Tanggal dan Waktu

## `<time>`

Digunakan untuk merepresentasikan **tanggal dan/atau waktu**.

```html
<time datetime="2026-10-06">
  6 Oktober 2026
</time>
```

Atribut `datetime` memberikan nilai dalam format yang dapat dibaca mesin.

Contoh:

```html
<time datetime="2026-10-06T20:00:00">
  6 Oktober 2026 pukul 20:00
</time>
```

---

## ISO 8601

Format tanggal dan waktu dapat menggunakan standar ISO 8601:

```text
YYYY-MM-DDTHH:MM:SS
```

Contoh:

```text
2026-10-06T20:00:00
```

Huruf `T` digunakan sebagai **pemisah antara tanggal dan waktu**.

---

# Superscript dan Subscript

## `<sup>`

Digunakan untuk menampilkan teks sebagai **superskrip**, yaitu berada di atas garis teks normal.

Contoh:

```html
<p>2<sup>2</sup> = 4</p>
```

Hasil:

```text
2² = 4
```

Penggunaan umum:

- Eksponen.
- Huruf superior.
- Bilangan ordinal.

---

## `<sub>`

Digunakan untuk menampilkan teks sebagai **subskrip**, yaitu berada di bawah garis teks normal.

Contoh:

```html
<p>H<sub>2</sub>O</p>
```

Hasil:

```text
H₂O
```

Penggunaan umum:

- Rumus kimia.
- Subskrip variabel.
- Catatan kaki tertentu.

---

# Menampilkan Kode

## `<code>`

Digunakan untuk merepresentasikan **cuplikan kode komputer**.

Contoh inline:

```html
<p>
  Gunakan <code>console.log()</code> untuk JavaScript.
</p>
```

Browser biasanya menggunakan font monospace sebagai gaya default untuk `<code>`.

---

## `<pre>`

Digunakan untuk merepresentasikan **teks yang telah diformat sebelumnya**.

Spasi dan baris baru akan dipertahankan.

```html
<pre>
Hello
    World
</pre>
```

---

## `<pre><code>`

Untuk kode yang memiliki beberapa baris, gunakan `<code>` di dalam `<pre>`.

```html
<pre><code>
function greet(name) {
  return "Hello " + name;
}
</code></pre>
```

Pola sederhananya:

```text
Kode pendek  → <code>
Kode panjang → <pre><code>
```

---

# Elemen `<u>`

Digunakan untuk menandai teks yang memiliki **anotasi non-tekstual**.

Contoh:

```html
<p>
  There is an <u>incorrect</u> spelling.
</p>
```

Browser biasanya menampilkan garis bawah pada teks tersebut.

Namun, `<u>` tidak sebaiknya digunakan hanya untuk kebutuhan styling.

Jika hanya ingin memberi garis bawah secara visual, gunakan CSS.

```css
.underline {
  text-decoration: underline;
}
```

---

# Elemen `<s>`

Digunakan ketika sebuah informasi **sudah tidak akurat atau tidak relevan**.

Contoh:

```html
<p>
  Harga lama:
  <s>Rp100.000</s>
</p>

<p>
  Harga baru:
  Rp75.000
</p>
```

Jika teks benar-benar dihapus dari dokumen, elemen yang lebih tepat adalah `<del>`.

---

# Ruby Annotation

## `<ruby>`

Digunakan untuk memberikan **anotasi pada teks**, terutama untuk menunjukkan pengucapan atau penjelasan pada tipografi Asia Timur.

```html
<ruby>
  日本語
  <rt>にほんご</rt>
</ruby>
```

---

## `<rt>`

Digunakan untuk menentukan **teks anotasi ruby**.

```html
<ruby>
  日本語
  <rt>にほんご</rt>
</ruby>
```

`日本語` adalah teks utama, sedangkan `にほんご` adalah anotasinya.

---

## `<rp>`

Digunakan sebagai **fallback** untuk browser yang tidak mendukung tampilan ruby.

Contoh:

```html
<ruby>
  日本語
  <rp>(</rp>
  <rt>にほんご</rt>
  <rp>)</rp>
</ruby>
```

---

# `tel:` dan `mailto:`

## `tel:`

Digunakan pada `href` untuk membuat link nomor telepon yang dapat diklik.

```html
<a href="tel:+6281234567890">
  +62 812-3456-7890
</a>
```

---

## `mailto:`

Digunakan untuk membuat link yang dapat membuka email baru pada email client.

```html
<a href="mailto:example@email.com">
  example@email.com
</a>
```

Kedua skema tersebut dapat digunakan pada elemen `<a>`.

---

# Internal Link

Link internal digunakan untuk menuju bagian tertentu dalam halaman yang sama.

Caranya dengan menggunakan `href="#id"`.

```html
<a href="#contact">
  Ke bagian Contact
</a>

<section id="contact">
  <h2>Contact</h2>
</section>
```

Strukturnya:

```text
href="#contact"
      ↓
    id="contact"
```

Penggunaan umum:

- Skip link.
- Daftar isi.
- Halaman panjang dengan banyak bagian.

---

# Presentational vs Semantic HTML

## Presentational HTML

Elemen presentasional berfokus pada bagaimana konten terlihat.

Beberapa elemen lama yang sudah tidak digunakan dalam HTML modern antara lain:

```text
<center>
<big>
<font>
```

Untuk kebutuhan tampilan, gunakan CSS.

---

## Semantic HTML

Elemen semantik memberikan **makna dan struktur** pada konten.

Contoh:

```html
<header>
<nav>
<main>
<section>
<article>
<figure>
<address>
```

Keuntungan utamanya adalah struktur dokumen menjadi lebih jelas dan bermakna.

---

# Tabel Ringkasan

| Elemen | Fungsi |
|---|---|
| `<header>` | Header dokumen atau bagian |
| `<main>` | Konten utama halaman |
| `<section>` | Membagi konten menjadi beberapa bagian |
| `<nav>` | Bagian navigasi |
| `<article>` | Konten mandiri |
| `<figure>` | Ilustrasi atau diagram |
| `<em>` | Penekanan |
| `<i>` | Teks dengan konteks berbeda |
| `<strong>` | Kepentingan kuat |
| `<b>` | Menarik perhatian |
| `<dl>` | Daftar istilah dan deskripsi |
| `<dt>` | Istilah |
| `<dd>` | Deskripsi istilah |
| `<blockquote>` | Kutipan panjang |
| `<cite>` | Judul karya atau sumber |
| `<q>` | Kutipan pendek |
| `<abbr>` | Singkatan |
| `<address>` | Informasi kontak |
| `<br>` | Baris baru |
| `<time>` | Tanggal/waktu |
| `<sup>` | Superskrip |
| `<sub>` | Subskrip |
| `<code>` | Cuplikan kode |
| `<pre>` | Teks dengan format yang dipertahankan |
| `<u>` | Anotasi non-tekstual |
| `<s>` | Informasi yang tidak lagi relevan |
| `<ruby>` | Anotasi ruby |
| `<rt>` | Teks anotasi ruby |
| `<rp>` | Fallback ruby |

---

# Kesimpulan

HTML semantik menggunakan elemen yang memiliki **makna sesuai dengan fungsi kontennya**.

Contoh struktur halaman semantik:

```html
<header>
  <h1>Website Akbar</h1>

  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
  </nav>
</header>

<main>
  <section>
    <h2>About</h2>

    <article>
      <h3>Belajar HTML</h3>
      <p>
        Saya sedang belajar
        <abbr title="HyperText Markup Language">HTML</abbr>.
      </p>
    </article>
  </section>
</main>

<footer>
  <address>
    <a href="mailto:example@email.com">
      example@email.com
    </a>
  </address>
</footer>
```

Intinya, **gunakan elemen HTML berdasarkan makna dan fungsi kontennya**, sedangkan kebutuhan tampilan sebaiknya ditangani dengan CSS.