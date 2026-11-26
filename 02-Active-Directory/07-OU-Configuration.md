# WS 2016 — OU Yapılandırması

[← Modül içindekiler](README.md) · [Tüm laboratuvar notları](../LAB-INDEX.md)

## 🗂️ Organizational Unit (OU) – Organizasyon Birimi

### 📌 Ne?

- OU, Active Directory içerisinde kullanıcıları, bilgisayarları ve grupları düzenlemek için kullanılan mantıksal klasördür.
- Şirketin departmanlarına göre OU oluşturulabilir: IT, Muhasebe, İnsan Kaynakları gibi.

### ⚙️ Neden?

- Active Directory'yi düzenli tutmak.
- Group Policy (GPO) ile belirli kullanıcılara veya bilgisayarlara kurallar uygulamak.
- Belirli OU'ların yönetimini farklı IT personellerine devretmek.

### 💡 Nerede Kullanılır?

Örneğin, şirkette `Muhasebe` adında bir OU oluşturduk.

- Muhasebe çalışanlarının hesaplarını bu OU'ya taşıdık.
- OU'ya bir GPO bağlayarak çalışanların Denetim Masası'na erişimini kısıtladık.
- Böylece ilgili politika yalnızca kapsamına giren kullanıcıları etkiler.

---

### **ORGANIZATIONAL  UNIT OLUŞTURMA**

![Ekran görüntüsü 2026-10-30 220313.png](screenshots/07-OU-Configuration/01.png)

![image.png](screenshots/07-OU-Configuration/02.png)

→ Ankara klasörünün içinde de OU oluşturabiliriz.Aşağıdaki fotoğrafta yaptık aynı yöntemle yapılıyor

![image.png](screenshots/07-OU-Configuration/03.png)

---

### **KULLANICIYI OLUŞTURDUĞUMUZ OU’YA AKTARMA**

![Ekran görüntüsü 2026-10-30 220727.png](screenshots/07-OU-Configuration/04.png)

---

### **ORGANIZATIONAL UNIT SİLME İŞLEMİ**

1. İlk baş deneme adında ou oluşturuyoruz

![Ekran görüntüsü 2026-10-30 222420.png](screenshots/07-OU-Configuration/05.png)

**→ “Protect container from accidental deletion” bunu işaretlediğimizde hemen silinmiyor nasıl sileceğimizi göstericem**

![Ekran görüntüsü 2026-10-30 222658.png](screenshots/07-OU-Configuration/06.png)

![image.png](screenshots/07-OU-Configuration/07.png)

→ Görünüm bu şekilde oluyor gizli dosyalar da gözüküyor

![Ekran görüntüsü 2026-10-30 222844.png](screenshots/07-OU-Configuration/08.png)

![Ekran görüntüsü 2026-10-30 222940.png](screenshots/07-OU-Configuration/09.png)

→ Sonrasında deneme klasörüne gelip sağ tıklayıp delete kısmına bastığımızda klasörümüz siliniyor
