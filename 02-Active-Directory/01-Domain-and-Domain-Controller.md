# Active Directory — Domain ve Domain Controller Nedir ?

[← Modül içindekiler](README.md) · [Tüm laboratuvar notları](../LAB-INDEX.md)

## 🧠 Benzetme

> Bir şirketi **site yönetimi** gibi düşün: **Domain (Etki Alanı)** sitenin tamamı, **Active Directory (Active Directory)** site sakinleri/daireler/kuralların kayıt sistemi, **Domain Controller (Etki Alanı Denetleyicisi)** ise güvenlik ve yönetim ofisidir.
## 📌 Nasıl Çalışır

### 1. Active Directory Nedir?

**Active Directory**, Microsoft'un şirket ağındaki kullanıcıları, bilgisayarları ve kaynakları **merkezi olarak yönetmesini** sağlayan sistemdir.

Active Directory içinde **Object (Nesne)** olarak şunlar bulunabilir:

- **User (Kullanıcı)**
- **Computer (Bilgisayar)**
- **Group (Grup)**
- **Printer (Yazıcı)**
- **Server (Sunucu)**

Örneğin 300 çalışan varsa her bilgisayarda ayrı ayrı kullanıcı açmak yerine:

```
Active Directory
├── Bora
├── Ahmet
├── Ayşe
└── Mehmet
```

hesapları merkezi olarak yönetilir.

Microsoft ortamında asıl kullanılan servis **AD DS – Active Directory Domain Services (Active Directory Etki Alanı Hizmetleri)**'dir.

---

### 2. Domain (Etki Alanı) Nedir?

**Domain**, Active Directory tarafından merkezi olarak yönetilen kullanıcıların, bilgisayarların ve diğer kaynakların oluşturduğu yönetim alanıdır.

Örneğin şirketin domain'i:

```
firma.local
```

olsun.

Bilgisayarlar domaine katılabilir:

```
PC-01 ─┐
PC-02 ─┼──► firma.local
PC-03 ─┘
```

Böylece çalışan farklı domain bilgisayarlarında kendi şirket hesabıyla oturum açabilir ve merkezi kurallar uygulanabilir.

> **Workgroup (Çalışma Grubu)** ortamında bilgisayarlar daha bağımsızdır; **Domain (Etki Alanı)** ortamında merkezi yönetim vardır.
---

### 3. Domain Controller (Etki Alanı Denetleyicisi) Nedir?

**Domain Controller – DC**, **AD DS** çalışan ve domain'i yöneten sunucudur.

Örneğin:

```
🖥️ Windows 11 PC
      │
      │ Kullanıcı: bora
      │ Parola: ****
      ▼
🗄️ Domain Controller
      │
      ├── Hesap var mı?
      ├── Parola doğru mu?
      └── Kullanıcı aktif mi?
```

Bilgiler doğruysa oturum açılmasına izin verir.

Bu işleme:

**Authentication (Kimlik Doğrulama)** denir.

> Önemli: Normal bir Windows 11 **client bilgisayara Domain Controller rolü kurulmaz.** **AD DS rolü Windows Server'a kurulur ve sunucu Domain Controller'a yükseltilir (promote edilir).**
## 🖥️ Active Directory Neden Client İşletim Sistemine Kurulmaz?

### 📌 Ne?

- Active Directory Domain Services (AD DS): Şirketlerde kullanıcıları, bilgisayarları ve erişim yetkilerini merkezi olarak yönetmeyi sağlayan Windows Server rolüdür.
- Windows Server: Active Directory'nin sunucu rolünün kurulabildiği işletim sistemidir.
- Client OS: Windows 10 ve Windows 11 gibi son kullanıcı işletim sistemleridir. Active Directory sunucu rolü bu sistemlere kurulamaz.

### ⚙️ Neden?

- Active Directory, birden fazla bilgisayarı ve kullanıcıyı merkezi olarak yönetmek için tasarlanmıştır.
- Bu nedenle sunucu işletim sistemi ve Domain Controller (Etki Alanı Denetleyicisi) altyapısı gerektirir.
- Windows 10/11, Active Directory sunucusu olamaz. Ancak uygun sürümleri bir Active Directory domain'ine katılabilir.
- Windows 10/11 üzerine RSAT araçları kurulabilir. Böylece Active Directory, istemci bilgisayardan uzaktan yönetilebilir.

### 💡 Nerede Kullanılır?

