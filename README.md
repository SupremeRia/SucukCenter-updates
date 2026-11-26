# SucukCenter — Windows kurulumları ve güncellemeler

Bu depo yalnız son kullanıcı kurulum dosyaları, güncelleme bilgileri ve sürüm notları içindir. Uygulamanın kaynak kodları ayrı bir özel depoda tutulur; buraya kaynak kodu veya kaynak geçmişi kopyalanmaz. Buradaki otomatik “Source code” arşivleri yalnız bu tanıtım dosyasını içerir.

[Kurulum ve sürüm notları](https://github.com/SupremeRia/SucukCenter-updates/releases)

## İndirme ve ilk geçiş

[**SucukCenter-1.10.0-rc.2-RiaCoding-Kurulum.exe**](https://github.com/SupremeRia/SucukCenter-updates/releases/download/v1.10.0-rc.2/SucukCenter-1.10.0-rc.2-RiaCoding-Kurulum.exe) hem tam kurulum hem güncelleyicisi olmayan eski sürüm için bir defalık yerinde geçiş paketidir. Eski uygulamada güvenli yedek alın, normal kapatın; kaldırmadan aynı konuma kurun. Node.js veya ayrı veritabanı kurulması gerekmez. “Source code” ZIP'i kurulum değildir.

**1.10.0-rc.2 kararlı uygulama içi güncelleme kanalında görünmez.** Hesap, form, liste ve çökme sonrası kurtarma düzeltmelerini içerir; ayrıntılar Release notlarındadır.

Bu ön sürüm yerel RiaCoding test sertifikası taşır; güvenilir üretim imzası değildir. Windows SmartScreen uyarısının kalkması vaat edilmez. Windows korumasını kapatmayın veya test kökü yüklemeyin. Güvenilir üretim sertifikası ve izole Windows test ortamı olmadığından iki kurulu sürüm arasında fiziksel otomatik güncelleme testi tamamlanmadı.

## Uygulama içi güncelleme

Ayarlar → Güncellemeler → **Güncellemeleri kontrol et** → **İndir** → **Güncelle ve yeniden başlat**. İndirme ve kurulum kullanıcı seçimiyle başlar; internet yokken temel işlevler çalışır. Yalnız eksiksiz kararlı sürümler sunulur; ön sürümler normal kullanıcılara önerilmez. Dosya özeti ve Windows tarafından güvenilen yayıncı imzası doğrulanmadan kurulum yapılmaz; yerel test imzası kabul edilmez.

Kaydedilmemiş form varsa forma dönüp kaydedebilir, vazgeçebilir veya kaydetmeden güncellemeyi seçebilirsiniz. Devam eden kayıt/yedek/geri yükleme sırasında kurulum başlamaz. Kurulumdan önce doğrulanmış veri yedeği oluşturulur ve kayıtlar güvenle kapatılır. Sihirbaz iptal edilirse mevcut uygulamayı normal kısayolundan açın.

Kayıtlar Windows'un belirlediği Belgeler/SucukCenter klasöründeki yerel SQLite dosyasındadır. Güncelleme kaynağı müşteri kayıtlarına, veritabanına veya kaynak depoya erişim gerektirmez; uygulamaya GitHub token gömülmez. Eski programı yeni veritabanı şemasına zorlamayın; eski sürüme dönüşte uyumlu uygulama ve geçiş öncesi doğrulanmış yedek birlikte kullanılmalıdır.

Her Release'te EXE, EXE.blockmap, latest.yml ve SHA256SUMS.txt birlikte yayınlanır. SHA özeti yayıncı imzasının yerine geçmez. Veritabanı, müşteri verisi, yedek, parola veya özel anahtar bu depoya eklenmez.