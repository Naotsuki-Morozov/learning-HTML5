# Proses Pembelajaran **HTML**

Halo ...

## HTML (HyperText Markup Language): Struktur dan Semantik

Apa itu HTML? Apakah HTML adalah bahasa pemrograman? Jelas bukan ya! HTML bukanlah bahasa pemrograman; ini adalah bahasa *markup*[^1]. Kalau di analogikan HTML adalah fondasi, tiang, dinding beton, dan struktur dasar dari rumah. HTML mendefinisikan secara mutlak "apa" yang ada di dalam bangunan tersebut (misalnya: ini adalah pintu, ini adalah jendela, ini adalah lantai).

**Konsep Mendalam & Standar Industri**: Aku sebagai pemula, berasumsi bahwa tugas HTML hanya untuk memunculkan teks atau gambar ke layar. Padahal di industri profesional, HTML digunakan untuk memberikan **makna** pada konten. Orang-orang menyebut praktik ini sebagai Semantic HTML.

Mengapa pendekatan semantik ini wajib dilakukan? 

- **Aksesibilitas (Accessibility / a11y)**: Bayangkan jika seorang user yang tunanetra sedang mengakses internet dan menggunakan fitur perangkat lunak yaitu *screen reader* (pembaca layar). Screen reader tidak melihat desain yang kita buat; ia hanya membaca struktur HTML. Jika Kita membuat sebuah elemen yang berfungsi sebagai tombol navigasi tetapi menggunakan tag HTML `<div>`, Screen reader tidak akan tahu bahwa itu bisa diklik. Situs tersebut akan menjadi cacat secara aksesibilitas.
- **SEO (Search Engine Optimization)**: Sistem Searching seperti Google mengerahkan robot yang buta warna dan tidak peduli dengan seberapa indah design situs tersebut. Mereka membaca struktur HTML untuk memahami hierarki informasi (dimana judul utama, dimana artikel, dimana bagian bawah situs). Struktur HTML yang buruk memastikan situs akan tenggelam di halaman terakhir hasil pencarian.

## Penjelasan Istilah Dalam HTML

Pada HTML terdapat beberapa istilah seperti TAG dan Attributes, Case Insensitivity, Entities, Comments, dan Whitespaces.

### Tags dan Attributes

<details>
  <summary>Penjelasan Lengkap...</summary>
 
  Dalam HTML, **Tag** adalah instruksi atau perintah kepada browser mengenai jenis konten apa yang ingin di tampilkan. Tag dibungkus oleh tanda kurung siku (`<` dan `>`). Mayoritas tag berpasangan: ada **Opening Tag** (tag pembuka) dan **Closing Tag** (tag penutup, tag yang ditandai dengan garis miring `/`). 

  ![sintaks-tag](./picture/sintaks-tag.svg)

  **Attributes (Atribut)** adalah informasi tambahan yang disematkan di dalam *Opening Tag* untuk mengatur perilaku atau memberikan identitas ekstra pada tag tersebut. Atribut selalu ditulis dalam format `nama_atribut="nilai"`.

  ![sintaks-tag-attribute](./picture/sintaks-tag-attribute.svg)
  - `<a>` adalah **tag** untuk membuat tautan (hyperlink). 
  - `href` adalah **nama atribut** (singkatan dari hypertext reference). 
  - `[https://google.com](https://google.com)` adalah **nilai atribut** (tujuan tautan). 

</details>

### Case Insensitivity (Ketidakpekaan Huruf Besar/Kecil di Dalam Code)

<details>
  <summary>Penjelasan Lengkap...</summary>

  Bahasa HTML bersifat case-insensitive, Artinya, browser tidak peduli apakah Kita menulis kode dengan huruf besar atau huruf kecil.

  ![case-insensitive](./picture/case-insensitive.svg)

  **Standar Industri**:
  Meskipun browser memaafkan penggunaan huruf besar, standar industri yang bersih dan profesional mewajibkan Kita menulis semua tag dan atribut menggunakan huruf kecil (lowercase). Menulis dengan huruf besar dianggap tidak rapi, kuno, dan mempersulit proses pembacaan kode saat bekerja dalam tim besar.

