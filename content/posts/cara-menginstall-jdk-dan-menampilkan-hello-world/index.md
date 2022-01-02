---
title: "Cara Menginstall JDK Dan Menampilkan Hello World"
author: "dhymas"
date: 2019-08-01T10:35:21+07:00
draft: false
tags: ["install JDK", "JAVA"]
categories: ["JAVA"]
---

**JDK** atau JAVA _Development Kit_ adalah salah satu dari tiga paket inti yang dibutuhkan pada bahasa JAVA. Dua lainnya ialah **JVM** (JAVA _Virtual Machine_) dan **JRE** (JAVA _Runtime Environment_).
Berikut perbedaan ketiganya:

- **JVM** adalah komponen dari platform JAVA yang berfungsi untuk mengeksekusi program-program

- **JRE** adalah bagian JAVA yang membuat **JVM**

- **JDK** membolehkan _developer_ untuk meng-_compile_ program JAVA, sehingga dapat di eksekusi oleh **JVM** dan **JRE**

Bagi yang baru memulai mempelajari JAVA pasti masih bingung dengan pembagian-pembagian dan istilah-istilah tersebut. Perbedaan mendasarnya ialah, **JDK** adalah _package_ untuk men-_develop_ program berbasis JAVA, yang mana membutuhkan JRE sebagai _package_ untuk menjalankan kode JAVA tersebut.

Berikut bagan bagaimana peranan **JDK**  pada JAVA:

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/jdk-01.png" class="img-fluid" >}}

----------

# <center>Menginstall JDK</center>

## Versi JDK apa yang harus di-_install_, _Thor_?

Bebas! Silahkan _download_ sesuai kebutuhan. Tapi, untuk kali ini kita akan menginstall JDK versi 8 saja untuk pertama kali belajar.

