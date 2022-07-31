# 28 Juli 2022

## Web Storage Javascript

Web Storage itu ada dua jenisnya yaitu localStorage dan sessionStorage. LocalStorage digunakan untuk menyimpan data pada browser dan data akan tetap tersimpan walaupun browser ditutup atau komputer dimatikan sekalipun. Sedangkan sessionStorage digunakan untuk menyimpan data pada browser hanya pada satu sesi dan data akan dihapus ketika browser ditutup.

Salah satu fungsi dari Local Storage dan Session Storage yaitu dapat mempermudah kita dalam membuat atau membangun sebuah website yang lebih responsive dari sisi client.

Property dan method yang digunakan pada localStorage dan sessionStorage yaitu:

>key(n) Mendapatkan nama key atau nama data urutan ke-n pada penyimpanan dimulai dari 0.

>length Mendapatkan jumlah item data yang disimpan pada storage

>getItem(nama_key) Mendapatkan data dari storage dengan nama yang disebutkan

>setItem(nama_key, data_disimpan) Menyimpan data ke storage

>removeItem(nama_key) Menghapus data pada storage dengan nama yang disebutkan

>clear() Mengosongkan semua data tersimpan pada storage

<b>Contoh menyimpan data ke localstorage</b>

<>!DOCTYPE html<>

<>html<>

<>head<>

    <>meta charset="utf-8">
    <>title>Belajar Javascript</title>
<>/head<>

<>body<>

<>script>

    <>localStorage.setItem('Makanan', 'Keju');
    <>localStorage.setItem('Minuman','Susu');
<>/script<>

<>/body<>

<>/html<>

<b>Contoh menyimpan data ke sessionstorage</b>

<>!DOCTYPE html<>

<>html<>

<>head<>

    <>meta charset="utf-8">
    <>title>Belajar Javascript</title>

<>/head<>

<>body<>

<>script<>

    <>sessionStorage.setItem('Makanan', 'Keju');
    <>sessionStorage.setItem('Minuman','Susu');

<>/script<>

<>/body<>

<>/html<>

>Untuk melihat apakah data tersebut sudah tersimpan, kamu dapat mengeceknya dengan cara seperti berikut :

Klik kanan pada web browser

Pilih Inspect Elemen / inspect / ctrl+shif+i jika 
ingin menggunakan shortcut

Pilih tab Application

Pilih penyimpan pada local storage/session storage

hasilnya:
<img src="web storage.JPG" alt="100">

<b>Menampilkan Data Dari Storage</b>

Untuk nampilkan data kita gunakan property getItem().

<b>Contoh menampilkan data dari localstorage</b>

<>!DOCTYPE html<>

<>html<>

<>head<>

    <meta charset="utf-8">
    <title>Belajar Javascript</title>

<>/head<>
<>body<>
<>script<>

    var tampil = localStorage.getItem('Makanan');
    console.log(tampil);

<>/script<>

<>/body<>

<>/html<>

<b>Contoh menampilkan data dari sessionstorage</b>

<>!DOCTYPE html<>

<>html<>

<>head<>

    <meta charset="utf-8">
    <title>Belajar Javascript</title>

<>/head<>

<>body<>

<>script<>

    var tampil = sessionStorage.getItem('Makanan');
    console.log(tampil);
<>/script<>

<>/body<>

<>/html<>

>Untuk melihat datanya tampil cara nya sama seperti sebelumnya namun pilih pada tab Console dan kira-kira hasilnya akan seperti dibawah:

<img src="hasil web storage.JPG" alt="100">

<b>Menghapus Data Dari Storage</b>

>Kalau kita menghapus  salah satu data dari storage, kita bisa menggunakan property removeItem(). 

maka hasilnya akan seperti ini:

<img src="hasil menghapus web storage.JPG" alt="100">

>jika menghapus seluruh data, kita bisa  menggunakan property clear().

maka hasilnya akan seperti ini:

<img src="menghapus seluruh data.JPG" alt="100">


