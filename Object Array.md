# 26 Juli 2022

## Multidimensional Array

Multidimensional array bisa kita sebut sebagai array didalam array. Contoh penggunaan array dalam array seperti kita mengenal sebuah matriks yang terdiri dari 3 angka kesamping dan 3 angka kebawah.

>Array dapat memiliki isi yang juga merupakan array. Kita bisa menggunakannya untuk array multidimensi, sebagai contoh untuk menyimpan matriks:

>let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

alert( matrix[1][1] ); // 5, elemen pusat


<b>Menemukan nilai dalam objek/array multidimensi dalam Javascript</b>

contoh objek multidimensi (pada dasarnya sebuah array):

<b>Object = {

   1 : { name : bob , dinner : pizza },

   2 : { name : john , dinner : sushi },

   3 : { name : larry, dinner : hummus }

} </b>

Jika kita ingin  mencari objek/array di mana kuncinya adalah "makan malam", dan melihat apakah itu cocok dengan "sushi".

kita tahu jQuery memiliki $ .inArray, tetapi sepertinya tidak bekerja pada array multidimensi. Atau mungkin kita salah. indexOf juga tampaknya hanya berfungsi pada satu level array.

Apakah tidak ada fungsi atau kode yang ada untuk ini?
jawabannya :

jika memilih array seperti dibawah ini:

var people = {

  { "name": "bob", "dinner": "pizza" },

  { "name": "john", "dinner": "sushi" },

  { "name": "larry", "dinner": "hummus" }

};

maka kita dapat menggunakan metode filter dari objek Array:

>people.filter(function (person) { return person.dinner == "sushi" });
  // => [{ "name": "john", "dinner": "sushi" }]

Dalam implementasi JavaScript yang lebih baru, Anda dapat menggunakan ekspresi fungsi:

>people.filter(p => p.dinner == "sushi")
  // => [{ "name": "john", "dinner": "sushi" }]

  jadi kita dapat mencari orang yang memiliki "dinner": "sushi" menggunakan map

  >people.map(function (person) {
  if (person.dinner == "sushi") {
    return person
  } else {
    return null
  }
}); // => [null, { "name": "john", "dinner": "sushi" }, null]

atau reduce

>people.reduce(function (sushiPeople, person) {
  if (person.dinner == "sushi") {
    return sushiPeople.concat(person);
  } else {
    return sushiPeople
  }
}, []); // => [{ "name": "john", "dinner": "sushi" }]


>var peoples = [
  { "name": "bob", "dinner": "pizza" },
  { "name": "john", "dinner": "sushi" },
  { "name": "larry", "dinner": "hummus" }
];

maka kita dapat melakukan hal berikut:

>jQuery.grep(peoples, function (person) { return person.dinner == "sushi" });
  // => [{ "name": "john", "dinner": "sushi" }]

  Jika kita sering melakukan pencarian ini, pertimbangkan untuk mengubah format objek kita sehingga makan malam sebenarnya adalah kuncinya. Ini seperti menetapkan kunci utama berkerumun dalam tabel database. Jadi, misalnya: 

>Obj = { 'pizza' : { 'name' : 'bob' }, 'sushi' : { 'name' : 'john' } }

kita sekarang dapat dengan mudah mengaksesnya seperti ini: Object['sushi']['name']. Atau jika objek benar-benar sesederhana ini (cukup 'nama' di objek), Anda bisa mengubahnya menjadi:

>Obj = { 'pizza' : 'bob', 'sushi' : 'john' }

Dan kemudian mengaksesnya seperti: Object['sushi'].





