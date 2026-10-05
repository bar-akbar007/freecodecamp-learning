# HTML `<time>` Element

## Pengertian

Elemen `<time>` digunakan untuk merepresentasikan **tanggal atau waktu tertentu** dalam HTML.

Elemen ini dapat digunakan untuk berbagai informasi, seperti:

- Waktu sebuah acara.
- Tanggal publikasi artikel.
- Jadwal atau janji temu.
- Tanggal dan waktu lainnya.

Penggunaan `<time>` membuat informasi waktu menjadi lebih **semantik**, sehingga browser dan sistem lain dapat memahami bahwa teks tersebut merupakan tanggal atau waktu.

---

## Sintaks Dasar

```html
<time>20:00</time>
```

Pada contoh tersebut, `20:00` ditampilkan sebagai teks waktu biasa.

Agar nilai waktu dapat diberikan dalam format yang dapat dibaca mesin, kita dapat menggunakan atribut `datetime`.

---

## Atribut `datetime`

Atribut `datetime` digunakan untuk memberikan nilai tanggal atau waktu dalam **format yang dapat dibaca mesin**.

Contoh:

```html
<time datetime="20:00">20:00</time>
```

Pada contoh tersebut:

- `datetime="20:00"` → nilai waktu yang dibaca mesin.
- `20:00` → teks yang ditampilkan kepada pengguna.

Teks yang ditampilkan kepada pengguna tidak harus sama dengan nilai pada `datetime`.

Contohnya:

```html
<time datetime="2026-10-05">5 Oktober 2026</time>
```

Nilai `datetime` menggunakan format yang terstruktur, sedangkan teks di dalam `<time>` dibuat agar mudah dibaca manusia.

---

## Format ISO 8601

Nilai `datetime` dapat menggunakan standar internasional **ISO 8601** untuk merepresentasikan tanggal dan waktu.

Format dasar tanggal dan waktu:

```text
YYYY-MM-DDTHH:MM:SS
```

Keterangan:

| Bagian | Keterangan |
|---|---|
| `YYYY` | Tahun |
| `MM` | Bulan |
| `DD` | Tanggal |
| `T` | Pemisah antara tanggal dan waktu |
| `HH` | Jam |
| `MM` | Menit |
| `SS` | Detik |

Contoh:

```html
<time datetime="2026-10-05T15:00:00">
  5 Oktober 2026 pukul 15:00
</time>
```

Nilai:

```text
2026-10-05T15:00:00
```

berarti:

- `2026` → tahun
- `10` → bulan Oktober
- `05` → tanggal 5
- `T` → pemisah tanggal dan waktu
- `15:00:00` → pukul 15:00:00

Huruf `T` **bukan bagian dari waktu**, tetapi berfungsi sebagai pemisah antara tanggal dan waktu.

---

## Contoh Menampilkan Waktu

```html
<time datetime="20:00">20:00</time>
```

Contoh tersebut mewakili pukul 20:00 atau 8 malam.

Contoh lainnya:

```html
<time datetime="15:00">15:00</time>
```

Mewakili pukul 15:00 atau 3 sore.

---

## Contoh Menampilkan Tanggal

```html
<time datetime="2026-10-05">5 Oktober 2026</time>
```

Pada contoh tersebut:

- `datetime` berisi tanggal dalam format `YYYY-MM-DD`.
- Teks di dalam `<time>` menggunakan format yang lebih mudah dibaca manusia.

---

## Contoh Tanggal dan Waktu

```html
<p>
  Acara dimulai pada
  <time datetime="2026-10-05T15:00:00">
    5 Oktober 2026 pukul 15:00
  </time>.
</p>
```

Dalam contoh tersebut terdapat dua representasi:

```text
Untuk mesin  → 2026-10-05T15:00:00
Untuk manusia → 5 Oktober 2026 pukul 15:00
```

Dengan cara ini, informasi tetap mudah dibaca manusia sekaligus memiliki format terstruktur untuk diproses oleh mesin.

---

## Mengapa Menggunakan `<time>`?

Tanpa `<time>`, tanggal atau waktu hanya dianggap sebagai teks biasa.

Contoh:

```html
<p>Artikel dibuat pada 5 Oktober 2026.</p>
```

Dengan menggunakan `<time>`:

```html
<p>
  Artikel dibuat pada
  <time datetime="2026-10-05">
    5 Oktober 2026
  </time>.
</p>
```

Cara kedua memberikan **makna semantik** yang lebih jelas bahwa `5 Oktober 2026` merupakan sebuah tanggal.

Informasi terstruktur pada `datetime` juga dapat membantu browser, mesin pencari, dan perangkat lunak lain dalam memahami data tanggal dan waktu.

---

## Contoh Penggunaan dalam Artikel

```html
<article>
  <h1>Belajar HTML Semantic</h1>

  <p>
    Artikel ini diterbitkan pada
    <time datetime="2026-10-05T15:00:00">
      5 Oktober 2026 pukul 15:00
    </time>.
  </p>
</article>
```

Contoh tersebut cocok digunakan pada blog atau website yang memiliki informasi waktu publikasi artikel.

---

## Contoh Lengkap

```html
<article>
  <h1>Belajar HTML Semantic</h1>

  <p>
    Artikel ini diterbitkan pada
    <time datetime="2026-10-05T15:00:00">
      5 Oktober 2026 pukul 15:00
    </time>.
  </p>

  <p>
    Pertemuan berikutnya akan dimulai pada
    <time datetime="2026-10-10T20:00:00">
      10 Oktober 2026 pukul 20:00
    </time>.
  </p>
</article>
```

---

## Ringkasan

- `<time>` digunakan untuk merepresentasikan **tanggal atau waktu**.
- `datetime` digunakan untuk memberikan **nilai tanggal atau waktu yang dapat dibaca mesin**.
- Format tanggal dan waktu dapat menggunakan standar **ISO 8601**.
- Huruf `T` digunakan sebagai **pemisah antara tanggal dan waktu**.
- `<time>` cocok digunakan untuk tanggal publikasi, jadwal acara, janji temu, dan informasi waktu lainnya.

### Pola Dasar

```html
<time datetime="nilai-tanggal-atau-waktu">
  Teks yang ditampilkan
</time>
```