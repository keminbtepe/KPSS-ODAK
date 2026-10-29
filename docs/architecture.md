# KPSSODAK · Teknik bakış

[← Uygulama tanıtımına dön](../README.md)

Bu sayfa portföy ziyaretçilerine ürünün genel yapısını anlatır. Kaynak kodu, özel proje belgeleri, üretim ayarları ve kurulum adımları paylaşılmaz.

## Bir ürün, birbirini tamamlayan üç deneyim

**Mobil uygulama**, adayın soru çözme, deneme, harita, not alma ve ilerleme takibi alanıdır. **Web yönetim paneli**, bu deneyimi besleyen içerik ve hesap yönetimini sağlar. **Tanıtım sitesi**, ürünü ve mağaza bağlantılarını ziyaretçiye sunar.

Mobil uygulama ve yönetim paneli aynı backend ile iletişim kurar. İçerik, değerlendirme ve erişim kuralları böylece ortak bir temelde yönetilir.

## Teknoloji tercihleri

| Alan | Kullanılan yaklaşım |
| --- | --- |
| Mobil | React Native, Expo ve TypeScript |
| Yönetim paneli | React, Vite ve Tailwind CSS |
| Servisler | ASP.NET Core, C# ve Entity Framework Core |
| Sunucu verisi | SQL Server |
| Desteklenen Android içerik okuması | Sınırlı yerel SQLite deposu |
| Tablet üzerinde çizim | Platforma özgü native çizim yüzeyleri |

## Mimari yaklaşım

Backend; HTTP giriş noktaları, uygulama iş kuralları, veri modelleri ve veritabanı erişimi olarak dört katmana ayrılır. Web ve mobil aynı ürün dilini paylaşır; arayüz bileşenleri her platformun ihtiyaçlarına göre geliştirilir.

Soru, şık ve çözüm gösteriminde ortak belge kuralları; yönetim arayüzünde tekrar kullanılan bileşenler; mobilde ise soru, deneme ve harita akışlarının ortak parçaları kullanılır.

## Veri ve erişim sınırları

Kimlik doğrulama, cevap değerlendirmesi, puanlama ve içerik erişiminde sunucu belirleyicidir. Desteklenen Android istemcilerde bazı içerik okumaları yerel depoyla hızlandırılır; bu, tüm platformlarda tam çevrimdışı soru çözümü anlamına gelmez. Kalem notlarının cihazda tutulması, hesap ve ilerleme verilerinin sunucu akışından ayrıdır.

## Geliştirme odağı

Okunabilir soru ekranları, tekrar kullanılabilir bileşenler, büyük listelerde sayfalama, kontrollü içerik okuması ve platforma uygun dokunma deneyimi ürünün başlıca mühendislik konularıdır. Cihaz ve native çizim davranışları ayrıca test gerektirir.

Uygulama içi güncellemeler yalnız uyumlu paketlerde kullanılır; native değişiklikler yeni mağaza paketi gerektirebilir. Bu depo ürün tanıtımıdır; tüm sürümlerin teknik kabul kaydı veya kaynak kod dağıtımı değildir.

