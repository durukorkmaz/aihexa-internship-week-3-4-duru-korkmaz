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

# Backend Nedir?

**Backend**, bir yazılım mimarisinin kullanıcı tarafından doğrudan erişilemeyen, sunucu tarafında (server-side) çalışan ve sistemin operasyonel altyapısını oluşturan kritik katmanıdır. Geleneksel olarak istemci (frontend) ile veritabanı arasında konumlanan bu yapı; uygulamanın iş mantığını, veri yönetimi süreçlerini, güvenlik protokollerini, performans optimizasyonlarını ve harici sistem entegrasyonlarını merkezi olarak yönetir. 

Modern yazılım mühendisliğinde backend, yalnızca bir veri deposu ile arayüz arasındaki köprü olmanın ötesinde; yüksek eşzamanlılık (concurrency), ölçeklenebilirlik, veri bütünlüğü ve sistem kararlılığını garanti eden ana omurgayı temsil eder.

---

## Temel Görevleri ve Sorumluluk Alanları

* **İş Mantığı Yönetimi (Business Logic):** Uygulamanın temel kurallarını, karmaşık hesaplama süreçlerini ve veri doğrulama prosedürlerini sunucu seviyesinde icra eder. İstemci tarafında manipüle edilemeyecek kuralların güvenli bir ortamda çalıştırılmasını sağlar.
* **Veri Yönetimi ve Kalıcılık (Data Persistence):** İlişkisel veya ilişkisel olmayan veritabanları ile doğrudan etkileşim kurarak; büyük veri setlerinin depolanmasını, güncellenmesini, optimize edilmiş sorgularla çağrılmasını ve ACID prensipleri çerçevesinde veri bütünlüğünün korunmasını sağlar.
* **API ve Servis Mimarisi:** İstemci katmanı (web, mobil, masaüstü uygulamaları) ile iletişim kurmak amacıyla HTTP/HTTPS protokolleri üzerinden RESTful, gRPC veya GraphQL gibi standartlaştırılmış servis uç noktaları (endpoints) tasarlar ve sunar.
* **Kimlik Doğrulama ve Güvenlik:** Kullanıcı oturumlarını güvenli token mekanizmalarıyla yönetir, rol tabanlı veya öznitelik tabanlı erişim denetimleri (RBAC/ABAC) uygular ve hassas verilerin şifrelenmesini (hashing, encryption) sağlar.
* **Hata Yönetimi ve Loglama (Error Handling & Logging):** Sistem genelinde oluşan istisnaları yakalar, kullanıcıya anlamlı hata kodları dönerken geliştirme ve denetim ekipleri için detaylı sistem logları oluşturur.
* **Harici Sistem Entegrasyonları:** Ödeme gateway servisleri, e-posta/SMS sağlayıcıları, bulut depolama hizmetleri ve üçüncü parti API'ler ile güvenli ve kesintisiz entegrasyonlar kurar.
* **Performans ve Kaynak Optimizasyonu:** Önbellekleme (caching - Redis, Memcached vb.) mekanizmaları kullanarak veritabanı yükünü azaltır, eşzamanlı istekleri (concurrency) yönetir ve sistemin yatay veya dikey olarak ölçeklenebilmesini sağlar.

---

## Mimari Yapı ve Katmanlar

Kapsamlı bir backend sistemi genellikle modüler veya katmanlı bir mimari üzerine kuruludur:

1. **Sunucu / Host Katmanı:** Uygulamanın barındırıldığı fiziksel veya bulut tabanlı (AWS, Google Cloud, Azure) altyapı.
2. **API / Rota Katmanı:** Gelen isteklerin karşılandığı, yönlendirildiği ve ilk doğrulamaların yapıldığı katman.
3. **Servis Katmanı:** İş mantığının (business logic) işlendiği ve algoritmaların çalıştığı ana çekirdek.
4. **Veri Erişim Katmanı (Data Access Layer):** Veritabanı sorgularının ORM (Object-Relational Mapping) araçları veya doğrudan sürücüler vasıtasıyla yürütüldüğü katman.
5. 
6. # REST API Nedir?

**REST API** (Representational State Transfer Application Programming Interface), web tabanlı sistemlerin birbiriyle iletişim kurmasını sağlayan, HTTP protokolü üzerine kurulu mimari bir standarttır. Roy Fielding tarafından 2000 yılında doktora tezinde tanımlanan REST prensipleri; farklı yazılım sistemlerinin (örneğin bir mobil uygulama ile bir sunucunun veya iki farklı mikroservisin) gevşek bağlı (loosely coupled), ölçeklenebilir ve standart bir dille veri alışverişi yapmasına olanak tanır.

