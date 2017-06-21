## Berikut adalah kode PHP yang diperlukan untuk membuat deret fibonacci:
```php
<?php
// siapkan 2 angka awal
$angka_sebelumnya=0;
$angka_sekarang=1;
 
//tampilkan 2 angka awal
echo "$angka_sebelumnya $angka_sekarang";

for ($i=0; $i<10; $i++)
{
  // hitung angka yang akan ditampilkan
  $output = $angka_sekarang + $angka_sebelumnya;
  echo " $output";
 
  //siapkan angka untuk perhitungan berikutnya
  $angka_sebelumnya = $angka_sekarang;
  $angka_sekarang = $output;
}

// hasil: 
// 0 1 1 2 3 5 8 13 21 34 55 89
?>
```

## Membuat Fungsi Deret Fibonnacci
```php
<?php
function print_deret_fibonacci($jumlah)
{
  // siapkan 2 angka awal
  $angka_sebelumnya=0;
  $angka_sekarang=1;
 
  //simpan string angka awal
  $hasil = "$angka_sebelumnya $angka_sekarang";

  for ($i=0; $i<$jumlah-2; $i++)
  {
    // hitung angka fibonacci
    $output = $angka_sekarang + $angka_sebelumnya;
    // hasilnya ditambahkan ke string $hasil
    $hasil = $hasil." $output";
 
    //siapkan angka untuk perhitungan berikutnya
    $angka_sebelumnya = $angka_sekarang;
    $angka_sekarang = $output;
  }
  return $hasil;
}
 
echo print_deret_fibonacci(8);
echo "<br>";
// hasil: 0 1 1 2 3 5 8 13

echo print_deret_fibonacci(10);
echo "<br>";
// hasil: 0 1 1 2 3 5 8 13 21 34

echo print_deret_fibonacci(20);
echo "<br>";
// hasil: 0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597 2584 4181
?>
```
## Mencari urutan tertentu deret fibonacci
```php
<?php
function cari_fibonacci($urutan)
{
  // siapkan 2 angka awal
  $angka_sebelumnya=0;
  $angka_sekarang=1;
 
  for ($i=0; $i<$urutan-1; $i++)
  {
    // hitung angka fibonacci
    $output = $angka_sekarang + $angka_sebelumnya;
 
    //siapkan angka untuk perhitungan berikutnya
    $angka_sebelumnya = $angka_sekarang;
    $angka_sekarang = $output;
  }
  return $output;
}
 
echo cari_fibonacci(5); // hasil: 5
echo "<br>";

echo cari_fibonacci(11); // hasil: 89
echo "<br>";

echo cari_fibonacci(30); // hasil: 832040
?>
```
## Membuat Piramida deret fibonacci
```php
<?php
function print_deret_fibonacci($jumlah)
{
  // siapkan 2 angka awal
  $angka_sebelumnya=0;
  $angka_sekarang=1;
 
  //simpan string angka awal
  $hasil = "$angka_sekarang";

  for ($i=0; $i<$jumlah-1; $i++)
  {
    // hitung angka fibonacci
    $output = $angka_sekarang + $angka_sebelumnya;
    // hasilnya ditambahkan ke string $hasil
    $hasil = $hasil." $output";
 
    //siapkan angka untuk perhitungan berikutnya
    $angka_sebelumnya = $angka_sekarang;
    $angka_sekarang = $output;
  }
  return $hasil;
}
 
function piramida_fibonacci($tingkat){
  for ($i=1; $i<$tingkat+1; $i++)
  {
    echo print_deret_fibonacci($i);
    echo "<br>";
  }
}
 
piramida_fibonacci(10);

// hasil:
// 1
// 1 1
// 1 1 2
// 1 1 2 3
// 1 1 2 3 5
// 1 1 2 3 5 8
// 1 1 2 3 5 8 13
// 1 1 2 3 5 8 13 21
// 1 1 2 3 5 8 13 21 34
// 1 1 2 3 5 8 13 21 34 55
?>
```
