
# Day 1: Temel Ağ Cihazları ve Kavramları (Network Devices)

## Ağ (Network) ve Düğüm (Node)
- **Ağ (Network):** Düğümlerin (nodes) birbirleriyle kaynak, veri ve servis paylaşmasını sağlayan iletişim altyapısıdır.
- **Node (Düğüm):** Ağ üzerinde veri alıp iletebilen her aktif cihazdır. İki bilgisayarın kabloyla doğrudan birbirine bağlanması dahi en küçük yerel ağı oluşturur.

## Uç Cihazlar (End Hosts / Endpoints)
- **Client (İstemci):** Bir sunucudan servis veya kaynak talep eden cihazdır (ör. web sayfasına erişen PC veya telefon).
- **Server (Sunucu):** İstemcilere veri, dosya veya servis sunan cihazdır (ör. web sunucusu, dosya sunucusu).
- **Rollerin Değişkenliği:** Bir cihazın donanımından ziyade anlık fonksiyonu rolünü belirler. Örneğin AirDrop ile dosya gönderirken gönderen cihaz sunucu, alan cihaz istemcidir.

## Ağ Anahtarı (Switch)
- Uç cihazların (PC, sunucu, yazıcı) toplandığı yüksek port sayılı (genellikle 24 veya 48 portlu) cihazdır.
- Veriyi yalnızca aynı **LAN (Local Area Network - Yerel Alan Ağı)** içinde iletir.
- Farklı yerel ağları veya yerel ağı doğrudan internete bağlayamaz.

## Yönlendirici (Router)
- Farklı yerel ağları (LAN) birbirine bağlar.
- Yerel ağlar ile internet arasındaki paket yönlendirmesini sağlar.
- Switch'lere kıyasla belirgin şekilde daha az sayıda ağ arayüzüne (portuna) sahiptir.

## Güvenlik Duvarı (Firewall)
- Ağ trafiğini belirlenen kurallara göre denetler; yetkili trafiğe izin verirken tehditleri engeller.
- **Network Firewall:** Tüm ağ trafiğini filtrelemek için kullanılan harici donanım cihazıdır (ör. Cisco ASA serisi).
- **Host-based Firewall:** Bilgisayarın işletim sisteminde çalışan yazılımsal güvenlik duvarıdır.
- **Next-Generation Firewall (NGFW):** Standart paket filtrelemenin yanı sıra IPS (Saldırı Önleme Sistemi) ve uygulama katmanı denetimi gibi gelişmiş yetenekler barındıran modern güvenlik duvarlarıdır.
