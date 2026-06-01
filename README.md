# Proses Pembelajaran **HTML**

Halo ...

## HTML (HyperText Markup Language): Struktur dan Semantik

Apa itu HTML? Apakah HTML adalah bahasa pemrograman? Jelas bukan ya! HTML bukanlah bahasa pemrograman; ini adalah bahasa *markup*. Kalau di analogikan HTML adalah fondasi, tiang, dinding beton, dan struktur dasar dari rumah. HTML mendefinisikan secara mutlak "apa" yang ada di dalam bangunan tersebut (misalnya: ini adalah pintu, ini adalah jendela, ini adalah lantai).

**Konsep Mendalam & Standar Industri**: Aku sebagai pemula, berasumsi bahwa tugas HTML hanya untuk memunculkan teks atau gambar ke layar. Padahal di industri profesional, HTML digunakan untuk memberikan **makna** pada konten. Orang-orang menyebut praktik ini sebagai Semantic HTML.

Mengapa pendekatan semantik ini wajib dilakukan? 

- **Aksesibilitas (Accessibility / a11y)**: Bayangkan jika seorang user yang memiliki masalah penglihatan (tunanetra) yang sedang mengakses internet dan menggunakan fitur perangkat lunak yaitu *screen reader*(pembaca layar). Screen reader tidak melihat desain yang Kita buat; ia hanya membaca struktur HTML. Jika Kita membuat membuat sebuah elemen yang berfungsi sebagai tombol navigasi tetapi menggunakan tag HTML `<div>`, Screen reader tidak akan tahu bahwa itu bisa diklik. Situs akan menjadi cacat secara aksesibilitas.
- **SEO (Search Engine Optimization)**: Sistem Searching seperti Google mengerahkan robot yang buta warna dan tidak peduli dengan seberapa indah design sistus. Mereka membaca struktur HTML untuk memahami hierarki informasi (yang mana judul utama, mana artikel, mana bagian bawah situs). Struktur HTML yang buruk memastikan situs Anda akan tenggelam di halaman terakhir hasil pencarian.

- [x] Introduction to HTML

## Penjelasan Istilah Dalam HTML

Pada HTML terdapat beberapa istilah seperti TAG dan Attributes, Case Insensitivity, Entities, Comments, dan Whitespaces.

### Tags dan Attributes

<details>
  <summary>Penjelasan Lengkap...</summary>
 
  Dalam HTML, **Tag** adalah instruksi atau perintah kepada web browser mengenai jenis konten apa yang ingin di tampilkan. Tag dibungkus oleh tanda kurung siku (`<` dan `>`). Mayoritas tag berpasangan: ada **Opening Tag** (tag pembuka) dan **Closing Tag** (tag penutup yang ditandai dengan garis miring `/`). 

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

  Bahasa HTML bersifat case-insensitive, Artinya, web browser tidak peduli apakah Kita menulis kode dengan huruf besar atau huruf kecil.

  ![case-insensitive](./picture/case-insensitive.svg)

  **Standar Industri**:
  Meskipun web browser memaafkan penggunaan huruf besar, standar industri yang bersih dan profesional mewajibkan Kita menulis semua tag dan atribut menggunakan huruf kecil (lowercase). Menulis dengan huruf besar dianggap tidak rapi, kuno, dan mempersulit proses pembacaan kode saat bekerja dalam tim besar.

</details>

### HTML Entities

<details>
  <summary>Penjelasan Lengkap...</summary>

  Ada beberapa karakter khusus yang tidak bisa di ketik langsung di dalam HTML karena karakter tersebut sudah dipesan oleh sistem web browser itu sendiri. Karakter yang paling sensitif adalah tanda kurang dari (`<`) dan lebih dari (`>`).

  Jika Kita menulis teks seperti ini di HTML:
  > Jika nilai X < Y maka...

  Web browser akan bingung dan mengira `<` Y adalah awal dari sebuah tag HTML baru yang rusak.

  Untuk mengatasi ini, kita menggunakan HTML Entities, yaitu kode khusus yang diawali dengan simbol ampersand (`&`) dan diakhiri dengan titik koma (`;`).

  | Syntax      | Description |
  | ----------- | ----------- |
  | Header      | Title       |
  | Paragraph   | Text        |

</details>

## Progress Belajar
[![roadmap.sh](https://roadmap.sh/card/wide/6a0b4fabfc9a13bb9bf0b95f?variant=dark)](https://roadmap.sh)