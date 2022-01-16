---
title: "Standard Library - OS"
author: "dhymas"
date: 2022-01-16T15:31:27+07:00
draft: false
tags: ["nodejs", "javascript", "library"]
categories: ["NodeJS"]
---


**Apa itu Standard Library?**

Seperti namanya, standard library merupakan library yang secara default disediakan oleh nodejs.

Kali ini, kita akan membahas sebuah standard library dari nodejs yaitu OS.

OS dapat digunakan untuk membantu kita mendapatkan informasi mengenai sistem operasi yang digunakan.

Beberapa contohnya sebagai berikut:

- `os.arch()` : digunakan untuk melihat arsitektur dari sistem operasi yang digunakan. 
- `os.cpus()` : digunakan untuk mengetahui detail CPU yang kita gunakan.
- `os.freemem()` : atau juga _free memory_, untuk mengetahui berapa besar memori yang tidak terpakai saat ini.
- `os.homedir()` : untuk mengetahui lokasi direktori _home_ user.
- `os.hostname()` : untuk mengetahui nama hostname.
- dan masih banyak lagi.

Untuk lebih detail, kalian bisa membaca di dokumentasi-nya langsung di [sini](https://nodejs.org/api/os.html).
Pada dokumentasi tersebut terdapat banyak detail penjelasan pemakaiannya, sampai apa saja yang di _return_ ketika kita memakai-nya.

Baik, sekarang mari kita coba beberapa dari contoh library OS ini.

Buatlah sebuah file baru `os.mjs`.

Kemudian mari lakukan _import_ untuk dapat menggunakan library OS ini.

```javascript
import os from 'os'
```

Setelah berhasil melakukan import, sekarang coba gunakan beberapa perintah yang tersedia di dokumentasi-nya. Kalian bisa melakukan-nya dengan menggunakan `console.info` misalnya, seperti sebagai berikut:

```javascript
console.info(os.platform())
console.info(os.arch())
console.info(os.freemem())
console.info(os.totalmem())
console.info(os.homedir())
console.info(os.hostname())
```

Sekarang kalian bisa coba untuk menjalankannya dengan menggunakan perintah `node os.mjs`.
Maka contoh _output_ yang terlihat pada laptop _author_ sebagai berikut:


{{< figure src="/img/os/output.jpg" class="img-fluid" >}}


Oke, mungkin kalian bisa melakukan hal lebih pada library ini. Silahkan lakukan eksplorasi lebih dalam pada dokumentasi-nya untuk penggunaan lebih lanjut.
