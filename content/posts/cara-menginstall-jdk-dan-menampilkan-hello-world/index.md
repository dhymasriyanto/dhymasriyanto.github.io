---
title: "Cara Menginstall JDK Dan Menampilkan Hello World"
date: 2019-08-01T10:35:21+07:00
draft: false
categories: ["JAVA"]
---

**JDK** atau JAVA Development Kit adalah salah satu dari tiga paket inti yang dibutuhkan pada bahasa JAVA. Dua lainnya ialah **JVM** (JAVA Virtual Machine) dan **JRE** (JAVA Runtime Environment).
Berikut perbedaan ketiganya:

- **JVM** adalah komponen dari platform JAVA yang berfungsi untuk mengeksekusi program-program

- **JRE** adalah bagian JAVA yang membuat **JVM**

- **JDK** membolehkan _developer_ untuk membuat program JAVA, sehingga dapat di eksekusi oleh **JVM** dan **JRE**

Bagi yang baru memulai mempelajari JAVA pasti masih bingung dengan pembagian-pembagian dan istilah-istilah tersebut. Pervedaan mendasarnya ialah, **JDK** adalah _package_ untuk men-_develop_ program berbasis JAVA, yang mana membutuhkan JRE sebagai _package_ untuk menjalankan kode JAVA tersebut.

Berikut bagan bagaimana peranan **JDK**  pada JAVA:

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/jdk-01.png" class="img-fluid" >}}


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

 Langkah selanjutnya, kita harus menyetting PATH untuk Environment Variable pada Windows.

## Apa itu PATH?

 PATH itu ialah istilah yang digunakan untuk menunjukkan alamat suatu file.

 Sebenarnya, JAVA sudah berhasil terinstall pada OS kita, tapi tidak secara otomatis ter-_setting_ PATH-nya. Untuk mengetahui hal tersebut tekan _Windows_ + R untuk membuka kotak dialog "Run" seperti berikut :

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/run.png" class="img-fluid" >}}
