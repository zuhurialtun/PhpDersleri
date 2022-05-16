![php](https://programlamadilleri.net/wp-content/uploads/2021/05/PHP-1.png)
# PhpDersleri

## Çalışma Ortamı

Php ortamında geliştirme yapmak için öncelikle ihtiyacımız olan; web sunucusu, php yorumlayıcı ve mysql veritabanı sunucusunun kurulumunu sağlamalıyız. Bu çalışma ortamını sağlayabilmemiz için geliştirilmiş uygulamalardan birini bilgisayarınıza yükleyebilirsiniz.
#### Uygulamalar
- [MAMP Server](https://www.mamp.info/en/downloads/)
- [XAMPP](https://www.apachefriends.org/tr/index.html)
- [WAMP Server](https://www.wampserver.com/en/)

## Php Dosyası Oluşturmak

#### Dosyanın Oluşturulacağı Dizin

- Php dosyamızı oluşturacağımız dizin:  **C:\xampp\htdocs**
- İlk olarak bulunduğumuz dizine bir klasör açmamız gerekiyor.
- Klasörümüzün ismi FirstProject olsun.
- Oluşturacağımız ilk dosyanın adı index.php dir. İndex.php dosyası Web sayfamız açıldığında ilk olarak görüntülenecek olan sayfadır.

## Php Etiketleri, Yazım Kuralları ve Açıklama Satırları
PHP oluşturduğumuz bir dosyayı çözümlerken, hangi bölümü yorumlayıp hangi bölümü yorumlamadan geçmesi gerektiğine karar vermek için php açılış ve kapanış etiketlerine bakar.

#### Echo ve Print
```
<?php 
    echo "Merhaba Dünya";
    print "Merhaba Dünya";
?>
```
"echo ve print" komutları kendinden sonra gelen ifadeyi ekrana yazdırmak için kullanılır.

#### Yazım Kuralları

```
<?php 
    echo "Birinci echo komutu";
    echo "İkinci echo komutu";
    echo "Üçüncü echo komutu";
?>
```
Php etiketleri arasına yazılan tüm komutların noktalı virgül( ; ) ile sonlandırılması gerekir. Aksi taktirde komut satırının nerede bittiği anlşılamaz ve kod hatalı çalışabilir.

#### Html içerisinde Gömülü Php Kullanımı
```
<?php
 $title = 'Php Basics';
?>

<h1><?= $title ?></h1>

<?= echo '<h3>' . $title . '</h3>'; ?>

<?= echo "<h5>$title</h5>"; ?>
```

#### Açıklama Satırları
PHP, 'C', 'C++' ve Unix kabuk tarzı (Perl tarzı) açıklamaların hepsini destekler.
```
<?php
    // Bu tek satırlık c++ tarzı açıklamadır
    
    /* Bu, C tarzı 
    çok satırlı
       bir açıklamadır */
    
    # Bu tek satırlık kabuk tarzı açıklamadır.
?>
```

## Değişkenler
#### Değişkenler
PHP'de bir değişken tanımlamak için dolar işareti ($) ardından da değişken adı ile yazılarak tanımlama yapılır.
- Değişken adı büyük-küçük harf duyarlıdır.
- Türkçe karakter içerebilir.
- Tüm veri tiplerini tutabilir.
- Harf ve alt çizgi ile başlar.
- Atama operatörü(=) ile değer ataması yapılır.
- $this atama yapılamayan özel bir değişkendir.(OOP derslerimizde ne anlama geldiğinden bahsediyor olacağız.)

```
$ad = "Osman BAKIRCI";
echo "Benim adım $ad";

$para = 50;
echo "Cebimdeki para $para TL";
```

#### Sabitler
Bir sabit tanımlamak için define() işlevi kullanılır. Sabit tanımlandıktan sonra asla değiştirilemez ve tanımsız yapılamaz.
- Harf ve alt çizgi ile başlar.
- Obje hariç tüm veri tiplerini tutabilir.
- Sayı ile başlayamaz.
- Türkçe karekter içerebilir.
- Geleneksel olarak, sabit isimleri daima büyük harfle yazılır.

```
define('SABIT_ADI','TUTULACAK_DEGER');
echo SABIT_ADI;
```

#### Veri Türleri
Php birden fazla veri türü içerir. Bunlar benzer şekilde tanımlansa da hepsi de birbirinden farklı amaçlar için kullanılır. Bir ifadenin değerinin ve türünün ne olduğuna öğrenmek istediğinizde var_dump() işlevini kullanabilirsiniz. Hata ayıklama amacıyla bir değişkenin türünü öğrenmek için ise gettype() işlevini kullanabilirsiniz.
- String "Şahin Ersever" 'Test' '3' "2"
- Integer 100 255
- Float(Double) 2.5
- Boolean(true, false)
- Array(Dizi) ['a','b'], array(1,2)
- Object(Nesne)
- NULL

```
$a_bool = TRUE;   // boolean türünde
$a_str  = "Şahin ERSEVER";  // string türünde
$a_str2 = 'Patika';  // string türünde
$an_int = 27;     // integer  türünde

echo gettype($a_bool); // boolean basar
echo gettype($a_str);  // string basar
```

## Operatörler
#### Aritmetik Operatörler
**Operatörler**
- Toplama (+)
- Çıkartma (–)
- Çarpma (*)
- Bölme (/)
- Mod (%)
Aritmetik operatörler matematikte olduğu gibi işlem sırasına göre çalışır. Önce Parantez içleri, çarpma/bölme ve toplama çıkarma işlemleri sırasıyla uygulanır.

**Toplama Operatörü:** (+) bir değişkeni ya da bir sayıyı, başka bir değişken ya da bir sayı ile toplamak için kullanılır.
```
<?php
 
$num1 = 4; // "num1" değişkenine 4 sayısını atar
$num2 = 3; // "num2" değişkenine 3 sayısını atar
 
$total = $num1 + $num2; // Sonuç 7 olur
$toplam = $num1 + 2; // Sonuç 6 olur
```

**Çıkarma Operatörü:** Çıkarma operatörü (-) bir değişkeni ya da bir sayıyı başka bir değişken yada sayıdan çıkarmak için kullanılır.
```
<?php
$num1 = 8; // "num1" değişkenine 8 değerini atar
$num2 = 2; // "num2" değişkenine 2 değerini atar
$result = $num1 - $num2; // Sonuç 6 Olur
$result = $num1 - 1; // Sonuç 7 olur.
```

**Çarpma Operatörü:** Çarpma operatörü (*) bir değişkeni ya da sayıyı başka bir değişken ya da sayı ile çarpmak için kullanılır.
```
<?php
$num1 = 2; // "num1" değişkenine 2 değerini atar
$num2 = 8; // "num2" değişkenine 82 değerini atar
$result = $num1 * $num2; // Sonuç 16 Olur
$result = $num1 * 2; // Sonuç 4 olur.
```

**Bölme Operatörü:** Bölme operatörü (/) bir değişkeni ya da sayıyı, başka bir değişkene ya da sayıya bölmek için kullanılır.
```
<?php
$num1 = 6; // "num1" değişkenine 6 değerini atar
$num2 = 3; // "num2" değişkenine 2 değerini atar
$result = $num1 / $num2; // Sonuç 2 olur
$result = $num1 / 2; // Sonuç 3 olur.
```

**Mod (Kalan) Operatörü:** (%) bir değişkenin ya da sayının, başka bir değişkene yada sayıya tam sayı şeklinde bölünmesinden sonra kalanını almak için kullanılır.
```
<?php
$num1 = 5; // "num1" değişkenine 5 değerini atar
$num2 = 3; // "num2" değişkenine 2 değerini atar
$result = $num1 % $num2; // Sonuç 2 olur
$result = $num1 % 4; // Sonuç 1 olur.
```

#### Karşılaştırma Operatörleri
Bu operatörler matematiksel olarak yaptıklarımızı programlama alanında yaparlar. Operatörlerimiz;
```
$a = 3;
$b = 4;

echo $a == $b; // Sonuç: false
echo $a === $b; // Sonuç: false
echo $a != $b; // Sonuç: true
echo $a !== $b; // Sonuç: true
echo $a < $b; // Sonuç: true
echo $a > $b; // Sonuç: false
echo $a <= $b; // Sonuç: true
echo $a >= $b; // Sonuç: false
echo $a <=> $b; // Sonuç: -1

```

#### Artırma ve Azaltma Operatörleri
Artırma ve azaltma operatörleri kısaca sayı değerlerini artırmak ve azaltmak için kullanılır.
**Operatörler**
- Artırma Operatörü (++)
- Azaltma Operatörü (--)
```
$a = 1;
$a++;
echo $a; // Ekrana 2 sonucunu yazar.

$a = 5;
echo ++$a; // Ekrana 6 sonucunu yazar.
echo $a; // Ekrana 6 sonucunu yazar.

$a = 5;
echo $a++; // Ekrana 5 sonucunu yazar.
echo $a; // Ekrana 6 sonucunu yazar.

$a = 5;
echo --$a; // Ekrana 4 sonucunu yazar.
echo $a; // Ekrana 4 sonucunu yazar.

$a = 5;
echo $a--; // Ekrana 5 sonucunu yazar.
echo $a; // Ekrana 4 sonucunu yazar.
```

#### Birleştirme ve Atama Operatörleri
**Birleştirme Operatörü**
Birleştirme operatörü nokta(.) ile gösterilir. İki ifadenin arasında yer alarak sağında bulunan ifade ile solunda bulunan ifadeyi birbirine birleştirir.
```
$isim = 'Osman';
$soyisim = 'KALAYCI';
$yas = 29;
echo 'Merhaba, benim ismim '. $isim.' soyismim '.$soyisim.'. Şuan '.$yaş.' yaşımdayım.';

// Ekrana "Merhaba, benim ismim Osman soyismim KALAYCI. Şuan 29 yaşımdayım." sonucunu yazar.

$html  = '<div>';
$html .=    '<h1>Herkese Merhaba</h1>';
$html .= '</div>';
echo $html;

// Ekrana "Herkese Merhaba" olarak basar.
```
**Atama Operatörü**
Atama operatörü matematikten de tanıdığımız eşittir (=) sembolüdür. Bu operatör sağında bulunan değeri solunda bulunan değişkene atar.
```
$yas = 29; // $yas değişkenine 29 sayısı atandı.
$isim = 'Osman'; $isim değişkenine Osman ifadesi atandı.
```
#### Mantıksal Operatörler

## Koşullu İfadeler
## Diziler
## Döngüler
## Fonksiyonlar


## Alıntılar
> - [Patika Web Sitesi](https://app.patika.dev)