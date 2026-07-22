# Spring Boot Nedir?

**Spring Boot**, popüler Spring Framework ekosistemi üzerine kurulmuş, Java tabanlı açık kaynaklı bir uygulama geliştirme çerçevesidir (framework). Geliştiricilerin minimum yapılandırmayla, hızlı bir şekilde bağımsız (standalone) ve üretime hazır (production-ready) uygulamalar ve mikroservisler geliştirmesini sağlar.

Geleneksel Spring projelerinde, XML dosyaları veya uzun Java sınıfları ile detaylı altyapı ve sunucu ayarları yapmak gerekirken, Spring Boot bu karmaşık süreçleri büyük ölçüde ortadan kaldırır.

---

## Spring Boot'un Temel Özellikleri

* **Otomatik Yapılandırma (Auto-Configuration):** Projenize eklediğiniz kütüphaneleri (örneğin bir veritabanı sürücüsü veya web bileşeni) algılar ve uygulamanızı akıllı bir şekilde otomatik olarak yapılandırır.
* **Gömülü Sunucu Desteği (Embedded Servers):** İçerisinde Apache Tomcat, Jetty veya Undertow gibi web sunucularını barındırır. Bu sayede harici bir sunucu kurmanıza gerek kalmadan uygulamanızı doğrudan bir JAR dosyası olarak çalıştırabilirsiniz.
* **Başlangıç Bağımlılıkları (Starter Dependencies):** Maven veya Gradle gibi araçlar için optimize edilmiş `spring-boot-starter` paketleri sunar. Tek bir paketle (örneğin `spring-boot-starter-web`) ihtiyacınız olan tüm kütüphaneleri otomatik olarak projenize dahil edebilirsiniz.
* **XML Yapılandırması Gerektirmez:** Tamamen Java tabanlı konfigürasyonları destekler; karmaşık XML dosyaları yazma zorunluluğunu ortadan kaldırır.
* **Üretime Hazır Araçlar (Spring Boot Actuator):** Canlı sistemdeki uygulamaların sağlık durumunu (health check), metriklerini ve performansını izlemenizi sağlayan dahili araçlar sunar.


## Spring ve Spring Boot Arasındaki Fark Nedir?

| Özellik | Spring Framework | Spring Boot |
| :--- | :--- | :--- |
| **Yapılandırma** | Manuel ve detaylı XML/Java konfigürasyonları gerektirir. | Otomatik yapılandırma (Auto-configuration) sunar. |
| **Sunucu Kurulumu** | Harici bir uygulama sunucusuna (Tomcat, WildFly vb.) ihtiyaç duyar. | İçerisinde gömülü sunucu barındırır (Harici kuruluma gerek yoktur). |
| **Geliştirme Hızı** | Fazla boilerplate (tekrar eden) kod ve kurulum süresi gerektirir. | Hızlı başlangıç sağlar, kod yükünü ve zaman kaybını azaltır. |

---

## Neden Spring Boot Tercih Edilir?

1. **Hız ve Kolaylık:** Fikir aşamasından canlı ortama geçiş süresini minimuma indirir.
2. **Mikroservis Uyumluluğu:** Modern bulut tabanlı ve mikroservis mimarileriyle mükemmel uyum sağlar.
3. **Geniş Ekosistem:** Spring Security, Spring Data ve Spring Cloud gibi güçlü alt projelerle sorunsuz entegre olur.
4. **Büyük Topluluk:** Dünyada milyonlarca geliştirici tarafından kullanıldığı için geniş bir dokümantasyon ve destek havuzuna sahiptir.
