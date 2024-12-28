# SAĞLIK MERKEZİ YÖNETİM SİSTEMİ VERİTABAN PROJESİ

## Katılımcılar

- FATMA HALİD <215260602/>
- FERHAT RAMMOK <215260618/>
- MUHAMMED ZARZOUR <215260614/>

  ## Proje hakkında

 Projemiz ; Sağlık Merkezi Yönetim Sistemi, farklı kullanıcı 
gruplarına özel yetkiler sunarak hastaların, 
doktorların, sekreterlerin ve yöneticilerin etkili bir 
şekilde görevlerini yerine getirmesini sağlar. Bu 
sistem, randevu takibi, tahlil ve reçete yönetimi gibi 
işlevleri içerirken, kullanıcıların bilgilerini güvenle 
saklamak için bir veri yedekleme mekanizmasına 
da sahiptir. Yöneticiler, doktorlar ve sekreterler 
kendi rollerine uygun işlemleri yapabilirken, 
hastalar da tahlil sonuçlarına, reçetelere ve 
randevu bilgilerine erişim sağlayabilir.

### Detaylar
Bu sistemde dört temel rol bulunmaktadır: 
Yöneticiler, Doktorlar, Sekreterler ve Hastalar. 
Sistem, her kullanıcının rolüne göre yetkiler 
tanıyarak, tüm işlemlerin güvenli ve geçerli bir 
şekilde gerçekleştirilmesini sağlar. Ayrıca, kullanıcı 
verilerine yeniden erişmesi amacıyla bir 
yedekleme sistemi bulunmaktadır.

### Yöneticiler
- Sistem, Süper Yönetici tarafından yönetilen 
bir yapıya sahiptir. Süper Yönetici, diğer tüm kullanıcılar sisteme ekleyebilir, kaldırabilir ve 
bilgilerini güncelleyebilir.
- Bütün yöneticiler, doktorların, sekreterlerin ve 
merkezde yer alan ilaçların yanı sıra doktor 
uzmanlıklarının bilgilerini de ekleyebilir, 
kaldırabilir ve güncelleyebilir.
-  Yöneticiler, doktorların izinli günlerini sisteme 
ekleyerek, bu bilgilere herkesin güvenilir 
şekilde erişebilmesini sağlar.

### Sekerterler
- Yeni hastalar için sistemde kayıt 
oluşturabilirler.
- Mevcut hastalar için güvenilir bir şekilde belirli 
bir tarih ve saat aralığında randevu 
planlayabilirler.

### Doktorlar
- Muayene sonrasında reçete yazabilir ya da 
hastadan tahlil isteyebilirler. Tahlil sonuçlarına 
göre gerekirse reçete düzenleyebilirler. 
Gerekmeyen durumlarda ne tahlil ne de reçete 
yazarlar.
- Ayrıca, doktorların izinli oldukları günler 
sisteme kaydedilerek, doktorların çalışma 
takvimi güvenilir bir biçimde yönetilir.

### Hastalar
- Aldıkları randevuların detaylarına güvenle 
ulaşabilirler.
- Yaptıkları tahlil sonuçlarına sistem üzerinden 
güvenilir şekilde erişebilirler.
- Reçetelerine ve reçetede belirtilen ilaç 
bilgilerine güvenle ulaşabilirler.

### Yedekleme Sistemi
- Sistemdeki tüm veriler, kullanıcıların 
geçerliliğini sağlamak ve güvenliğini korumak 
amacıyla düzenli olarak yedeklenir. Bu 
sayede, hasta, doktor ve diğer kritik bilgiler 
kaybolma riskine karşı güvence altına 
alınmıştır.

# E-R Diyagram

