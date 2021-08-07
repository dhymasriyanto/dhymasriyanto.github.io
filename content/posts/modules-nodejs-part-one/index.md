---
title: "Modules NodeJS - Common Module"
date: 2021-08-07T14:32:50+07:00
draft: false
tags: ["nodejs", "javascript", "modules", "import", "export"]
categories: ["NodeJS"]
---

Karena tidak ada nya GUI, HTML, maupun CSS pada NodeJS, mengakibatkan tidak adanya _script tag_ (`<script><script>`) untuk memasukkan file JavaScript kita pada aplikasi kita.

Nah, untuk itu lah kita memerlukan _modules_ untuk saling berbagi satu JS ke JS lainnya.

# <center> Apa itu _Module_? <center>

_Module_ merupakan sebuah fungsi baik simpel maupun kompleks yang bisa dipakai ulang.

_Module_ ini diibaratkan seperti potongan Lego, yang mana bisa dibuat, diimpor juga dibagikan. Sehingga module ini tidak akan mengganggu _global scope_.

Karena pada dasar nya sama saja seperti membungkus kode JS kita ke dalam sebuah fungsi. Fungsi ini tidak akan mengganggu _scope_ lain sampai ia dipanggil.

Ada dua tipe _module_, untuk postingan kali ini kita akan membahas tentang _module_ yang pertama, yaitu _module_ umum.

## Module umum

Pada dasarnya, secara _default_ NodeJS menggunakan module JavasScript yang umum.

Bagaimana itu? Mari kita buat.

Pertama buat lah file baru bernama `index.js`.

Lalu buat kode seperti ini:

```javascript
const action = () => {
  console.log("hello");
};
```

Kita telah membuat fungsi yang disimpan ke dalam konstanta `action`. Fungsi tersebut melakukan _logging_ ke _console_ berupa kata `hello`.

Kode ini dapat dijalankan pada browser maupun Node.

Kita juga bisa membagikan fungsi `action` ini ke file JavaScript lainnya.

Namun ada sebuah perbedaaan, jika kita melakukannya di browser, file ini akan di _attach_ ke _global_ sehingga dapat diakses via `window` pada file JS lainnya.

Tetapi pada NodeJS, tidak ada `window`, tidak ada yang di _attach_ di _global_ (`window`) secara _default_. Karena seluruh file di dalam NodeJS sebenarnya di-enkapsulasi di dalam sebuah modul tersendiri, sehingga tidak terjadi kebocoran.

Yang harus kita lakukan adalah mengekspos kode kita sehingga bisa digunakan oleh file lain.

Nah untuk penggunaan modul secara umum, kita dapat menambah kode berikut di bawah kode yang telah kita tulis tadi:

```javascript
module.exports = action;
```

Kode di atas menyatakan bahwa kita telah melakukan _export_ fungsi `action`. Dimana kita memasukkan nilai ataupun fungsi `action` ke dalam `module.exports`.

Nah, kali ini kita telah berhasil membuat fungsi `action` terekspos.

Lalu selanjutnya, buat lah file baru bernama `app.js` misalnya, lalu tulis kode berikut:

```javascript
const action = require("./index");
```

Kita membuat sebuah kode _global_ bernama `action` lagi, dimana kita memasukkan file `index.js` ke dalamnya dengan menggunakan fungsi _global_ `require`.

Note:
Secara _default_ `require` membaca untuk file dengan ekstensi `.js`. Jika file yang kita butuhkan merupakan file dengan ekstensi `.js` maka kita tidak harus menuliskan parameter pada fungsi require secara lengkap beserta ekstensinya. Namun jika file yang kita butuhkan bukan merupakan file `.js` maka kita harus menambahkan ekstensi tersebut.

Selanjutnya tambahkan di _line_ berikutnya, kode seperti berikut :

```javascript
action();
```

Pada kode di atas kita memanggil fungsi `action()` yang sudah berada di dalam konstanta `action` untuk dijalankan.

Pada akhirnya file `index.js` akan terlihat seperti berikut:

```javascript
const action = () => {
  console.log("hello");
};

module.exports = action;
```

Sedangkan file `app.js` akan terlihat seperti berikut:

```javascript
const action = require("./index");

action();
```

Selanjutnya, coba jalankan `node app.js` pada terminal kita.

{{< figure src="/img/modules-nodejs/app.png" class="img-fluid" >}}

Nah, kita berhasil membuat _module_ umum...

Kalian juga bisa membungkus fungsi `action` pada file `index.js` menjadi sebuah objek. Sehingga kodenya akan terlihat seperti ini:

```javascript
const action = () => {
  console.log("hello");
};

module.exports = { action };
```

Nah, kita telah menjadikan fungsi `action` pada `index.js` sebagai objek.

Selanjutnya, untuk file `app.js` ada sedikit perubahan yang harus kita lakukan.

```javascript
const action = require(".index");

action.action();
```

Pada kode di atas, terlihat konstanta `action` telah berubah menjadi objek setelah menyimpan JS pada file `index.js`.

Untuk itu, ketika ingin memanggil fungsi `action` pada file `index.js` kita tidak bisa langsung memanggil `action()`, melainkan harus dengan `action.action()`.

Hal ini dikarenakan kita telah menjadikan fungsi `action` pada file `index.js` sebagai objek, dan kita memanggil fungsi `action` file `index.js` di dalam objek `action` pada file `app.js` tersebut.

Silahkan jalankan `node app` kembali untuk melihat _output_ fungsi `action` setelah dibungkus menjadi objek.

...

Oke segitu dulu, lanjut ke tipe module kedua di next postingan...
