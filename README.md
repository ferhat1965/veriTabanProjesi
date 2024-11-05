# SAĞLIK MERKEZİ YÖNETİM SİSTEMİ VERİTABAN PROJESİ

## Katılımcılar

- FATMA HALİD < 215260602 />
-  FERHAT RAMMOK <215260618 />
-  MUHAMMED ZARZOUR < 215260614 />

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
bir yapıya sahiptir. Süper Yönetici, diğer 
yöneticileri sisteme ekleyebilir, kaldırabilir ve 
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

## 1.Doktorlar

| özellik       | Açıklama    | 
|--------------|--------------|
| ID           | İçerik 2     |
| Ad           | İçerik 5     |
| Soyad        | İçerik 8     |
| Telefon      |              |
| Cinsiyet     |              |
|Doğum tarihi  |              |

## 2.Hasta

|özellik   | Açıklama |
|----------|----------|
|ID        |          |
|Tc        |          |
|Ad        |          |
|Soyad     |          |
|yaş       |          |
|Cinsiyet  |          |
|Doğum Tarihi |       |
|Telefon   |          |

## 3.Sekreter

|özellik   | Açıklama |
|----------|----------|
|ID        |          |
|Ad        |          |
|Soyad     |          |
|yaş       |          |
|Cinsiyet  |          |
|Doğum Tarihi |       |
|Telefon   |          |

## 4.ilaç

|özellik   | Açıklama |
|----------|----------|
|ID        |          |
|Ad        |          |
|Amaç      |          |
|Max yaş   |          |
|Min yaş   |          |
|Firma     |          |
|Tür       |          |
|Etkin madde|          |

## 5.Uzmanlık

|özellik   | Açıklama |
|----------|----------|
|ID        |          |
|Ad        |          |
|Açıklama  |          |

## 6.Günler

|özellik   | Açıklama |
|----------|----------|
|ID        |          |
|Ad        |          |

## 7.Randevu

|özellik   | Açıklama |
|----------|----------|
|ID        |          |
|Tarih     |          |
|saat      |          |

## 8.Tahliller

|özellik   | Açıklama |
|----------|----------|
|ID        |          |
|Ad        |          |
|Max değer |          |
|Min değer |          |



# Varlıklar-ilişkiler tablosu
|Varlık 1  | Varlık 2 | ilişki Türü|
|----------|----------|------------|
|          |          |            |
|          |          |            |
|          |          |            | 
|          |          |            | 
|          |          |            |
|          |          |            |
|          |          |            |
|          |          |            |