Modern web ve mobil ekosistemlerin temel iletişim omurgasını oluşturan REST API, istemci (client) ile sunucu (server) arasındaki veri transferini standartlaştırarak platform bağımsız bir çalışma ortamı sunar.

---

## REST Mimarisinin Temel İlkeleri ve Kısıtlamaları

Bir web servisinin "RESTful" kabul edilebilmesi için belirli mimari kısıtlamalara ve prensiplere uyması gerekir:

* **İstemci-Sunucu Ayrımı (Client-Server Architecture):** Kullanıcı arayüzü (istemci) ile veri depolama ve iş mantığı (sunucu) birbirinden tamamen bağımsızdır. Bu ayrım, her iki tarafın kendi içinde bağımsız olarak geliştirilebilmesini ve ölçeklenebilmesini sağlar.
* **Durumsuzluk (Statelessness):** Sunucu, istemciden gelen her bir isteği tamamen bağımsız olarak ele alır. İstemciye ait hiçbir oturum bilgisi (state) sunucu tarafında tutulmaz; her istek, işlemin gerçekleştirilmesi için gereken tüm bilgileri (kimlik doğrulama token'ları vb.) içermek zorundadır.
* **Önbelleklenebilirlik (Cacheability):** Yanıtlar (responses), istemci veya ara sunucular tarafından önbelleklenebilir (cacheable) olarak etiketlenmelidir. Bu sayede aynı verilere yapılan tekrar eden isteklerde sunucu yükü azaltılır ve performans artırılır.
* **Katmanlı Sistem (Layered System):** İstemci, doğrudan son sunucuyla iletişim kurduğunu varsayabilir ancak arada yük dengeleyiciler (load balancers), güvenlik duvarları veya önbellek sunucuları gibi katmanlar bulunabilir. Bu durum sistemin esnekliğini artırır.
* **Tekdüze Arayüz (Uniform Interface):** REST mimarisinin en belirleyici özelliğidir. Kaynakların (resources) tanımlanması, manipüle edilmesi ve yanıtların formatı standart bir arayüz üzerinden yürütülür.

---

## REST API'nin Temel Bileşenleri ve HTTP Metotları

REST mimarisinde her şey birer **kaynaktır (resource)** ve bu kaynaklar benzersiz URL (Uniform Resource Identifier) adresleri ile temsil edilir. Kaynaklar üzerinde gerçekleştirilecek işlemler ise standart **HTTP metotları** ile belirlenir:

* **GET:** Belirtilen URI adresindeki kaynağın verisini okumak veya listelemek için kullanılır. Güvenli ve idempotent (tekrarlandığında sonucu değiştirmeyen) bir metottur.
* **POST:** Sunucu üzerinde yeni bir kaynak oluşturmak için kullanılır. Idempotent değildir; her çağrıldığında yeni bir kayıt oluşturabilir.
* **PUT:** Mevcut bir kaynağın tamamını güncellemek veya kaynak yoksa belirtilen URI ile oluşturmak için kullanılır. Idempotenttir.
* **PATCH:** Mevcut bir kaynağın yalnızca belirli alanlarını (kısmi güncelleme) değiştirmek için kullanılır.
* **DELETE:** Belirtilen kaynağın sunucudan silinmesi amacıyla kullanılır.

---

## Veri Formatları ve İletişim

REST API'ler platformlar arası bağımsızlığı sağlamak için veri alışverişinde standart formatlar kullanır. Tarihsel olarak XML sıkça tercih edilmiş olsa da, günümüzde okunabilirliği, hafifliği ve ayrıştırma (parsing) kolaylığı nedeniyle neredeyse tamamen **JSON (JavaScript Object Notation)** formatı standart haline gelmiştir. İstek ve yanıt başlıklarında (headers) yer alan Content-Type ve Accept alanları, tarafların hangi veri formatıyla iletişim kuracağını belirler.

# JSON Nedir?

**JSON** (JavaScript Object Notation), insan tarafından okunabilir, hafif ve dil bağımsız bir veri değişim formatıdır. Adında "JavaScript" geçmesine rağmen tamamen bağımsız bir formattır ve hemen hemen tüm modern programlama dilleri (Java, Python, C#, PHP, Go vb.) tarafından yerleşik olarak desteklenir.

Geleneksel olarak veri alışverişinde kullanılan XML formatına kıyasla çok daha az yer kaplaması, hafif olması ve ayrıştırılmasının (parsing) kolay olması nedeniyle günümüzde web servislerinin, REST API'lerin ve NoSQL veritabanlarının vazgeçilmez veri standardı haline gelmiştir.

---

## JSON Formatının Temel Yapı Taşları ve Veri Tipleri

JSON, temel olarak anahtar-değer ilişkilerine ve sıralı listelere dayanan iki yapı üzerine kuruludur:

1. **Nesne (Object):** Süslü parantezler (`{ }`) içinde tanımlanır. İçerisinde anahtar-değer çiftleri barındırır. Anahtar ifadeler her zaman tırnak içinde (`"key"`) yazılır.
2. **Dizi / Liste (Array):** Köşeli parantezler (`[ ]`) içinde tanımlanır. Sıralı bir veri kümesini temsil eder.

### Desteklenen Veri Tipleri:
* **String (Metin):** Çift tırnak içinde yazılan karakter dizileri (`"Ahmet"`).
* **Number (Sayı):** Ondalıklı veya tam sayılar (`42`, `3.14`).
* **Boolean (Mantıksal):** Doğru veya yanlış değerler (`true` veya `false`).
* **Null (Boş):** Değersizlik veya yokluk durumu (`null`).
* **Array (Dizi):** Birden fazla verinin liste halinde tutulması (`["elma", "armut"]`).
* **Object (Nesne):** İç içe nesne yapıları oluşturulması.


# Controller Nedir?

**Controller** (Kontrolcü), MVC (Model-View-Controller) mimari deseninde kullanıcı ile sistem arasındaki etkileşimi yöneten, gelen istekleri (requests) karşılayan ve uygun yanıtları (responses) üreten bileşendir. Mimari içerisindeki köprü görevi sayesinde, istemciden gelen girdileri işler, model katmanındaki verileri günceller veya sorgular ve sonuçları kullanıcıya sunulmak üzere hazırlar.

Modern web uygulamalarında ve REST API mimarilerinde controller, yönlendirme (routing) mekanizmalarıyla doğrudan entegre çalışarak gelen HTTP isteklerini ilgili iş mantığı (business logic) fonksiyonlarına yönlendirir.

---

## Temel Görevleri ve Sorumluluk Alanları

* **İstek Karşılama ve Yönlendirme:** İstemciden (tarayıcı, mobil uygulama vb.) gelen HTTP isteklerini (GET, POST, PUT, DELETE vb.) karşılar ve doğru metodun çalıştırılmasını sağlar.
* **Girdi Doğrulama (Input Validation):** Kullanıcıdan gelen verilerin (form girdileri, query parametreleri, JSON payload) kurallara uygun olup olmadığını ve güvenlik kriterlerini karşılayıp karşılamadığını denetler.
* **Model ile İletişim:** Veritabanı veya iş mantığı katmanlarıyla (Services) iletişim kurarak gerekli verilerin çekilmesini, güncellenmesini veya kaydedilmesini talep eder.
* **Yanıt Üretme (Response Generation):** İşlenen verileri uygun formata dönüştürür. Geleneksel MVC yapılarında bir arayüzü (View) verilerle doldururken, REST API projelerinde doğrudan JSON formatında yanıt döner.
* **Hata Yönetimi (Error Handling):** İstek sırasında oluşabilecek hataları yakalar ve istemciye anlamlı HTTP durum kodları (200, 400, 404, 500 vb.) ile birlikte hata mesajları iletir.

---

## MVC Mimarisindeki Rolü

Katmanlı yapılarda sorumlulukların ayrılması (Separation of Concerns) prensibi gereği controller, verinin nasıl saklandığıyla (Model) veya nasıl gösterildiğiyle (View) doğrudan ilgilenmez:

1. **İstemci (Client):** Sunucuya bir istek gönderir (Örn: `/kullanici/profil`).
2. **Controller:** İsteği yakalar, ilgili servisi çağırarak veriyi hazırlar.
3. **Model:** Veritabanından gerekli kullanıcı bilgilerini getirir.
4. **Controller:** Gelen veriyi alır ve View katmanına (veya API istemcisine doğrudan JSON olarak) iletir.
5. **View / İstemci:** Sonuç kullanıcıya arayüz üzerinden sunulur.

---

## Örnek Kullanım Senaryosu (REST API)

Tipik bir modern web çatısında (örneğin Spring Boot veya Express.js) bir controller sınıfı şu şekilde yapılandırılır:

```java
@RestController
@RequestMapping("/api/urunler")
public class UrunController {

    private final UrunService urunService;

    public UrunController(UrunService urunService) {
        this.urunService = urunService;
    }

    @GetMapping("/{id}")
    public ResponseEntity<Urun> urunGetir(@PathVariable Long id) {
        Urun urun = urunService.idyeGoreGetir(id);
        return ResponseEntity.ok(urun);
    }

    @PostMapping
    public ResponseEntity<Urun> urunOlustur(@RequestBody Urun yeniUrun) {
        Urun kaydedilen = urunService.kaydet(yeniUrun);
        return ResponseEntity.status(HttpStatus.CREATED).kaydedilen;
    }
}
```
# Service Nedir?

**Service** (Servis), yazılım mimarilerinde (özellikle katmanlı mimarilerde ve Spring Boot gibi modern çatılarda) **iş mantığının (business logic)** ve kuralların barındırıldığı, yönetildiği temel bileşendir. Controller katmanından gelen ham verileri alır, gerekli hesaplamaları, doğrulamaları veya algoritma işlemlerini gerçekleştirir ve veritabanı işlemleri için model/repository katmanıyla iletişim kurar.

Yazılım geliştirme süreçlerinde **Sorumlulukların Ayrılması (Separation of Concerns)** prensibinin bir gereği olarak, HTTP isteklerini karşılayan Controller ile veri tabanı operasyonlarını yöneten Repository katmanları arasındaki köprüyü ve mantıksal beyni oluşturur.

---

## Temel Görevleri ve Sorumluluk Alanları

* **İş Mantığının İcrası (Business Logic Execution):** Uygulamanın temel kurallarını ve hesaplamalarını yürütür. Örneğin, bir e-ticaret uygulamasında sepet tutarına göre kargo ücretinin hesaplanması veya indirim kuponunun uygulanması gibi mantıksal işlemler burada yapılır.
* **Veri İşleme ve Doğrulama (Data Processing & Validation):** Controller'dan gelen verileri iş kuralı açısından denetler, veritabanına gitmeden önce gerekli dönüşümleri (mapping) gerçekleştirir.
* **İşlem Yönetimi (Transaction Management):** Birbirine bağlı birden fazla veritabanı işleminin (örneğin hem sipariş kaydı oluşturulması hem de stoktan düşülmesi) tek bir bütün halinde çalışmasını sağlar. Herhangi bir adımda hata oluşursa tüm işlemleri iptal ederek (rollback) veri bütünlüğünü korur.
* **Kod Tekrarını Önleme (Reusability):** Aynı iş mantığının birden fazla farklı Controller (örneğin hem Web API hem de Mobil API) tarafından ortak bir şekilde kullanılabilmesini sağlar.

---

## Örnek Kullanım Senaryosu (Spring Boot)

Spring Boot projelerinde bir servis sınıfı genellikle `@Service` anotasyonu ile tanımlanır ve constructor injection ile controller içerisinden çağrılır:

```java
@Service
public class UrunService {

    private final UrunRepository urunRepository;

    public UrunService(UrunRepository urunRepository) {
        this.urunRepository = urunRepository;
    }

    public Urun idyeGoreGetir(Long id) {
        // İş mantığı veya hata kontrolü burada yapılabilir
        return urunRepository.findById(id)
                .orElseThrow(() -> new RuntimeException("Ürün bulunamadı!"));
    }

    public Urun kaydet(Urun urun) {
        // Ürün fiyatı doğrulama gibi iş kuralları
        if (urun.getFiyat() < 0) {
            throw new IllegalArgumentException("Ürün fiyatı negatif olamaz.");
        }
        return urunRepository.save(urun);
    }
}
```
# Repository Nedir?

**Repository**, yazılım mimarilerinde veritabanı işlemlerini (veri tabanı sorgulama, ekleme, güncelleme, silme) yürüten ve iş mantığı katmanı ile veri kaynağı arasında soyutlama sağlayan katmandır.

## Temel Özellikleri ve Görevleri

* **Veritabanı Soyutlama:** Veritabanı sorgularını iş mantığından ayırarak kodun daha düzenli ve bağımsız olmasını sağlar.
* **CRUD İşlemleri:** Veriler üzerinde oluşturma (Create), okuma (Read), güncelleme (Update) ve silme (Delete) operasyonlarını gerçekleştirir.
* **Tekrar Eden Kodları Azaltma:** Standart veritabanı sorgularını merkezi bir yerde toplarak her defasında aynı SQL veya ORM komutlarının yazılmasını önler.
* **Veri Kaynağı Bağımsızlığı:** Uygulamanın kullandığı veritabanı teknolojisi (SQL, NoSQL vb.) değişse bile kodun geri kalanının minimum düzeyde etkilenmesini sağlar.
* **Test Edilebilirlik:** Veritabanı işlemlerini izole ederek servis katmanının birim testlerinin (unit test) daha kolay yazılmasına olanak tanır.

# Entity Nedir?

**Entity**, yazılım mimarilerinde (özellikle veri tabanı ve ORM yapılarında) veritabanındaki bir tabloyu temsil eden ve nesne yönelimli dillerde bir sınıf (class) olarak karşılık bulan veri modelidir.

## Temel Özellikleri ve Görevleri

* **Tablo Temsili:** Veritabanındaki ilişkisel bir tablonun, kod tarafındaki nesne yönelimli karşılığıdır.
* **Alan (Property) Eşlemesi:** Veritabanı tablosundaki sütunları (columns), sınıftaki özellikler (properties/fields) olarak ifade eder.
* **Veri Taşıma:** Veritabanı ile uygulama katmanları arasında verilerin nesne halinde taşınmasını sağlar.
* **İlişki Yönetimi:** Tablolar arasındaki ilişkileri (örneğin bire-bir, bire-çok veya çok-taya) kod düzeyinde nesne bağlarıyla temsil eder.
* **ORM Entegrasyonu:** JPA/Hibernate veya Entity Framework gibi araçlar vasıtasıyla SQL sorgusu yazmadan veritabanı işlemlerinin nesneler üzerinden yürütülmesine olanak tanır.

# DTO Nedir?

**DTO** (Data Transfer Object - Veri Transfer Nesnesi), farklı katmanlar veya sistemler arasında veri taşımak amacıyla kullanılan, içinde yalnızca veri alanları (properties) barındıran ve herhangi bir iş mantığı (business logic) içermeyen sade Java/yazılım sınıflarıdır.

## Temel Özellikleri ve Görevleri

* **Veri İzolasyonu:** Veritabanı tablolarını temsil eden Entity sınıflarının doğrudan dış dünyaya (istemciye) açılmasını önleyerek güvenlik ve gizlilik sağlar.
* **Sınırlı Veri Aktarımı:** İstemciye yalnızca ihtiyaç duyulan alanların (örneğin şifre gibi hassas veriler hariç tutularak) taşınmasına olanak tanır.
* **Ağ Trafiği Optimizasyonu:** Gereksiz verilerin transferini engelleyerek performans artışı sağlar ve payload boyutunu küçültür.
* **Katmanlar Arası Ayrım:** UI (Arayüz) ile Service veya Database katmanları arasındaki veri yapılarını birbirinden bağımsız hale getirir.
* **İş Mantığı İçermez:** Sadece veriyi taşımaya yarar; içerisinde herhangi bir operasyon, hesaplama veya veri tabanı sorgusu barındırmaz.

# JPA Nedir?

**JPA** (Java Persistence API), Java nesnelerini ilişkisel veritabanı tablolarına kalıcı olarak kaydetmek (persistence), sorgulamak ve yönetmek için kullanılan standart bir Java özellikler (specification) kümesidir.

## Temel Özellikleri ve Görevleri

* **ORM Standardı:** Nesne Yönelimli Programlama (OOP) dünyasındaki sınıflar ile ilişkisel veritabanındaki tablolar arasındaki eşleşmeyi standartlaştırır.
* **SQL Bağımsızlığı:** Doğrudan SQL sorguları yazma zorunluluğunu azaltarak JPQL (Java Persistence Query Language) veya nesne tabanlı metotlar üzerinden veri yönetimi sağlar.
* **Veritabanı Taşınabilirliği:** Alttaki veritabanı yönetim sistemi (MySQL, PostgreSQL, Oracle vb.) değiştirildiğinde kodun minimum düzeyde etkilenmesini sağlar.
* **Yaşam Döngüsü Yönetimi:** Nesnelerin veritabanındaki durumlarını (yeni, yönetilen, detached vb.) otomatik olarak takip eder ve yönetir.
* **Hibernate vb. Altyapılara Standart Sağlama:** JPA bir arayüzdür (specification); arkasında çalışan ve bu standardı uygulayan Hibernate, EclipseLink gibi popüler sağlayıcılar (providers) bulunur.

# Hibernate Nedir?

**Hibernate**, Java uygulamalarında nesne yönelimli programlama ile ilişkisel veritabanları arasındaki veri uyumsuzluğunu ortadan kaldıran, açık kaynaklı bir ORM (Object-Relational Mapping) aracıdır ve JPA standardının en popüler uygulayıcısıdır (provider).

## Temel Özellikleri ve Görevleri

* **ORM Uygulaması:** Java sınıflarını (Entity) ve nesnelerini veritabanı tablolarına otomatik olarak eşler.
* **HQL ve JPQL Desteği:** SQL yerine nesneler üzerinden sorgulama yapmayı sağlayan nesne odaklı sorgulama dilleri sunar.
* **Otomatik Tablo Oluşturma:** Uygulama çalıştırıldığında Java sınıflarına bakarak veritabanı tablolarını otomatik olarak oluşturabilir veya güncelleyebilir.
* **Önbellekleme (Caching):** Veritabanı sorgu performansını artırmak için birinci ve ikinci seviye önbellek mekanizmaları barındırır.
* **İşlem ve Bağlantı Yönetimi:** Veritabanı bağlantılarını ve transaction süreçlerini otomatik olarak yöneterek geliştirici yükünü azaltır.

# Maven Nedir?

**Apache Maven**, Java projelerinde proje yönetimi, yapılandırma (build) ve bağımlılık (dependency) yönetimi amacıyla kullanılan, proje model nesnesine (POM) dayalı popüler bir otomasyon aracıdır.

## Temel Özellikleri ve Görevleri

* **Bağımlılık Yönetimi:** Projede kullanılan dış kütüphanelerin ve sürümlerinin merkezi bir depo (Maven Central Repository) üzerinden otomatik olarak indirilmesini ve yönetilmesini sağlar.
* **Proje Yapılandırması ve Build Süreçleri:** Kodun derlenmesi, test edilmesi, paketlenmesi (JAR/WAR haline getirilmesi) ve dağıtılması gibi süreçleri standartlaştırır ve tek komutla çalıştırır.
* **Standart Proje Yapısı:** Tüm Maven projelerinde dosya ve klasör yerleşiminin (örneğin `src/main/java`, `src/test/java`) belirli bir standartta olmasını zorunlu kilarak ekip içi uyumu artırır.
* **POM (Project Object Model) Dosyası:** Projenin tüm ayarlarını, bağımlılıklarını ve eklenti yapılandırmalarını tek bir `pom.xml` dosyası üzerinden merkezi olarak yönetir.
* **Eklenti (Plugin) Ekosistemi:** Derleme, test etme veya raporlama gibi ek görevlerin eklentiler vasıtasıyla kolayca entegre edilmesine olanak tanır.

* # POM.xml Ne İşe Yarar?

**POM.xml** (Project Object Model), Apache Maven projelerinin kalbini oluşturan, projenin yapılandırma ayarlarını, bağımlılıklarını ve build süreçlerini XML formatında barındıran temel konfigürasyon dosyasıdır.

## Temel Özellikleri ve Görevleri

* **Bağımlılık (Dependency) Yönetimi:** Projede kullanılan harici kütüphanelerin ve kütüphane sürümlerinin merkezi bir şekilde tanımlanmasını ve otomatik olarak indirilmesini sağlar.
* **Proje Bilgilerinin Tanımlanması:** Projenin adını, sürümünü (version), paketleme türünü (JAR, WAR vb.) ve grup kimliğini (`groupId`) merkezi olarak saklar.
* **Build Süreçlerinin Yapılandırılması:** Kodun derlenmesi, test edilmesi, paketlenmesi ve dağıtılması sırasında hangi eklentilerin (plugins) ve kuralların çalışacağını belirler.
* **Modül ve Profil Yönetimi:** Büyük projelerde alt modüllerin yönetimini ve farklı ortamlara (geliştirme, canlı vb.) göre build profilleri oluşturulmasını sağlar.
* **Merkezi Kontrol:** Projeye ait tüm yapılandırma detaylarının tek bir dosya üzerinden yönetilmesine olanak tanıyarak sürdürülebilirliği artırır.

# Application.properties Nedir?

**application.properties**, Spring Boot projelerinde uygulamanın çalışma zamanı (runtime) davranışını, sunucu ayarlarını, veritabanı bağlantılarını ve harici konfigürasyon parametrelerini yönetmek için kullanılan merkezi yapılandırma dosyasıdır.

## Temel Özellikleri ve Görevleri

* **Merkezi Konfigürasyon:** Veritabanı URL'leri, kullanıcı adları, şifreler, port numaraları ve loglama seviyeleri gibi tüm kritik ayarları tek bir yerde toplar.
* **Ortam Yönetimi:** Farklı ortamlar (geliştirme, test, canlı) için ayarların kolayca ayrıştırılmasını sağlar (örneğin `application-dev.properties`).
* **Otomatik Özelleştirme:** Spring Boot'un sunduğu varsayılan otomatik yapılandırma (auto-configuration) değerlerini projeye özel olarak geçersiz kılmaya (override etmeye) olanak tanır.
* **Harici Parametreleme:** Kod üzerinde herhangi bir değişiklik yapmadan, uygulama parametrelerinin dışarıdan (çevre değişkenleri veya komut satırı argümanlarıyla) yönetilmesini sağlar.
* **Anahtar-Değer Yapısı:** Ayarların `anahtar = değer` (key-value) formatında sade bir şekilde yazılmasına ve okunmasına imkan tanır.

# Application.yml Nedir?

**application.yml**, Spring Boot projelerinde `application.properties` dosyasına alternatif olarak kullanılan, uygulama ayarlarını ve konfigürasyon parametrelerini **YAML (YAML Ain't Markup Language)** formatında tutan merkezi yapılandırma dosyasıdır.

## Temel Özellikleri ve Görevleri

* **Hiyerarşik Yapı:** Ayarların girintili (indentation) ve ağaç yapısında yazılmasına imkan tanıyarak daha okunabilir ve düzenli bir konfigürasyon sunar.
* **Tekrarları Önleme:** Aynı öneke sahip parametrelerin tekrar tekrar yazılmasını engeller, bu sayede dosya boyutunu ve karmaşıklığını azaltır.
* **Çoklu Profil Desteği:** Tek bir dosya içerisinde veya farklı dosyalar aracılığıyla (örneğin `application-dev.yml`, `application-prod.yml`) farklı ortamların ayarlarını kolayca yönetmeyi sağlar.
* **Aynı İşlevsellik:** `application.properties` ile aynı görevi görür; veritabanı bağlantıları, port numaraları ve harici parametreler bu dosya üzerinden tanımlanır.
* **Tip Güvenliği:** Yapılandırma verilerinin daha düzenli bir yapıda tutulmasına olanak tanır.

# HTTP Metotları (GET, POST, PUT, DELETE) Nedir ve Ne İşe Yarar?

**HTTP metotları**, web üzerindeki istemciler (tarayıcılar, mobil uygulamalar vb.) ile sunucular arasındaki iletişimi sağlayan, bir kaynağa (resource) hangi işlemin uygulanacağını belirten standart komutlardır.

## Temel HTTP Metotları ve Görevleri

* **GET:** Sunucudan belirtilen bir kaynağın verisini okumak veya listelemek için kullanılır; herhangi bir veri değişikliğine yol açmaz ve güvenlidir.
* **POST:** Sunucu üzerinde yeni bir kaynak oluşturmak veya mevcut kaynağa veri göndermek (örneğin form doldurmak veya veri kaydetmek) için kullanılır.
* **PUT:** Sunucudaki mevcut bir kaynağın tamamını güncellemek veya kaynak yoksa belirtilen URI ile yenisini oluşturmak için kullanılır.
* **DELETE:** Sunucu üzerinde belirtilen bir kaynağın silinmesi amacıyla kullanılır.

# HTTP Status Kodları Nedir?

**HTTP status kodları** (HTTP durum kodları), bir istemcinin (tarayıcı, mobil uygulama vb.) sunucuya gönderdiği isteğin sonucunu, sunucunun istemciye bildirdiği üç haneli sayısal standart kodlardır.

## Temel Sınıfları ve Görevleri

* **1xx (Bilgilendirme - Informational):** İsteğin alındığını ve işlemin devam ettiğini belirtir.
* **2xx (Başarılı - Success):** İsteğin sunucu tarafından başarıyla alındığı, anlaşıldığı ve işleme konulduğunu gösterir (Örn: `200 OK`, `201 Created`).
* **3xx (Yönlendirme - Redirection):** İsteğin tamamlanabilmesi için istemcinin başka bir eylem gerçekleştirmesini veya farklı bir adrese yönlendirilmesini sağlar (Örn: `301 Moved Permanently`).
* **4xx (İstemci Hatası - Client Error):** İsteğin hatalı yazıldığını, yetkisiz olduğunu veya ulaşılamayan bir kaynağı istediğini belirtir (Örn: `400 Bad Request`, `401 Unauthorized`, `404 Not Found`).
* **5xx (Sunucu Hatası - Server Error):** İsteğin geçerli olmasına rağmen sunucunun bu isteği yerine getiremediği durumlarda ortaya çıkan hatalardır (Örn: `500 Internal Server Error`, `502 Bad Gateway`).

# Yaygın HTTP Status Kodları ve Anlamları

**HTTP durum kodları**, sunucunun istemciye ilettiği isteğin sonuç durumunu gösteren üç haneli kodlardır. Sık kullanılan belirli kodların anlamları şunlardır:

## Başarılı Durum Kodları (2xx)

* **200 OK:** İsteğin başarılı bir şekilde gerçekleştirildiğini ve sunucunun istenen veriyi döndürdüğünü belirtir.
* **201 Created:** İsteğin başarılı olduğunu ve sunucu üzerinde yeni bir kaynağın (örneğin yeni bir kayıt) oluşturulduğunu gösterir.

## İstemci Hata Kodları (4xx)

* **400 Bad Request:** İsteğin hatalı, bozuk veya eksik sözdizimi nedeniyle sunucu tarafından anlaşılamadığını belirtir.
* **401 Unauthorized:** İsteğin gerçekleştirilmesi için kullanıcının kimlik doğrulaması (authentication) yapması gerektiğini gösterir.
* **403 Forbidden:** Sunucunun isteği anladığını ancak kullanıcının bu kaynağa erişim yetkisinin (authorization) olmadığını belirtir.
* **404 Not Found:** İstenen kaynağın sunucu üzerinde bulunamadığını gösterir.

## Sunucu Hata Kodları (5xx)

* **500 Internal Server Error:** Sunucunun isteği yerine getirmesini engelleyen beklenmeyen ve genel bir hata oluştuğunu belirtir.

# Backend Hata Mesajı Nasıl Okunur?

**Backend hata mesajı**, sunucu tarafında bir işlem başarısız olduğunda sistemin ürettiği, hatanın türünü, nedenini ve kod içerisindeki konumunu belirten tanısal metindir.

## Hata Mesajı Okuma Adımları

* **HTTP Durum Koduna Bakma:** Hataya sebep olan isteğin hangi HTTP sınıfına ait olduğunu (örneğin 4xx istemci hatası veya 5xx sunucu hatası) inceleyerek sorunun kaynağını ilk aşamada tespit etmek.
* **Stack Trace (Hata İzleme) İnceleme:** Konsolda veya loglarda yukarıdan aşağıya doğru akan metin yığınında, kendi yazdığınız sınıfların ve metotların geçtiği satırları (genellikle en üstteki satırlar) bularak hatanın nerede tetiklendiğini görmek.
* **Hata Türünü (Exception Type) Okuma:** Mesajın başında yer alan ifadeyi (örneğin `NullPointerException`, `IllegalArgumentException`, `SQLException`) inceleyerek hatanın kategorisini anlamak.
* **Hata Açıklama Mesajını Okuma:** Hata türünün yanındaki veya altındaki detay metnini inceleyerek (örneğin "Veritabanı bağlantısı kurulamadı" veya "Bu ID ile kayıt bulunamadı") sorunun özünü yakalamak.
* **Kök Nedene (Root Cause) Odaklanma:** İç içe geçmiş hata loglarında en altta veya "Caused by" ifadesinin arkasında yer alan asıl tetikleyici hataya odaklanmak.

# Stack Trace Backend Tarafında Nasıl Yorumlanır?

**Stack trace** (hata izleme kaydı), bir yazılım hatası (exception) meydana geldiğinde programın o an hangi metot çağrı yığınından geçtiğini adım adım gösteren detaylı hata raporudur.

## Yorumlama Adımları ve Unsurlar

* **Hatanın Türünü (Exception Class) Belirleme:** Raporun ilk satırında yer alan hata sınıfını (örneğin `NullPointerException`, `IllegalArgumentException`) inceleyerek hatanın genel kategorisini anlamak.
* **Hata Açıklama Mesajını Okuma:** Hata sınıfının yanında yer alan metni inceleyerek hatanın neden tetiklendiğine dair ipucunu (örneğin "Index 5 out of bounds for length 5") görmek.
* **Kendi Kodunuza Odaklanma (Kendi Paketiniz):** Log yığını içerisinde Java'nın kendi dahili kütüphanelerini (örneğin `java.base` veya `tomcat`) geçerek, kendi projenize ait paket adının (örneğin `com.ornek.proje`) geçtiği ilk satırı bulmak.
* **Dosya Adı ve Satır Numarasını Tespit Etme:** İlgili satırın sonunda parantez içinde yer alan dosya adını ve hata kodunun bulunduğu satır numarasını (örneğin `UrunService.java:42`) inceleyerek hatanın kodda tam olarak nerede yaşandığını görmek.
* **Tetikleyici Nedeni (Caused by) İnceleme:** Hata raporunun alt kısımlarında yer alan "Caused by:" ifadelerini takip ederek, asıl soruna yol açan kök nedeni (root cause) ortaya çıkarmak.
