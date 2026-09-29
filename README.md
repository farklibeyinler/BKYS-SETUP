# BKYS — Beton Kalite Yönetim Sistemi

Hazır beton santrallerinde ve yapı malzemesi laboratuvarlarında kullanılan bir masaüstü kalite yönetim programı. Dışarıdan bir yazılım şirketinin tasarladığı bir ürün değil; kendi santralimizde, kendi laboratuvarımızda geliştirildi ve hâlâ aynı ekip tarafından her gün kullanılıyor.

Verileriniz kendi bilgisayarınızda saklanır, buluta gönderilmez. Günlük iş için internet gerekmez; internet yalnızca lisans işlemleri, güncelleme kontrolü ve isterseniz Telegram bildirimleri için kullanılır.

## Neden Excel Değil?

Excel'de kırım tarihini kendiniz hesaplarsınız ve günü geldiğinde hatırlatan olmaz. Sahada alınan numunenin plakası, kusuru, fotoğrafı tabloya sığmaz; akşam ofise dönünce hafızadan yazılır. Hangi satırı kimin girdiği bir süre sonra bilinmez.

BKYS bu bilgileri numunenin kendisine bağlar. Döküm tarihini girdiğinizde kırım tarihlerini hesaplar, günü gelince hatırlatır, sahadan gelen her kaydın hangi teknisyenden geldiğini tutar ve numunenin şantiyede, telefondan, o an açılmasına izin verir. Gerisi aşağıda.

## Masaüstünde Ne Var?

Numune kaydı TS EN 206 mantığıyla kurulu: döküm tarihini girersiniz, 7, 14 ve 28 günlük kırım tarihleri kendiliğinden hesaplanır; 3 günlük kırım isteğe bağlıdır, numune bazında açılır. Reçeteler kayıtlıdır; listeden seçip numuneye uygularsınız, santral düzeltmesine göre m³ başına gerçek malzeme miktarı da hesaplanır. Cari, şantiye adresi ve yapı denetim bilgisi numuneyle birlikte durur. Cihazların kalibrasyon süreleri takip edilir ve dolmadan önce hatırlatılır. Veritabanı düzenli aralıklarla yedeklenir; her sürüm güncellemesinden önce ayrıca bir güvenlik yedeği alınır. Günün kırımları ile yaklaşan kalibrasyonlar Telegram'a düşer. Raporu tek tıkla PDF olarak alırsınız.

Bunların hiçbiri yeni değil; yıllardır bizim laboratuvarımızda çalışıyor. Asıl yeni olan, aşağıdaki.

## Sahadan Numune Kaydı

Bir hazır beton laboratuvarının günü genelde şöyle geçer: sabahtan birkaç şantiyeye gidilir, numuneler alınır, fabrikaya dönülür ve o gün alınan numuneler hafızadan Excel'e (ya da başka bir programa) işlenir. Hangi araçtan alındığı hatırlanmaya çalışılır. Numune sahada bozuk (ayrışmış, kusmuş, katkısı fazla kaçmış) çıktıysa, o an fotoğraflanamadığı için — gün sonunda ekip zaten yorgun döndüğünde — bu gözlem çoğu zaman hiç kayda geçmez.

Saha kaydı bunun için var. Laboratuvar personeli kendi telefonundan, şantiyedeyken BKYS'ye bağlanır ve numuneyi orada oluşturur:

