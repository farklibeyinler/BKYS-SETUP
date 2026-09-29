<div align="center">

# BKYS — Beton Kalite Yönetim Sistemi

**Hazır beton santralleri ve yapı malzemesi laboratuvarları için numune, kırım, reçete ve kalibrasyon takibi.**

[![Sürüm](https://img.shields.io/github/v/release/farklibeyinler/BKYS-SETUP?label=s%C3%BCr%C3%BCm&color=2563eb)](https://github.com/farklibeyinler/BKYS-SETUP/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011-0078D6)](#sistem-gereksinimleri)
[![Lisans](https://img.shields.io/badge/lisans-ticari-orange)](#lisans-ve-fiyatlandırma)

### [En Son Sürümü İndir](https://github.com/farklibeyinler/BKYS-SETUP/releases/latest)

Windows 10 / 11 · 30 günlük ücretsiz deneme

</div>

---

BKYS'yi bir yazılım şirketi değil, biz yazdık: kendi santralimizin laboratuvarında, kendi işimiz için. Aynı ekip onu hâlâ her gün kullanıyor.

Verileriniz kendi bilgisayarınızda saklanır, buluta gönderilmez (Telegram'ı açarsanız yalnızca bildirim mesajları Telegram üzerinden iletilir). Masaüstündeki günlük iş için internet gerekmez; internet yalnızca lisans işlemleri, güncelleme kontrolü, isterseniz Telegram bildirimleri ve sahadan numune kaydı için kullanılır.

<div align="center">

[![BKYS Dashboard](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/01-dashboard.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/01-dashboard.png)

*Dashboard — bugünkü, yaklaşan ve geciken kırımlar tek ekranda.*

</div>

## Neden Excel Değil?

Excel'de her şeyi siz hatırlarsınız. BKYS'de her bilgi numuneye bağlıdır; kırımın günü gelince program size hatırlatır.

| İş | Excel'de | BKYS'de |
|---|---|---|
| Kırım tarihleri | Elle hesaplanır | Döküm tarihi girilince 7, 14 ve 28 günlük kırım tarihleri kendiliğinden çıkar; 3 günlük kırım isteğe bağlı |
| Hatırlatma | Tabloyu açıp bakmanız gerekir | Bugünkü, yaklaşan ve geciken kırımlar ekranda; istenirse Telegram'a da düşer |
| Reçete | Ayrı sayfalarda, kopyala-yapıştır | Kayıtlı reçete listeden seçilir; su/çimento (S/Ç) oranı kendiliğinden hesaplanır |
| Santral düzeltmesi | Elle formül | m³ başına gerçek malzeme miktarı hesaplanır |
| Sahadaki gözlem | Akşam hafızadan yazılır | Plaka, kusur ve fotoğraf şantiyede, telefondan o an girilir |
| Kaydı kim girdi | Bir süre sonra bilinmez | Sahadan gelen her kayıt teknisyenin adını taşır |
| Kalibrasyon | Ayrı bir liste | Süreler takip edilir, dolmadan önce uyarılır |
| Yedek | Elle kopyalamayı unutursanız yedek yok | Ayarlar'dan bir kez açınca her gün, seçtiğiniz saatte otomatik yedek |

## Masaüstünde Ne Var?

**Numune ve kırım**
- **Numune kaydı:** TS EN 206 mantığıyla tutulur; kırım planı döküm tarihinden kendiliğinden çıkar.
- **Küp bazında giriş:** her küpün dayanımı ve kütlesi ayrı girilir, ortalama kendiliğinden alınır.
- **Cihazdan Oku:** sonuç kırım presinden (şu an Bars PCM305 / PCM304) doğrudan okunur; yük eğrili kırım raporu numuneye eklenir.
- **Arama ve filtre:** numuneler cari, plaka, beton sınıfı, yapı denetim ve kırım durumuna göre bulunur.
- **Numune karşılaştırma:** 2 ile 8 numune yan yana; yazdırılır ya da PDF olarak kaydedilir.

**Reçete ve santral**
- **Reçeteler:** kayıtlı reçete listeden seçilip numuneye uygulanır.
- **Düzeltmeli miktar hesabı:** santral düzeltmesine göre m³ başına gerçek miktar.
- **Santraldan Getir:** Vuruşkan kullanıyorsanız reçete, plaka ve döküm tarihine göre santral kayıtlarından çekilir; santrale hiçbir şey yazılmaz, yalnızca okunur.
- **Deneme karışımı:** pan mikser denemesi için gram cinsinden tartım ve S/Ç hesabı.

**Takip, bildirim ve kayıt**
- **Cari, şantiye adresi, yapı denetim bilgisi ve araç plakaları** numuneyle birlikte tutulur.
- **Cihaz ve kalibrasyon takibi:** kalibrasyon süreleri, dolmadan önce uyarı.
- **Telegram bildirimleri:** bugünkü, yarınki ve geciken kırımlar, kalibrasyonu yaklaşan ya da geçmiş cihazlar ve girilen her kırım sonucu telefonunuza.
- **PDF rapor:** firma antetli numune raporu tek tıkla; listeden seçilen numuneler toplu olarak da yazdırılır.
- **Yedekleme:** Ayarlar'dan açtığınızda her gün seçtiğiniz saatte otomatik yedek ve yedekten geri yükleme. Veritabanını değiştiren güncellemelerden önce ise her durumda ayrıca güvenlik yedeği alınır.
- **Güncelleme bildirimi:** yeni sürüm çıkınca uygulama haber verir.

Bunlar yıllardır kendi laboratuvarımızda her gün kullanılıyor. 1.13.0'ın yeniliği ise sahadan numune kaydı.

## Sahadan Numune Kaydı

Bir hazır beton laboratuvarının günü genelde şöyle geçer: sabahtan birkaç şantiyeye gidilir, numuneler alınır, fabrikaya dönülür ve o gün alınan numuneler hafızadan Excel'e (ya da başka bir programa) işlenir. Hangi araçtan alındığı hatırlanmaya çalışılır. Numune sahada bozuk çıktıysa (ayrışmış, kusmuş, katkısı fazla kaçmış), o an fotoğrafı çekilmediği ve ekip akşam yorgun döndüğü için bu gözlem çoğu zaman hiç kayda geçmez.

Saha kaydı bunun için var. Laboratuvar personeli kendi telefonundan, şantiyedeyken BKYS'ye bağlanır ve numuneyi orada oluşturur:

- **Araç plakası** o an, aracın önünde girilir; hafızaya bırakılmaz.
- **Kayıtlı bir reçete şablonu** tek dokunuşla numuneye uygulanır.
- **Gözlemlenen kusur** (ayrışma, kusma/terleme, katkı fazlası, çok katı, erken priz, topaklanma) anında işaretlenir.
- **Fotoğraf** doğrudan telefonun kamerasından eklenir; telefonda otomatik küçültülür (genellikle 1 MB'ın altına iner), yedekleriniz şişmez.
- Her kayıt **hangi teknisyenin girdiğini** taşır. Ekip birden fazla kişiyse kim ne zaman ne girmiş, bellidir.

Bilerek yapmadığımız bir şey var: santral otomasyon sisteminizle (örneğin Vuruşkan) entegrasyonunuz varsa, reçete sahada o sistemden otomatik çekilmiyor. Aynı gün aynı araç birkaç sefer yapmış olabilir; hangi sevkiyatın doğru olduğuna bir insanın bakması gerekir. Bunu telefonda kendiliğinden yaptırsaydık, yanlış reçete kimse fark etmeden numuneye işlenebilirdi. O adım ofiste kalıyor; siz ya da ekibiniz kontrol ederek yapıyorsunuz. Fark şu: numune artık plakası ve saatiyle kayıtlı olarak sizi bekliyor, listede de reçetesinin eksik olduğu görünüyor.

Bağlantı şöyle kurulu: telefon, santral bilgisayarınıza herkese açık bir internet adresi üzerinden değil, Tailscale üzerinden bağlanır. Tailscale, telefona ve bilgisayara kurulan ve yalnızca sizin izin verdiğiniz cihazları kendi aralarında şifreli olarak görüştüren bir ağ programıdır. Şantiyede telefonun mobil verisi yeterlidir; ofiste bilgisayarın açık, internete bağlı ve BKYS'nin çalışıyor olması gerekir. Bu bağlantıyı BKYS'nin içindeki «Saha Sunucusu» sağlar; Ayarlar'dan açılır, varsayılan olarak kapalıdır ve yalnızca Tailscale ağı üzerinden erişilebilir. Ofis Wi-Fi'sinden veya internetten görünmez; Tailscale kapalıysa hiç açılmaz. Adres yazmak yerine BKYS'de Ayarlar'da çıkan QR kodu telefonla okutursunuz; sayfa bir kez açıldıktan sonra telefonun ana ekranına eklenip normal bir uygulama gibi kullanılabilir.

## Ekran Görüntüleri

| Numune Listesi | Numune Detayı |
|:---:|:---:|
| [![Numune Listesi](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/02-numune-listesi.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/02-numune-listesi.png) | [![Numune Detayı](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/03-numune-detay-kirim-sonuclari.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/03-numune-detay-kirim-sonuclari.png) |
| Her numunede kırım ilerlemesi ve durum. | Kırım sonuçları (dayanım, kütle) ve malzeme reçetesi. |

| Yeni Numune Ekleme | Düzeltmeli Miktar Hesabı |
|:---:|:---:|
| [![Yeni Numune](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/04-yeni-numune-ekle.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/04-yeni-numune-ekle.png) | [![Düzeltmeli Miktar](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/05-duzeltmeli-miktar-hesabi.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/05-duzeltmeli-miktar-hesabi.png) |
| Kimlik, plaka, reçete ve kendiliğinden hesaplanan kırım tarihleri. | Santral düzeltmesine göre m³ başına gerçek miktar. |

| Cihaz / Kalibrasyon Takibi | Telegram Bildirimleri |
|:---:|:---:|
| [![Kalibrasyon](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/06-cihaz-kalibrasyon-takibi.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/06-cihaz-kalibrasyon-takibi.png) | [![Telegram](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/07-telegram-bildirimleri.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/07-telegram-bildirimleri.png) |
| Kalibrasyon geçmişi ve yaklaşan kalibrasyon uyarısı. | Kırım ve kalibrasyon uyarıları telefonunuza. |

<div align="center">

[![Otomatik Yedekleme](https://github.com/farklibeyinler/BKYS-SETUP/raw/main/docs/screenshots/08-otomatik-yedekleme.png)](https://github.com/farklibeyinler/BKYS-SETUP/blob/main/docs/screenshots/08-otomatik-yedekleme.png)

*Yedekleme — zamanlanmış otomatik yedek ve yedekten geri yükleme.*

</div>

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
