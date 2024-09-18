# Jarkom-1-2024-IT24

* Amoes Noland (5027231028)
* Radella Chesa Syaharani (5027231064)

## Advance Sanity Check

1. Mendapat username dari HTTP export objects
![](assets/sanity/1.png)
2. Disuruh buka Peraturan Praktikum lalu mendapat string
![](assets/sanity/2.png)
![](assets/sanity/3.png)
3. Saya melihat pola "==" di ujung string dan langsung memikirkan Base64 decode
![](assets/sanity/4.png)

## EZ

![](assets/ez/1.png)
![](assets/ez/2.png)
1. Melihat stream terlihat ada string yang menunjukkan jawaban dan saya mengecek port asal dari string tersebut

## Pegawai Negeri Sebelah

1. Dengan filter mencari password yang diminta, didapatkan sebuah list besar yang bisa saya extract menjadi text.
2. Saya lakukan grep untuk setiap hal yang diminta dan melihat urutan awal dan akhir
![](assets/pns/1.png)

## Illegal Breakthrough

1. Mendapat seluruh detail tentang IP, port, dan endpoint dari Export Objects
![](assets/illegal/1.png)
2. Menemukan tools Fuzz Faster U Fool (ffuf) dan kredensial lengkap yang berhasil, saya temu karena brute force mencari stream yang tidak terdapat invalid user.
![](assets/illegal/2.png)

## Packets Barrage

1. Menemukan source IP dari ribuan attempt, untuk dihitung jumlah packet (terdapat di status bar bawah Wireshark)
![](assets/packets/1.png)
2. Menemukan file Regev.zip melalui Export Objects, lalu saya dapatkan file .txt dengan extract zip tersebut.
![](assets/packets/2.png)

## FTP Login

1. Menemukan username dan password melalui sebuah stream acak yang saya ikuti setelah memfilter contains "Login"
![](assets/ftplogin/1.png)

## Surprise

1. Menemukan nama server melalui packet yang di-highlight tersebut
![](assets/surprise/1.png)
2. Melakukan extract object sebuah file c++
![](assets/surprise/2.png)
3. Melakukan compile dan mendapat string terakhir
![](assets/surprise/3.png)

## Corporate Breach

1. Mendapat nama Nakhimov dari filter contains "name"
2. Mendapat kredensial setelah brute force melihat banyak stream sampai ketemu yang tidak menunjukkan pesan gagal
![](assets/breach/1.png)

## Gajah Terbang (Server Recon)

1. Menemukan nama database dan portnya melalui melihat packet
![](assets/gajah1/1.png)
2. Menemukan berbagai macam informasi mengenai database dan isinya melalui satu stream panjang di bawah
![](assets/gajah1/2.png)
3. Melakukan dekripsi MD5 dari password admin
![](assets/gajah1/3.png)

## Gajah Terbang (Attacker Recon)

1. Mendapatkan nama penyerang dari perintah mengubah id=3 menjadi admin
![](assets/gajah2/1.png)
2. Melakukan dekripsi password penyerang
![](assets/gajah2/2.png)
3. Menemukan waktu banned dari `SELECT * from banned_users`
4. Tabel yang dimodif adalah dari query `UPDATE` dan `DELETE`
5. Melihat barang pembelian dan jumlah pengeluaran adalah dengan menghubungkan id sesuai tabel
![](assets/gajah2/3.png)

## Rizznet
1. Saya melihat 'sus' disini
![](assets/rizzset/1.jpg)
2. Setelah masuk kedalam `nc 10.15.42.60 59500`, saya memasukkan jawaban pertama yaitu `www.its.ac.id`
3. Pada pertanyaan selanjutnya diminta IP Address pada domain `its.ac.id`. Disini saya membuat tab terminal baru dan menggunakan command `nslookup its.ac.id`, untuk mendapatkan IP
![](assets/rizzset/2.jpg)
4. Untuk mendapatkan JARM Fingerprint, gunakan command `python jarm.py its.ac.id` (Sebelumnya harus menginstall jarm terlebih dahulu lalu masuk ke direktori jarm)
![](assets/rizzset/3.jpg)
5. Submit lalu dapatkan flagnya!
![](assets/rizzset/SOLVED.jpg)
