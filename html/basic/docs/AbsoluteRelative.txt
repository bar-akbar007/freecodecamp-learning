Apa Perbedaan Antara Jalan Absolut dan Relatif?
Jalur adalah string yang menentukan lokasi file atau direktori dalam sistem file. Dalam pengembangan web, jalur memungkinkan pengembang menautkan ke sumber daya seperti gambar, stylesheet, skrip, dan halaman web lainnya. Ada jalur absolut dan relatif - keduanya penting ketika menentukan lokasi file dalam sistem file. Mari kita lihat keduanya sehingga Anda dapat memutuskan mana yang akan digunakan dan kapan.

Absolute Paths
Jalur absolut adalah tautan lengkap ke sumber daya. Ini dimulai dari direktori root, mencakup setiap direktori lain, dan akhirnya nama file dan ekstensi. "Direktori root" mengacu pada direktori atau folder tingkat atas dalam hierarki.

Jika Anda menautkan ke sumber daya di mesin lokal Anda, gunakan jalur absolut, yang mencakup lokasi direktori lengkap file. Berikut cara menautkan ke about.html file dengan path absolut:

<p>
  Read more on the
  <a
    href="/Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/about.html"
    >About Page</a
    >
</p>
Sepertinya ini karena kita memulai dari root dan masuk ke folder bernama Users, kemudian ke dalam folder yang disebut user, kemudian ke dalam folder yang disebut Desktop, kemudian ke dalam folder yang disebut fCC, kemudian ke dalam folder yang disebut script-code, kemudian ke dalam folder yang disebut absolute-vs-relative-paths, kemudian ke dalam folder yang disebut pages untuk akhirnya mendapatkan about.html file.

Absolut URL
URL absolut adalah alamat lengkap yang digunakan untuk mengakses sumber daya. Ini termasuk protokol (yang bisa http, https, atau file), dan nama domain jika sumber daya ada di web. Berikut adalah contoh URL absolut yang tertaut ke logo freeCodeCamp:

<a href="https://design-style-guide.freecodecamp.org/img/fcc_secondary_small.svg">
  View fCC Logo
</a>
Dalam contoh ini, protokolnya adalah https, nama domain adalah design-style-guide.freecodecamp.org, dan nama filenya adalah fcc_secondary_small.svg.

Inilah tampilan URL absolut di bilah alamat browser:

file:///Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/about.html
URL tersebut meliputi protokol, file://. Ini juga termasuk jalur, yang terlihat seperti ini: /Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/, dan mewakili rangkaian folder yang mengarah ke file. Dan terakhir, ini juga mencakup about.html, yang merupakan nama file dan ekstensi.

Jalur absolut menunjukkan lokasi lengkap file dalam sistem file dan biasanya digunakan untuk sumber daya pada mesin lokal. URL absolut mencakup informasi akses - seperti protokol dan, untuk sumber daya web, nama domain - yang memberi tahu browser bagaimana dan di mana mengambil sumber daya tersebut.

Relative Paths
Sekarang, mari kita lihat jalur relatifnya. Jalur relatif menentukan lokasi file relatif terhadap direktori file saat ini. Ini tidak menyertakan protokol atau nama domain, sehingga lebih pendek dan fleksibel untuk tautan internal dalam situs web yang sama. Berikut contoh link ke about.html halaman dari contact.html halaman, keduanya berada dalam folder yang sama:

<p>
  Read more on the
  <a href="about.html">About Page</a>
</p>
Jadi bayangkan Anda berada di contact.html halaman, dan karena about.html halaman berada di tempat yang sama, Anda cukup mendapatkan nama file. Ini adalah contoh penggunaan relative file path.

Kapan Menggunakan Jalur Absolut, URL Absolut, dan Jalur Relatif
Jadi, mana yang harus Anda gunakan dan kapan: jalur absolut, URL absolut, atau jalur relatif? Berikut adalah aturan yang harus Anda ikuti:

Gunakan jalur absolut ketika Anda ingin mereferensikan sumber daya dari lokasi tetap, seperti dari akar situs Anda atau direktori yang dikenal di mesin lokal Anda.

Gunakan URL absolut saat menautkan ke sumber daya yang dihosting di situs web eksternal.

Gunakan jalur relatif saat menautkan ke sumber daya dalam situs web yang sama.

Gunakan jalur relatif jika Anda ingin menjaga kode Anda lebih bersih dan lebih mudah dipelihara selama pengembangan.

Gunakan jalur relatif selama pengujian lokal untuk memastikan tautan berfungsi tanpa koneksi internet.

