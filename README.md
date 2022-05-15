![php](https://programlamadilleri.net/wp-content/uploads/2021/05/PHP-1.png)
# PhpDersleri
---
## Çalışma Ortamı

Php ortamında geliştirme yapmak için öncelikle ihtiyacımız olan; web sunucusu, php yorumlayıcı ve mysql veritabanı sunucusunun kurulumunu sağlamalıyız. Bu çalışma ortamını sağlayabilmemiz için geliştirilmiş uygulamalardan birini bilgisayarınıza yükleyebilirsiniz.
#### Uygulamalar
- [MAMP Server](https://www.mamp.info/en/downloads/)
- [XAMPP](https://www.apachefriends.org/tr/index.html)
- [WAMP Server](https://www.wampserver.com/en/)
---
## Php Dosyası Oluşturmak

#### Dosyanın Oluşturulacağı Dizin

- Php dosyamızı oluşturacağımız dizin:  **C:\xampp\htdocs**
- İlk olarak bulunduğumuz dizine bir klasör açmamız gerekiyor.
- Klasörümüzün ismi FirstProject olsun.
- Oluşturacağımız ilk dosyanın adı index.php dir. İndex.php dosyası Web sayfamız açıldığında ilk olarak görüntülenecek olan sayfadır.

---

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
## Koşullu İfadeler
## Diziler
## Döngüler
## Fonksiyonlar


## Alıntılar
- [Patika Web Sitesi](https://app.patika.dev)