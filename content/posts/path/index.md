---
title: "Standard Library - Path"
author: "dhymas"
date: 2022-01-16T17:53:30+07:00
draft: false
tags: ["nodejs", "library", "path"]
categories: ["NodeJS"]
---

Setelah OS, ada lagi standard library yang dapat kita gunakan untuk keperluan kita.

Kali ini kita akan membahas mengenai Path.

Path merupakan sebuah standard library nodejs yang bisa digunakan untuk bekerja dengan lokasi file dan direktori/folder.

Perlu digarisbawahi bahwa kita library ini bekerja dengan lokasi file, bukan file nya.

Beberapa contoh penggunaan _function_ sebagai berikut:

- `path.basename(path([, ext]))` : digunakan ketika ingin mengetahui basename dari lokasi file kita.
- `path.delimiter()` : dikarenakan delimiter tiap OS berbeda beda, sehingga memungkinkan untuk menetukan nya dengan fungsi ini.
- `path.dirname()` : digunakan untuk mendapatkan nama direktori.
- `path.extname()` : digunakan untuk mendapatkan ekstensi dari file tersebut.
- dan lain-lain.

Untuk lebih detail, kalian bisa membaca di dokumentasi-nya langsung di [sini](https://nodejs.org/api/path.html). Pada dokumentasi tersebut terdapat banyak detail penjelasan pemakaiannya, sampai apa saja yang di _return_ ketika kita memakai-nya.

Mari kita buat sebuah file `path.mjs`, lalu seperti biasa mari kita import path dari library yang seperti sebagai berikut: 

```javascript
import path from 'os'
```

Sebelumnya mari kita buat sebuah _variable_ `file`, sebagai direktori dari file kita. Namun file dari direktori ini tidak harus ada, karena ini hanya sebuah _String_ dari lokasi file.

```javascript
const file = '/home/user/contoh.txt'
```

Baiklah selanjutnya sekarang coba beberapa contoh pada dokumentasi, seperti sebagai berikut:

```javascript
console.info(path.dirname(file))
console.info(path.basename(file))
console.info(path.extname(file))
```

Nah ketika kita menjalankan kode di atas dengan `node path.mjs` maka akan menghasilkan _output_ sebagai berikut:

{{< figure src="/img/path/output.jpg" class="img-fluid" >}}

Dari output di atas dapat kita lihat bahwa ketika kita menggunakan `path.dirname()` akan mengeluarkan _output_ berupa _String_ lokasi file yaitu `/home/user`.

Dan kemudian ketika ingin mengetahui nama dari file dapat menggunakan fungsi _basename_, dan juga mampu menyediakan informasi dari ekstensi file yang tersimpan pada variabel `file` dengan fungsi `extname`.

Library ini berguna untuk mengekstrak informasi dari lokasi file, bukan untuk memanipulasi file, seperti membuat file, atau memasukkan data ke file.

Jika ingin seperti itu kita harus menggunakan _library file system_ pada postingan selanjutnya.