</details>

### HTML Entities

<details>
  <summary>Penjelasan Lengkap...</summary>

  Ada beberapa karakter khusus yang tidak bisa di ketik langsung di dalam HTML karena karakter tersebut sudah dipesan oleh sistem browser itu sendiri. Karakter yang paling sensitif adalah tanda kurang dari (`<`) dan lebih dari (`>`).

  Jika Kita menulis teks seperti ini di HTML:
  > Jika nilai X < Y maka...

  Browser akan bingung dan mengira `<` Y adalah awal dari sebuah tag HTML baru yang rusak.

  Untuk mengatasi ini, kita menggunakan HTML Entities, yaitu kode khusus yang diawali dengan simbol ampersand (`&`) dan diakhiri dengan titik koma (`;`).

  | Karakter    | Nama Entitas                    | Kode HTML Entity |
  | ----------- | ------------------------------- | ---------------- |
  | `<`         | Less Than                       | `&lt;`           |
  | `>`         | Greater Than                    | `&gt;`           |
  | `&`         | Ampersand                       | `&amp;`          |
  | ` `         | Non-Breaking Space (Spasi)      | `&nbsp;`         |

  Jadi, penulisan yang benar dan aman di industri adalah:
  > Jika nilai X `&lt;` Y maka...

</details>

### HTML Comments

<details>
  <summary>Penjelasan Lengkap...</summary>

  Comments adalah catatan atau penjelasan yang kita tulis di dalam kode untuk diri sendiri atau programmer lain. Segala sesuatu yang berada di dalam pembungkus komentar tidak akan diproses oleh browser dan tidak akan muncul di layar pengguna.

  Sintaksis penulisan komentar di HTML adalah: `<!-- Isi komentar di sini -->`

  ![tag-comment](./picture/tag-comment.svg)

  **Standar Industri**:
  Gunakan komentar untuk menjelaskan "mengapa" kode itu ditulis seperti itu (alasan logisnya), bukan "apa" yang dilakukan kode itu.
  - Buruk: `<!-- Ini tag judul --> <h1>Artikel</h1>` (Ini membuang waktu karena tag h1 sudah jelas adalah judul).
  - Bagus: `<!-- Menggunakan h1 di sini untuk mendongkrak keyword SEO artikel utama -->`

</details>

### Whitespaces (*Ruang Kosong*)

<details>
  <summary>Penjelasan Lengkap...</summary>

  Whitespace adalah spasi, tab, atau baris baru (enter) yang kita ketik di dalam teks editor. HTML memiliki perilaku unik yang disebut **Whitespace Collapse**. Browser akan meringkas atau memotong whitespace yang berlebihan menjadi satu spasi saja.

  Jika Kita menulis seperti ini di dalam kode:

  ![whitespace](./picture/whitespace.svg)

  Browser akan mengabaikan jarak tersebut dan tetap menampilkannya di layar sebagai:

  > Halo nama saya Наоцуки.

  **Standar Industri**:
  Karena browser mengabaikan spasi berlebih, kita memanfaatkan whitespace (terutama tombol Tab atau Spasi) untuk membuat Indentasi (jarak menjorok ke dalam) agar struktur kode yang bertingkat-tingkat mudah dibaca oleh mata manusia.
</details>

## Basic Tags

HTML disusun menggunakan tag-tag dasar yang menentukan isi dan struktur HTML tersebut. Terdapat Tag !DOCTYPE, html, head, meta, dan body.

![basic-tag](./picture/basic-tag.svg)

### !DOCTYPE

<details>
  <summary>Penjelasan Lengkap...</summary>

  ![doctype-html](./picture/doctype-html.svg)

  `<!DOCTYPE html>` bukan tag HTML. Ini adalah **Deklarasi** yang bertugas memberi tahu browser: "*Situs ini ditulis menggunakan standar HTML5 terbaru.*"

  Jika melewatkan baris ini, browser akan masuk ke mode kuno yang disebut *Quirks Mode*. Browser akan mencoba menebak-nebak kode situs menggunakan standar tahun 1990-an, yang berakibat pada hancurnya tampilan CSS modern pada situs tersebut. Baris ini wajib berada di baris nomor satu, tanpa pengecualian.

