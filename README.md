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

## 1.kullanici

| özellik       | Açıklama    |
|--------------|--------------|
| kul_id       | Kullanıcı kimliği (PK)                     |
| ad           | Kullanıcının adı                           |
| soyad        | Kullanıcının soyadı                        |
| telefon      | Kullanıcının telefon numarası              |
| cinsiyet     | Kullanıcının cinsiyeti                     |
| email        | Kullanıcının e-posta adresi                |
| sifre        | Kullanıcının şifresi                       |
| dogumTarihi  | Kullanıcının doğum tarihi                  |
| rol          | Kullanıcının sistemdeki rolü               |

## 2.yonetici

| özellik       | Açıklama    | 
|--------------|--------------|
| yon_id       | Yönetici kimliği (PK)                      |
| kul_id       | Kullanıcı kimliği (FK, kullanici.kul_id)   |

## 3.doktor

| özellik       | Açıklama    | 
|--------------|--------------|
| dktr_id      | Doktor kimliği (PK)                        |
| kul_id       | Kullanıcı kimliği (FK, kullanici.kul_id)   |
| basUzmYili   | Doktorun uzmanlık başlangıç yılı           |
| deneyimYili  | Doktorun deneyim yılı sayısı               |
| aktif        | Doktorun aktiflik durumu (true/false)      |

## 4.hasta

|özellik   | Açıklama |
|----------|----------|
|hst_id    | Hasta kimliği (PK)                             |
|kul_id    | Kullanıcı kimliği (FK, kullanici.kul_id)       |
|tc        | Hastanın T.C. kimlik numarası (benzersiz)      |

## 5.sekreter

|özellik   | Açıklama |
|----------|----------|
|skr_id    | Sekreter kimliği (PK)                          |
|kul_id    | Kullanıcı kimliği (FK, kullanici.kul_id)       |
|aktif     | Sekreterin aktiflik durumu (true/false)        |

## 6.tarih_yas

|özellik   | Açıklama |
|----------|----------|
|dogumTarihi | Kullanıcının doğum tarihi (PK)               |
|yas         | Doğum tarihine göre hesaplanan yaş           |

## 7.uzmanlik

|özellik   | Açıklama |
|----------|----------|
|uzm_id    | Uzmanlık kimliği (PK)                          |
|ad        | Uzmanlık adı (Kardiyoloji vb.)                 |
|anaUzm_id | Ana uzmanlık kimliği (alt uzmanlıklar için, FK)|

## 8.doktor_uzmanlik

|özellik   | Açıklama |
|----------|----------|
|dktrUzm_id  | Doktor ve uzmanlık ilişkisi kimliği (PK)     |
|dktr_id     | Doktor kimliği (FK, doktor.dktr_id)          |
|uzm_id      | Uzmanlık kimliği (FK, uzmanlik.uzm_id)       |

## 9.gunler

|özellik   | Açıklama |
|----------|----------|
|gun_id    | Gün kimliği (PK)                               |
|ad        | Günün adı (örneğin, Pazartesi)                 |

## 10.doktor_gunler

|özellik   | Açıklama |
|----------|----------|
|dktr_id   | Doktor kimliği (FK, doktor.dktr_id)           |
|gun_id    | Gün kimliği (FK, gunler.gun_id)               |

## 11.sekreter_gunler

|özellik   | Açıklama |
|----------|----------|
|skr_id    | Sekreter kimliği (FK, sekreter.skr_id)        |
|gun_id    | Gün ID (FK, gunler.gun_id)                    |

## 12.randevu

|özellik   | Açıklama |
|----------|----------|
|rndv_id   | Randevu kimliği (PK)                          |
|dktr_id   | Randevu doktor kimliği (FK, doktor.dktr_id)   |
|hst_id    | Randevu hasta kimliği (FK, hasta.hst_id).     |
|durum     | Randevunun durumu ("Beklemede", "İptal" vb.)  |
|tarih     | Randevu tarihi  |
|saat      | Randevu saati   |

## 13.ilac

