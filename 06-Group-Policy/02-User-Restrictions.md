# WS 2016 — Group Policy ile kullanıcılara yasak atamak

[← Modül içindekiler](README.md) · [Tüm laboratuvar notları](../LAB-INDEX.md)

![Ekran görüntüsü 2026-11-18 213540.png](screenshots/02-User-Restrictions/01.png)

![Ekran görüntüsü 2026-11-18 213856.png](screenshots/02-User-Restrictions/02.png)

![Ekran görüntüsü 2026-11-18 214033.png](screenshots/02-User-Restrictions/03.png)

![Ekran görüntüsü 2026-11-18 214831.png](screenshots/02-User-Restrictions/04.png)

- Group Policy ayarını yapılandırdıktan sonra **Mimar ve Mühendisler** grubuna üye olan herhangi bir kullanıcı hesabıyla oturum açıyoruz. Ardından, uyguladığımız politikanın doğru çalıştığını doğrulamak için **C: sürücüsünün Dosya Gezgini'nde görünmediğini** kontrol ediyoruz.

![image.png](screenshots/02-User-Restrictions/05.png)

---

- Group Policy ayarlarının uygulanmasında gecikme yaşanırsa ilgili bilgisayarda veya Windows Server 2016 üzerinde `gpupdate /force` komutunu çalıştırarak grup ilkelerinin yeniden uygulanmasını sağlıyoruz. Bu sayede yeni yapılandırmaların etkinleşmesini hızlandırıyoruz.
