Dokumentasi Dasar HTML

Catatan pembelajaran HTML dari freeCodeCamp, dirapikan untuk
dokumentasi dan referensi pribadi.

Daftar Isi

1. Dasar HTML

2. Elemen HTML Umum

3. Pengidentifikasi dan
Pengelompokan

4. Karakter Khusus dan Linking

5. Boilerplate dan Pengkodean

6. SEO dan Berbagi Sosial

7. Elemen Media dan Optimasi

8. Integrasi Multimedia

9. Jenis Atribut Target

10. Jalur Absolut vs. Relatif

11. Link States

1. Dasar HTML

Peran HTML

HTML digunakan untuk mewakili isi dan struktur halaman web.

Elemen HTML

Elemen adalah blok bangunan untuk dokumen HTML. Elemen dapat digunakan
untuk membuat judul, paragraf, tautan, gambar, dan berbagai jenis konten
lainnya.

Sebagian besar elemen HTML terdiri dari:

Tag pembuka

Konten

Tag penutup

<elementName>Content goes here</elementName>

Elemen Void

Elemen void tidak memiliki konten dan hanya menggunakan tag awal.
Contohnya adalah img dan meta.

<img>
<meta>

Beberapa basis kode menggunakan garis miring / pada elemen void.
Keduanya dapat digunakan:

<img>
<img />

Atribut

Atribut adalah nilai yang ditempatkan di dalam tag pembuka elemen HTML.
Atribut memberikan informasi tambahan atau menentukan bagaimana elemen
harus berperilaku.

<element attribute="value"></element>

Atribut Boolean

Atribut boolean adalah atribut yang dapat ada atau tidak ada dalam tag
HTML.

Jika atribut ada → nilainya dianggap true.

Jika atribut tidak ada → nilainya dianggap false.

Contoh:

disabled

readonly

required

Komentar

Komentar digunakan untuk meninggalkan catatan bagi diri sendiri atau
pengembang lain.

<!-- This is an HTML comment. -->

2. Elemen HTML Umum

Heading

HTML memiliki enam elemen heading:

<h1>Judul Utama</h1>
<h2>Subjudul</h2>
<h3>Subjudul</h3>
<h4>Subjudul</h4>
<h5>Subjudul</h5>
<h6>Subjudul</h6>

h1 memiliki tingkat kepentingan paling tinggi, sedangkan h6 paling
rendah.

Paragraf

Elemen p digunakan untuk membuat paragraf pada halaman web.

<p>Ini adalah sebuah paragraf.</p>

Elemen img

Elemen img digunakan untuk menampilkan gambar. Atribut src digunakan
untuk menentukan lokasi gambar, sedangkan alt digunakan untuk
memberikan teks alternatif.

<img src="gambar.jpg" alt="Deskripsi gambar">

Elemen body

Elemen body berisi konten utama yang ditampilkan pada halaman web.

<body>
  <h1>Hello World</h1>
</body>

Elemen section

Elemen section digunakan untuk membagi konten menjadi beberapa bagian
yang lebih kecil dan terstruktur.

<section>
  <h2>Profil</h2>
  <p>Informasi profil.</p>
</section>

Elemen div

Elemen div merupakan elemen HTML generik tanpa makna semantik khusus.
Biasanya digunakan sebagai wadah untuk mengelompokkan elemen lain.

<div>
  <p>Konten di dalam div.</p>
</div>

Elemen a

Elemen a digunakan untuk membuat tautan ke halaman atau sumber daya
lain. Atribut href menentukan tujuan tautan.

<a href="https://freecodecamp.org">Visit freeCodeCamp</a>

Daftar ul dan ol

ul digunakan untuk membuat daftar tidak berurutan, sedangkan ol
digunakan untuk membuat daftar berurutan. Item daftar menggunakan elemen
li.

<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>

<ol>
  <li>Belajar HTML</li>
  <li>Belajar CSS</li>
  <li>Belajar JavaScript</li>
</ol>

Elemen em

Elemen em digunakan untuk memberikan penekanan pada teks.

<p>Ini adalah <em>teks penting</em>.</p>

Elemen strong

Elemen strong digunakan untuk memberikan penekanan kuat pada teks,
misalnya untuk menunjukkan urgensi atau keseriusan.

