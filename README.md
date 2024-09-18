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