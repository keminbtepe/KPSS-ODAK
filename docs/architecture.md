# ⚙️ KPSSODAK teknik bakış

[← Uygulama tanıtımına dön](../README.md)

Bu sayfa portföy ziyaretçilerine ürünün genel yapısını anlatır. Kaynak kodu, özel proje belgeleri, üretim ayarları ve kurulum adımları paylaşılmaz.

## 🧩 Bir ürün, birbirini tamamlayan üç deneyim

📱 **Mobil uygulama**, adayın soru çözme, deneme, harita, not alma ve ilerleme takibi alanıdır.

🖥️ **Web yönetim paneli**, bu deneyimi besleyen içerik ve hesap yönetimini sağlar.

🌐 **Tanıtım sitesi**, ürünü ve mağaza bağlantılarını ziyaretçiye sunar.

Mobil uygulama ve yönetim paneli aynı sunucuyla iletişim kurar. İçerik, değerlendirme ve erişim kuralları böylece ortak bir temelde yönetilir.

## 🛠️ Teknoloji tercihleri

| Alan | Ne işe yarar | Kullanılan teknoloji |
| --- | --- | --- |
| 📱 Mobil uygulama | Tek kod tabanından iPhone ve Android uygulaması | React Native, Expo, TypeScript |
| 🖥️ Yönetim paneli | Tarayıcıda çalışan içerik ve hesap yönetimi | React, Vite, Tailwind CSS |
| 🧠 Sunucu servisleri | Soru, deneme, puan ve üyelik kurallarını yürüten ortak sunucu | ASP.NET Core, C#, Entity Framework Core |
| 🗄️ Veritabanı | Hesap, içerik ve ilerleme kayıtlarının tutulduğu yer | SQL Server |
| 🤖 Android'de hızlı içerik | Bazı içeriklerin cihazda saklanıp daha hızlı açılması | SQLite (cihaz içi veritabanı) |
| ✍️ Tablette çizim | Kalemle yazarken gecikmesiz, cihaza özgü çizim yüzeyi | Android Ink, Apple PencilKit |

Teknoloji adları özel isim olduğu için özgün yazımlarıyla bırakıldı; ne işe yaradıkları yanlarında açıklandı.

## 🏗️ Mimari yaklaşım

Sunucu tarafı; istek giriş noktaları, uygulama iş kuralları, veri modelleri ve veritabanı erişimi olarak dört katmana ayrılır. Web ve mobil aynı ürün dilini paylaşır; arayüz bileşenleri her platformun ihtiyaçlarına göre geliştirilir.

Soru, şık ve çözüm gösteriminde ortak belge kuralları; yönetim arayüzünde tekrar kullanılan bileşenler; mobilde ise soru, deneme ve harita akışlarının ortak parçaları kullanılır.

## 🔐 Veri ve erişim sınırları

Kimlik doğrulama, cevap değerlendirmesi, puanlama ve içerik erişiminde sunucu belirleyicidir. Desteklenen Android istemcilerde bazı içerik okumaları yerel depoyla hızlandırılır; bu, tüm platformlarda tam çevrimdışı soru çözümü anlamına gelmez. Kalem notlarının cihazda tutulması, hesap ve ilerleme verilerinin sunucu akışından ayrıdır.

## 🎯 Geliştirme odağı

Okunabilir soru ekranları, tekrar kullanılabilir bileşenler, büyük listelerde sayfalama, kontrollü içerik okuması ve platforma uygun dokunma deneyimi ürünün başlıca mühendislik konularıdır. Cihaza özgü çizim davranışları ayrıca test gerektirir.

Uygulama içi güncellemeler yalnız uyumlu paketlerde kullanılır; cihaza özgü değişiklikler yeni mağaza paketi gerektirebilir. Bu depo ürün tanıtımıdır; tüm sürümlerin teknik kabul kaydı veya kaynak kod dağıtımı değildir.

