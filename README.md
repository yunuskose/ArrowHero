<div align="center">

# 🏹 Arrow Hero — Okçunun Yolu

**Hızlı tempolu, roguelite tarzı bir okçu arena oyunu.**
Karanlık zindanlarda oda oda ilerle, düşman sürülerini oklarınla temizle, boss'ları alt et; her turda yeni yetenekler seç, kalıcı güçlerini geliştir ve karakterini özelleştir.

*A fast-paced, roguelite archery arena game for iOS & Android. Clear room after room of enemies, defeat bosses, pick roguelite upgrades each run, and progress a permanent skill tree. Built as a single-file HTML5 Canvas game wrapped with Capacitor.*

[![Platform](https://img.shields.io/badge/platform-iOS%20%7C%20Android-blue)]()
[![Version](https://img.shields.io/badge/version-1.1.0-green)]()
[![Engine](https://img.shields.io/badge/engine-HTML5%20Canvas%20%2B%20Capacitor-orange)]()

📱 **App Store:** [Arrow Hero](https://apps.apple.com/tr/app/arrow-hero/id6768756560)

</div>

---

## 🎮 Oyun Hakkında

Arrow Hero, tek dokunuşla oynanan (joystick ile hareket, otomatik nişan/atış) sürükleyici bir aksiyon oyunudur. Her "run" (oyun turu) rastgele yeteneklerle şekillenir; ölürsen baştan başlarsın ama kazandığın **altın** ve **elmasla** kalıcı gelişim sağlarsın. Basit ama derinleşen mekaniğiyle her yaştan oyuncuya hitap eder.

### Öne Çıkan Özellikler
- ⚔️ **Roguelite tur sistemi** — her turda yelpaze şeklinde sunulan yeteneklerden seçim (Çift Ok, Üçlü Ok, Delici Ok, Takip Eden Ok, Sektiren Ok, Öfke, Yaşam Çalma, Büyük Hasar…)
- 🗺️ **Bölümler & odalar** — her bölüm 20 oda; dalga temposu, artan zorluk ve her 5 odada bir **boss**
- 👹 **7 düşman tipi** — Goblin, Yarasa, Trol, Büyücü, Bombacı, Alev Yılanı, Cellat (her biri kendine özgü davranış ve görünüm)
- 👑 **5 boss tipi** — Trol Kral, Şeytan Yarasa, Büyücü Lordu, Bomba Lordu, Gölge Kral (farklı saldırı desenleri)
- 🌳 **Kalıcı yetenek ağacı** — Can, Hasar, Hız, Atış Hızı, Başlangıç Altını, Şans
- 🛡️ **Ekipman sistemi** — Yay, Zırh, Eldiven, Taç; 5 nadirlik seviyesi (Normal → Mitik)
- 🎨 **Kozmetikler** — Kostümler (skin), Kahramanlar, Yoldaşlar (pet) ve tek seferlik paketler
- 💰 **Çift para birimi** — Altın (oyun içi) + Elmas (premium)
- 🎁 **Günlük ödül** ve **reklam izleyerek bonus** sistemi
- 💾 **Otomatik kayıt** (yerel) + hesap yedekleme

---

## 🛠️ Teknoloji

| Katman | Teknoloji |
|---|---|
| **Oyun motoru** | Saf HTML5 **Canvas 2D** + vanilla JavaScript — harici oyun motoru **yok**, tüm oyun tek dosyada ([`www/index.html`](www/index.html)) |
| **Grafikler** | Sprite/PNG kullanılmaz; tüm karakter ve canavarlar **prosedürel canvas çizimi** (gradyan + kontur) — animasyonlar kod ile |
| **Mobil sarmalayıcı** | [Capacitor 8](https://capacitorjs.com/) (iOS + Android), Swift Package Manager |
| **Reklamlar** | Google AdMob ([`@capacitor-community/admob`](https://github.com/capacitor-community/admob)) — ödüllü video reklamlar + ATT |
| **Satın alma** | [RevenueCat](https://www.revenuecat.com/) ([`@revenuecat/purchases-capacitor`](https://github.com/RevenueCat/purchases-capacitor)) — elmas paketleri |

---

## 📁 Proje Yapısı

```
Oyun1ArrowHero/
├── www/
│   └── index.html          # ← TÜM OYUN burada (Canvas + oyun mantığı + UI)
├── ios/                    # Capacitor iOS projesi (Xcode)
│   └── App/App.xcodeproj
├── android/                # Capacitor Android projesi (Android Studio)
├── capacitor.config.json   # Capacitor yapılandırması
├── package.json
└── docs/                   # Dokümanlar
```

> ℹ️ Oyunun tamamı **[`www/index.html`](www/index.html)** içindedir. Web varlıkları `npx cap copy` ile native projelere kopyalanır.

---

## 🚀 Geliştirme / Derleme

### Gereksinimler
- [Node.js](https://nodejs.org/) (18+)
- **iOS için:** macOS + Xcode 15+ (SPM tabanlı, CocoaPods gerekmez)
- **Android için:** Android Studio + JDK 17

### Adımlar
```bash
# 1. Bağımlılıkları kur
npm install

# 2. Web varlıklarını native projelere senkronla
npx cap sync

# 3a. iOS'ta çalıştır
npx cap open ios          # Xcode açılır → Run

# 3b. Android'de çalıştır
npx cap open android      # Android Studio açılır → Run
```

Sadece oyunu (web tarafını) tarayıcıda test etmek için `www/index.html` dosyasını bir tarayıcıda açman yeterlidir. (Reklam/satın alma yalnızca gerçek cihazda çalışır.)

### 🔐 İmzalama Anahtarları (repoda YOK)
Güvenlik gereği yayın imzalama anahtarları bu depoya **dâhil edilmemiştir**:
- Android keystore (`*.jks`)
- Apple App Store Connect / abonelik anahtarları (`*.p8`)

Yayın (release) derlemesi almak için kendi imzalama sertifikalarını sağlaman gerekir. Bu dosyalar [`.gitignore`](.gitignore) ile kalıcı olarak dışlanmıştır.

---

## 📌 Sürüm

- **Güncel:** 1.1.0 (build 5) — görsel yenileme, "Çift Ok" düzeltmesi, oda süre sayacı ve genel iyileştirmeler
- **Platform:** iOS App Store'da yayında; Android yapılandırması hazır

---

## 👤 Geliştirici

**YK Yazılım** — YK Yazılım Proje ve Danışmanlık Ltd. Şti.
🌐 [ykyazilim.com.tr](https://www.ykyazilim.com.tr)

---

## 📄 Lisans

Bu depo şu an belirli bir açık kaynak lisansı taşımamaktadır. Aksi belirtilmedikçe **tüm hakları saklıdır** — kodu görüntüleyebilirsin, ancak izinsiz kullanım/dağıtım için geliştiriciyle iletişime geç. (İleride bir lisans eklemek istersen `LICENSE` dosyası oluşturulabilir.)
