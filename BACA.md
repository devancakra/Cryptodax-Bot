[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://github.com/devancakra/Cryptodax-Bot)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Cryptodax-Bot)
![PHP](https://img.shields.io/badge/-PHP-grey.svg?&logo=PHP&logoColor=white)

# Cryptodax-Bot
<strong>Tugas Pemrograman API</strong><br>
Pembacaan Cryptocurrency Indodax Melalui Bot Telegram Berbasis PHP

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Fitur | Baca, Pengendalian Masalah |
| Kode | PHP |
| Kerangka Kerja | Botman |
| Peralatan | XAMPP (PHP Versi 7.4) & Ngrok |

<br><br>

## Unduh & Instal
1. XAMPP dengan PHP versi 7.4

   <table><tr><td width="810">

   ```
   https://bit.ly/XAMPP_PHP7_Installer
   ```

   </td></tr></table><br>

2. Ngrok

   <table><tr><td width="810">
      
   ```
   https://bit.ly/NGROK_Installer
   ```

   </td></tr></table><br>

3. Composer

   <table><tr><td width="810">
      
   ```
   https://bit.ly/Composer_Installer
   ```

   </td></tr></table><br>

4. Git 

   <table><tr><td width="810">
      
   ```
   https://bit.ly/GIT_Installer
   ```

   </td></tr></table>
    
<br><br>

## Memulai
1. Unduh repositori ini lalu ekstrak.<br><br>

2. Pindahkan direktori ``` Cryptodax-Bot ``` ke dalam direktori ``` htdocs ```, yang rinciannya dapat anda lihat sebagai berikut: ``` C:\xampp\htdocs ```.<br><br>
   
3. Buka ``` XAMPP ```, lalu mulai bagian ``` Apache ```.<br><br>

4. Buat akun Ngrok terlebih dahulu di halaman berikut: <strong>https://dashboard.ngrok.com/login</strong>.<br><br>

5. Hubungkan akun ngrok dengan cara berikut:

   <table><tr><td width="810">

   ```bash
   ngrok config add-authtoken [YOUR NGROK AUTHTOKEN]
   ```

   </td></tr></table><br>

6. Buka berkas ``` ngrok.yml ``` di dalam direktori ``` C:\Users\[User Name]\AppData\Local\ngrok ``` , kemudian atur tunnel agar dapat digunakan untuk banyak port sekaligus dengan menuliskan perintah berikut di dalamnya: 

   <table><tr><td width="810">

   ```bash
   version: "2"
   authtoken: [YOUR NGROK AUTHTOKEN]
   tunnels:
     tunnel-1:
       proto: http
       addr: 80
       schemes: ["https"]
     tunnel-2:
       proto: http
       addr: 80
       schemes: ["http", "https"]
   ```

   </td></tr></table><br>
   
7. Ketik perintah berikut ke dalam ``` NGROK.exe ``` dan tekan enter:

   <table><tr><td width="810">

   ```bash
   ngrok start --all
   ```

   </td></tr></table><br>
   
8. Salin ``` API Bot Telegram ``` anda dari ``` @BotFather ``` dan tempelkan ke dalam folder (direktori) berikut: ``` Cryptodax-Bot -> private -> token.txt ```.<br><br>
       
9. Buka ``` CMD (Command Prompt) ``` dan ketikkan perintah dengan aturan berikut untuk menjalankan bot:<br>``` curl -d url=[URL Https NGROK]/[Folders If Any]/bot.php -X POST https://api.telegram.org/bot[TOKEN]/setWebhook ```<br><br>

    • Contoh penulisan:

   <table><tr><td width="810">
      
    ```bash
    curl -d url=https://e6e5-2001-448a-5021-617-ecb0-7d4d-1d9e-27f2.ngrok-free.app/Cryptodax-Bot/bot.php -X POST https://api.telegram.org/bot1496456979:AAE7MCBAeRznBN3G-E4J65GgVYzHo0oZmog/setWebhook 
    ```
    
    </td></tr></table><br>

    • Hasilnya akan muncul (tanda Bot sudah bekerja / aktif): ``` {"ok":true,"result":true,"description":"Webhook was set"} ```.<br><br>
         
11. Jika anda ingin menyelesaikan ``` sesi webhook ``` yang sedang berjalan, maka buka ``` browser ``` dengan mengetikkan perintah berikut: 

    <table><tr><td width="810">

    ```bash
    https://api.telegram.org/bot[TOKEN]/setWebhook
    ```

    </td></tr></table>
    
<br><br>

## Permasalahan yang sering muncul
1. Masalah yang biasanya terjadi pada bot telegram berbasis Botman adalah saat pengguna telah meninggalkan bot tersebut dalam rentang waktu yang lama, hal ini dapat mengakibatkan ``` API Token menjadi kadaluarsa ```. Masalah ini biasanya ditandai dengan keadaan ``` bot telegram yang tidak normal ```, misalnya ketika pengguna memberikan perintah ``` /start ``` ataupun perintah lainnya, bot ini tetap tidak merespon. Solusi dari permasalahan ini yaitu anda ``` hanya perlu membuat bot telegram yang baru lagi ``` (otomatis dapat API Token yang baru), selanjutnya untuk kode program silakan atur berdasarkan kebutuhan anda masing-masing.
<br>

2. Jika masalah pada poin 1 tidak teratasi, maka anda harus :
   
   • Menghapus 3 file yang ada di dalam direktori ``` C:\xampp\htdocs\Cryptodax-Bot ``` yaitu ``` composer.json ```, ``` composer.lock ```, dan ``` vendor ```.

   • Instal depedensi ``` Botman ``` melalui ``` GitBash ``` dengan memberikan perintah seperti berikut:

   <table><tr><td width="810">

   ```bash
   composer require "botman/driver-telegram"
   ```

   </td></tr></table>

<br><br>

## Sorotan
<table>
<tr>
<th colspan="4">Bot Telegram</th>
</tr>
<tr>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/a8aa403d-aae6-4fe9-9c6c-6f217ed599a5" alt="TGbot-1"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/7bffc607-0692-4b7a-9fd7-8ec2ce848e5d" alt="TGbot-2"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/b0dc2f06-5abc-46a1-9fac-68e7432c0225" alt="TGbot-3"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/2435cdd7-86b5-4a4e-9935-08d6410a93ea" alt="TGbot-4"></td>
</tr>
<tr>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/b3fe335d-e733-4fa2-b626-5fbe13dd754d" alt="TGbot-5"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/8a961333-602e-4329-a447-922b45a8b4cf" alt="TGbot-6"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/bd00baa9-f206-4aa8-b596-58ac9427368f" alt="TGbot-7"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/da6a2b20-cef6-47af-8d0c-e3f82cdaf24b" alt="TGbot-8"></td>
</tr>
<tr>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/11320b99-8ea1-4930-9f60-82f83e4647e0" alt="TGbot-9"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/f889ff7a-45cf-407c-9d71-bb3511802f4b" alt="TGbot-10"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/c845b3ea-7638-4b44-a5be-699a18fd5ab2" alt="TGbot-11"></td>
<td width="210"><img src="https://github.com/devancakra/Cryptodax-Bot/assets/54527592/60eff8ad-5fd8-4865-a113-af107e5edb23" alt="TGbot-12"></td>
</tr>
</table>

<br><br>

## Demonstrasi Aplikasi
Via Telegram: <a href="http://t.me/cryptodax_bot">@cryptodax_bot</a>

<br><br>

## Apresiasi
Jika karya ini bermanfaat bagi anda, maka dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan mengklik tombol ``` ⭐Bintang ``` di bagian atas repositori.

<br><br>

## Penafian
Aplikasi ini dibuat dengan menyertakan sumber-sumber dari pihak ketiga. Pihak ketiga di sini adalah penyedia layanan, yang layanannya berupa pustaka, kerangka kerja, dan lain-lain. Saya ucapkan terima kasih banyak atas layanannya. Telah terbukti sangat membantu dan dapat diimplementasikan.

<br><br>

## LISENSI 
LISENSI MIT - Hak Cipta © 2020 - Devan Cakra Mudra Wijaya

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
