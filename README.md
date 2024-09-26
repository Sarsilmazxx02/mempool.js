
beta
Bütün Bitcoin ekosistemini incele
@UmutKaya1242146
Yağma
Abonelikler
Ayarlar
Dökümantasyon
SSS
API - REST
API - WebSocket
Mempool Enterprise® ile daha yüksek API limitlerine ulaşın
Aşağıda Bitcoin REST API servisi için bir referans bulunmaktadır .

Oran sınırlarını uyguladığımızı unutmayın. Bu sınırları aşarsanız, bir HTTP 429 hatası alırsınız. Sınırları tekrar tekrar aşarsanız, hizmete erişiminiz tamamen yasaklanabilir. Daha yüksek API sınırlarına ihtiyacınız varsa bir kurumsal sponsorluk düşünün.

Genel
# Zorluk Ayarını Al
* Çıkış, GET /api/v1/zorluk-ayarlaması
*Tanım
Zorluk ayarlaması hakkında detayları döndürür.
Kod:

```bash
curl -sSL "https://mempool.space/api/v1/difficulty-adjustment"

```
# Cevap
{
  progressPercent: 44.397234501112074,
  difficultyChange: 98.45932018381687,
  estimatedRetargetDate: 1627762478,
  remainingBlocks: 1121,
  remainingTime: 665977,
  previousRetarget: -4.807005268478962,
  nextRetargetHeight: 741888,
  timeAvg: 302328,
  adjustedTimeAvg: 302328,
  timeOffset: 0
}
Fiyat Al
Çıkış
/api/v1/fiyatları al
Tanım
Bitcoin'in ana para birimlerindeki son fiyatını döndürür.
kıvrımlı
Kod:
curl -sSL "https://mempool.space/api/v1/prices"
Cevap
{
  time: 1703252411,
  USD: 43753,
  EUR: 40545,
  GBP: 37528,
  CAD: 58123,
  CHF: 37438,
  AUD: 64499,
  JPY: 6218915
}
Tarihi Fiyatı GET
Çıkış
GET /api/v1/historical-price?currency=EUR×tamp=1500000000
Tanım
Ana para birimlerinde belirtilen bitcoin tarihi fiyatını döndürür. Kullanılabilir sorgu parametreleri: currency, timestamp. Hiçbir parametre sağlanmazsa, tüm para birimleri için tam fiyat geçmişi döndürülür.
kıvrımlı
Kod:
curl -sSL "https://mempool.space/api/v1/historical-price?currency=EUR&timestamp=1500000000"
Cevap
{
  prices: [
    {
      "time": 1499904000,
      "EUR": 1964,
      "USD": 2254.9
    }
  ],
  exchangeRates: {
    "USDEUR": 0.92,
    "USDGBP": 0.78,
    "USDCAD": 1.36,
    "USDCHF": 0.89,
    "USDAUD": 1.53,
    "USDJPY": 149.48
  }
}
Adresler
Adresi Al
Çıkış
GET /api/adres/:adres
Tanım
Bir adres hakkında ayrıntıları döndürür. Kullanılabilir alanlar: address, chain_stats, ve mempool_stats. chain_statsve her biri , , , , ve mempool_statsiçeren bir nesne içerir .tx_countfunded_txo_countfunded_txo_sumspent_txo_countspent_txo_sum
kıvrımlı
OrtakJS
ES Modülü
Kod:
curl -sSL "https://mempool.space/api/address/1wiz18xYmhRX6xStj2b9t1rwWX4GKUgpv"
Cevap
{
  address: "1wiz18xYmhRX6xStj2b9t1rwWX4GKUgpv",
  chain_stats: {
    funded_txo_count: 5,
    funded_txo_sum: 15007599040,
    spent_txo_count: 5,
    spent_txo_sum: 15007599040,
    tx_count: 7
  },
  mempool_stats: {
    funded_txo_count: 0,
    funded_txo_sum: 0,
    spent_txo_count: 0,
    spent_txo_sum: 0,
    tx_count: 0
  }
}
GET Adres İşlemleri
Çıkış
GET /api/adres/:adres/txs
Tanım
after_txidBelirtilen adres/scripthash için işlem geçmişini alın, en yenisi ilk olacak şekilde sıralayın. En fazla 50 mempool işlemi ve ilk 25 onaylanmış işlemi döndürür. Bir sorgu parametresi kullanarak daha fazla onaylanmış işlem talep edebilirsiniz .
kıvrımlı
OrtakJS
ES Modülü
Kod:
curl -sSL "https://mempool.space/api/address/1wiz18xYmhRX6xStj2b9t1rwWX4GKUgpv/txs"
Cevap
[
  {
    txid: "dba43fd04b7ae3df8e5b596f2e7fab247c58629d622e3a5213f03a5a09684430",
    version: 1,
    locktime: 0,
    vin: [ [Object] ],
    vout: [ [Object], [Object] ],
    size: 255,
    weight: 1020,
    fee: 10000,
    status: {
      confirmed: true,
      block_height: 326148,
      block_hash: "00000000000000001e4118adcfbb02364bc13c41c210d8811e4f39aeb3687e36",
      block_time: 1413798020
    }
  },
  ...
]
GET Adres İşlemleri Zinciri
Çıkış
GET /api/adres/:adres/txs/zincir
Tanım
Belirtilen adres/scripthash için onaylanmış işlem geçmişini alın, en yenisi ilk olacak şekilde sıralayın. Sayfa başına 25 işlem döndürür. Önceki sorgu tarafından görülen son txid belirtilerek daha fazlası talep edilebilir.
kıvrımlı
OrtakJS
ES Modülü
Kod:
curl -sSL "https://mempool.space/api/address/1wiz18xYmhRX6xStj2b9t1rwWX4GKUgpv/txs/chain"
Cevap
