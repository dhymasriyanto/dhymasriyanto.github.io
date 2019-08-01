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

Pilih PATH seperti pada gambar dibawah:

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/environment.png" class="img-fluid" >}}

Pilih _New_.

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/edit.png" class="img-fluid" >}}

Kemudian _paste_ alamat yang telah kita _copy_ tadi.\

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/new.png" class="img-fluid" >}}

Setelah itu klik _OK_ di semua menu sampai anda keluar.

Naaahhh... Akhirnya kita telah berhasil mengatur agar JDK terdapat di dalam PATH.

Tapi, untuk membuktikan hal itu, mari kita coba di _Command Prompt_. Oh iya, kita harus _close_ dulu _Command Prompt_ sebelumnya, agar reload data baru.

Kemudian buka lagi _Command Prompt_ dan coba ketikkan kembali ``javac``, jika berhasil maka tampilannya akan seperti ini :

{{< figure src="/img/cara-menginstall-jdk-dan-menampilkan-hello-world/success.png" class="img-fluid" >}}

# <center>Membuat Hello World  Pada JAVA</center>

Untuk membuat Hello World pada JAVA, kita akan melakukan _compile_ dengan menggunakan _syntax_ ``javac`` tadi.