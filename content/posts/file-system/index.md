---
title: "Standard Library - File System"
author: "dhymas"
date: 2022-01-17T17:13:29+07:00
draft: false
tags: ["file", "system", "nodejs", "javascript"]
categories: ["NodeJS"]
---

_File system_ merupakan _standard library_ yang bisa digunakan untuk memanipulasi _file system_.

Terdapat 3 jenis _library_ dalam _File System_, yakni:

- _Library_ yang bersifat _blocking_ atau _synchronous_
- _Library_ yang bersifat _non-blocking_ atau _asynchronous_ menggunakan _callback_
- _Library_ yang bersifat _non-blocking_ atau _asynchronous_ tapi menggunakan _promise_


Untuk dokumentasi lebih lanjut dapat di lihat [disini](https://nodejs.org/api/fs.html)

_Author_ sendiri menyarankan menggunakan _promise_, karena lebih mudah, dan juga bisa menggunakan `async await`.

Jika menggunakan _callback_, kita harus menggunakan _callback_ terus menerus, dan malah menyebabkan _callback hell_.

Sedangkan untuk _blocking_ sendiri dapat digunakan untuk pembelajaran, namun kalau bisa jangan gunakan untuk sebuah _project_, karena dia akan melakukan _blocking_ terhadap _event-loop nodejs_-nya.

Untuk penulisan fungsi pada penerapan antara _blocking_, _promise_ ataupun _callback_ dapat dilihat pada dokumentasi resmi nya.

Untuk contoh penggunaan _blocking_ dan juga _callback_ dapat dilihat sebagai berikut:

Buat sebuah file bernama `file-system.mjs` terlebih dahulu, lalu buat contoh kode di bawah ini:

```javascript
import fs from 'fs'
```

Kode di atas memungkinkan kita untuk melakukan _import_ terhadap library _File System_. Untuk library yang ini, dapat dipakai untuk _blocking_ dan juga _callback_.

Perbedaan mendasar antara _blocking_ dan juga _callback_ ialah ketika salah satu fungsi terdapat kata `Sync()` maka itu merupakan _library_ yang menggunakan tipe _blocking_, begitu pula sebaliknya.

Contoh jika kita ingin menggunakan _blocking_, maka kita dapat menggunakan kode seperti ini:

```javascript
fs.readFileSync('file-system.mjs')
```

Sedangkan ketika ingin menggunakan _callback_ maka kode di atas akan menjadi seperti ini:

```javascript
fs.readFile('file-system.mjs', (err, data) => {
  if (err) throw err;
  console.log(data.toString());
}) )
```

Pada kode di atas terlihat kita tidak menggunakan tambahan kata `Sync()` pada fungsi ketika menggunakan _callback_, namun kita harus menggunakan _callback_ di dalam parameternya.

Baiklah, selanjutnya kita akan menggunakan _library_ yang lebih _author_ rekomendasikan, yaitu _promise_

Untuk menggunakan _promise_, pada saat melakukan _import_ akan menjadi seperti berikut:

```javascript
import fs from 'fs/promises'
```

Nah ketika telah meng-import `fs/promises` maka sudah menjadi promise.

Sekarang coba tulis kode di bawah:

```javascript
const buffer = await fs.readFile('file-system.mjs')

console.info(buffer.to String())
```

Kode di atas merupakan kode yang kita tulis ketika kita menggunakan _library_ yang bersifat _promise_,  dan untuk penggunaan-nya kita bisa memakai await sebagai `key`.

Kode di atas memungkinkan kita untuk membaca isi file `file-system.mjs` itu sendiri, dan kemudian menuliskannya ke konsol dengan menggunakan `buffer` (`buffer` akan di bahas di postingan lain). 

Kemudian kita mengubah `buffer` file menjadi _String_ dengan menggunakan fungsi `.toString()`.

Jika kita _run_ kode di atas dengan `node file-system.mjs` maka akan menampilkan _output_ sebagai berikut:

{{< figure src="/img/file-system/output.jpg" class="img-fluid" >}}

Selanjutnya coba kita buat sebuah kode untuk menuliskan data ke dalam sebuah file, seperti dibawah ini:

```javascript
await fs.writeFile('tempt.txt', 'hello')
```

Jika kita jalankan kode di atas maka akan menampilkan _output_ berupa file `temp.txt` pada direktori _project_ kita. 

Baiklah, begitulah yang bisa kita lakukan dengan _standard library_ dari nodejs _file system_, kita mampu memanipulasi file, baik dari membaca, ataupun mengubah, menghapus, dan sebagainya. Kalian hanya perlu membaca dokumentasi lebih lanjut pada website resminya.

Apalagi jika kalian sudah familiar dengan perintah terminal linux, kalian akan lebih mengenal dengan mudah, karena beberapa fungsi mengambil referensi yang sama dengan perintah-perintah di linux, seperti `rmdir`, `rm`, `mkfile`, `cp`, `link`, dan lain sebagainya.
