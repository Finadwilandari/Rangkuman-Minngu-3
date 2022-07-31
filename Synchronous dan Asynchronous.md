# 29 Juli 2022

## Synchronous dan Asynchronous

<b>Synchronous</b>

Synchronous (sync), merupakan mode default dalam proses eksekusi perintah kode. Perhatikan baris kode berikut

<b>function tanyaKabar(name) {
    console.log('Apa kabar,', name);
}

function katakanHallo(name) {
    console.log('Hallo,', name);
}

katakanHallo('Guntur');
tanyaKabar('Gun'); </b>

maka pada layar console dibrowser anda akan muncul seperti gambar berikut:

<img src="synchronous.PNG" alt="100">

<b>Asynchronous</b>

Jika pada sync, kode diproses baris perbaris, maka di async kode diproses secara baris perbaris juga. 
Dalam skenario-nya, sebenarnya kode async telah diproses, hanya saja sebatas penjadwalan untuk dieksekusi pada tahapan berikutnya. Artinya, kode yang berperilaku async tidak akan langsung dieksekusi, tetapi di skip dan akan melakukan eksekusi baris perintah berikutnya.

<b>function tanyaKabar(name) {
    console.log('Apa kabar,', name);
}

function katakanHallo(name) {
    setImmediate(function () {
        console.log('Hallo,', name);
    });
}

katakanHallo('Guntur');
tanyaKabar('Gun'); </b>

maka pada layar console dibrowser anda akan muncul seperti gambar berikut:


<img src="Asynchronous.PNG" alt="100">

>Pemanfaatan async sangat berguna pada saat melakukan operasi-operasi yang tidak harus menunggu proses yang lainnya. Misalnya, memanipulasi DOM ketika melakukan proses ajax. Agar bisa memahami, kita perlu mengetahui cara menghandle kode async tersebut dengan cara callback ataupun promises.




