---
title: "Modules Nodejs - ECMAScript Module"
author: "dhymas"
date: 2021-08-13T16:00:44+07:00
draft: true
tags: ["nodejs", "javascript", "modules", "import", "export"]
categories: ["NodeJS"]
---

Untuk penggunaan _module_ pada postingan sebelumnya, sebenarnya tidak disarankan, karena merupakan default _syntax_ untuk NodeJS yang sudah jarang dipakai dan termasuk cara dasar.

Agar _JavaScript_ benar-benar universal di segala _environtment_, untuk itu diperlukan cara yang lebih futuristik.

Untuk itu, hadirlah ES _module_ atau ECMAScript _module_.

Nah, pada postingan kali ini kita akan membahas tentang ES _module_ tersebut.

Sebelum memulai, hal yang harus kita lakukan adalah memberi tahu kepada NodeJS, berapa versi _module_ yang kita inginkan.

Ada beberapa cara yang dapat kita lakukan.

## Ekstensi `.mjs`

`.mjs` atau juga _module_ JS merupakan sebuah ekstensi khusus yang digunakan untuk aplikasi NodeJS.

Dengan menggunakan ekstensi `.mjs`, membuat Node tahu bahwa kita sedang menggunakan ES _module_ di dalam file ini, dibandingkan dengan `.js`.

_Apa ni, `.js` aja pusing, nambah lagi `.mjs`!_

Tenang, kalian masih tetap bisa menggunakan ekstensi `.js`, kok.

Kalian bisa melakukan _setting_ di file `package.json` dengan menambahkan `"type": "module"` yang mana masih menbolehkan kalian menggunakan ekstensi `.js` .

Namun hadirnya ekstensi `.mjs` merupakan cara mudah yang diberikan agar pengerjaan aplikasi yang menggunakan NodeJS tidak membingungkan diri kita dan lebih simpel.
