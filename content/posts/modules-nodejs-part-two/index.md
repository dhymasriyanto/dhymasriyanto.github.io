---
title: "Modules Nodejs - ECMAScript Module"
author: "dhymas"
date: 2022-01-03T00:00:44+07:00
draft: true
tags: ["nodejs", "javascript", "modules", "import", "export"]
categories: ["NodeJS"]
---

Untuk penggunaan _module_ pada postingan sebelumnya, sebenarnya tidak disarankan, karena merupakan default _syntax_ untuk NodeJS yang sudah jarang dipakai dan termasuk cara dasar.

Agar _JavaScript_ benar-benar universal di segala _environment_, untuk itu diperlukan cara yang lebih futuristik.

Untuk itu, hadirlah ES _module_ atau ECMAScript _module_.

Nah, pada postingan kali ini kita akan membahas tentang ES _module_ tersebut.

<!--Sebelum memulai, hal yang harus kita lakukan adalah memberi tahu kepada NodeJS, berapa versi _module_ yang kita inginkan.-->

<!--Ada beberapa cara yang dapat kita lakukan.-->

## Ekstensi `.mjs`

`.mjs` atau juga _module_ JS merupakan sebuah ekstensi khusus yang digunakan untuk aplikasi NodeJS.

Dengan menggunakan ekstensi `.mjs`, membuat Node tahu bahwa kita sedang menggunakan ES _module_ di dalam file ini, dibandingkan dengan `.js`.

_Apa ni, `.js` aja pusing, nambah lagi `.mjs`!_

Tenang, kalian masih tetap bisa menggunakan ekstensi `.js`, kok.

Kalian bisa melakukan _setting_ di file `package.json` dengan menambahkan `"type": "module"` yang mana masih membolehkan kalian menggunakan ekstensi `.js` .

Namun hadirnya ekstensi `.mjs` merupakan cara mudah yang diberikan agar pengerjaan aplikasi yang menggunakan NodeJS tidak membingungkan diri kita dan lebih simpel.

Untuk itu, kita harus membuat file yang memiliki ekstensi `.mjs` terlebih dahulu untuk dapat menggunakan ES _module_ ini.

Disini contohnya ialah file `index.mjs`. 

Pada file `index.mjs` ini, cobalah untuk membuat _code_ berikut:

``` javascript
export const action = () => {
	console.log('hello')
}
```

Sama seperti pada postingan sebelumnya, kita telah membuat fungsi yang disimpan pada konstanta `action` dan fungsi tersebut melakukan _logging_ kata `hello` pada _console_.

Namun jika diperhatikan dengan seksama, terdapat sebuah perbedaan dengan cara pada CommonJS sebelumnya.

Pada CommonJS kita diharuskan mengekspos kode dengan menggunakan `modules.export`, namun pada ES _module_ ini, kita hanya tinggal menambahkan keyword `export` di awal kode.

Lebih simpel bukan?

Baiklah, selanjutnya pada file baru, contohnya dengan nama `app.mjs` untuk melakukan _import_ dapat kita lakukan sebagai berikut:

```javascript
import {action} from './index.mjs'
```

Kali ini kita tidak perlu memakai _keyword_ `require` lagi.

Selanjutnya tambahkan di _line_ berikutnya, kode seperti berikut:

```javascript
action()
```

Sama seperti sebelumnya, kita memanggil fungsi `action()` yang telah di _export_.

Pada akhirnya file `index.mjs` akan terlihat seperti berikut:

```javascript
export const action = () => {
	console.log('hello')
}
```

Dan file `app.mjs` akan terlihat sebagai berikut:

```javascript
import {action} from './index.mjs'

action()
```


