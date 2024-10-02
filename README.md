# Proje Adı

Bu proje, Android tabanlı bir uygulamadır. Kotlin dilinde yazılmış ve modern yazılım geliştirme prensipleri olan MVVM, MVI ve Clean Architecture baz alınarak yapılandırılmıştır.

## Proje Yapısı

Proje, aşağıdaki katmanlardan oluşmaktadır:

### 1. **app** Katmanı
- **MainActivity**: Uygulamanın başlangıç noktasıdır.
- **App**: Uygulamanın genel ayarlarını içeren sınıf.

### 2. **core** Katmanı
Bu katman, projenin temel işlevselliklerini sağlayan kodları içerir. Tekrar kullanılabilir yapılar bu katmana eklenir.
- **base**: Temel sınıflar ve soyutlamalar. Tüm modüllerin veya komponentlerin ortak özelliklerini burada tanımlayabilirsiniz.
- **data**: Veri katmanı, API çağrıları veya veri tabanı işlemleri bu klasör altında yer alır.
- **domain**: İş kurallarının ve veri modellerinin tanımlandığı katman. Use case'ler burada yer alır.
- **extension**: Kotlin uzantıları (Kotlin extensions) bu klasör altında bulunur.
- **module**: Proje modüllerinin bağımlılıklarını yöneten kısım.
- **utils**: Yardımcı fonksiyonlar ve sınıflar.

### 3. **presentation** Katmanı
Bu katman, kullanıcı arayüzünü yönetir ve ViewModel'leri barındırır.
- **components**: Tekrar kullanılabilir arayüz bileşenleri.
- **ui**: Uygulamanın farklı ekranlarına ait sınıflar ve arayüzler bu klasörde yer alır.

## Kullanılan Teknolojiler

- **Kotlin**: Projenin ana dili olarak Kotlin kullanılmıştır.
- **AndroidX**: AndroidX kütüphaneleri ile modern Android geliştirme.
  - **Core KTX**: Kotlin için geliştirilmiş genişletme fonksiyonlarını içerir.
  - **AppCompat**: Geriye dönük uyumluluk ve yeni özellikler için kullanılır.
  - **Fragment KTX**: Fragment'lar için Kotlin'e özgü uzantılar sağlar.
- **Material Components**: Google'ın Material Design bileşenlerini içerir.
- **Navigation Component**: Ekranlar arası geçişleri ve yönlendirmeyi kolaylaştıran bir kütüphane.
- **Hilt**: Dagger tabanlı bağımlılık enjeksiyonu sistemi.
- **JUnit**: Test kütüphanesi, birim testlerini yazmak için kullanılır.
- **Espresso**: UI testlerini yazmak için kullanılan bir framework.
- **Glide**: Görsellerin hızlı ve etkili bir şekilde yüklenmesi için kullanılan bir kütüphane.
- **Retrofit**: HTTP isteklerini gerçekleştirmek için kullanılan bir kütüphane.
- **OkHttp**: Ağ isteklerini yönetmek için kullanılan kütüphane.
- **Timber**: Loglama işlemleri için kullanılan hafif bir kütüphane.

## Mimariler

- **MVVM (Model-View-ViewModel)**: Bu mimari ile iş mantığı (business logic) ve kullanıcı arayüzü ayrıştırılmıştır. ViewModel'ler, View ile model arasındaki köprü görevi görür.
  
- **MVI (Model-View-Intent)**: Kullanıcı etkileşimlerini, durum yönetimini ve güncellemeleri daha yönetilebilir hale getirmek için tercih edilen bir mimari.
  
- **Clean Architecture**: Katmanlı bir yapı benimsenmiştir. Bu yapı ile sorumlulukların belirginleşmesi ve test edilebilirliğin artması sağlanır. Proje katmanları, veri, iş kuralları (domain), ve sunum (presentation) olarak ayrılmıştır.

## Kurulum

Projeyi yerel ortamınızda çalıştırmak için aşağıdaki adımları izleyin:

1. Projeyi klonlayın:
   ```bash
   git clone https://github.com/kullaniciadi/proje-adi.git