---
title: "Mengeksekusi Nodejs"
date: 2021-08-07T10:54:07+07:00
draft: false
tags: ["nodejs", "javascript"]
categories: ["NodeJS"]
---

# <center> Bagaimana cara mengeksekusi NodeJS? <center>

Nah, setelah kita berhasil menginstall NodeJS berdasarkan postingan sebelumnya, kali ini kita akan mencoba mengeksekusi NodeJS, agar dapat digunakan.

## Node REPL

**Apa itu REPL?**

REPL merupakan singkatan dari _Read, Evaluate, Print, Loop_.

_Mangsudnya?_

Pada umumnya REPL itu merupakan _shell_ interaktif, yang berguna untuk membaca, mengeksekusi, mengeprint, dan loop sesuai dengan konteks runtime yang kita pilih. Ya dalam kasus kita ini contohnya Node. Yang menjadikan kita juga punya _console_ yang sama kayak di browser.

Untuk menggunakan REPL, tinggal ketik :

```shell
node
```

di _terminal_ ataupun _command prompt_ kalian.

Nah, nanti akan muncul seperti ini:

{{< figure src="/img/executing-nodejs/execute.png" class="img-fluid" >}}

Nah, itu kalian sudah masuk ke Node REPL, loh!

Nah, kalian bisa kreasikan _script_ yang telah kalian pelajari pada JavaScript di dalam REPL ini.

Contohnya coba kalian ketik seperti ini:

```javascript
const me = "Dhymas";
```

Lalu silahkan tekan Enter.

Nah, apa yang kalian lakukan sudah persis seperti pada _console tools_ pada browser kalian.

Sekarang coba ketik ini:

```javascript
me;
```

Bahkan, sebelum kalian enter, REPL dapat menentukan nilai pada konstanta `me`.

Inilah yang disebut dengan interaktif _shell_.

Selanjutnya, coba kalian ketik seperti ini:

```javascript
alert("Hallo Dunia!");
```

Dan tekan Enter.

Pasti, kalian akan mendapatkan _error_ seperti ini:

{{< figure src="/img/executing-nodejs/alert.png" class="img-fluid" >}}

**Lah Kok bisa?**

Ini terjadi karena pada dasarnya meskipun NodeJS menggunakan JavaScript sebagai bahasa pemrogramannya, tidak semua fungsi yang bisa dilakukan di dalam browser ada di NodeJS. Hal ini karena REPL pada dasarnya tidak memiliki GUI untuk menampilkan modal _alert_ tersebut

## Eksekusi melalui file

Keren juga sih REPL, tapi kalo make itu, kalian mungkin ga bisa _build_ aplikasi besar. Mungkin sih, tergantung kalian juga, wkwk :V

Nah cara yang pada umumnya dilakukan ialah kita menulis program kita pada file, dan meminta NodeJS untuk mengeksekusi nya.

**Bikin file index.js**

Pertama, coba kalian bikin file `index.js`. Dalam file itu coba kalian ketik _syntax_ sederhana dari JavaScript. Semisal `console.log('Hallo Dunia')`.

Untuk mengeksekusi file ini pada _runtime_ NodeJS, silahkan buka terminal ataupun _command prompt_ di lokasi kalian menyimpan file `index.js` tadi.

Setelah itu, untuk mengeksekusi file ini kalian bisa mengetikkan seperti ini:

```shell
node index.js
```

Done! Selamat udah bisa mengeksekusi file dengan menggunakan NodeJS!

...

Oke untuk ini segini dulu... Lanjut lagi nanti, hehe...