|özellik   | Açıklama |
|----------|----------|
|ilac_id   | İlaç kimliği (PK)       |
|ad        | İlaç adı                |
|amac      | İlaç kullanım amacı     |
|maxYas    | Maksimum kullanıcı yaşı |
|minYas    | Minimum kullanıcı yaşı  |
|firma     | İlaç üreten firma       |
|tur       | İlaç türü (tablet, şurup vb.)    |
|etkinMadde| İlaçta bulunan etkin madde       |

## 14.recete

|özellik   | Açıklama |
|----------|----------|
|rct_id    | Reçete kimliği (PK)                                |
|rndv_id   | Randevu kimliği (FK, randevu.rndv_id)              |
|aciklama  | Reçete hakkında açıklama                           |
|gecerlilikGunSayisi | Reçetenin geçerlilik süresi (gün olarak) |

## 15.recetede_ilaclar

|özellik   | Açıklama |
|----------|----------|
|rct_id    | Reçete kimliği (FK, recete.rct_id) |
|ilac_id   | İlaç kimliği (FK, ilac.ilac_id)    |
|kutuAdedi | Reçetede ilaç kutu sayısı          |
|doz       | Günlük alınması gereken doz        |

## 16.tahlil

|özellik   | Açıklama |
|----------|----------|
|tah_id    | Tahlil kimliği (PK)    |
|ad        | Tahlil adı             |
|maxDeger  | Maksimum normal değer  |
|minDeger  | Minimum normal değer   |

## 17.tahlil_talebi

|özellik   | Açıklama |
|----------|----------|
|tahTlb_id | Tahlil talebi kimliği (PK)                             |
|rndv_id   | Randevu kimliği (FK, randevu.rndv_id)                  |
|durum     | Tahlil talep durumu ("Beklemede", "Teslim edildi" vb.) |
|tlbTarih  | Tahlil talep tarihi                                    |

## 18.tahlil_sonucu

|özellik   | Açıklama |
|----------|----------|
|tahTlb_id | Tahlil talebi kimliği (FK, tahlil_talebi.tahTlb_id) |
|tah_id    | Tahlil kimliği (FK, tahlil.tah_id)        |
|deger     | Tahlil sonucu değeri                      |
|sncTarih  | Tahlil sonuç tarihi                       |
|aciklama  | Tahlil sonuç açıklaması                   |

## 19.alerji

|özellik   | Açıklama |
|----------|----------|
|alrj_id   | Alerji kimliği (PK)                       |
|turu      | Alerji türü (gıda, ilaç vb.)              |
|etkMadde  | Etkileyen maddeler (alerji sebebi)        |

## 20.hasta_alerjileri

|özellik   | Açıklama |
|----------|----------|
|hst_id    | Hasta kimliği (FK, hasta.hst_id)          |
|alrj_id   | Alerji kimliği (FK, alerji.alrj_id)       |
|aciklama  | Hasta alerjileri hakkında açıklama        |

## 21.log

|özellik   | Açıklama |
|----------|----------|
|log_id    | Log kimliği (PK)                          |
|kul_id    | Kullanıcı kimliği (FK, kullanici.kul_id)  |
|islem     | Yapılan işlem tipi                        |
|tarih     | Log tarihi                                |
|detay     | Log hakkında detaylar                     |


# Varlıklar-ilişkiler tablosu
| Varlık 1 |	Varlık 2	|İlişki Türü |
|----------|----------|------------|
|kullanici | yonetici  | Bir (1,1) |
|kullanici | doktor	   | Bir (1,1) |
|kullanici | hasta	   | Bir (1,1) |
|kullanici | sekreter	 | Bir (1,1) |
|kullanici | tarih_yas | Ait (1,1) |
|uzmanlik  | uzmanlik	 | Dallandığı (1,n)|
|uzmanlik	 | doktor	   | Uzmanlığı (n,m) |
|gunler	   | doktor	   | Çalıştığı (n,m) |
|gunler	   | sekreter  | Çalıştığı (n,m) |
|hasta     | doktor	   | Randevu (n,m)   |
|randevu   | recete	   | Yazıldığı (1,1) |
|recete    | ilac	     | içerdiği (n,m)  |
|randevu   | tahlil_talebi| İstenmiş (1,n)|
|tahlil_talebi| tahlil | içerdiği (n,m)  |
|hasta     | alerji    | Yaşadığı (n,m)  |
|kullanici | log	     | Yaratığı (1,n)|

