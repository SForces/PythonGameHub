# ADAM ASMACA V4.5.0 README FILE
Tr: Bu Adam Asmaca Oyunu İçin bir beni oku dosyasıdır

## Kurulum
TR:
Kurulum için dizindeki [setup.py](setup.py) dosyasını çalıştırmanız gerekmektedir, bu dosya kurulum sırasında [PyYaml](https://pypi.org/project/PyYAML/) kütüphanesini kuracaktır. bunu önceden siz yapmak isterseniz;

```bash
pip install pyyaml
```
# NASIL OYNANIR?
Kurulum sonrasında tek yapmanız gereken [game.py](game.py) Dosyanızı çalıştırıp [Kayıt](game.py#L135) Olmanızdır.
Sonrasında oyunu oynamaya başlayabilirsiniz.

# ÖZELLİKLER
## Her Kullanıcı için farklı login/signup özelliği

Kullanıcılar giriş yaparak hesaplarını kaybetmezler.

## Admin Modu:

	1) oyun dosyalarina eris ve onlari degistir.

	2) kategoriye yeni kelime ekle

	3) yeni kategori ekle

	4) admin modunda oyun oyna (kaydedilmez)

	5) oyun çalıştırma özelliklerini görüntüle (temel değerleri tek seferde ekrana yazar.)

    6) Author.ini Dosyasını oku.

    7) Oyun Dosya Konumlarını Al.

## CONFIG DOSYASI

Oyunun tüm ayarlarının editleyebileceğiniz bir config dosyası

Example Config;
```yaml
admin_kullanici_adi: admin
admin_sifresi: cokgizlisifre

#Oyunlar kaydediliyormu? True haric her deger False sayilir.
Oyunlar_Kaydedilsinmi: True

#Oyuna baslayan bir oyuncunun hesabina yazilan baslangic coini. DIKKAT BU DEGER VE ASAGIDAKI DEGERLER ASLA VE ASLA 0 YA DA FALSE OLMAMALIDIR. YUKARIDAKI DEGER ICIN TRUE DISI BIR SEY YAZMANIZ YETERLIDIR EGER 0 YA DA FALSE KULLANIRSANIZ KODU BOZARSINIZ.
Baslama_coini: 1

#Oyun sonunda kelimeuzunlugu * value olarak hesaplanan coin verme islemleri
COIN_Kolay_Carpani: 2
COIN_Normal_Carpani: 5
COIN_Zor_Carpani: 10

#Harf alma bedelleri
COIN_Kolay_Harf_Alma_Bedeli: 8
COIN_Normal_Harf_Alma_Bedeli: 20
COIN_Zor_Harf_Alma_Bedeli: 40

#Guvenlik Protokolu:
#0) Guvenlik yok.
#1) En Az 8 Haneli Bir Sifre.
#2) En Az 8 Haneli, Bir rakam bulunduran sifre
#3) En Az 8 Haneli, Bir rakam bulunduran , Buyuk-kucuk harf olan sifre.
#4) En Az 8 Haneli, Bir rakam bulunduran , Buyuk-kucuk harf , Ozel Karakter Bulunduran Sifre
guvenlik_protokolu: 2

#Bunu elleme.
config_version: 4.5.0_PB_RLS_BqUtsZ985
```


### OYUN MODU SECIMI

-En Kolay Mod: 

    12 can hakki   
    kategoriler belirli  
    kalan can * 5 Puan Carpani 
    [örn 1 canınız kaldığında: 5P]
    Harf Alma Bedeli = config

-Orta Seviye Mod:

    6 can hakki    
    kategoriler belirli    
    kalan can * 10 Puan Carpani
    [örn 2 canınız kaldığında: 20P]
    Harf Alma Bedeli = config
-Zor Mod:

    4 can hakki
    kategoriler belirsiz
    kalan can * 30 Puan Carpani [örn 4 canınız kaldığında:120P]
    Harf Alma Bedeli = config

Yukarıda gördüğünüz can haric tüm değerler config.yaml dosyasından editlenebilir.


## Gerçekçi bir Adam Asmaca Oyunu
	+ Adam can sayiniza göre ekranda asılır.
	+ kelimenin kaç harfli olduğu _ ile gösterilir örn kelime elma ise --» _ _ _ _
	+ kalan can sayınıza göre puan hesaplanır
	+ kazandığınız / kaybettiğiniz oyunlar saklanır

## Oyunlar aşağıdaki formatta kaydedilir:
```yaml
    Oyun -> <tarih>-<saat>:
        Oyun zorluk modu: <>
        Kazanilan Oyun Sayisi: <>
        Kaybedilen Oyun Sayisi: <>
        Kazanilan Puan: <>
        Oyun Suresi: <saat-dakika-saniye>
```

## Dosya konumları:
    Hesaplar --» data/main/accounts.txt (format = <username>?<password>)
    Kategoriler --» data/main/categories/ (klasörün içeriğinde tüm kategoriler mevcuttur, all.txt dosyası tüm kategori isimlerini içerir)
    Kayıt dosyaları --» data/player.saves/<username>.txt
## Coin sistemi:
	Her maç başına bulunan kelimenin harfleri * <zorluk katsayısı> kadar coin kazanılır bu coinle !harfal komutu ile gizlenmiş bir harf ortaya çıkartılabilir.
## İstatistikler:
	Giriş bölümünde istatistikleri görebilme özelliği.

    Ex;
```yaml
XoX Adli Oyuncunun Istatistikleri:
Kazanilan toplam oyun sayisi: 1
Kaybedilen toplam oyun sayisi: 0
Oyun icinde gecirilen toplam sure: 1:20
Kazanilan toplam puan: 105
Hesaptaki anlik coin: 950
```
## Renkli Bir Oyun Deneyimi:
    Oyun Tamamen Renklendirilmiş ve ASCII ART Kullanılarak süslenmiştir.


## Lisans

[MIT](https://choosealicense.com/licenses/mit/)
