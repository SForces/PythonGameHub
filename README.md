# <span style="color: #FF0000;">**ADAM ASMACA V5.0.0 README FILE**</span>
<span style="color: #87CEEB">Bu Adam Asmaca Oyunu İçin bir beni oku dosyasıdır</span>

## <span style="color: #007FFF;">**Kurulum**</span>
<span style="color: #87CEEB">Kurulum için dizindeki [setup.py](setup.py) dosyasını çalıştırmanız gerekmektedir, bu dosya kurulum sırasında [PyYaml](https://pypi.org/project/PyYAML/),[TimePrint](https://pypi.org/project/TimePrintOnPYPI/) Ve [Colorama](https://pypi.org/project/colorama/) Kütüphanelerini kuracaktır. bunu önceden siz yapmak isterseniz;</span>

```bash
pip install pyyaml
pip install TimePrintOnPYPI
pip install colorama
```
# <span style="color: #007FFF;">**NASIL OYNANIR?**</span>
<span style="color: #87CEEB">Kurulum sonrasında tek yapmanız gereken game.py Dosyanızı çalıştırıp Kayıt Olmanızdır.
Sonrasında oyunu oynamaya başlayabilirsiniz.</span>

# <span style="color: yellow;">**ÖZELLİKLER**</span>

## <span style="color: orange;">**Her Kullanıcı için farklı login/signup özelliği**</span>

<span style="color: #E9967A;">Kullanıcılar giriş yaparak hesaplarını kaybetmezler.</span>

## <span style="color: orange;">**Şifre Oluşturucu!**</span>

<span style="color: #E9967A;">5.0.0 Güncellemesiyle eklenen kayıt olurken seçenek olarak çıkan 'şifre oluşturucu'!</span>

## <span style="color: orange;">**Admin Modu**:</span>
<span style="color: #E9967A;">

	1) oyun dosyalarina eris ve onlari degistir.

	2) kategoriye yeni kelime ekle

	3) yeni kategori ekle

	4) admin modunda oyun oyna (kaydedilmez)

	5) oyun çalıştırma özelliklerini görüntüle (temel değerleri tek seferde ekrana yazar.)

    6) Author.ini Dosyasını oku.

    7) Oyun Dosya Konumlarını Al.
</span>

## <span style="color: orange;">**CONFIG DOSYASI**</span>

<span style="color: #E9967A;">Oyunun tüm ayarlarının editleyebileceğiniz bir config dosyası<br>
Örnek Config;</span>

```yaml
#           _____          __  __             _____ __  __          _____            __      _______  ___   ___  
#     /\   |  __ \   /\   |  \/  |     /\    / ____|  \/  |   /\   / ____|   /\      \ \    / / ____|/ _ \ / _ \ 
#    /  \  | |  | | /  \  | \  / |    /  \  | (___ | \  / |  /  \ | |       /  \      \ \  / /| |__ | | | | | | |
#   / /\ \ | |  | |/ /\ \ | |\/| |   / /\ \  \___ \| |\/| | / /\ \| |      / /\ \      \ \/ / |___ \| | | | | | |
#  / ____ \| |__| / ____ \| |  | |  / ____ \ ____) | |  | |/ ____ \ |____ / ____ \      \  /   ___) | |_| | |_| |
# /_/____\_\_____/_/ _  \_\_|__|_|_/_/____\_\_____/|_|  |_/_/    \_\_____/_/    \_\      \/   |____(_)___(_)___/ 
#  / ____|  / __ \  | \ | | |  ____| |_   _|  / ____|                                                            
# | |      | |  | | |  \| | | |__      | |   | |  __                                                             
# | |      | |  | | | . ` | |  __|     | |   | | |_ |                                                            
# | |____  | |__| | | |\  | | |       _| |_  | |__| |                                                            
#  \_____|  \____/  |_| \_| |_|      |_____|  \_____|                                                            
                                                                                                                
#Elleme dedigim yerleri ellemezsen bir sorun olmaz
#"" gibi metin isaretlerini Kesinlikle Kullanmamalisin.
#Ve Son olarak kesinlikle degerleri yazarken 0 veya false kullanma kodu bozabilir.

#=======================
# === GENEL AYARLAR ====
#=======================

