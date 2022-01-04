---
title: "Global Async"
author: "dhymas"
date: 2022-01-04T20:01:06+07:00
draft: false
tags: ["nodejs", "javascript", "modules", "async"]
categories: ["NodeJS"]
---

Pada JavaSript biasanya kita menggunakan `async await` kita perlu membuat _function_ yang ditandai  sebagai `async`.

Nah, pada saat menggunakan _module_ secara _default_ kita sudah menggunakan `async`, untuk itu kita sudah bisa menggunakan `async` tanpa harus menggunakan _keyword_ `async`.

Mari kita coba dengan contoh berikut:

Buatlah sebuah file `async.js`

```javascript
function contohPromise(){
	return Promise.resolve('hello')
}
```

Karena kode di atas merupakan _promise_, jadi kita bisa menggunakan `await` di baris selanjutnya;

```javascript
const hallo = await contohPromise()
console.info(hallo)
```

Sekarang coba _run_ kode di atas, maka akan menghasilkan _output_ sebagai berikut:

{{< figure src="/img/global-async/error1.png" class="img-fluid" >}}

Jika kita tetap menginginkan untuk membuat file dengan tipe `.js` maka kita harus membuat sebuah fungsi dengan tipe `async`, seperti sebagai berikut:

```javascript
async function run() {
	const hallo = await contohPromise()
	console.info(hallo)
}
```

Lalu jalan tambahkan baris baru untuk memanggil fungsi `run()` di atas.

```javascript
run()
```

Dan ketika kalian jalankan maka akan nampak _output_ sebagai berikut:

{{< figure src="/img/global-async/hello1.jpg" class="img-fluid" >}}

Sekarang, mari kita coba menggunakan `.mjs` untuk menggunakan fungsi `async` secara default.

Buat file baru bernama `async.mjs` dan buat kode seperti yang sebelumnya:

```javascript
function contohPromise(){
	return Promise.resolve('hello')
}

const hallo = await contohPromise()
console.info(hallo)
```

Maka, ketika kita jalankan, maka akan menghasilkan _output_ sebagai berikut:

{{< figure src="/img/global-async/async.jpg" class="img-fluid" >}}


Jadi, dapat disimpulkan, bahwa dengan menggunakan file yang memiliki ekstensi `.mjs` secara  _default_ sudah merupakan `async` _function_, sehingga sudah dapat menggunakan _keyword_ `await` pada file tersebut.
