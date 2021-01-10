## Pegenalan PHP
- PHP singkatan dari PHP:Hypertext Preprocessor
- PHP adalah bahasa pemrograman yang opensource dan gratis untuk digunakan
- PHP pertama kali dibuat oleh Rasmus Lerdorf pada tahun 1995
- PHP banyak digunakan sebagai bahasa pemrograman yang dikhusukan untuk web development
- PHP sangat mudah digunakan dan banyak sekali diaposi oleh web programmer
- Banyak web di dunia dibuat dengan menggunakan PHP
- PHP dapat di download di website php.net 
- atau bisa lihat source codenya dihalaman github php [https://github.com/php/php-src](https://github.com/php/php-src)


### Kenapa belajar PHP ?
Karena php masuk dalam kategori 10 bahasa terpopuler di dunia, banyak web dan company yang menggunakan php 

### Apa yang bisa dibuat menggunakan PHP?
- Server-side scripting. ini adalah salahs atu fokus utama web untuk membuat aplikasi server side. Biasanya digunakan sebagai aplikasi web menggunakan bantuan web server dan kita bisa melihat output aplikasi menggunakan web browser.
- Command line scripting. PHP juga bisa digunakan untuk membuat program berbasis command line tanpa harus menggunakan web server.
- Dekstop application, walaupun jarang digunakan tapi php juga bisa digunakan untuk membuat aplikasi dekstop menggunakan PHP-GTK

### Menginstall PHP
- PHP bisa di install di sistem operasi apapun (Windows, Mac, Linux)
- Menginstall PHP secara manual tidak terlalu mudah oleh karena itu untuk belajar, direkomendasikan menginsall php dengan bantuan tool-tool yang sudah mem-budle PHP dengan teknologi pendukungnya misalnya XAMPP.
- XAMPP dapat di download gratis melalui link  [apachefriends.org](https://www.apachefriends.org/)

### Setting PATH
Setelah install php kita perlu atur PATH, inti dari setting PATH ini adalah agar kita bisa mengakses PHP dari command prompt/terminal. Tapi jika kita menggunakan XAMPP maka tidak perlu setting PATH.

### Text Editor
- VisualStudio Code
- Sublime Text
- Atom 
- PHPStorm 

### File PHP
- File kode program PHP diakhiri dengan extension .php
- Diawal kode program PHP, wajid menambahkan <?php dan diakhir kode program perlu ditambahkan ?> (tapi tidak wajib). Tidak wajib jika dikode tersebut hanya ada kode php aja tapi kalo kodenya campur sama html maka ?> wajib ditulis.
- Penamaan file di PHP tidak ada aturan, jadi kita bisa membuat nama file PHP sesuka hati, namun agar mempermudah saat menjalakan file PHP direkomendasikan tidak menggunakan spasi. Contoh nama file php yang baik : index.php, about.php, latihan1.php
- Untuk menampilkan tulisan di PHP kita bisa menggunakan perintah echo

Contoh kode php untuk menampilkan tulisan hello world 
```php
<?php
  echo "Hello World";
```

### Tipe Data Number

Di PHP ada 2 jenis tipe data number
- int : Bilangan bulat desimal
- float : Bilangan bulat pecahan
Di PHP kita bisa menambahkan _ (garis bawah) di angka, ini hanya untuk agar mudah dibaca. Saat dijalankan garis bawah ini akan di abaikan (ignore). contoh : 1_000_000


#### Integer Overflow
- Batasan atau kapasistas di php sistem operasi 32 bit yaitu 2147483647
- Batasan atau kapasistas di php sistem operasi 64 bit yaitu 9223372036854775807
- Jika nilai integer melebihi kapasitas diatas maka secara otomatis tipe number akan berubah menjadi floating point

### Tipe Data Boolean
- Tipe data boolean adalah tipe data paling sederhana di PHP
- Tipe data boolean adalah tipe data dengan nilai kebenaran (benar atau salah)
- Nilai benar adalah true dan nilai salah adalah false

### Tipe Data String
- Tipe data string adalah tipe data representasi dari teks
- String bisa mengandung kosong atau banyak karakter
- Untuk membuat string bisa menggunakan single quote ' contoh : 'Nama : '
- Untuk membuat string kita juga bisa menggunakan double quote "
  - Kelebihan menggunakan double quote adalah kita bisa menggunakan escape sequence
  - Contoh : echo "Fiki\t Dedi\t Andika\n";
  - \t untuk Tab
  - \n Untuk Enter

### Multiline String
- Kadang kita ingin membuat data string lebih dari satu baris. Untuk melakukan itu sebenarnya kita bisa menggunakan \n sebagai ENTER
- Namun PHP punya fitur yaitu Heredoc dan Nowdoc untuk menghandle-nya.

#### Heredoc

contoh :
```php
<?php
echo <<<DESEMBER
Ini adalah contoh string yang panjang
kita tidak perlu ngetik ENTER secara manual
bisa juga pake "quote"
DESEMBER;
```

#### Nowdoc

contoh :
```php
<?php
echo <<<'DESEMBER'
Ini adalah contoh string yang panjang
kita tidak perlu ngetik ENTER secara manual
bisa juga pake "quote"
DESEMBER;
```

## Variable
- adalah tempat untuk menyimpan data sehingga bisa kita gunakan lagi di kode program selanjutnya
- di PHP variable bisa menampung berbagai jenis tipe data dan bisa berubah-ubah tipe data
- untuk membuat variable kita bisa menggunakan tanda $ (dolar) diikuti dengan nama variablenya
- variable tidak boleh mengandung spasi
- variable tidak boleh diawali angka

contoh :
```php
<?php
$nama = 'Fiki';
echo "Nama : ";
echo $nama;
```

## Constant
- adalah tempat untuk menyimpan data yang tidak bisa dirubah lagi setelah di deklarasikan
- untuk membuat constant kita bisa menggunakan function define()
- Best practice pembuatan nama constant adalah menggunakan UPPER_CASE (huruf kapital)

contoh :
```php
<?php
define("AUTHOR", "Fiki Dedi Andika");
define("APP_VERSION", 100);

echo AUTHOR;
echo "\n";
echo APP_VERSION;
```


### Data NULL
- Nilai NULL merepresentasikan sebuah variable tanpa nilai
- Saat kita membuat variable lalu ingin menghapus data yang terdapat di variable tersebut kita bisa menggunakan NULL untuk mengosongkan variable tersebut
- Untuk membuat data NULL kita bisa menggunakan kata kunci NULL (case insensitive)

contoh :
```php
<?php
$nama = "Fiki";
$nama = null;

echo "Nama : ";
echo $nama;
```

#### Mengecek Apakah Data NULL
- kadang kita ingin tahu apakah sebuah data bernilai null atau tidak
- untuk mengecek apakah sebuah data bernilai null, kita bisa menggunakan function is_null($variable)

contoh :
```php
<?php
	$nama = "Fiki Dedi Andika";
	$umur = null; //ini data null
	
	
	$cek_data_nama = is_null($nama);
	
	echo "Cek data nama : ? ";
	var_dump($cek_data_nama);
	
	echo "Cek data umur : ? ";
	var_dump(is_null($umur));
```