#Admin hesabina erisim
admin_kullanici_adi: admin
admin_sifresi: cokgizlisifre
#Guvenlik Protokolu:
#0) Guvenlik yok.
#1) En Az 8 Haneli Bir Sifre.
#2) En Az 8 Haneli, Bir rakam Ve Harf bulunduran sifre
#3) En Az 8 Haneli, Bir rakam bulunduran , Buyuk+kucuk harf olan sifre.
#4) En Az 8 Haneli, Bir rakam bulunduran , Buyuk+kucuk harf , Ozel Karakter Bulunduran Sifre
#5) En Az 16 Haneli, Bir rakam bulunduran , Buyuk+kucuk harf , Ozel Karakter Bulunduran Sifre
guvenlik_protokolu: 2
#Oyuna baslayan bir oyuncunun hesabina yazilan baslangic coini
Baslama_coini: 1
#Oyunlar kaydediliyormu? True haric her deger False sayilir.
Oyunlar_Kaydedilsinmi: True
#Oyunda Renk kodlari kullaniliyormu ? True haric her deger False Sayilir.
Oyunda_Renkler_Aktif_Ediliyormu: True

#=======================================
# === ADAM ASMACA OYUNU ICIN AYARLAR ===
#=======================================

#Oyuncularin sahip oldugu can sayilari (default: 12,6,4)
AA_Can_Kolay: 12
AA_Can_Normal: 6
AA_Can_Zor: 0
#Oyun sonunda kelimeuzunlugu * value olarak hesaplanan coin verme islemleri
COIN_Kolay_Carpani: 2
COIN_Normal_Carpani: 5
COIN_Zor_Carpani: 10
#Harf alma bedelleri
COIN_Kolay_Harf_Alma_Bedeli: 8
COIN_Normal_Harf_Alma_Bedeli: 20
COIN_Zor_Harf_Alma_Bedeli: 40

#================================
# === KELIME AVI ICIN AYARLAR ===
#================================

#Bu oyunda kayit dosyasi olusmaz. icine yazilcak veri yetersizdir.

#Modlara gore can degerleri (default: 8,4,1) _Egitim Modunda Can Sinirsizdir Bu Yuzden Burada Yok.
KA_Can_Normal: 8
KA_Can_Zor: 4
KA_Can_Imkansiz: 1

#Modlara Gore Coin Carpani (Kalan Can * value)
KA_CoinCarp_Normal: 4
KA_CoinCarp_Zor: 10
KA_CoinCarp_Imkansiz: 50 
#Asagidaki Degisken Sonsuz Oyun Modu Icindir Bunun Coini Bulunan Kelime * value Olarak hesaplanir. buna dikkat etmelisiniz.
KA_CoinCarp_Inf: 10
#Sonsuz Moddaki Oyun Kac SANIYE Surecek ? [gireceginiz deger 0 dan kucuk olursa 120 olarak sifirlanir.]
KA_GameTime_Inf: 120
#Modlara Gore Harf Alma Bedelleri;
KA_GetWord_Price_Normal: 10
KA_GetWord_Price_Zor: 20
KA_GetWord_Price_Imkansiz: 35

# ==============================
# === KKB OYUNU ICIN AYARLAR ===
# ==============================

#Oyun Sureleri (SN); default (45,30,15)
KKB_Sure_Kolay: 45
KKB_Sure_Normal: 30
KKB_Sure_Zor: 15
#Kazanma Durumunda Alinacak Coin = (kalan sure * value)
KKB_wincoin_kolay: 1
KKB_wincoin_normal: 2
KKB_wincoin_zor: 3

