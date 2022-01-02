---
title: "Global NodeJS"
author: "dhymas"
date: 2021-08-07T12:11:46+07:00
draft: false
tags: ["nodejs", "javascript", "global", "object"]
categories: ["nodeJS"]
---

# <center> Apa itu Global pada NodeJS? <center>

Global merupakan _object_ yang terdapat pada NodeJS.

_Global object_ dapat digunakan secara global pada aplikasi dan pada semua _module_.

Tidak perlu melakukan _include_ pada aplikasi lagi, kalian tinggal pakai saja _global object_ ini.

**Umum**

Berikut list umum yang diberikan oleh objek global pada NodeJS:

1. `global` : Dimana dapat digunakan sama halnya seperti `window` pada _console_ browser.
   Coba kembali pada file `index.js` yang telah kita buat kemarin...
   Lalu buat `console.log(global)`.
   Kemudian buka terminal pada lokasi anda menyimpan file `index.js` tersebut, dan ketikkan `node index.js`.
   Maka kalian akan mendapatkan _output_ seperti ini:
   {{< figure src="/img/global-nodejs/global.png" class="img-fluid" >}}

2. `__dirname` : Merupakan _value_ `String` global yang menunjukkan nama direktori dari file yang digunakan.
   Jika kalian ingin mengetahui nya coba kembali pada file `index.js`.
   Lalu buat `console.log(__dirname)`.
   Kemudian buka terminal pada lokasi anda menyimpan file `index.js` tersebut, dan ketikkan `node index.js`.
   Maka kalian akan mendapatkan _output_ seperti ini:
   {{< figure src="/img/global-nodejs/__dirname.png" class="img-fluid" >}}
3. `__filename` : Konsep yang sama seperti `__dirname`, namun lebih menunjukkan value `String` dari nama filenya.
   Jika kalian ingin mengetahui nya coba kembali pada file `index.js`.
   Lalu buat `console.log(__filename)`.
   Kemudian buka terminal pada lokasi anda menyimpan file `index.js` tersebut, dan ketikkan `node index.js`.
   Maka kalian akan mendapatkan _output_ seperti ini:
   {{< figure src="/img/global-nodejs/__filename.png" class="img-fluid" >}}
4. `process` : Objek yang berisi semua konteks yang kita butuhkan tentang program yang sedang dijalankan. Mulai dari `env vars`, hingga mesin yang kita pakai.
   Jika kalian ingin mengetahui nya coba kembali pada file `index.js`.
   Lalu buat `console.log(process)`.
   Kemudian buka terminal pada lokasi anda menyimpan file `index.js` tersebut, dan ketikkan `node index.js`.
   Maka kalian akan mendapatkan _output_ seperti ini:
   {{< figure src="/img/global-nodejs/process.png" class="img-fluid" >}}
5. `exports`, `module`, dan `require` : Berfungsi untuk membuat dan mengekspor _module_ melalui aplikasi kita. (Cara _module_ lama).

**Tidak umum (Namun perlu diketahui)**

Penggunaan _global object_ bergantung pada aplikasi yang akan kita buat. Dan macam-macam _global_ berbeda-beda tergantung versi dari NodeJS kita. Kalian bisa cek dokumentasi lengkapnya [disini](https://nodejs.org/api/globals.html).

...

Oke segitu dulu, hehe.. Lanjut lagi next...
