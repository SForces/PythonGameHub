# <span style="color: #FF0000;">**PYTHON GAME HUB V6.0.3 - README**</span>
<span style="color: #87CEEB">Bu Python Game Hub Projesi İçin Bir Beni Oku Dosyasıdır.</span>

# <span style="color: #007FFF;">**Kurulum**</span>
<span style="color: #87CEEB">Bu BETA sürümünde cihazınızda python ya da diğer yan kaynak uygulamalarının yüklü olmasına gerek yoktur tüm özellikler 1 .exe dosyasında toplanmıştır. [PGH_Client_V6.0.3](https://github.com/SForces/PythonGameHub/releases/download/PGHV6_0_3/PGH_Client_V6.0.3.exe)
\
Kurulum için [PGH_Client_V6.0.3](https://github.com/SForces/PythonGameHub/releases/download/PGHV6_0_3/PGH_Client_V6.0.3.exe) Dosyasınız çalıştırmanız yeterli olucaktır gerekli yönergeleri dosyadan takip edebilirsiniz.
</span>

# <span style="color: #007FFF;">**NASIL OYNANIR?**</span>
<span style="color: #87CEEB">Kurulum sonrasında tek yapmanız gereken [PGH_Client_V6.0.3](https://github.com/SForces/PythonGameHub/releases/download/PGHV6_0_3/PGH_Client_V6.0.3.exe) Dosyanızı çalıştırıp `Kayıt` Olmanızdır.
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
#  _______     _________ _    _  ____  _   _     _____          __  __ ______ _    _ _    _ ____   __      ____   ___   ___  
# |  __ \ \   / /__   __| |  | |/ __ \| \ | |   / ____|   /\   |  \/  |  ____| |  | | |  | |  _ \  \ \    / / /  / _ \ / _ \ 
# | |__) \ \_/ /   | |  | |__| | |  | |  \| |  | |  __   /  \  | \  / | |__  | |__| | |  | | |_) |  \ \  / / /_ | | | | | | |
# |  ___/ \   /    | |  |  __  | |  | | . ` |  | | |_ | / /\ \ | |\/| |  __| |  __  | |  | |  _ <    \ \/ / '_ \| | | | | | |
# | |      | |     | |  | |  | | |__| | |\  |  | |__| |/ ____ \| |  | | |____| |  | | |__| | |_) |    \  /| (_) | |_| | |_| |
# |_|___  _|_| _ __|_| _|_|  |_|\____/|_| \_|___\_____/_/_ _ \_\_|__|_|______|_|  |_|\____/|____/      \/  \___(_)___(_)___/ 
#  / ____|  / __ \  | \ | | |  ____| |_   _|  / ____|                                                            
# | |      | |  | | |  \| | | |__      | |   | |  __                                                             
# | |      | |  | | | . ` | |  __|     | |   | | |_ |                                                            
# | |____  | |__| | | |\  | | |       _| |_  | |__| |                                                            
#  \_____|  \____/  |_| \_| |_|      |_____|  \_____|                                                            
                                                                                                                
#Elleme dedigim yerleri ellemezsen bir sorun olmaz
# Degerler 'float' - 'string' turunde olamazlar program duzgun calismayacaktir ya da algilayabilirse size hata mesajını verir.
#desteklenen degerler: (bool , integer)[(bool = True yazdiginiz yerler)]
#Ve Son olarak kesinlikle degerleri yazarken 0 veya False kullanma kodu bozabilir.

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

#Oyuncularin sahip oldugu can sayilari (default: kolay: 12,normal: 6,zor: 4)
AA_Can_Kolay: 12
AA_Can_Normal: 6
AA_Can_Zor: 0
#Oyun sonunda (kelime uzunlugu * asagidaki deger) olarak hesaplanan coin verme islemleri
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

#ADAM ASMACA OYUNU HARIC OYUNLARDA KAYIT DOSYASI YAZILMAZ. (YAN OYUN OLARAK GORULUR)

#Modlara gore can degerleri (default: 8,4,1) _Egitim Modunda Can Sinirsizdir Bu Yuzden Burada Yok.
KA_Can_Normal: 8
KA_Can_Zor: 4
KA_Can_Imkansiz: 1

#Modlara Gore Coin Carpani (Kalan Can * asagidaki deger)
KA_CoinCarp_Normal: 4
KA_CoinCarp_Zor: 10
KA_CoinCarp_Imkansiz: 50 
#Asagidaki Degisken Sonsuz Oyun Modu Icindir Bunun Coini Bulunan Kelime * asagidaki deger Olarak hesaplanir. buna dikkat etmelisiniz.
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

#Oyun Sureleri (SN); default (kolay: 45,normal: 30,zor: 15)
KKB_Sure_Kolay: 45
KKB_Sure_Normal: 30
KKB_Sure_Zor: 15
#Kazanma Durumunda Alinacak Coin = (kalan sure * asagidaki deger)
KKB_wincoin_kolay: 1
KKB_wincoin_normal: 2
KKB_wincoin_zor: 3

# ==============================
# === TSB OYUNU ICIN AYARLAR ===
# ==============================

#Seviyeye Gore Can Sayilari:
TSB_Cok_Kolay_Can: 10
TSB_Kolay_Can: 7
TSB_Normal_Can: 5
TSB_Zor_Can: 3

#Seviyeye Gore alinacak coin carpani (Kalan can * asagidaki deger)
TSB_Cok_Kolay_Coin_Carpani: 1
TSB_Kolay_Coin_Carpani: 2
TSB_Normal_Coin_Carpani: 3
TSB_Zor_Coin_Carpani: 4

#         ===========================
#         === ALT SISTEM AYARLARI ===
#         ===========================

# Asagidaki ayarlari aktif etmek icin baslarindaki # isaretini silmeniz yeterlidir. program algilayacaktir.

# =============
# === EKRAN ===
# =============

# KULLANMAK ICIN 'pyautogui' KUTUPHANESINI INDIRIR!!!
# Bu Ayar her acilista programi Tam ekran modunda baslatir.
#FULL_SCREEN: True

#Log dosyasi olussunmu ?
#log_files: True
#[SADECE YUKARIDAKI DEGER 'True' OLDUGUNDA CALISIR] log dosyasindaki 1 gunluk kaydin alabilecegi maksimum satir sayisi.
log_file_max_lines: 600
#Bunu elleme.
config_version: PGH_6.0.0_DKCusxnxcudcg_Config_XDFECVDUN
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

<span style="color: #E9967A;">Yukarıda gördüğünüz can dahil tüm değerler config.yaml dosyasından editlenebilir.</span>


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
    Bu proje Temelde Bir Adam Asmaca Oyunu Olsada, İçerisinde 'Kelime Avı' , 'Karıştırılmış Kelimeyi Bul' ve 'Tutulan Sayıyı Bul (TSB)' İsimli 3 Tane Daha Oyun Vardır Bunlarada Göz Atmayı Unutmayın!
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

## <span style="color: orange;">**Tutulan Sayıyı Bul Oyunu (TSB)**</span>
    5 Farklı Zorluk Seviyesi (Çok Kolay - Kolay - Normal - Zor - Sonsuz)
    1,2,3,4;
        Canlarınız bitmeden önce tutulan sayıyı bulun ve coin kazanın.
    5;
        Kendi belirlediğiniz sayı aralığında sonsuz can ile sayınızı arayın.
## <span style="color: red;">**Lisans**</span>
<br>
<span style= "color: red;">© 2023 SForces GNU 2.0</span>

[LICENSE](https://github.com/SForces/PythonGameHub/blob/main/LICENSE)
