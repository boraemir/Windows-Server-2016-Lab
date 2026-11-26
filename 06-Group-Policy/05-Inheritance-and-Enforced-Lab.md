# WS 2016 — Group Policy Miras ve Enforced Uygulama

[← Modül içindekiler](README.md) · [Tüm laboratuvar notları](../LAB-INDEX.md)

![image.png](screenshots/05-Inheritance-and-Enforced-Lab/01.png)

- Ankara OU'su için oluşturduğumuz **Group Policy (GPO)** ile bilgisayarı kapatma (Shut Down) ve yeniden başlatma (Restart) seçeneklerini kısıtlayacağız. Bu politika, miras (Inheritance) yoluyla Ankara OU'su altında bulunan tüm alt birimlerdeki kullanıcılara uygulanacaktır.

![Ekran görüntüsü 2026-11-20 142521.png](screenshots/05-Inheritance-and-Enforced-Lab/02.png)

![Ekran görüntüsü 2026-11-20 142652.png](screenshots/05-Inheritance-and-Enforced-Lab/03.png)

- Group Policy yapılandırmasını tamamladıktan sonra Ankara OU'su altında bulunan herhangi bir kullanıcı hesabıyla oturum açıyoruz. Ardından, bilgisayarı kapatma (Shut Down) ve yeniden başlatma (Restart) seçeneklerinin kaldırıldığını kontrol ederek uyguladığımız politikanın doğru çalıştığını doğruluyoruz. (Hakkı Bilge — Muhendis)

![Ekran görüntüsü 2026-11-20 142941.png](screenshots/05-Inheritance-and-Enforced-Lab/04.png)

---

Ankara OU'su altındaki IT biriminin üst birimden gelen grup ilkelerinden etkilenmemesi için ilgili **IT OU'suna** sağ tıklayarak **Block Inheritance (Mirası Engelle)** seçeneğini etkinleştiriyoruz.

Böylece üst birimlerden miras yoluyla gelen politikaların IT birimine uygulanmasını engelliyoruz.

**Not:** Enforced (Zorunlu) olarak işaretlenen GPO'lar, Block Inheritance özelliğinden etkilenmez.

![Ekran görüntüsü 2026-11-20 143500.png](screenshots/05-Inheritance-and-Enforced-Lab/05.png)

---

- Oluşturduğumuz grup ilkesinin zorunlu olarak uygulanmasını ve **Block Inheritance (Mirası Engelle)** özelliğinden etkilenmemesini istiyorsak GPO bağlantısı üzerinde **Enforced (Zorunlu Uygulama)** seçeneğini etkinleştiriyoruz. Böylece ilgili politika, mirası engelleyen alt OU'larda da uygulanmaya devam eder.

![Ekran görüntüsü 2026-11-20 144059.png](screenshots/05-Inheritance-and-Enforced-Lab/06.png)

---
