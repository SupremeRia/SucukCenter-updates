# SucukCenter — Windows kurulumları ve güncellemeler

Bu depo yalnız kurulum dosyaları, güncelleme metaverileri ve sürüm notları içindir. Kaynak kod ayrı bir private depodadır. Otomatik Source code ZIP/TAR arşivleri yalnız bu README'yi içerir; kurulum dosyası değildir.

## Güncel sürüm: 1.11.3

1.11.3: Farenin geri ve ileri tuşlarıyla uygulama içi gezinme düzeltildi.

[Tam kurulum / yerinde yükseltme EXE](https://github.com/SupremeRia/SucukCenter-updates/releases/download/v1.11.3/SucukCenter-1.11.3-Kurulum.exe) · [Sürüm notları ve tüm dosyalar](https://github.com/SupremeRia/SucukCenter-updates/releases/tag/v1.11.3)

1.10.0-rc.1/rc.2'den **bir defalık manuel geçiş** gerekir: uygulamadan doğrulanmış yedek alın, normal kapatın, kaldırmadan aynı konuma bu EXE'yi kurun. Eski istemcinin Windows sertifika şartı ve yeni yayın anahtarını bilmemesi uzaktan değiştirilemez. Node.js veya veritabanı sunucusu gerekmez.

## Uygulama içi güncelleme

1.10.0 ve sonrasında Ayarlar → Güncellemeler → Güncellemeleri kontrol et → İndir → Güncelle ve yeniden başlat. Uygulama eksiksiz ve daha yeni kararlı sürümleri bulur, indirir, doğrular ve kullanıcı seçimiyle kurulumunu başlatır. Ön sürümler normal kullanıcılara önerilmez. Kullanıcının seçimi olmadan indirme/normal çıkışta kurulum yapılmaz.

Güvenilir Windows kod sertifikası gerekmez. Güncelleme imzası, uygulamaya gömülü sabit Ed25519 yayın anahtarıyla doğrulanır. İmza; uygulama/depo, sürüm, EXE adı, boyut ve SHA-512 değerini bağlar. Yalnız hash karşılaştırması yeterli sayılmaz. Eksik/sahte imza ve değiştirilmiş paket engellenir; yeni anahtar ağdan alınmaz.

Bu EXE'de Windows Authenticode sertifikası yoktur. Windows güvenlik/SmartScreen uyarıları ayrıca çıkabilir; uygulama Windows korumalarını değiştirmez. İlk manuel paketin güveni, henüz yeni anahtarı taşımayan eski istemcide otomatik doğrulanmış sayılamaz. Gerçek iki kurulu Windows sürümü arası NSIS yükseltmesi izole ortam olmadığı için henüz doğrulanmadı; ağ indirme ve veri uyum testleri bunun yerine sayılmaz.

Güncelleme öncesi doğrulanmış geri dönüş yedeği, açık form/kayıt kontrolü ve güvenli veritabanı kapatma uygulanır. Kayıtlar Windows Belgeler/SucukCenter klasöründedir; işletme verileri güncelleme kaynağına gönderilmez. Uygulamaya GitHub token veya özel yayın anahtarı gömülmez.

Her yeni release EXE, EXE.blockmap, latest.yml, SHA256SUMS.txt ve release-signature.json içerir. Müşteri verisi, SQLite dosyası, yedek, parola veya özel anahtar bu depoya eklenmez.