<p><strong>Peringatan:</strong> Data harus disimpan.</p>

Elemen figure dan figcaption

figure digunakan untuk mengelompokkan konten seperti gambar atau
diagram. figcaption digunakan sebagai keterangan untuk konten
tersebut.

<figure>
  <img src="diagram.png" alt="Diagram sistem">
  <figcaption>Diagram sistem aplikasi.</figcaption>
</figure>

Elemen main

Elemen main digunakan untuk mewakili konten utama pada halaman web.

<main>
  <h1>Konten Utama</h1>
</main>

Elemen footer

Elemen footer biasanya ditempatkan di bagian bawah dokumen HTML dan
dapat berisi informasi hak cipta atau tautan penting lainnya.

<footer>
  <p>&copy; 2026 Akbar</p>
</footer>

Elemen button

Elemen button digunakan untuk membuat tombol yang dapat diklik.

<button>Klik Saya</button>

3. Pengidentifikasi dan Pengelompokan

ID

id digunakan sebagai pengidentifikasi unik untuk sebuah elemen HTML.

Nama id sebaiknya hanya digunakan satu kali dalam satu dokumen HTML.

<h1 id="title">Movie Review Page</h1>

Nama id tidak boleh memiliki spasi. Jika terdiri dari beberapa kata,
gunakan tanda hubung atau garis bawah.

<div id="red-box"></div>

Class

class digunakan untuk mengelompokkan elemen, terutama untuk styling
dan perilaku menggunakan CSS atau JavaScript.

<div class="box"></div>

Berbeda dengan id, nama class dapat digunakan kembali pada banyak
elemen.

Satu elemen juga dapat memiliki beberapa class:

<div class="box red-box"></div>
<div class="box blue-box"></div>

4. Karakter Khusus dan Linking

Entitas HTML

Entitas HTML atau character references digunakan untuk menampilkan
karakter yang memiliki arti khusus dalam HTML.

Contoh:

&amp; → &

&lt; → <

<p>This is an &lt;img /&gt; element</p>

Elemen link

Elemen link digunakan untuk menghubungkan dokumen HTML dengan sumber
daya eksternal, seperti stylesheet CSS atau ikon.

<link rel="stylesheet" href="./styles.css">

Atribut penting:

rel → menentukan hubungan antara dokumen dan sumber daya.

href → menentukan lokasi sumber daya.

Elemen script

Elemen script digunakan untuk menanamkan atau menghubungkan kode
JavaScript.

JavaScript dapat ditulis langsung:

<body>
  <script>
    alert("Welcome to freeCodeCamp");
  </script>
</body>

Namun, untuk project, lebih baik menggunakan file JavaScript eksternal:

<script src="path-to-javascript-file.js"></script>

Atribut src menentukan lokasi file JavaScript eksternal.

5. Boilerplate dan Pengkodean

HTML Boilerplate

HTML boilerplate adalah struktur dasar yang berisi elemen-elemen penting
yang dibutuhkan oleh dokumen HTML.

<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Judul Halaman</title>
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>

DOCTYPE

DOCTYPE digunakan untuk memberi tahu browser bahwa dokumen menggunakan
standar HTML.

Elemen html

Elemen html merupakan elemen akar atau tingkat paling atas dari
dokumen HTML.

Atribut lang digunakan untuk menentukan bahasa dokumen.

<html lang="id">

Elemen head

Bagian head berisi metadata dan informasi yang dibutuhkan browser
serta mesin pencari.

Elemen meta

Elemen meta digunakan untuk menyimpan metadata halaman, seperti
pengkodean karakter dan informasi lain yang digunakan browser atau
platform tertentu.

Elemen title

Elemen title menentukan teks yang ditampilkan pada tab atau jendela
browser.

<title>Belajar HTML</title>

Pengkodean UTF-8

UTF-8 merupakan pengkodean karakter yang banyak digunakan di web.

Untuk menentukan UTF-8:

<meta charset="UTF-8">

6. SEO dan Berbagi Sosial

SEO

SEO (Search Engine Optimization) adalah praktik mengoptimalkan halaman
web agar lebih mudah ditemukan dan memiliki visibilitas yang lebih baik
di mesin pencari.

Meta description

Meta description digunakan untuk memberikan deskripsi singkat tentang
halaman dan membantu SEO.

