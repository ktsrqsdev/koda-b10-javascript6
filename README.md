# Built-in Method and Functions
## Built-in Method
### String

``` JavaScript
let teks = "Belajar JavaScript";
```
1. toUpperCase()
Mengubah semua **huruf** menjadi **huruf kapital**.
```javascript
console.log(teks.toUpperCase());
```
> Output: "BELAJAR JAVASCRIPT"

2. toLowerCase()
Mengubah semua **huruf** menjadi **huruf kecil**.
```javascript
console.log(teks.toLowerCase());
```
> Output: "belajar javascript"

3. includes()
Memeriksa apakah teks mengandung kata atau karakter tertentu. Menghasilkan **true** atau **false**.
```javascript
console.log(teks.includes("JavaScript"));
```
> Output: true

4. slice()
Mengambil sebagian **teks** berdasarkan **indeks**.
```javascript
console.log(teks.slice(0, 7));
```
> Output: "Belajar"

5. replace()
Mengganti bagian **teks** dengan **teks yang baru**.
```javascript
console.log(teks.replace("JavaScript", "Python"));
```
> Output: "Belajar Python"


### Number
```javascript
let angka = 123.4567;
```
1. toFixed()
Membulatkan **tampilan angka** menjadi jumlah **digit desimal** tertentu.
Menghasilkan **String**.
```javascript
console.log(angka.toFixed(2));
```
> Output: "123.46"

2. toPrecision()
Mengatur **jumlah digit** signifikan pada **angka**.
Menghasilkan **String**.
```javascript
console.log(angka.toPrecision(4));
```
> Output: "123.5"

3. toString()
Mengubah **angka** menjadi **String**.
```javascript
console.log(angka.toString());
```
> Output: "123.4567"

4. toExponential()
Mengubah **angka** menjadi **notasi eksponensial**.
```javascript
console.log(angka.toExponential(2));
```
> Output: "1.23e+2"

5. toLocaleString()
Memformat **angka** sesuai format **lokal**.
```javascript
console.log((1234567.89).toLocaleString("id-ID"));
```
> Output: "1.234.567,89"

### Array
```javascript
let bilangan = [10, 20, 30];
```
1. push()
Menambahkan **elemen baru** ke **akhir array**.
```javascript
bilangan.push(40);
console.log(bilangan);
```
> Output: [10, 20, 30, 40]

2. pop()
Menghapus **elemen terakhir** dari **array** dan **mengembalikannya**.
```javascript
console.log(bilangan.pop());
```
> Output: 40
```javascript
console.log(bilangan);
```
> Output: [10, 20, 30]

3. includes()
Memeriksa apakah **array** memiliki **elemen tertentu**.
```javascript
console.log(bilangan.includes(20));
```
> Output: true

4. map()
Membuat **array baru** dari hasil pemrosesan setiap elemen.
```javascript
let hasilMap = bilangan.map(nilai => nilai * 2);
console.log(hasilMap);
```
> Output: [20, 40, 60]

5. filter()
Membuat array baru yang hanya berisi elemen yang memenuhi kondisi tertentu.
```javascript
let hasilFilter = bilangan.filter(nilai => nilai >= 20);
console.log(hasilFilter);
```
> Output: [20, 30]

### Object
```javascript
let mahasiswa = {
    nama: "Budi",
    umur: 20,
    jurusan: "Informatika"
};
```
1. Object.keys()
Menghasilkan array yang berisi semua nama properti (key).
```javascript
console.log(Object.keys(mahasiswa));
```
> Output: ["nama", "umur", "jurusan"]

2. Object.values()
Menghasilkan array yang berisi semua nilai properti (value).
```javascript
console.log(Object.values(mahasiswa));
```
> Output: ["Budi", 20, "Informatika"]

3. Object.entries()
Menghasilkan array berisi pasangan key dan value.
```javascript
console.log(Object.entries(mahasiswa));
```
> Output: [["nama", "Budi"], ["umur", 20], ["jurusan", "Informatika"]]

4. Object.hasOwn()
Memeriksa apakah object memiliki properti miliknya sendiri.
```javascript
console.log(Object.hasOwn(mahasiswa, "nama"));
```
> Output: true

5. Object.assign()
Menyalin properti dari satu atau beberapa object ke object tujuan.
```javascript
let tambahan = { semester: 4 };
Object.assign(mahasiswa, tambahan);
console.log(mahasiswa);
```
> Output: { nama: "Budi", umur: 20, jurusan: "Informatika", semester: 4 }


## Built-in Function
### ParseInt
```javascript
let bil = "250";
```
Mengubah String menjadi bilangan bulat.
Pembacaan angka berhenti ketika ditemukan karakter yang tidak sesuai dengan sistem bilangan yang digunakan.
```javascript
console.log(parseInt(bil));
```
> Output: 250
```javascript
console.log(parseInt("25.8"));
```
> Output: 25

### ParseFloat
```javascript
let angka = "12.75";
```
Mengubah String menjadi angka yang dapat memiliki desimal.
```javascript
console.log(parseFloat(angka));
```
> Output: 12.75
```javascript
console.log(parseFloat("3.14abc"));
```
> Output: 3.14

### isNaN
```javascript
let angka1 = "Hello";
let angka2 = 100;
```
Memeriksa apakah suatu nilai menghasilkan NaN setelah dikonversi menjadi Number.
```javascript
console.log(isNaN(angka1));
```
> Output: true
```javascript
console.log(isNaN(angka2));
```
> Output: false

### isFinite
```javascript
let angka1 = 100;
let angka2 = Infinity;
```
Memeriksa apakah nilai yang dikonversi menjadi angka
menghasilkan angka yang terbatas (bukan Infinity atau NaN).
```javascript
console.log(isFinite(angka1));
```
> Output: true
```javascript
console.log(isFinite(angka2));
```
> Output: false

### encodeURIComponent
```javascript
let teks = "belajar JavaScript & HTML";
```
Mengubah karakter tertentu menjadi format
yang aman digunakan sebagai bagian dari URL.
```javascript
console.log(encodeURIComponent(teks));
```
> Output: belajar%20JavaScript%20%26%20HTML
