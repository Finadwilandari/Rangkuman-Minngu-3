# 25 Juli 2022

## Array
Array merupakan struktur data yang digunakan untuk menyimpan sekumpulan data dalam satu tempat. Setiap data dalam Array memiliki indeks, sehingga kita akan mudah memprosesnya.

> <b>Indeks array selalu dimulai dari angka nol (0) </b> Ukuran array akan bergantung dari banyaknya data yang ditampung di dalamnya.

<b> Cara Membuat Array pada Javascript</b>

Pada javascript, array dapat kita buat dengan tanda kurung siku ('[...]').
Contoh:

> <b>var products = []; </b>

Maka variabel products akan berisi sebuah array kosong. Kita bisa mengisi data ke dalam array, lalu setiap data dipisah dengan tanda koma (',').
Contoh:

> <b>var products = ["Flashdisk", "SDD", "Monitor"]; </b>

karena javascript merupakan bahasa pemrograman yang dynamic typing, maka kita bisa menyimpan dan mencampur apapun di dalam array.

> <b>var myData = [12, 2.1, true, 'C', "BelajarArray"]; </b>

Array akan menyimpan sekumpulan data dan memberinya nomer indeks agar mudah diakses.Indeks array selalu dimauli dari nol '0'. Misalkan kita punya array seperti ini:

> var makanan = ["Nasi Goreng", "Mie Ayam", "Mie Gelas"];

Bagaimana cara kita mengambil nilai "Mie Ayam"?

maka awabannya seperti ini:

> makanan[1] //-> "Mie Ayam"

Kenapa bukan 2?
karena indeks array selalu dimulai dari nol.

<b>Mencetak isi Array dengan Perulangan</b>

>document.write(products[0]);
document.write(products[1]);
document.write(products[2]);
document.write(products[3]);
document.write(products[4]);

Pada contoh di atas, kita menggunakan properti 'length' untuk mengambil panjang array.

Kita memiliki '4' data di dalam array 'products', maka properti 'length' akan bernilai '4'.

Lalu kita gunakan properti ini untuk membatasi jumlah perulangan di dalam for.

>for(let i = 0; i < products.length; i++){
    document.write(`<li>${ products[i] }</li>`);
}

di dalam blok for, kita mencetak isi produk dengan indeks yang mengacu pada variabel i.

>adapun cara lain yaitu kita bisa mengunakan perulangan dengan method forEach().

<b>Cara Menambahkan Data ke Dalam Array</b>

Ada dua cara yang bisa dilakukan untuk menambah data ke dalam array:

>Mengisi menggunakan indeks

>Mengisi menggunakan method push()

Misal kita punya array dengan isi sebagai berikut:

> <b> var buah = ["Apel", "Jeruk", "Manggis"]; </b>

Artinya terdapat tiga data di dalam array buah dengan indeks:
0: "Apel"
1: "Jeruk"
2: "Manggis"

>Apabila kita memasukan nomer indeks sembarangan, maka nanti yang akan terjadi adalah data yang ada di daalam indeks tersebut akan ditindih. Maka solusinya Kita gunakan method push().

Kita tidak perlu tahu berapa panjang array-nya, karena method push() akan menambahkan data ke dalam array dari ekor atau belakang.

<b>Cara Menghapus Data Array</b>

Sama seperti menambahkan data ke array, menghapus data juga memiliki dua cara:

>Menggunakan delete

>Menggunakan method pop()

contoh:

> <b>delete buah[2]; </b>

Kita dapat menghapus data dengan nomer indeks tertentu dengan 'delete'. Sedangkan 'pop()' akan menghapus dari belakang. Kekurangan dari 'delete', ia akan menciptakan ruang kosong di dalam array.

Cara kedua menggunakan method pop(), kebalikan dari method push(). Method 'pop()' akan menghapus array yang ada di paling belakang. Array pada javascript dapat kita pandang sebagai sebuah stack (tumpukan), yang mana memiliki sifat 'LILO' (Last in Last out).

>Method pop() akan mengembalikan nilai item atau data yang terhapus dari array.

<b>Menghapus Data dari Depan</b>

Kita dapat menghapus data dari depan dengan menggunakan method 'shift()'.

contoh:

><b> var bunga = ["Mawar", "Melati", "Anggrek", "Sakura"]; </b>

>// hapus data dari depan
bunga.shift();

Maka data yang terhapus adalah "Mawar"

<b>Menghapus Data pada Indeks Tertentu</b>

Apabila kita ingin menghapus data pada inteks tertentu, maka fungsi atau method yang digunakan adalah splice().

Fungsi ini memiliki dua parameter yang harus diberikan:

><b>array.splice(<indeks>, <total>);</b>

dimana:

> indeks adalah indeks dari data di dalam array yang akan dihapus;
>total adalah jumlah data yang akan dihapus dari indeks tersebut.

Biasanya kita berikan nilai total dengan nilai '1' agar hanya menghapus satu data saja.

contoh:

><b>var bunga = ["Mawar", "Melati", "Anggrek", "Sakura"];</b>

>// hapus Anggrek
bunga.splice(2, 1);

<b>Mengubah isi Array</b>

><b>var bahasa = ["Javascript", "Kotlin", "Java", "PHP", "Python"];
bahasa[1] = "C++";</b>

## Method-method penting pada Array

1. Method filter() berfungsi untuk menyaring data dari array. Parameter yang harus diberikan pada method filter() sama seperti method forEach(), yaitu: sebuah fungsi callback.

Contoh:
><b>const angka = [1, 2, 3, 4, 5, 6, 7, 8, 9];

// Kita ambil data yang hanya habis dibagi dua saja
>const filteredArray = angka.filter((item) => {return item % 2 === 0});

console.log(filteredArray) // -> [2, 4, 6, 8]</b>

Pada contoh di atas, kita memberikan arrow function sebagai fungsi callback yang akan melakukan penyaringan terhadap array.
adapun cara sederhananya yaitu:

><b>const filteredArray = angka.filter(item => item % 2 === 0);</b>

 2. Method includes()
Method ini berfungsi untuk mengecek apakah sebuah data ada di dalam array atau tidak. Biasanya digunakan untuk melakukan pencarian untuk memastikan data sudah ada di dalam array.

contoh:

><b>var tanaman = ["Padi", "Kacang", "Jagung", "Kedelai"];

// apakah kacang sudah ada di dalam array tanaman?
>var adaKacang = tanaman.includes("Kacang");

console.log(adaKacang); // -> true

// apakah bayam ada?
>var adaBayam = tanaman.includes("Bayam");

console.log(adaBayam); // -> false </b>

3. Method sort()
Method sort() berfungsi untuk mengurutkan data pada array.

Contoh:

><b>var alfabet = ['a','f','z','e','r','g'];

>var angka = [3,1,2,6,8,5]; 

console.log(alfabet.sort()); //->  ["a", "e", "f", "g", "r", "z"]

console.log(angka.sort()); // -> [1, 2, 3, 4, 5, 6, 7, 8, 9] </b>