<meta
  name="description"
  content="Discover expert tips and techniques for gardening in small spaces."
>

Open Graph

Open Graph digunakan untuk mengatur bagaimana konten halaman ditampilkan
ketika dibagikan ke platform media sosial seperti Facebook dan LinkedIn.

Properti Open Graph ditempatkan di dalam head.

og:title

Menentukan judul yang ditampilkan pada postingan media sosial.

<meta content="freeCodeCamp.org" property="og:title">

og:type

Menentukan jenis konten yang dibagikan, misalnya artikel, website,
video, atau musik.

<meta property="og:type" content="website">

og:image

Menentukan gambar yang digunakan pada preview media sosial.

<meta
  content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
  property="og:image"
>

og:url

Menentukan URL yang akan digunakan ketika pengguna mengklik postingan.

<meta property="og:url" content="https://www.freecodecamp.org">

7. Elemen Media dan Optimasi

Elemen yang Diganti (Replaced Elements)

Elemen yang diganti adalah elemen yang isinya ditentukan oleh sumber
daya eksternal, bukan oleh CSS secara langsung.

Contohnya adalah iframe.

iframe (inline frame) digunakan untuk menyematkan dokumen atau
konten HTML lain ke dalam halaman.

<iframe
  src="https://www.example.com"
  title="Example Site"
></iframe>

Atribut allowfullscreen dapat digunakan untuk memungkinkan konten
iframe ditampilkan dalam mode layar penuh.

<iframe
  src="video-url"
  width="800"
  height="450"
  allowfullscreen
></iframe>

video dan embed juga termasuk contoh elemen yang dapat berperilaku
sebagai replaced elements.

Contoh input dengan tipe image:

<input
  type="image"
  alt="Descriptive text goes here"
  src="example-img-url"
>

Optimasi Media

Saat menggunakan media seperti gambar, ada tiga hal utama yang perlu
diperhatikan:

Ukuran

Format

Kompresi

Kompresi digunakan untuk mengurangi ukuran file atau data.

Format Gambar

PNG dan JPG merupakan format gambar yang umum digunakan. Untuk kebutuhan
web modern, format seperti WebP atau AVIF dapat dipertimbangkan
apabila tidak membutuhkan dukungan untuk browser lama.

Lisensi Gambar

Jenis lisensi menentukan bagaimana sebuah gambar boleh digunakan.

Public domain → tidak memiliki hak cipta yang melekat dan dapat
digunakan tanpa batasan hak cipta.

CC0 → dirancang untuk melepaskan hak cipta sejauh yang diizinkan
hukum.

Lisensi permisif lainnya dapat memiliki ketentuan penggunaan
tertentu, misalnya Creative Commons atau BSD.

Selalu periksa lisensi sebelum menggunakan aset dari internet.

SVG

SVG (Scalable Vector Graphics) menyimpan grafik menggunakan jalur dan
persamaan untuk menentukan titik, garis, dan kurva.

Karena berbasis vektor, SVG dapat diperbesar atau diperkecil tanpa
kehilangan kualitas seperti gambar raster.

8. Integrasi Multimedia

Elemen audio dan video

Elemen audio dan video digunakan untuk menambahkan konten suara dan
video ke dokumen HTML.

Format yang disebutkan dalam materi:

audio → MP3, WAV, OGG

video → MP4, OGG, WebM

Contoh audio:

<audio src="CrystalizeThatInnerChild.mp3"></audio>

Atribut controls

Atribut controls menampilkan kontrol pemutaran bawaan browser.

<audio
  src="audio.mp3"
  controls
></audio>

Pengguna dapat menggunakan kontrol tersebut untuk mengatur volume,
menjeda, atau melanjutkan pemutaran.

controls merupakan atribut boolean. Jika atribut tidak ditulis,
kontrol bawaan tidak ditampilkan.

Atribut autoplay

autoplay membuat audio atau video mulai diputar secara otomatis ketika
browser mengizinkannya.

<video src="video.mp4" autoplay></video>

Atribut loop

loop membuat media diputar kembali secara terus-menerus.

<audio src="audio.mp3" controls loop></audio>

Atribut muted

muted membuat audio atau video dimulai dalam keadaan tanpa suara.

<video src="video.mp4" controls muted></video>

Elemen source

