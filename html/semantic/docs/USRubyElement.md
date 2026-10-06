# HTML `<u>`, `<s>`, dan `<ruby>` Element

HTML memiliki beberapa elemen semantik khusus untuk memberikan makna tertentu pada teks, yaitu `<u>`, `<s>`, dan `<ruby>`.

Masing-masing memiliki fungsi yang berbeda dan tidak sebaiknya digunakan hanya untuk mengubah tampilan teks.

---

## Elemen `<u>`

Elemen `<u>` digunakan untuk menandai **teks sebaris yang memiliki anotasi non-tekstual**.

Salah satu contohnya adalah menandai kata yang memiliki kesalahan ejaan.

Contoh:

```html
<p>
  This word has an <u>incorrect</u> spelling.
</p>
```

Browser biasanya memberikan gaya default berupa **garis bawah** pada teks di dalam `<u>`.

Namun, garis bawah tersebut bukan tujuan utama dari elemen `<u>`.

### `<u>` Bukan untuk Styling

Pada HTML lama, khususnya HTML4, `<u>` sering digunakan untuk memberikan gaya garis bawah pada teks.

Dalam HTML5, penggunaan tersebut tidak lagi menjadi tujuan utama `<u>`.

Jika kita hanya ingin membuat teks bergaris bawah untuk kebutuhan visual, gunakan **CSS**.

Contoh:

```html
<p class="underline">Teks ini digarisbawahi.</p>
```

```css
.underline {
  text-decoration: underline;
}
```

Jadi:

```text
Makna/Anotasi → <u>
Styling       → CSS
```

---

## Elemen `<s>`

Elemen `<s>` digunakan untuk menunjukkan bahwa **teks tersebut sudah tidak lagi akurat, relevan, atau berlaku**.

Browser biasanya menampilkan teks di dalam `<s>` dengan garis coret.

Contoh:

```html
<p>
  Harga lama: <s>Rp100.000</s>
</p>

<p>
  Harga baru: Rp75.000
</p>
```

Hasilnya menunjukkan bahwa `Rp100.000` merupakan informasi lama yang sudah tidak berlaku.

### Contoh Pembatalan Acara

```html
<p>
  <s>Workshop dimulai pukul 09:00.</s>
</p>

<p>
  Workshop dibatalkan karena kondisi cuaca.
</p>
```

Elemen `<s>` menunjukkan bahwa informasi sebelumnya sudah tidak relevan.

---

## Jangan Gunakan `<s>` untuk Konten yang Dihapus

Elemen `<s>` tidak digunakan untuk menunjukkan bahwa sebuah teks **dihapus dari dokumen**.

Untuk perubahan dokumen, gunakan elemen yang lebih tepat:

- `<del>` → menunjukkan teks yang dihapus.
- `<ins>` → menunjukkan teks yang ditambahkan.

Contoh:

```html
<p>
  Harga:
  <del>Rp100.000</del>
  <ins>Rp75.000</ins>
</p>
```

Perbedaannya:

```text
<s>   → informasi sudah tidak berlaku/relevan
<del> → teks dihapus dari dokumen
<ins> → teks ditambahkan ke dokumen
```

---

## Elemen `<ruby>`

Elemen `<ruby>` digunakan untuk menampilkan **anotasi kecil yang berkaitan dengan teks utama**.

Penggunaan yang paling umum adalah untuk menunjukkan **pengucapan karakter Asia Timur**, seperti bahasa Jepang dan Mandarin.

Contoh sederhana:

```html
<ruby>
  漢
  <rt>かん</rt>
</ruby>
```

Pada contoh tersebut:

- `漢` → karakter utama.
- `<rt>` → anotasi atau pengucapan karakter tersebut.

Browser akan menampilkan anotasi kecil di sekitar karakter utama.

---

## Elemen `<rt>`

Elemen `<rt>` berarti **Ruby Text**.

Elemen ini digunakan untuk menentukan **teks anotasi** yang ditampilkan bersama elemen `<ruby>`.

Contoh:

```html
<ruby>
  日本
  <rt>にほん</rt>
</ruby>
```

