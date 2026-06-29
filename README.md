# meseburak.github.io

GitHub Pages — **tek repoda iki uygulama** (Arrow Flow + Decision Hub).

## Klasör yapısı

```
/
├── index.html
├── app-ads.txt                    # Ana geliştirici sitesi (kök)
├── assets/site.css
├── arrow-flow/
│   ├── index.html
│   ├── app-ads.txt                # Arrow Flow mağaza doğrulaması
│   └── privacy/index.html
└── decision-hub/
    ├── index.html
    ├── app-ads.txt                # Decision Hub mağaza doğrulaması
    └── privacy/
        ├── index.html
        └── en.html
```

## app-ads.txt — birden fazla dosya sorun olur mu?

**Hayır.** Aynı AdMob yayıncı hesabını (`pub-6475922412547411`) kullandığın sürece her dosyada **aynı satır** olur. Bu normal ve doğrudur.

| Dosya | Ne zaman kullanılır |
|--------|---------------------|
| `/app-ads.txt` | Play Console / App Store’da geliştirici sitesi `https://meseburak.github.io` ise |
| `/arrow-flow/app-ads.txt` | Arrow Flow sitesi `https://meseburak.github.io/arrow-flow/` ise |
| `/decision-hub/app-ads.txt` | Decision Hub sitesi `https://meseburak.github.io/decision-hub/` ise |

Google, mağazada yazdığın **geliştirici web sitesinin köküne** `app-ads.txt` koymanı ister. Her uygulama için alt klasörü site olarak verirsen, o klasördeki dosya doğrulanır.

### Android ve iOS

**Ayrı app-ads.txt gerekmez.** AdMob yayıncı kimliği (`pub-…`) hesap bazlıdır; aynı dosya hem Google Play hem App Store için geçerlidir. Platforma özel ikinci bir dosya oluşturma.

İleride bir uygulama **farklı** AdMob hesabı kullanırsa, yalnızca o uygulamanın `app-ads.txt` dosyasına ikinci satır eklenir; kök dosyaya da her iki satır yazılır:

```
google.com, pub-6475922412547411, DIRECT, f08c47fec0942fa0
google.com, pub-XXXXXXXXXXXXXXXX, DIRECT, f08c47fec0942fa0
```

## Play Console / App Store ayarları

### Arrow Flow

| Alan | Değer |
|------|--------|
| Paket | `com.burak.arrowflow` |
| Web sitesi | `https://meseburak.github.io/arrow-flow/` |
| Gizlilik | `https://meseburak.github.io/arrow-flow/privacy/` |
| app-ads.txt | `https://meseburak.github.io/arrow-flow/app-ads.txt` |

### Decision Hub (Karar Merkezi)

| Alan | Değer |
|------|--------|
| Paket | `com.decisionhub.app` |
| Web sitesi | `https://meseburak.github.io/decision-hub/` |
| Gizlilik | `https://meseburak.github.io/decision-hub/privacy/` |
| app-ads.txt | `https://meseburak.github.io/decision-hub/app-ads.txt` |

AdMob → Uygulama ayarları → app-ads.txt alanına yukarıdaki URL’yi yapıştır.

## URL özeti

| Uygulama | Sayfa | Gizlilik | app-ads.txt |
|----------|--------|----------|-------------|
| Arrow Flow | [/arrow-flow/](https://meseburak.github.io/arrow-flow/) | [/arrow-flow/privacy/](https://meseburak.github.io/arrow-flow/privacy/) | [/arrow-flow/app-ads.txt](https://meseburak.github.io/arrow-flow/app-ads.txt) |
| Decision Hub | [/decision-hub/](https://meseburak.github.io/decision-hub/) | [/decision-hub/privacy/](https://meseburak.github.io/decision-hub/privacy/) | [/decision-hub/app-ads.txt](https://meseburak.github.io/decision-hub/app-ads.txt) |

Eski gizlilik yolları (`arrow-flow-privacy/`, `karar-merkezi-privacy/`) yeni adreslere yönlendirilir.