Langkah awal, silahkan kunjungi [website oracle](https://www.oracle.com/technetwork/java/javase/downloads/index.html) terlebih dahulu untuk men-_download_ JDK 8.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/web-oracle.png" class="img-fluid" >}}


JAVA saat ini sudah mengeluarkan versi JDK terbaru. Namun tidak apa-apa, JDK 8 masih _powerfull_ kok untuk belajar di awal-awal. Maka abaikan saja JDK versi terbaru tersebut, langsung saja pilih yang sudah _Author_ tandai.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/halaman-download.png" class="img-fluid" >}}

Langkah selanjutnya, untuk dapat men-_download_ JDK tersebut, anda harus menyetujui terlebih dahulu kebijakan yang di buat. Maka klik _Accept License Agreement_ untuk melanjutkan.

Setelah itu silahkan pilih file sesuai dengan sistem operasi anda. Jika menggunakan _Windows_, silahkan pilih antara kedua yang sudah _Author_ tandai sesuai dengan versi _Windows_ anda.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/halaman2.png" class="img-fluid" >}}

Selanjutnya, anda akan dibawa ke menu login untuk akun Oracle. Jika belum punya anda sebaiknya membuat akun terlebih dahulu. Ketika sudah selesai membuat akun, silahkan masuk untuk dapat men-_download_ JDK 8 tadi.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/oracle.png" class="img-fluid" >}}

Simpan ditempat yang di inginkan.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/simpan.png" class="img-fluid" >}}


Setelah selesai men-_download_, silahkan jalankan file _jdk-8u221-windows-x64.exe_ tadi.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/aplikasi.png" class="img-fluid" >}}

Klik _next_. Anda dapat mengganti lokasi penyimpanan JDK ini, namun untuk kali ini biarkan saja JDK tersimpan secara _default_ di Local Disk (C:). Klik _next_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/aplikasi2.png" class="img-fluid" >}}

Tunggu sebentar.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/tunggu.png" class="img-fluid" >}}

Selanjutnya anda dapat juga mengganti lokasi penyimpanan JRE ini, namun untuk kali ini biarkan saja JRE tersimpan secara _default_ di Local Disk (C:). Klik _next_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/jre.png" class="img-fluid" >}}

Tunggu sampai selesai meng-_install_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/installing.png" class="img-fluid" >}}

Jika sudah selesai, silahkan _close_ program.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/close.png" class="img-fluid" >}}

Nais!! Kita sudah berhasil meng-_install_ JDK pada Windows.

## Lah, terus sekarang ngapain?

 Langkah selanjutnya, kita harus menyetting PATH untuk _Environment Variable_ pada Windows.

## Apa itu PATH?

 PATH itu ialah istilah yang digunakan untuk menunjukkan alamat suatu file.

 Sebenarnya, JAVA sudah berhasil terinstall pada OS kita, tapi tidak secara otomatis ter-_setting_ PATH-nya. Untuk mengetahui hal tersebut tekan ``Windows + R`` untuk membuka kotak dialog "Run" seperti berikut :

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/run.png" class="img-fluid" >}}

Lalu ketik ``cmd`` dan tekan Enter. Maka program _Command Prompt_ akan terbuka seperti ini :

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/cmd.png" class="img-fluid" >}}

Lalu ketik ``javac`` pada _Command Prompt_ dan tekan Enter.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/javac.png" class="img-fluid" >}}

Hal diatas terjadi karena kita belum mengatur PATH pada _environment variable_. Untuk melakukan hal tersebut, kita harus pergi ke _system properties_.

Sebelum ke _system properties_ kita harus dapatkan terlebih dahulu alamat yang ingin kita tuju. Alamat ini  merupakan alamat menuju ke dalam folder JDK yang telah kita _install_.

Buka _File Explorer_. Lalu pergi ke Local Disk (C:) dan masuk ke folder _Program Files_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/c.png" class="img-fluid" >}}

Pada folder _Program Files_ masuk lagi ke dalam folder _Java_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/files.png" class="img-fluid" >}}

Di dalam folder _Java_ inilah JDK terinstall. Setelah itu masuklah ke dalam folder *jdk1.8.0_221*.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/java.png" class="img-fluid" >}}

Masuk ke dalam folder _bin_

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/jdk8.png" class="img-fluid" >}}

Di dalam folder _bin_ tersebut, klik pada _address bar_ lalu _copy_ alamat tersebut.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/bin.png" class="img-fluid" >}}


Untuk ke _system properties_, kita cukup lakukan hal yang hampir sama dengan sebelumnya.

Tekan ``Windows + R`` pada _keyboard_ lalu ketikkan ``sysdm.cpl`` dan tekan _Enter_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/sysdm.png" class="img-fluid" >}}

Lalu silahkan pilih tab _Advanced_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/system-properties.png" class="img-fluid" >}}

Lalu pilih _Environment Variables_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/advanced.png" class="img-fluid" >}}

Pilih PATH seperti pada gambar dibawah, lalu pilih _Edit_ untuk mengedit isi PATH.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/environment.png" class="img-fluid" >}}

Di sini silahkan pilih _New_ untuk membuat PATH baru.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/edit.png" class="img-fluid" >}}


Kemudian _paste_ alamat yang telah kita _copy_ tadi.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/new.png" class="img-fluid" >}}

Setelah itu klik _OK_ di semua menu sampai anda keluar.

Diatas merupakan cara mengatur PATH pada _Windows_ 10. Untuk _Windows_ 7 caranya sama, hanya berbeda pada saat masuk menu _Edit_ PATH.

Setelah anda masuk ke dalam _Edit_ PATH, maka tampilannya akan seperti ini :

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/path-windows-7.png" class="img-fluid" >}}

Jika sudah, sama seperti pada sebelumnya, kita harus _paste_ alamat yang telah kita _copy_.

Namun yang harus diperhatikan ialah sebelum kita _copy_, kita harus memberikan _separator_ untuk PATH baru. _Separator_ tersebut ialah tanda titik koma (';').

Untuk itu, letakkan titik koma (';') di ujung tulisan pada _field Edit_ PATH tersebut. Lalu silahkan _paste_ alamat yang telah tersimpan, lalu tekan OK di semua _dialog box_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/path-separate.png" class="img-fluid" >}}

Naaahhh... Akhirnya kita telah berhasil mengatur agar JDK terdapat di dalam PATH.

Tapi, untuk membuktikan hal itu, mari kita coba di _Command Prompt_. Oh iya, kita harus _close_ dulu _Command Prompt_ sebelumnya, agar reload data baru.

Kemudian buka lagi _Command Prompt_ dan coba ketikkan kembali ``javac``, jika berhasil maka tampilannya akan seperti ini :

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/success.png" class="img-fluid" >}}

Selanjutnya untuk memastikan bahwa versi JDK sudah sesuai, yakni JDK versi 8, maka ketikkan perintah ``javac -version``.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/java-version.png" class="img-fluid" >}}

Selamat, kita telah berhasil mengatur PATH pada OS kita.

----------


# <center>Membuat Hello World  Pada JAVA</center>

Akhirnya, setelah PATH untuk JDK kita telah selesai diatur, mari kita coba untuk melakukan _compile_ pada bahasa pemrograman JAVA. Seperti yang _Author_ katakan sebelumnya, bahwa JDK berfungsi untuk meng-_compile_ kode JAVA kita.

Kita akan melakukan _compile_ dengan menggunakan perintah ``javac`` tadi.

Pertama buka editor favorit kalian, bisa [Notepad++](https://notepad-plus-plus.org/download/v7.7.1.html), [Atom](https://atom.io), [Visual Studio Code](https://code.visualstudio.com/) atau bahkan Notepad biasa (yang ini untuk **PRO** :v). Disini _Author_ menggunakan Visual Studio Code.

Setelah dibuka, silahkan ketikkan _syntax_ berikut :

```java
public class HelloWorld{
    public static void main (String [] args){
        System.out.println("Hello World!");
    }
}
```

Kemudian simpan dengan nama file "HelloWorld.java" pada direktori yang anda inginkan. Pada kali ini _Author_ menyimpan file "HelloWorld.java" tersebut pada  direktori ``C:\User\Gamers\Documents``.

Nah, sekarang kita akan menampilkan hal tersebut pada _Command Prompt_.

Pertama buka _Command Prompt_ terlebih dahulu.

Perlu diketahui, bahwa secara _default_, _Command Prompt_ akan mengarahkan kita ke direktori ``C:\User\namauser``. Nah, disini kita perlu untuk mengubah direktori tersebut. Untuk melakukan hal itu, kita akan menggunakan salah satu perintah pada _Command Prompt_,  yaitu ``cd`` yang merupakan perintah untuk menuju ke direktori tertentu.

Jika kita ketikkan command ``help`` pada _Command Prompt_, maka akan tampil penjelasan semua perintah di _Command Prompt_, namun untuk saat ini yang perlu kita ketahui hanya perintah ``cd`` saja.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/help.png" class="img-fluid" >}}

Ada beberapa hal yang harus diketahui pada perintah ``cd`` ini. Yakni :


- Jika kita ingin pergi ke _Disk_ selain _Local Disk (C:)_, maka cukup ketikkan nama _Disk_-nya. Seperti jika kita ingin ke _Disk_ D:, maka ketikkan ``D:``.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/d.png" class="img-fluid" >}}

- Jika kita ketik : ``cd /``. maka akan mengarahkan kita ke direktori inti pada _Disk_ tersebut.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/root.png" class="img-fluid" >}}

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/root2.png" class="img-fluid" >}}

- Jika kita ketik : ``cd ..``, maka akan mengarahkan kita ke direktori sebelumnya.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/back.png" class="img-fluid" >}}

- Jika kita ketik : ``cd namadirektori``, maka akan mengarahkan kita ke direktori yang kita inginkan (tetapi direktori harus ada).

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/go-to.png" class="img-fluid" >}}

- Kita bisa menulis langsung direktori lengkap dengan mengetik : ``cd nama/direktori/yang/dituju``.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/langsung.png" class="img-fluid" >}}

- Jika kita ketik : ``cd``, maka _Command Prompt_ akan menampilkan direktori kita saat ini.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/cd.png" class="img-fluid" >}}

Oke, karena sudah tau cara penggunaan perintah ``cd`` ini, maka langsung saja kita coba untuk melakukan _compile_ pada file "HelloWorld.java" kita tadi.

Karena _Author_ menyimpan file-nya di ``C:\User\GAMERS\Documents``, maka langsung saja kita arahkan _Command Prompt_ kita kesana.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/docu.png" class="img-fluid" >}}

Jika kita sudah pada direktori yang sesuai, mari kita lakukan _compile_ pada file "HelloWorld.java" kita dengan menggunakan perintah ``javac``.

Untuk melakukannya kita ketikkan : ``javac HelloWorld.java``.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/compile.png" class="img-fluid" >}}

Jika berhasil, dia tidak akan menampilkan apa-apa. Jika tidak berhasil, itu dikarenakan ada _error_ pada kode kita. Misalnya seperti ini :

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/error.png" class="img-fluid" >}}

Jangan khawatir! Kita hanya perlu memperbaiki _error_ nya. Lagipula, semakin sering _error_, semakin pusing juga kita. Eh, maksudnya kita akan semakin paham dan mengerti dengan kode kita. :v

Selanjutnya, mari kita tampilkan kode kita pada _Command Prompt_ dengan menggunakan perintah ``java``. 

Untuk melakukannya kita ketikkan : ``java HelloWorld``.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/hello.png" class="img-fluid" >}}

Selamat!! Akhirnya anda berhasil menjadi _hekel_!! :v (bercanda)

Mungkin sekian saja postingan untuk kali ini. Maaf kalo kepanjangan. Semoga dapat dipahami, dan silahkan bertanya ataupun memberikan saran.

Terima kasih!! :)