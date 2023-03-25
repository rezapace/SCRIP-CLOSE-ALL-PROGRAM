# SCRIP-CLOSE-ALL-PROGRAM

Program di atas menggunakan PowerShell untuk mengambil daftar semua proses yang sedang berjalan di komputer dan memeriksa apakah mereka memiliki judul jendela (mainwindowtitle) dan bukan PowerShell itu sendiri. Jika mereka memenuhi syarat, maka perintah stop-process akan digunakan untuk menutup program tersebut. 

Dalam hal ini, perintah yang ditambahkan adalah { $_.processname -ne "powershell" }, yang menghindari penghentian PowerShell itu sendiri.

Penjelasan program ini dapat ditambahkan dalam format README.md seperti di bawah ini:

# Penjelasan Sederhana Program 'SCRIP-CLOSE-ALL-PROGRAM'

Program ini menggunakan PowerShell untuk mengambil daftar semua proses yang sedang berjalan di komputer dan memeriksa apakah mereka memiliki judul jendela dan bukan PowerShell itu sendiri. Jika mereka memenuhi syarat, maka perintah stop-process akan digunakan untuk menutup program tersebut.

## Cara Menggunakan

- Silakan unduh file script-close-all-program.ps1.
- Double-click file tersebut untuk menjalankannya.
- Setelah dijalankan, program akan menutup semua program yang sedang berjalan di komputer, kecuali PowerShell.

## Perhatian

- Pastikan untuk menyimpan pekerjaan Anda dan menutup program yang ingin Anda simpan sebelum menjalankan script ini.
- Anda akan kehilangan semua data tidak disimpan atau disimpan dengan benar jika program ditutup oleh script ini.

```
(get-process | ? { $_.mainwindowtitle -ne "" -and $_.processname -ne "powershell" } )| stop-process
jelaskan program di atas
```