![erd yeni](https://github.com/user-attachments/assets/7a21eff1-58a9-443e-ae92-af5f1b6fcba2)

# Tablolar ve Varlık - Nitelik İlişkisi

## 1.Kullanicilar

| özellik       | Açıklama    |
|--------------|--------------|
| K_ID         | Kullanıcı ID (PK)  |
| Ad           | Kullanıcının adı    |
| Soyad        | Kullanıcının soyadı     |
| Telefon      | Kullanıcının telefonu             |
| Cinsiyet     | Kullanıcının cinsiyeti            |
| Email        | Kullanıcının e-posta adresi            |
| Sifre        | Kullanıcının şifresi              |
| Dogum tarihi | Kullanıcının doğum tarihi              |
| Yas          | Kullanıcının yaşı              |
| Rol          | Kullanıcının rolu             | 

## 2.Yoneticiler

| özellik       | Açıklama    | 
|--------------|--------------|
| Y_ID         | Yönetici ID |
| K_ID         | Kullanıcı ID (PK, FK-Kullanıcılar.kullanıcıID)|

## 3.Doktorlar

| özellik       | Açıklama    | 
|--------------|--------------|
| D_ID         | Doktor ID     |
| K_ID         | Kullanıcı ID (PK, FK-Kullanıcılar.kullanıcıID)     |
| BasUzYili   | Çalışma başlangıç yılı    |
| DeneyimYili   | Deneyim yılı    |
| Aktif   | Dokrorun aktiflik durumu     |

## 4.Hastalar

|özellik   | Açıklama |
|----------|----------|
|H_ID      | Hasta ID |
|K_ID      | Kullanıcı ID (PK, FK-Kullanıcılar.kullanıcıID)|
|Tc        | Hasta TC (PK)         |

## 5.Sekreter

|özellik   | Açıklama |
|----------|----------|
|S_ID| Sekreter ID         |
|K_ID| Kullanıcı ID (PK, FK-Kullanıcılar.kullanıcıID)           |
| Aktif   | Sekreterin aktiflik durumu     |

## 6.ilaç

|özellik   | Açıklama |
|----------|----------|
|ilac_ID   | İlaç ID (PK)         |
|Ad        | İlac adı           |
|Amaç      | İlac amacı         |
|Max yaş   | Maksimum kullanıcı yaşı        |
|Min yaş   | Minimum kullanıcı yaşı         |
|Firma     | İlacı üreten firma         |
|Tür       | İlac türü         |
|Etkin madde| İlaç içinde etkin madde         |

## 7.Uzmanlik

|özellik   | Açıklama |
|----------|----------|
|Uz_ID     | Uzmanlık kimliği (PK)          |
|Ad        | Uzmanlık adı         |
|AnaUzmanlikID | Ana uzmanlık kimliği (alt uzmanlıklar için) (FK-Uzmanlik.Uz_ID)       |

## 8.DoktorUzmanlik

|özellik   | Açıklama |
|----------|----------|
|DoktorUzmanlikID     | İlişki kimliği (PK)   |
|D_ID       | Doktor kimliği ( FK-Doktorlar.D_ID)        |
|Uz_ID | Uzmanlık kimliği (FK-Uzmanlik.Uz_ID)       |

## 9.Gunler

|özellik   | Açıklama |
|----------|----------|
|Gun_ID    | Gün ID (PK)         |
|Ad        | Gün adı         |

## 10.Randevu

|özellik   | Açıklama |
|----------|----------|
|Rnd_ID    | Randevu ID (PK)         |
|Durum     | Randevunun durumu         |
|Tarih     | Randevunun tarihi         |
|saat      | Randevunun saatı         |

## 11.Tahliller

|özellik   | Açıklama |
|----------|----------|
|Tah_ID    | Tahlil ID (PK)         |
|Ad        | Tahlil adı         |
|Max_deger | Maksimum normal değer         |
|Min_deger | Minimum normal değer         |

## 12.Istenmis_Tahliller

|özellik   | Açıklama |
|----------|----------|
|Is_Tah_id | İstenmiş tahlil ID (PK)        |
|randevu_id| Randevu ID (FK)        |
|tahlil_id | Tahlilerin ID'leri         |
|Durum     | İstenmiş tahlil durumu          |

## 13.TAHLIL_SONUCLARI

|özellik   | Açıklama |
|----------|----------|
|Tah_Sc_id | Tahlil sonuç ID (PK)        |
|Is_Tah_id | İstenmiş tahlil ID (FK)         |
|degerler  | Her tahlilnin değeri         |
|tarih     | Tahlil sonuç tarihi         |
|Aciklama  | Tahlil açıklaması         |

## 14.ALERJİLER

|özellik   | Açıklama |
|----------|----------|
|Alej_ID   | Alerji ID         |
|Turu      | Alerji türü         |
|Etk_madde | Etkileyen maddeler      |          |
|Aciklama  | Alerji açıklaması        |

## 15.HASTA_ALERJİLERİ

|özellik   | Açıklama |
|----------|----------|
|H_id      | Hasta ID  |
|alerji_id | Alerji ID    |
|açıklama  | Hasta alerjiler açıklaması         |

## 16.LOG

|özellik   | Açıklama |
|----------|----------|
|Log_id          | Log ID         |
|K_id        | Kullanıcı ID|
|işlem       | Yapildığı işlem         |
|tarih       | Log tarihi         |
|detay       | Log hakkında detaylar         |

# Varlıklar-ilişkiler tablosu
|Varlık 1  | Varlık 2 | ilişki Türü|
|----------|----------|------------|
| Kullanicilar          |  Hastalar        |  Bir (1, 1)         |
|    Kullanicilar      |    Sekreter      |  Bir (1, 1)          |
| Kullanicilar         |  Doktorlar        |   Bir (1, 1)         | 
| Kullanicilar         |   Yoneticiler       |  Bir (1, 1)          | 
|  Sekreter        |   Gunler       |   Çalıştığı (n,m)         |
|   Doktorlar       |   Gunler       |  Çalıştığı (n,m)         |
|  Uzmanlık       |     Doktorlar     | Uzmanlığı (n,m)           |
|  Hastalar        |   Doktorlar       |   Randevu(n,m)         |
|  Randevu        |   Reçete       |   Verdiği (1,1)         |
|   Randevu       |   Gunler       |  Çalıştığı (n,m)         |



