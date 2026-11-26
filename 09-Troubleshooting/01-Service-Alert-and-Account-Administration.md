# WS 2016 — DİĞER NOTLAR 1

[← Modül içindekiler](README.md) · [Tüm laboratuvar notları](../LAB-INDEX.md)

![Ekran görüntüsü 2026-10-30 192611.png](screenshots/01-Service-Alert-and-Account-Administration/01.png)

Ekran görüntüsünde Local Server → Services bölümünde kırmızı `1` görünmesinin sebebi, bir Windows servisinin durdurulmuş olmasıdır.

Soruna neden olan servis:

- Service Name: MapsBroker
- Display Name: Downloaded Maps Manager
- Status: Stopped (Durduruldu)
- Start Type: Automatic (Delayed Start) – Otomatik (Gecikmeli Başlatma)

### ⚙️ Neden?

- Windows, otomatik başlaması beklenen bir servisin çalışmadığını tespit ettiği için uyarı gösteriyor.
- Downloaded Maps Manager, çevrimdışı haritaların indirilmesi ve yönetilmesiyle ilgilidir.
- Servis ihtiyaç olmadığında durabilir. Bu durum tek başına ciddi bir arıza anlamına gelmez.
- Active Directory veya DNS hizmetlerinin bozulduğu anlamına gelmez.

**—> Bu servisin bizi rahatsız etmemesi için kapatıyoruz şimdi onun adımlarını göstericem :**

![Ekran görüntüsü 2026-10-30 193009.png](screenshots/01-Service-Alert-and-Account-Administration/02.png)

![Ekran görüntüsü 2026-10-30 193135.png](screenshots/01-Service-Alert-and-Account-Administration/03.png)

![Ekran görüntüsü 2026-10-30 193258.png](screenshots/01-Service-Alert-and-Account-Administration/04.png)

→ Sonrasında dashboard’ı yenilediğimizde bu uyarı birdaha gözükmez

---

### **KULLANICILARIN DOMAİN ŞİFRELERİNİ SIFIRLAMAK**

![Ekran görüntüsü 2026-11-01 163132.png](screenshots/01-Service-Alert-and-Account-Administration/05.png)

---

### **DOMAİN KULLANICILARININ OTURUM AÇMA SAATLERİNİ BELİRLEMEK**

![Ekran görüntüsü 2026-11-01 163442.png](screenshots/01-Service-Alert-and-Account-Administration/06.png)

![Ekran görüntüsü 2026-11-01 163705.png](screenshots/01-Service-Alert-and-Account-Administration/07.png)

---

### **GEÇİCİ ÇALIŞANLAR İÇİN DOMAİN HESABI OLUŞTURMAK**

![Ekran görüntüsü 2026-11-01 164014.png](screenshots/01-Service-Alert-and-Account-Administration/08.png)

---

### **BİR DOMAİN HESABINI DEVRE DIŞI BIRAKMAK**

![Ekran görüntüsü 2026-11-01 164412.png](screenshots/01-Service-Alert-and-Account-Administration/09.png)

---