`日本` merupakan teks utama, sedangkan `にほん` merupakan anotasi pengucapannya.

---

## Elemen `<rp>`

Elemen `<rp>` berarti **Ruby Parenthesis**.

Elemen ini menyediakan teks cadangan berupa tanda kurung untuk browser yang tidak mendukung tampilan anotasi ruby dengan baik.

Contoh:

```html
<ruby>
  漢字
  <rp>(</rp>
  <rt>かんじ</rt>
  <rp>)</rp>
</ruby>
```

Browser yang mendukung ruby dapat menampilkan anotasi dengan format ruby.

Browser yang tidak mendukungnya dapat menggunakan tanda kurung sebagai fallback.

---

## Struktur `<ruby>`

Struktur umum ruby dapat ditulis seperti ini:

```html
<ruby>
  Teks Utama
  <rp>(</rp>
  <rt>Anotasi</rt>
  <rp>)</rp>
</ruby>
```

Keterangan:

| Elemen | Fungsi |
|---|---|
| `<ruby>` | Wadah untuk teks utama dan anotasinya |
| `<rt>` | Menentukan teks anotasi ruby |
| `<rp>` | Fallback berupa tanda kurung untuk browser yang tidak mendukung ruby |

---

## Contoh Bahasa Jepang

Berikut contoh penggunaan `<ruby>` untuk memberikan cara baca kanji:

```html
<ruby>
  学校
  <rt>がっこう</rt>
</ruby>
```

Contoh lain:

```html
<p>
  <ruby>
    日本語
    <rt>にほんご</rt>
  </ruby>
</p>
```

Ruby sangat berguna pada materi pembelajaran bahasa yang menggunakan karakter tertentu karena pembaca dapat melihat karakter utama sekaligus informasi pengucapannya.

---

## Perbedaan `<u>`, `<s>`, dan `<ruby>`

| Elemen | Fungsi utama | Contoh |
|---|---|---|
| `<u>` | Menandai anotasi non-tekstual pada teks | Kesalahan ejaan |
| `<s>` | Menandai informasi yang sudah tidak akurat atau relevan | Harga lama |
| `<ruby>` | Menampilkan anotasi pada teks utama | Pengucapan Kanji |

Elemen pendukung `<ruby>`:

| Elemen | Fungsi |
|---|---|
| `<rt>` | Teks anotasi ruby |
| `<rp>` | Fallback tanda kurung |

---

## Contoh Lengkap

```html
<section>
  <h2>Elemen U</h2>

  <p>
    There is an <u>incorrect</u> spelling here.
  </p>

  <h2>Elemen S</h2>

  <p>
    Harga lama:
    <s>Rp100.000</s>
  </p>

  <p>
    Harga sekarang:
    Rp75.000
  </p>

  <h2>Elemen Ruby</h2>

  <p>
    <ruby>
      日本語
      <rp>(</rp>
      <rt>にほんご</rt>
      <rp>)</rp>
    </ruby>
  </p>
</section>
```

---

## Ringkasan

### `<u>`

Digunakan untuk menandai **teks sebaris yang menerapkan anotasi non-tekstual**.

```html
<u>incorrect</u>
```

Jangan menggunakan `<u>` hanya untuk membuat teks bergaris bawah. Gunakan CSS untuk kebutuhan styling.

### `<s>`

Digunakan untuk menunjukkan bahwa **informasi sudah tidak akurat atau tidak relevan**.

```html
<s>Harga lama</s>
```

Untuk teks yang benar-benar dihapus dari dokumen, gunakan `<del>`.

### `<ruby>`

Digunakan untuk menampilkan **anotasi pada teks utama**, terutama untuk menunjukkan pengucapan karakter Asia Timur.

```html
<ruby>
  日本語
  <rt>にほんご</rt>
</ruby>
```

### `<rt>`

Berisi teks anotasi atau pengucapan untuk elemen `<ruby>`.

### `<rp>`

Digunakan sebagai **fallback** untuk browser yang tidak mendukung tampilan ruby.