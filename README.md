# ADAM ASMACA V4.7.0 README FILE
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
#Adam asmaca oyunu resmi config dosyasi, elleme dedigim yerleri ellemezsen bir sorun olmaz ve "" gibi metin isaretlerini kullanmana gerek yok.

#DIKKAT ASAGIDAKI DEGERLER ASLA VE ASLA 0 YA DA FALSE OLMAMALIDIR. EGER 0 YA DA FALSE KULLANIRSANIZ KODU BOZARSINIZ.

#=======================
# === GENEL AYARLAR ====
#=======================

#Admin hesabina erisim
admin_kullanici_adi: admin
admin_sifresi: cokgizlisifre
#Guvenlik Protokolu:
#0) Guvenlik yok.
#1) En Az 8 Haneli Bir Sifre.
#2) En Az 8 Haneli, Bir rakam bulunduran sifre
#3) En Az 8 Haneli, Bir rakam bulunduran , Buyuk-kucuk harf olan sifre.
#4) En Az 8 Haneli, Bir rakam bulunduran , Buyuk-kucuk harf , Ozel Karakter Bulunduran Sifre
guvenlik_protokolu: 2

#=======================================
# === ADAM ASMACA OYUNU ICIN AYARLAR ===
#=======================================

#Oyunlar kaydediliyormu? True haric her deger False sayilir.
Oyunlar_Kaydedilsinmi: True
#Oyuna baslayan bir oyuncunun hesabina yazilan baslangic coini
Baslama_coini: 1
#Oyuncularin sahip oldugu can sayilari (default: 12,6,4)
AA_Can_Kolay: 12
AA_Can_Normal: 6
AA_Can_Zor: 4
#Oyun sonunda kelimeuzunlugu * value olarak hesaplanan coin verme islemleri
COIN_Kolay_Carpani: 2
COIN_Normal_Carpani: 5
COIN_Zor_Carpani: 10
#Harf alma bedelleri
COIN_Kolay_Harf_Alma_Bedeli: 8
COIN_Normal_Harf_Alma_Bedeli: 20
COIN_Zor_Harf_Alma_Bedeli: 40

#===============================
# === KKB OYUNU ICIN AYARLAR ===
#===============================

#Bu oyunda kayit dosyasi olusmaz. icine yazilcak veri yetersizdir.

#Oyun sureleri (default: 45,30,15)
KKB_Sure_Kolay: 45
KKB_Sure_Normal: 30
KKB_Sure_Zor: 15

#Tur sonunda Kalan Sure * value olarak hesaplanan coin verme islemleri
#Burada Kazanilan coinler adam asmaca oyununda kullanilabilecek.
COIN_Kolay_Carpani_KKB: 1
COIN_Normal_Carpani_KKB: 2
COIN_Zor_Carpani_KKB: 4

#Bunu elleme.
config_version: 4.6.1_PB_RLS_IUAFma
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
## Özel Yazma Efekti:
    Oyun içine özel olarak kodlanmış yazma efekti eklenmiştir. yazılar bir anda ekrana çıkmaktansa belirli saniyelerde yazılmaya başlanmıştır.
## Tek Proje Birden Fazla Oyun!
    Bu proje Temelde Bir Adam Asmaca Oyunu Olsada, İçerisinde 'Karıştırılan Kelimeyi Bul' Ve 'Kelime Avı' İsimli 2 Tane Daha Oyun Vardır Bunlarada Göz Atmayı Unutmayın!
## Karıştırılan Kelimeyi Bul (KKB)
    Bu Oyun 3 farklı zorluk seviyesine sahiptir (kolay-orta-zor) bu zorluk seviyelerine göre oyun zorlugu belirlenir
    örneğin: kolay modda oynuyorsanız 45 saniye süre içerisinde 'belirli' bir kategoriden seçilen kelimenin doğru yazılmış halini bulmanız gerekir
    kelime = elma ise mlae olarak ekrana çıkar ve kategori = yiyecek olabilir zorluk seviyelerinin tüm özellikleri [config.yaml](config.yaml) dosyasından düzenlenebilir.
## Kelime Avı Oyunu (KA)
    Bu Oyunda 4 Farklı Zorluk Seviyesi Vardır (eğitim-normal-zor-imkansız)
    eğitim modunda coin kazanılamaz.
    diğer modlar için oyun 'tanımı' verilen kelimeyi kategori vs verilmeden bulmaya çalışmaktır örneğin kelime okul ise oyun aşağıdaki gibi görünür:
        + _ _ _ _
        + Kelime Tanımı: Eğitim Görülen Yer.
        + Bu Hangi Kelime ? (Bir Harf Ya da Kelime Tahmin Et: )




## Lisans

[MIT](https://choosealicense.com/licenses/mit/)