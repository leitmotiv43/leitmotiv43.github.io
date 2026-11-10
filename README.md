# Relax IPTV Player — GitHub Pages Kurulum Rehberi (`privacy-policy.html` & `app-ads.txt`)

Bu klasördeki dosyaları GitHub Pages üzerinden ücretsiz yayınlayarak Play Console **Gizlilik Politikası** ve AdMob **`app-ads.txt`** doğrulaması için kullanabilirsiniz.

## 1. Doğru GitHub Deposu Adı (Çok Önemli)
- GitHub hesabınızda **`<github-kullanici-adiniz>.github.io`** adında **Public (Herkese Açık)** yeni bir depo (repository) oluşturun.
  *(Örn: GitHub kullanıcı adınız `ahmetyilmaz` ise depo adı birebir `ahmetyilmaz.github.io` olmalıdır; başka bir alt proje adı kullanırsanız `app-ads.txt` sitenin kök dizininde açılmaz.)*
- Bu `github-pages/` klasörünün içindeki **tüm dosyaları** (`index.html`, `privacy-policy.html`, `app-ads.txt`) doğrudan o deponun kök dizinine yükleyin.
- **Önce E-posta Düzenlemesi:** `privacy-policy.html` dosyasındaki `[BURAYA PLAY CONSOLE DESTEK E-POSTANIZI YAZIN]` / `[ENTER YOUR PLAY CONSOLE SUPPORT EMAIL HERE]` alanlarına kendi geliştirici destek e-posta adresinizi yazın.
- **AdMob Sonrası:** Faz 4B'de AdMob hesabınızdan `pub-...` kimliğinizi aldıktan sonra `app-ads.txt` içindeki yorum satırlarını silip yalnızca tek satır (`google.com, pub-..., DIRECT, f08c47fec0942fa0`) bırakın.

## 2. GitHub Pages'i Aktifleştirme
1. Deponuzda **Settings -> Pages** bölümüne gidin.
2. **Build and deployment -> Source** altında **Deploy from a branch** seçin, `main` ve `/ (root)` seçip **Save** tıklayın.
3. 1–2 dakika içinde sayfalarınız yayına alınır:
   - Ana Sayfa / Mağaza Web Sitesi: `https://<kullanici-adiniz>.github.io`
   - Gizlilik Politikası URL'si: `https://<kullanici-adiniz>.github.io/privacy-policy.html`
   - `app-ads.txt` URL'si: `https://<kullanici-adiniz>.github.io/app-ads.txt`

## 3. `local.properties` ve Play Console Bağlantısı
- `https://<kullanici-adiniz>.github.io/privacy-policy.html` adresini proje kökündeki `local.properties` dosyasına `PRIVACY_POLICY_URL=...` olarak ekleyin ve Play Console **App content -> Privacy policy** alanına girin.
- Play Console **Store listing -> Store settings -> Website** alanına `https://<kullanici-adiniz>.github.io` adresini girin.

> **Not (`github.io` ve AdMob Tarayıcısı):** `github.io` Public Suffix List üzerinde yer aldığı için birçok kullanıcı site root (`<kullanici>.github.io/app-ads.txt`) üzerinden sorunsuz doğrulama alsa da, Google AdMob tarayıcısının nadiren ücretsiz alt alan adlarını geç doğruladığı veya reddettiği durumlar görülebilmektedir. Böyle bir durumla karşılaşırsanız ücretsiz **Firebase Hosting (`*.web.app`)** veya GitHub Pages'e bağlı ucuz bir özel alan adı (Custom Domain `CNAME`) geçişi 5 dakikada çözüm sağlar.

