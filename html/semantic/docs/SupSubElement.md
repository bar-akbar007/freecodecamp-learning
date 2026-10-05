# HTML `<sup>` dan `<sub>` Element

## Pengertian

HTML menyediakan dua elemen khusus untuk menampilkan teks dengan posisi yang berbeda dari garis teks normal, yaitu:

- `<sup>` untuk **superskrip**.
- `<sub>` untuk **subskrip**.

Keduanya sering digunakan dalam penulisan matematika, rumus kimia, catatan kaki, dan kebutuhan tipografi lainnya.

---

## Elemen `<sup>`

Elemen `<sup>` digunakan untuk menampilkan teks sebagai **superskrip**.

Superskrip adalah karakter yang ditampilkan lebih kecil dan berada **di atas garis teks normal**.

Contoh:

```html
<p>2<sup>2</sup> = 4</p>
```

Hasilnya akan terlihat seperti:

```text
2² = 4
```

Pada contoh tersebut, angka `2` yang berada di dalam `<sup>` menjadi lebih kecil dan posisinya naik.

---

## Penggunaan `<sup>`

Salah satu penggunaan paling umum `<sup>` adalah untuk **eksponen dalam matematika**.

Contoh:

```html
<p>x<sup>2</sup></p>
<p>10<sup>3</sup> = 1000</p>
```

Beberapa penggunaan lainnya:

- Eksponen atau pangkat.
- Huruf superior.
- Bilangan ordinal tertentu.
- Kebutuhan tipografi lainnya.

Contoh huruf superior:

```html
<p>Dr<sup>g</sup></p>
```

Huruf yang berada dalam `<sup>` akan ditampilkan lebih tinggi dari teks normal.

---

## Jangan Gunakan `<sup>` Hanya untuk Styling

Elemen `<sup>` sebaiknya digunakan ketika posisi teks memang memiliki **makna tipografi atau semantik tertentu**, bukan sekadar untuk membuat teks terlihat lebih tinggi.

Contoh yang tidak tepat:

```html
<p>Text<sup>Style</sup></p>
```

Jika tujuan kita hanya ingin menaikkan posisi teks untuk kebutuhan visual, sebaiknya gunakan **CSS**.

Contoh:

```html
<p class="raised-text">Text</p>
```

```css
.raised-text {
  position: relative;
  top: -5px;
}
```

Jadi, `<sup>` bukan pengganti CSS untuk styling biasa.

---

## Elemen `<sub>`

Elemen `<sub>` digunakan untuk menampilkan teks sebagai **subskrip**.

Subskrip adalah karakter yang ditampilkan lebih kecil dan berada **di bawah garis teks normal**.

Contoh:

```html
<p>H<sub>2</sub>O</p>
```

Hasilnya akan terlihat seperti:

```text
H₂O
```

Angka `2` menjadi subskrip karena berada di dalam elemen `<sub>`.

---

## Penggunaan `<sub>`

Salah satu penggunaan paling umum `<sub>` adalah untuk menampilkan **rumus kimia**.

Contoh:

```html
<p>CO<sub>2</sub></p>
```

Hasilnya:

```text
CO₂
```

Contoh lainnya:

```html
<p>H<sub>2</sub>O</p>
<p>O<sub>2</sub></p>
<p>C<sub>6</sub>H<sub>12</sub>O<sub>6</sub></p>
```

Elemen `<sub>` juga dapat digunakan untuk:

- Rumus kimia.
- Subskrip pada variabel matematika.
- Catatan kaki tertentu.
- Kebutuhan tipografi lainnya.

---

## Perbedaan `<sup>` dan `<sub>`

| Elemen | Nama | Posisi | Contoh |
|---|---|---|---|
| `<sup>` | Superskrip | Di atas garis teks | `2²` |
| `<sub>` | Subskrip | Di bawah garis teks | `H₂O` |

Contoh:

```html
<p>2<sup>2</sup> = 4</p>

<p>H<sub>2</sub>O</p>
```

Hasil:

```text
2² = 4

H₂O
```

---

## Contoh Persamaan Matematika

```html
<p>x<sup>2</sup> + y<sup>2</sup> = z<sup>2</sup></p>
```

Hasil:

```text
x² + y² = z²
```

Contoh lain:

```html
<p>2<sup>3</sup> = 8</p>
<p>5<sup>2</sup> = 25</p>
```

---

## Contoh Rumus Kimia

```html
<p>H<sub>2</sub>O</p>
<p>CO<sub>2</sub></p>
<p>O<sub>2</sub></p>
```

Hasil:

```text
H₂O
CO₂
O₂
```

---

## Contoh Lengkap

```html
<section>
  <h2>Superscript</h2>

  <p>2<sup>2</sup> = 4</p>
  <p>x<sup>2</sup> + y<sup>2</sup> = z<sup>2</sup></p>

  <h2>Subscript</h2>

  <p>H<sub>2</sub>O</p>
  <p>CO<sub>2</sub></p>
  <p>C<sub>6</sub>H<sub>12</sub>O<sub>6</sub></p>
</section>
```

---

## Kapan Menggunakan `<sup>` dan `<sub>`?

Gunakan `<sup>` ketika teks memang perlu ditampilkan sebagai **superskrip**, misalnya:

```html
2<sup>2</sup>
```

Gunakan `<sub>` ketika teks memang perlu ditampilkan sebagai **subskrip**, misalnya:

```html
H<sub>2</sub>O
```

Jika hanya ingin mengubah posisi teks untuk keperluan **visual atau styling**, gunakan **CSS**, bukan `<sup>` atau `<sub>`.

---

## Ringkasan

### `<sup>`

Digunakan untuk menampilkan teks **di atas garis teks normal**.

```html
2<sup>2</sup>
```

### `<sub>`

Digunakan untuk menampilkan teks **di bawah garis teks normal**.

```html
H<sub>2</sub>O
```

### Catatan Penting

`<sup>` dan `<sub>` digunakan untuk kebutuhan **tipografi yang memiliki makna**, seperti eksponen dan rumus kimia.

Untuk menaikkan atau menurunkan teks hanya demi tampilan, gunakan **CSS**.