- **Araç plakası** o an, aracın önünde girilir; hafızaya bırakılmaz.
- **Kayıtlı bir reçete şablonu** tek dokunuşla numuneye uygulanır.
- **Gözlemlenen kusur** (ayrışma, kusma/terleme, katkı fazlası, çok katı, erken priz, topaklanma) anında işaretlenir.
- **Fotoğraf** doğrudan telefonun kamerasından eklenir; telefonda otomatik küçültülür (1 MB'ın altına iner), günlük yedekleriniz şişmez.
- Her kayıt **hangi teknisyenin girdiğini** taşır. Ekip birden fazla kişiyse kim ne zaman ne girmiş, bellidir.

Bir noktada bilerek geri durduk: santral otomasyon sisteminizle (örneğin Vuruşkan) entegrasyonunuz varsa, o sistemden reçete sahada otomatik çekilmiyor. Aynı gün aynı araç birden fazla sefer yapmış olabilir; doğru sevkiyatı seçmek insan kararı gerektiriyor ve bunu telefonda, gözetimsiz otomatikleştirmek yanlış reçetenin numuneye sessizce işlenmesi riski taşır. O adım ofiste kalıyor; siz ya da ekibiniz kontrol ederek yapıyorsunuz. Fark şu: numune artık plakası ve saatiyle kayıtlı olarak sizi bekliyor, listede de reçetesinin eksik olduğu görünüyor.

Bağlantı şöyle kurulu: telefon, santral bilgisayarınıza internet üzerinden değil, Tailscale üzerinden bağlanır. Tailscale, telefona ve bilgisayara kurulan ve yalnızca sizin izin verdiğiniz cihazları kendi aralarında görüştüren bir ağ programıdır. Bu bağlantıyı BKYS'nin içindeki «Saha Sunucusu» sağlar; Ayarlar'dan açılır, varsayılan olarak kapalıdır ve yalnızca Tailscale ağının adresine bağlanır. Ofis Wi-Fi'sinden veya internetten görünmez; Tailscale kapalıysa hiç açılmaz. Adres yazmak yerine masaüstündeki QR kodu telefonla okutursunuz; sayfa bir kez açıldıktan sonra telefonun ana ekranına eklenip normal bir uygulama gibi kullanılabilir.

## Ekran Görüntüleri

[![BKYS Dashboard](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/01-dashboard.png)](/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/01-dashboard.png)

*Dashboard — bugünkü, yaklaşan ve geciken kırımlar tek ekranda.*

| Numune Listesi | Numune Detayı |
|---|---|
| [![Numune Listesi](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/02-numune-listesi.png)](/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/02-numune-listesi.png) | [![Numune Detayı](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/03-numune-detay-kirim-sonuclari.png)](/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/03-numune-detay-kirim-sonuclari.png) |

| Yeni Numune Ekleme | Düzeltmeli Miktar Hesabı |
|---|---|
| [![Yeni Numune](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/04-yeni-numune-ekle.png)](/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/04-yeni-numune-ekle.png) | [![Düzeltmeli Miktar](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/05-duzeltmeli-miktar-hesabi.png)](/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/05-duzeltmeli-miktar-hesabi.png) |

| Cihaz / Kalibrasyon Takibi | Telegram Bildirimleri |
|---|---|
| [![Kalibrasyon](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/06-cihaz-kalibrasyon-takibi.png)](/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/06-cihaz-kalibrasyon-takibi.png) | [![Telegram](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/07-telegram-bildirimleri.png)](/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/07-telegram-bildirimleri.png) |

## Kimler İçin?

- Hazır beton santralleri ve şantiye laboratuvarları
- Yapı malzemesi test laboratuvarları
- Kalite kontrol ve kalibrasyon sorumluları

## Kurulum

1. [En son sürümü indirin](https://github.com/farklibeyinler/BKYS-SETUP/releases/latest) (`BKYS Setup x.x.x.exe`).
2. İndirilen dosyayı çalıştırın, kurulum adımlarını izleyin.
3. Uygulama ilk açıldığında iki seçenek sunulur:
   - **30 günlük demo** — firma adınızı ve telefon numaranızı girip başlatabilirsiniz; satın alma veya bizimle görüşme beklemenize gerek yok.
   - **Lisans etkinleştirme** — satın aldıysanız:
     - **Çevrimiçi:** aktivasyon kodunuzu (`BKYS-XXXX-XXXX-XXXX`) girin.
     - **Çevrimdışı:** gösterilen Makine Kodu'nu bize iletin, gönderdiğimiz lisans dosyasını (`.lic`) yükleyin.

## Sistem Gereksinimleri

| | |
|---|---|
| İşletim Sistemi | Windows 10 / 11 (64-bit) |
| Disk | ~250 MB boş alan |
| İnternet | Yalnızca lisanslama, güncelleme ve (isteğe bağlı) bildirimler için |
| Veritabanı | Yerel SQLite — verileriniz kendi bilgisayarınızda |

## Lisans ve Fiyatlandırma

BKYS ticari bir yazılımdır ve makineye bağlı lisans ile çalışır. Demo ve yıllık lisans seçenekleri mevcuttur. Lisans ve fiyat bilgisi için iletişime geçin.

## İletişim

| | |
|---|---|
| Osman Soylu | 0544 968 19 83 |

---

**BKYS** · Beton Kalite Yönetim Sistemi · Windows Masaüstü Uygulaması
