## Membuat deret angka 1 ke n kebawah ex:1-9
```php
<?php
for($i=1; $<10; $i++){
    echo $i . "<br>";
}
?>
```
## Membuat deret angka piramida
1
22
333
4444
55555
666666
7777777
88888888
999999999
```php
<?php
$number = 5;

for ($i = 1; $i <= $number; $i++) {
    for ($j = $number; $j >= 1; $j--) {
        if ($i < $j) {
            echo '-';
        } else {
            echo $i;
        }
    }

    echo "<br>";
}
?>