</details>

### HTML Element

<details>
  <summary>Penjelasan Lengkap...</summary>

  ![html-element](./picture/html-element.svg)

  Ini adalah akar (*root element*). Semua kode HTML wajib berada di dalam pasangannya (`<html>` dan `</html>`). Atribut `lang="id"` memberi tahu sistem operasi dan mesin pencari bahwa bahasa utama situs ini adalah Bahasa Indonesia. Ini penting agar fitur penerjemah otomatis (seperti Google Translate) tahu kapan harus menawarkan terjemahan kepada pengguna luar negeri.

</details>

### Tag Head

<details>
  <summary>Penjelasan Lengkap...</summary>

  ![head-tag](./picture/head-tag.svg)

  Tag `<head>` berisi informasi-informasi di balik layar yang **tidak akan muncul di browser**. Ini adalah area konfigurasi, pengaturan SEO, pemanggilan berkas CSS, dan instruksi untuk mesin pencari.

  Di dalam `<head>`, wajib ada dua Meta Tags krusial ini:
  - `<meta charset="UTF-8">`: Mengatur sistem pengodean karakter. UTF-8 memastikan browser bisa menampilkan semua karakter huruf, simbol, hingga emoji dari berbagai bahasa di dunia dengan benar tanpa mengalami eror teks rusak (*mojibake*).
  - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Ini adalah code wajib untuk Responsive Web Design. Tanpa baris ini, situs web akan terlihat sangat kecil dan tidak bisa menyesuaikan ukuran layar saat dibuka di smartphone.
  - `<title>`: Menentukan teks yang muncul di tab browser.
</details>

### Tag Body

<details>
  <summary>Penjelasan Lengkap...</summary>

  Ini adalah area utama. Semua tag yang ditulis di dalam pasangannya (`<body>` dan `</body>`) seperti gambar, teks, tombol, dan video, adalah komponen yang **akan terlihat secara visual oleh pengguna di layar komputer mereka**.
</details>

## Textual Tag

Tag tekstual dalam HTML digunakan untuk menyusun dan memformat konten teks pada sebuah halaman web. Tag ini menentukan bagaimana teks harus muncul, apakah sebagai paragraf, judul, kata yang ditekankan, atau bagian kutipan. Tag-tag ini memberikan makna semantik pada teks, membantu browser dan mesin pencari memahami organisasi dan tujuan dari konten tersebut.

### Headings

HTML menyediakan enam tingkatan judul, mulai dari `<h1>` (tertinggi/paling penting) hingga `<h6>` (terendah).

<details>
  <summary>Penjelasan Lengkap...</summary>

  ![heading-tag](./picture/heading-tag.svg)

  **Standard Industri & Mengapa**:
  Secara visual kuno, `<hr>` menampilkan garis abu-abu horizontal di layar. Namun secara semantik modern (HTML5), `<hr>` bukan sekadar alat pembuat garis, melainkan sebuah **Thematic Break** penanda pergantian topik atau transisi cerita yang drastis dalam satu halaman. Di industri, garis visualnya sering kali dihilangkan atau diubah desainnya menggunakan CSS, namun makna pemisah topiknya tetap dipertahankan di HTML.
</details>

## Progress Belajar

- [x] Introduction
- [x] Understanding the Terms
- [x] Basic Tags
- [ ] Grouping Text
- [ ] Standard Attributes
- [ ] Lists and Types
- [ ] Table Tag
- [ ] Embedding Media
- [ ] Using Forms
- [ ] Semantic Markup

[![roadmap.sh](https://roadmap.sh/card/wide/6a0b4fabfc9a13bb9bf0b95f?variant=dark)](https://roadmap.sh)

[^1]: Bahasa markup adalah sistem kode yang digunakan untuk menstrukturkan, mengatur format, atau memberi anotasi pada sebuah dokumen. Berbeda dengan bahasa pemrograman yang melakukan logika atau perhitungan, bahasa markup hanya berfungsi sebagai "petunjuk" bagi komputer atau browser dalam menampilkan teks, gambar, atau elemen lainnya.