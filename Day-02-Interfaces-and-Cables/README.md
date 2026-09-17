# Day 2: Arayüzler ve Kablolar (Interfaces and Cables)

## Bakır Kablolar (Twisted Pair / UTP)
- Veriyi **elektrik sinyalleri** halinde iletir; **RJ-45** konnektörü kullanır.
- Parazitleri (crosstalk / EMI) önlemek için içindeki tel çiftleri birbirine bükülmüştür.
- Standart Ethernet UTP kablolarının maksimum kesintisiz menzili **100 metre**dir.
- Yaygın standartlar: Cat5e, Cat6, Cat6a (kategori arttıkça hız ve bant genişliği artar).

## Fiber Optik Kablolar
- Veriyi cam veya plastik damarlar içinden **ışık sinyalleri** (fotonlar) halinde iletir.
- Elektromanyetik parazitlerden etkilenmez ve bakıra göre çok daha uzun mesafeleri destekler.
- **Single-Mode Fiber (SMF):** Çok ince çekirdeklidir, lazer ışığı tek doğrultuda gider. Onlarca kilometre mesafeyi ve omurga (backbone) hatlarını destekler.
- **Multi-Mode Fiber (MMF):** Daha kalın çekirdeklidir, LED kaynaklı ışık yansıyarak ilerler. Kampüs/bina içi veya veri merkezleri gibi daha kısa mesafeler için uygundur ve daha ekonomiktir.

## Ethernet Hız Standartları
| Standart | Hız | Kablo Tipi |
| :--- | :--- | :--- |
| **10BASE-T** | 10 Mbps | Bakır (Cat3/Cat5) |
| **100BASE-TX** (FastEthernet) | 100 Mbps | Bakır (Cat5+) |
| **1000BASE-T** (GigabitEthernet) | 1 Gbps (1000 Mbps) | Bakır (Cat5e/Cat6) |
| **10GBASE-T / SR / LR** | 10 Gbps | Bakır (Cat6a) veya Fiber |

- **BASE:** Temel bant (baseband) iletimi anlamına gelir.
- **T:** Twisted Pair (bakır) kabloyu ifade eder.
- **SR / LR:** Short Range (kısa mesafe / MMF) ve Long Range (uzun mesafe / SMF).

## Bakır Kablo Tipleri: Düz vs. Çapraz
- **Düz Kablo (Straight-Through):** Farklı türdeki cihazları birbirine bağlar.
  - Switch ↔ Router
  - Switch ↔ PC
  - Switch ↔ Server
- **Çapraz Kablo (Crossover):** Benzer çalışma mantığına sahip (aynı katmandaki) cihazları birbirine bağlar.
  - Switch ↔ Switch
  - Router ↔ Router
  - PC ↔ PC
  - PC ↔ Router *(İkisi de aynı iletim pinlerini kullandığı için çapraz kablo gerektirir)*
- **Auto-MDIX:** Portun takılan kablo tipini otomatik algılayıp pinleri gerektiği gibi yapılandıran teknolojidir.

## İletişim Yöntemleri (Duplex)
- **Simplex:** Tek yönlü iletim (ör. radyo yayını).
- **Half-Duplex:** İki yönlü iletim ancak aynı anda değil (ör. telsiz haberleşmesi, eski hub ağları). Çakışma (collision) riski vardır.
- **Full-Duplex:** Aynı anda iki yönlü veri iletimi (ör. modern switch ağları). Çakışma oluşmaz.

## Konsol Bağlantısı (Console Cable / Rollover)
- Ağ cihazlarına ağ üzerinden değil, doğrudan fiziksel olarak bağlanıp CLI (komut satırı) yapılandırması yapmak için kullanılan seri kablodur.
- Bilgisayarın seri portundan (veya USB adaptöründen) cihazın mavi renkli **Console** portuna takılır.