Bir şirkette 100 bilgisayar olduğunu düşün:

- Windows Server üzerine AD DS kurulur.
- Sunucu, Domain Controller olarak yapılandırılır.
- Çalışanların kullanıcı hesapları Active Directory üzerinde oluşturulur.
- Bilgisayarlar domain'e katılır.
- IT uzmanı, kullanıcıların yetkilerini ve bilgisayarların bazı ayarlarını merkezi olarak yönetebilir.

---

### 4. Authentication ve Authorization Farkı

Bu ikisini karıştırma:

**Authentication (Kimlik Doğrulama)**

> “Sen gerçekten Bora mısın?”
Kullanıcı adı/parola kontrol edilir.

**Authorization (Yetkilendirme)**

> “Bora hangi dosyalara ve sistemlere erişebilir?”
Örneğin:

```
Bora → IT klasörü ✅
Bora → Muhasebe klasörü ❌
```

---

### 5. Group (Grup) Neden Kullanılır?

100 kullanıcıya tek tek izin vermek yerine kullanıcıları gruplara koyarsın:

```
IT-Users
├── Bora
├── Ahmet
└── Mehmet
```

Sonra:

```
IT-Users → IT klasörüne erişebilir
```

dersin.

Bu, yönetimi ciddi şekilde kolaylaştırır.

---

### 6. OU — Organizational Unit (Organizasyon Birimi)

Active Directory içindeki nesneleri düzenlemek için kullanılan klasör benzeri yapıdır.

```
firma.local
│
├── IT
│   ├── Bora
│   └── PC-IT-01
│
├── Muhasebe
│   ├── Ayşe
│   └── PC-MUH-01
│
└── İnsan Kaynakları
```

OU'lar özellikle kullanıcıları/bilgisayarları düzenlemek ve üzerlerine politikalar uygulamak için kullanılır.

---

### 7. Group Policy (Grup İlkesi)

**Group Policy – GPO (Grup İlkesi)**, domain bilgisayarlarına merkezi olarak ayar göndermeyi sağlar.

Örneğin IT yöneticisi:

```
USB kullanımını engelle
Masaüstü arka planını belirle
Control Panel'i kapat
Parola politikası uygula
Belirli yazılımları dağıt
```

gibi kurallar uygulayabilir.

```
Domain Controller
      ↓
     GPO
      ↓
PC1  PC2  PC3  PC4  PC5
```

Yüzlerce bilgisayarı tek tek gezmek gerekmez.

---

### 8. Active Directory ve DNS İlişkisi

Active Directory için **DNS (Domain Name System / Alan Adı Sistemi)** çok önemlidir.

Bilgisayar:

> “Benim Domain Controller'ım nerede?”
diye aradığında DNS yardımıyla DC'yi bulur.

```
Client
  ↓
 DNS
  ↓
Domain Controller
```

Bu yüzden Active Directory sorunlarında **DNS yapılandırması** IT Support için önemli kontrol noktalarından biridir.

---

### 9. Birden Fazla Domain Controller Olabilir mi?

Evet.

Şirketlerde tek DC kullanmak riskli olabilir:

```
DC01 ❌
↓
Domain hizmetlerinde problem
```

Bu nedenle örneğin:

```
DC01 ✅ ←→ ✅ DC02
```

iki veya daha fazla Domain Controller bulunabilir.

DC'ler Active Directory bilgilerini birbirleriyle **Replication (Çoğaltma)** yoluyla senkronize eder.

---

## 💡 Örnekler

**Örnek 1 — Yeni çalışan geldi**

IT Support olarak:

```
1. Active Directory'de User oluştur
2. Gerekli Group'lara ekle
3. Bilgisayarı Domain'e kat
4. Kullanıcının domain hesabıyla girişini test et
```

yapabilirsin.

**Örnek 2 — Ticket: “Şirket bilgisayarına giriş yapamıyorum.”**

Kontrol edebileceğin şeyler:

- Kullanıcı hesabı kilitli mi?
- Parola yanlış/süresi dolmuş mu?
- Bilgisayar Domain Controller'a ulaşabiliyor mu?
- DNS doğru mu?
- Bilgisayar hâlâ domain üyesi mi?

**Örnek 3 — 200 bilgisayarda USB kapatılacak**

Tek tek bilgisayarlara gitmek yerine **Group Policy (Grup İlkesi)** uygulanabilir.

---