#Bunu elleme.
config_version: 5.0.0_PB_RLS_YsTaRZshNSFFNEXTfuvTXB
```


### <span style="color: orange;">**OYUN MODU SECIMI (ADAM ASMACA)**</span>

<span style="color: #E9967A;">**En Kolay Mod:**<span>

    12 can hakki   
    kategoriler belirli  
    kalan can * 5 Puan Carpani 
    [örn 1 canınız kaldığında: 5P]
    Harf Alma Bedeli = config

<span style="color: #E9967A;">**Orta Seviye Mod:**</span>

    6 can hakki    
    kategoriler belirli    
    kalan can * 10 Puan Carpani
    [örn 2 canınız kaldığında: 20P]
    Harf Alma Bedeli = config
<span style="color: #E9967A;">**Zor Mod:**</span>

    4 can hakki
    kategoriler belirsiz
    kalan can * 30 Puan Carpani 
    [örn 4 canınız kaldığında:120P]
    Harf Alma Bedeli = config

<span style="color: #E9967A;">Yukarıda gördüğünüz can haric tüm değerler config.yaml dosyasından editlenebilir.</span>


## <span style="color: orange;">**Gerçekçi bir Adam Asmaca Oyunu**</span>
	+ Adam can sayiniza göre ekranda asılır.
	+ kelimenin kaç harfli olduğu _ ile gösterilir örn kelime elma ise --» _ _ _ _
	+ kalan can sayınıza göre puan hesaplanır
	+ kazandığınız / kaybettiğiniz oyunlar saklanır

## <span style="color: orange;">**Oyunlar aşağıdaki formatta kaydedilir:**</span>
```yaml
    Oyun -> <tarih>-<saat>:
        Oyun zorluk modu: <>
        Kazanilan Oyun Sayisi: <>
        Kaybedilen Oyun Sayisi: <>
        Kazanilan Puan: <>
        Oyun Suresi: <saat-dakika-saniye>
```

## <span style="color: orange;">**Dosya konumları:**</span>
    Hesaplar --» data/main/accounts.txt (format = <username>?<password>)
    Kategoriler --» data/main/categories/ (klasörün içeriğinde tüm kategoriler mevcuttur, all.txt dosyası tüm kategori isimlerini içerir)
    Kayıt dosyaları --» data/player.saves/<username>.txt
## <span style="color:orange;">**Coin sistemi:**</span>
	Her maç başına bulunan kelimenin harfleri * <zorluk katsayısı> kadar coin kazanılır bu coinle !harfal komutu ile gizlenmiş bir harf ortaya çıkartılabilir.
## <span style="color: orange;">**İstatistikler:**</span>
	Giriş bölümünde istatistikleri görebilme özelliği.

    Örn;
```yaml
XoX Adli Oyuncunun Istatistikleri:
Kazanilan toplam oyun sayisi: 1
Kaybedilen toplam oyun sayisi: 0
Oyun icinde gecirilen toplam sure: 1:20
Kazanilan toplam puan: 105
Hesaptaki anlik coin: 950
```
## <span style="color: orange;">**Renkli Bir Oyun Deneyimi:**</span>
    Oyun Tamamen Renklendirilmiş ve ASCII ART Kullanılarak süslenmiştir.
## <span style="color: orange;">**Özel Yazma Efekti:**</span>
    Oyun içine özel olarak kodlanmış yazma efekti eklenmiştir. yazılar bir anda ekrana çıkmaktansa belirli saniyelerde yazılmaya başlanmıştır.
## <span style="color: orange;">**Tek Proje Birden Fazla Oyun!**</span>
    Bu proje Temelde Bir Adam Asmaca Oyunu Olsada, İçerisinde 'Kelime Avı' Ve 'Karıştırılmış Kelimeyi Bul' İsimli 2 Tane Daha Oyun Vardır Bunlarada Göz Atmayı Unutmayın!
## <span style="color: orange;">**Kelime Avı Oyunu (KA)**</span>
    Bu Oyunda 5 Farklı Zorluk Seviyesi Vardır (eğitim-normal-zor-imkansız-sonsuz)
    eğitim modunda coin kazanılamaz.
    diğer modlar için oyun 'tanımı' verilen kelimeyi kategori vs verilmeden bulmaya çalışmaktır örneğin kelime okul ise oyun aşağıdaki gibi görünür:
        + _ _ _ _
        + Kelime Tanımı: Eğitim Görülen Yer.
        + Bu Hangi Kelime ? (Bir Harf Ya da Kelime Tahmin Et: )

    Sonsuz Modda Belirlenen Sure Icerisinde Bulabildiginiz Kadar Kelimeyi Bulmaya Calisirsiniz. Config Dosyasinda Ayrıntılar vardır
## <span style="color: orange;">**Karıştırılmış Kelimeyi Bul Oyunu (KKB)**</span>
    3 Farklı Zorluk Seviyesi (kolay-orta-zor)
    Kolay Orta:
        + Kategorisi verilen Kelimeyi Süreniz Bitmeden Bulun.
    Zor:
        + Kategorisi Verilmeyen Kelimeyi Süreniz Bitmeden Bulun.


## <span style="color: red;">**Lisans**</span>

[MIT](https://choosealicense.com/licenses/mit/)