Elemen source memungkinkan kita menyediakan beberapa sumber file.
Browser akan memilih sumber pertama yang dapat didukungnya.

<audio controls>
  <source src="audio.ogg" type="audio/ogg">
  <source src="audio.wav" type="audio/wav">
  <source src="audio.mp3" type="audio/mpeg">
</audio>

Atribut yang dipelajari pada audio juga dapat digunakan pada video,
seperti loop, controls, dan muted.

Atribut poster

Atribut poster digunakan pada video untuk menentukan gambar yang
ditampilkan sebelum video diputar atau ketika video belum menampilkan
frame.

<video
  src="video.mp4"
  controls
  poster="thumbnail.jpg"
></video>

9. Jenis Atribut Target

Atribut target pada elemen a menentukan konteks tempat URL akan
dibuka.

Nilai yang umum:

Nilai                               Fungsi

_self                             Membuka tautan pada konteks saat
ini. Ini adalah nilai default.

_blank                            Membuka tautan pada konteks
browsing baru, biasanya tab baru.

_parent                           Membuka tautan pada konteks induk.
Berguna pada penggunaan iframe.

_self

<a href="https://freecodecamp.org" target="_self">
  Visit freeCodeCamp
</a>

_blank

<a href="https://freecodecamp.org" target="_blank">
  Visit freeCodeCamp
</a>

_parent

<a href="https://freecodecamp.org" target="_parent">
  Visit freeCodeCamp
</a>

_top

<a href="https://freecodecamp.org" target="_top">
  Visit freeCodeCamp
</a>

Materi juga menyebut _unfencedTop sebagai nilai lain yang digunakan
untuk eksperimen FencedFrame API.

10. Jalur Absolut vs. Relatif

Definisi Path

Path adalah string yang menunjukkan lokasi file atau direktori dalam
sistem file.

Dalam pengembangan web, path digunakan untuk menghubungkan sumber daya
seperti:

Gambar

Stylesheet

JavaScript

Halaman web

File lainnya

Sintaks Path

Beberapa sintaks penting:

/ → pemisah path.

. → direktori saat ini.

.. → direktori induk.

Contoh:

public/index.html
./favicon.ico
../src/index.css

Jalur Absolut

Jalur absolut merupakan rute lengkap menuju sebuah sumber daya dalam
sistem file. Jalur ini dimulai dari direktori root dan mencakup
direktori hingga nama file.

Absolute URL

Absolute URL mencakup informasi lengkap seperti protokol dan domain.

Contoh:

https://www.freecodecamp.org

Relative Path

Relative path menentukan lokasi file berdasarkan posisi file saat ini.

Relative path tidak membutuhkan protokol atau nama domain sehingga cocok
untuk menghubungkan sumber daya dalam website yang sama.

Contoh:

<p>
  Read more on the
  <a href="about.html">About Page</a>
</p>

Jika contact.html dan about.html berada di folder yang sama,
href="about.html" merupakan relative path.

11. Link States

CSS menyediakan beberapa state untuk elemen tautan.

:link

State default untuk tautan yang belum dikunjungi.

a:link {
  /* style */
}

:visited

Digunakan ketika pengguna sudah mengunjungi halaman yang ditautkan.

a:visited {
  /* style */
}

:hover

Aktif ketika kursor berada di atas tautan.

a:hover {
  /* style */
}

:focus

Aktif ketika tautan sedang mendapatkan fokus, misalnya melalui keyboard.

a:focus {
  /* style */
}

:active

Aktif ketika tautan sedang diaktifkan oleh pengguna, misalnya saat
proses klik.

a:active {
  /* style */
}

Ringkasan

Materi ini mencakup dasar-dasar HTML yang penting untuk membangun
halaman web, mulai dari:

Struktur dan elemen HTML.

Atribut dan atribut boolean.

Heading, paragraf, gambar, tautan, list, dan elemen semantik.

id dan class.

Entitas HTML.

link dan script.

HTML boilerplate dan UTF-8.

SEO dan Open Graph.

iframe, gambar, SVG, audio, dan video.

Atribut media seperti controls, autoplay, loop, muted, dan
poster.

target pada tautan.

Absolute URL dan relative path.

Link states pada CSS.

Dokumentasi ini dapat digunakan sebagai catatan referensi saat
mengerjakan latihan HTML dan project web.