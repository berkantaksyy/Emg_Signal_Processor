Bu kod, bir EMG (Elektromiyografi) sinyal işleme uygulamasıdır. EMG, kasların elektriksel aktivitesini ölçen bir tekniktir ve bu uygulama, EMG sinyallerini filtrelemek, analiz etmek ve görselleştirmek için kullanılır. İşte kodun temel işlevleri ve nasıl çalıştığı:   

1. Giriş Ekranı (LoginWindow)
Amaç: Kullanıcıların uygulamaya giriş yapmasını sağlar.
Nasıl Çalışır?
-Kullanıcı adı ve şifre giriş alanları bulunur.
-Kullanıcı adı ve şifre, önceden tanımlanmış geçerli kimlik bilgileriyle eşleştirilir.
-Doğru kimlik bilgileri girildiğinde, EMG işleme uygulamasına erişim sağlanır.
-Arka plan resmi (deneme.png) yüklenir ve görüntülenir.

2. EMG İşleme Uygulaması (EMGProcessorApp)
Amaç: EMG sinyallerini yüklemek, filtrelemek, analiz etmek ve görselleştirmek.
Nasıl Çalışır?
-Kas Kütüphanesi: Farklı kas grupları için önceden tanımlanmış filtreleme parametreleri içerir (örneğin, Biceps Brachii, Quadriceps Femoris gibi).
-GUI (Grafik Kullanıcı Arayüzü): Kullanıcılar, kas kategorisi ve kas seçimi yapabilir.
-Filtreleme parametreleri (lowcut, highcut, envelope, RMS window) girilebilir veya önceden tanımlanmış değerler kullanılabilir.
-Notch filtresi (50 Hz veya 60 Hz) ve Q faktörü ayarlanabilir.
-FFT (Hızlı Fourier Dönüşümü) ve PSD (Güç Spektral Yoğunluğu) analiz parametreleri ayarlanabilir.
-Dosya Yükleme: Kullanıcılar, EMG sinyallerini içeren TXT veya CSV dosyalarını yükleyebilir.

Sinyal İşleme:
-Yüklenen sinyaller, notch filtresi ve bandpass filtresi ile işlenir.
-RMS (Root Mean Square) zarfı hesaplanır.
-Frekans analizi (FFT ve PSD) yapılır.

Görselleştirme:
-Ham sinyal, filtrelenmiş sinyal, RMS zarfı ve frekans analizi grafikleri çizilir.

3. Sinyal İşleme Fonksiyonları
-Notch Filtresi: Belirli bir frekanstaki gürültüyü (örneğin, 50 Hz şebeke gürültüsü) bastırmak için kullanılır.
-Bandpass Filtresi: Sinyali belirli bir frekans aralığında filtreler (örneğin, 20-450 Hz).
-RMS Zarfı: Sinyalin genlik zarfını hesaplar, kas aktivasyonunu temsil eder.
-FFT ve PSD: Sinyalin frekans bileşenlerini analiz eder.

4. Görselleştirme
Zaman Domain Grafikleri:
-Ham sinyal
-Filtrelenmiş sinyal
-RMS zarfı

Frekans Domain Grafikleri:
-Ham sinyalin FFT'si
-Filtrelenmiş sinyalin PSD'si
-RMS zarfının FFT'si

5. Hata Yönetimi
-Kullanıcı girdileri ve sinyal işleme sırasında oluşabilecek hatalar yakalanır ve kullanıcıya bilgi verilir.
-Parametrelerin geçerliliği kontrol edilir (örneğin, lowcut < highcut olmalı).
