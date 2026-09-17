# Day 3: OSI Modeli ve TCP/IP Modeli (Network Models)

## 1. Ağ Modelleri Neden Kullanılır?
- Farklı üreticilerin donanım ve yazılımlarının birbiriyle uyumlu çalışmasını sağlamak.
- Veri iletim sürecini katmanlara bölerek hata tespitini ve protokol geliştirmeyi standartlaştırmak.

---

## 2. OSI Modeli (7 Katmanlı Referans Model)
*Sıralama: Katman 7'den Katman 1'e (All People Seem To Need Data Processing)*

- **Katman 7 - Application (Uygulama):** Kullanıcının ağ servisleriyle doğrudan etkileşime girdiği katmandır (HTTP, HTTPS, DNS, FTP, SSH).
- **Katman 6 - Presentation (Sunum):** Verinin biçimlendirilmesi, karakter setleri (ASCII, Unicode), şifreleme/çözme (SSL/TLS) ve veri sıkıştırma işlemleri yapılır.
- **Katman 5 - Session (Oturum):** Cihazlar arasındaki oturumun başlatılması, yönetilmesi ve sonlandırılmasından sorumludur.
- **Katman 4 - Transport (Taşıma):** Uçtan uca veri aktarımı, akış denetimi ve hata kontrolü sağlar.
  - **TCP:** Güvenilirdir, el sıkışma (3-way handshake) yapar, kaybolan paketleri tekrar talep eder.
  - **UDP:** Hızlıdır, kontrol mekanizması yoktur; ses, video ve canlı yayın akışlarında tercih edilir.
- **Katman 3 - Network (Ağ):** Mantıksal adresleme (IP Adresleri) ve en uygun yolun tespiti (Routing) yapılır. Cihazı: **Router**.
- **Katman 2 - Data Link (Veri Bağlantısı):** Fiziksel adresleme (MAC Adresleri), yerel ağ içi veri iletimi ve hata kontrolü yapılır. Cihazı: **Switch**.
- **Katman 1 - Physical (Fiziksel):** Verinin kablo, ışık veya radyo frekansları üzerinden 0 ve 1'ler (bitler) halinde elektriksel/fiziksel aktarımıdır.

---

## 3. TCP/IP Modeli (4 Katmanlı Pratik Model)
Modern internetin ve ağ altyapısının fiilen kullandığı mimaridir:

| TCP/IP Katmanı | Karşılık Gelen OSI Katmanları | Protokoller / Örnekler |
| :--- | :--- | :--- |
| **Application** | Katman 7, 6, 5 | HTTP, HTTPS, DNS, SSH, DHCP |
| **Transport** | Katman 4 | TCP, UDP |
| **Internet** | Katman 3 | IP, ICMP, ARP |
| **Network Access (Link)** | Katman 2, 1 | Ethernet, Wi-Fi |

---

## 4. Kapsülleme (Encapsulation) ve PDU (Protocol Data Unit)
Veri üst katmandan alt katmanlara inerken her katman verinin önüne kendi başlığını (header) ekler. Bu sürece **Encapsulation**, alıcı tarafta başlıkların sökülmesine **De-encapsulation** denir.

| Katman (OSI) | PDU Adı | Eklenen Başlık / Bilgi |
| :--- | :--- | :--- |
| **Katman 7, 6, 5** | **Data** | Ham uygulama verisi |
| **Katman 4** | **Segment** | Kaynak ve Hedef Port Numaraları |
| **Katman 3** | **Packet** | Kaynak ve Hedef IP Adresleri |
| **Katman 2** | **Frame** | Kaynak/Hedef MAC Adresleri + Kuyruk (FCS/Trailer) |
| **Katman 1** | **Bits** | Fiziksel sinyaller (0 ve 1) |

> **Önemli Not:** Katman 2 (Data Link), paketin hem başına bir başlık (Header) hem de sonuna hata denetimi amacıyla bir kuyruk (**Trailer / FCS - Frame Check Sequence**) ekleyen tek katmandır.

---

## 5. Temel Cihaz - Katman İlişkisi
- **Switch:** Katman 2 cihazıdır; yerel ağdaki cihazları bulmak için **Hedef MAC Adresine** bakar.
- **Router:** Katman 3 cihazıdır; farklı ağlar arası yönlendirme yapmak için **Hedef IP Adresine** bakar.
