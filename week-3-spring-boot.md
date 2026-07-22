# Spring Boot Nedir?

**Spring Boot**, popüler Spring Framework ekosistemi üzerine kurulmuş, Java tabanlı açık kaynaklı bir uygulama geliştirme çerçevesidir (framework). Geliştiricilerin minimum yapılandırmayla, hızlı bir şekilde bağımsız (standalone) ve üretime hazır (production-ready) uygulamalar ve mikroservisler geliştirmesini sağlar.

Geleneksel Spring projelerinde, XML dosyaları veya uzun Java sınıfları ile detaylı altyapı ve sunucu ayarları yapmak gerekirken, Spring Boot bu karmaşık süreçleri büyük ölçüde ortadan kaldırır.

---

## Spring Boot'un Temel Özellikleri

* **Otomatik Yapılandırma (Auto-Configuration):** Projenize eklediğiniz kütüphaneleri (örneğin bir veritabanı sürücüsü veya web bileşeni) algılar ve uygulamanızı akıllı bir şekilde otomatik olarak yapılandırır.
* **Gömülü Sunucu Desteği (Embedded Servers):** İçerisinde Apache Tomcat, Jetty veya Undertow gibi web sunucularını barındırır. Bu sayede harici bir sunucu kurmanıza gerek kalmadan uygulamanızı doğrudan bir JAR dosyası olarak çalıştırabilirsiniz.
* **Başlangıç Bağımlılıkları (Starter Dependencies):** Maven veya Gradle gibi araçlar için optimize edilmiş spring-boot-starter paketleri sunar. Tek bir paketleihtiyacınız olan tüm kütüphaneleri otomatik olarak projenize dahil edebilirsiniz.
* **XML Yapılandırması Gerektirmez:** Tamamen Java tabanlı konfigürasyonları destekler; karmaşık XML dosyaları yazma zorunluluğunu ortadan kaldırır.
* **Üretime Hazır Araçlar (Spring Boot Actuator):** Canlı sistemdeki uygulamaların sağlık durumunu (health check), metriklerini ve performansını izlemenizi sağlayan dahili araçlar sunar.
