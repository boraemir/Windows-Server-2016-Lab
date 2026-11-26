# Workgroup (Çalışma Grubu) ve Domain (Etki Alanı) Farkı

[← Modül içindekiler](README.md) · [Tüm laboratuvar notları](../LAB-INDEX.md)

### 📌 Ne?

- Workgroup: Bilgisayarların birbirinden bağımsız çalıştığı, merkezi yönetimin bulunmadığı ağ yapısıdır.
- Domain: Bilgisayarların ve kullanıcıların Active Directory üzerinden merkezi olarak yönetildiği yapıdır.
- Önemli: Workgroup için 10–15 bilgisayar şeklinde kesin bir teknik sınır yoktur. Bu sayı, yönetimin zorlaşmaya başladığı küçük ağlar için pratik bir örnektir.

### ⚙️ Neden?

- Workgroup'ta her bilgisayarın kullanıcı hesapları, şifreleri ve güvenlik ayarları ayrı ayrı yönetilir.
- Bilgisayar sayısı arttıkça IT uzmanının iş yükü artar.
- Domain ortamında kullanıcılar, bilgisayarlar ve güvenlik politikaları merkezi olarak yönetilebilir.
- Group Policy (Grup İlkesi) sayesinde birçok bilgisayara aynı ayarlar uygulanabilir.

### 💡 Nerede Kullanılır?

| Özellik | Workgroup | Domain |
| --- | --- | --- |
| Kullanım | Ev, küçük ofis | Şirket, kurum |
| Yönetim | Her bilgisayar ayrı | Merkezi |
| Kullanıcı hesapları | Yerel | Active Directory |
| 100 bilgisayar | Yönetimi zor | Yönetimi kolay |

Örnek: 100 bilgisayarlı bir şirkette USB kullanımını kısıtlamak istediğimizde Workgroup'ta bilgisayarları tek tek yapılandırmamız gerekebilir. Domain ortamında ise GPO ile ilgili bilgisayarlara merkezi olarak kural uygulayabiliriz.
