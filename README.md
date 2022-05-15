![php](https://programlamadilleri.net/wp-content/uploads/2021/05/PHP-1.png)
# PhpDersleri
---
## Çalışma Ortamı

Php ortamında geliştirme yapmak için öncelikle ihtiyacımız olan; web sunucusu, php yorumlayıcı ve mysql veritabanı sunucusunun kurulumunu sağlamalıyız. Bu çalışma ortamını sağlayabilmemiz için geliştirilmiş uygulamalardan birini bilgisayarınıza yükleyebilirsiniz.
### Uygulamalar
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






## Alıntılar
- [Patika Web Sitesi](https://app.patika.dev/courses/php-temel/yazim-kurallari)