Apa Jenis Atribut Target yang Berbeda, dan Bagaimana Cara Kerjanya?
Anda mungkin telah melihat target atribut pada elemen jangkar, atau tautan. Atribut penting ini memberi tahu browser tempat membuka URL untuk elemen jangkar.

Aktifkan editor interaktif, klik tautannya dan Anda akan diarahkan ke beranda freeCodeCamp di tab browser baru.

Ada empat kemungkinan nilai penting untuk atribut ini. Perhatikan bahwa setiap nilai didahului oleh garis bawah.

Nilai pertama adalah _self, yang merupakan nilai default. Ini membuka tautan dalam konteks penjelajahan saat ini. Dalam kebanyakan kasus, ini akan menjadi tab atau jendela saat ini.

Nilai kedua adalah _blank, yang membuka link dalam konteks browsing baru. Biasanya, ini akan terbuka di tab baru. Namun beberapa pengguna mungkin mengonfigurasi browser mereka untuk membuka jendela baru.

Nilai ketiga adalah _parent, yang membuka link di induk dari konteks saat ini. Misalnya, jika situs web Anda memiliki iframe, a _parent nilai dalam hal itu iframe akan terbuka di tab/jendela situs web Anda, bukan di bingkai tertanam.

Nilai keempat adalah _top, yang membuka tautan dalam konteks penelusuran paling atas - pikirkan "orang tua dari orang tua". Hal ini mirip dengan _parent, tetapi link akan selalu terbuka di tab/jendela browser penuh, bahkan untuk frame tertanam bersarang.

Ada nilai kelima, yang disebut _unfencedTop, yang saat ini digunakan untuk API FencedFrame eksperimental. Pada saat pelajaran ini, Anda mungkin belum memiliki alasan untuk menggunakan yang satu ini.

Memilih yang kanan target nilai untuk mengontrol di mana pengguna Anda berakhir adalah pertimbangan penting saat membuat situs web.

