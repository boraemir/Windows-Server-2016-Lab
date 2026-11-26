# WS 2016 — DHCP Nedir & Nasıl Kurulur

[← Modül içindekiler](README.md) · [Tüm laboratuvar notları](../LAB-INDEX.md)

### **🧠 Benzetme**

> Bir otele gelen müşterilere resepsiyonun boş oda numarası vermesi gibi, DHCP de ağa bağlanan bilgisayarlara otomatik IP adresi dağıtır.
### **📌 Ne?**

**DHCP (Dynamic Host Configuration Protocol)**, ağa bağlanan cihazlara otomatik olarak IP adresi ve gerekli ağ ayarlarını dağıtan protokoldür.

DHCP sunucusu şu bilgileri verebilir:

- **IP Address:** Bilgisayarın ağdaki adresi.
- **Subnet Mask:** Bilgisayarın hangi yerel ağda olduğunu belirler.
- **Default Gateway:** Diğer ağlara ve internete çıkış için kullanılan yönlendirici adresi.
- **DNS Server:** Domain ve diğer alan adlarını çözümleyen sunucunun adresi.

### **⚙️ Neden Kullanılır?**

- Her bilgisayara tek tek statik IP vermeyi önler.
- IP adreslerinin merkezi olarak yönetilmesini sağlar.
- Yanlış IP yapılandırması ve IP çakışması riskini azaltır.
- Yeni cihazlar ağa bağlandığında otomatik IP alabilir.

![image.png](screenshots/01-DHCP-Overview-and-Installation/01.png)

### **🛠️ Windows Server 2016 – DHCP Kurulumu**

**1. DHCP rolünü yükle**

`Server Manager → Manage → Add Roles and Features`

1. **Role-based or feature-based installation** seç.
2. Kurulum yapılacak sunucuyu belirle.
3. **DHCP Server** rolünü işaretle.
4. **Install** ile kurulumu tamamla.
5. **Complete DHCP configuration** üzerinden gerekli yapılandırmayı ve Active Directory yetkilendirmesini tamamla.

---

#### **KURULUM ADIMLARI**

![Ekran görüntüsü 2026-11-23 222729.png](screenshots/01-DHCP-Overview-and-Installation/02.png)

![Ekran görüntüsü 2026-11-23 222740.png](screenshots/01-DHCP-Overview-and-Installation/03.png)

![Ekran görüntüsü 2026-11-23 222754.png](screenshots/01-DHCP-Overview-and-Installation/04.png)

![Ekran görüntüsü 2026-11-23 223041.png](screenshots/01-DHCP-Overview-and-Installation/05.png)

![Ekran görüntüsü 2026-11-23 223055.png](screenshots/01-DHCP-Overview-and-Installation/06.png)

---
