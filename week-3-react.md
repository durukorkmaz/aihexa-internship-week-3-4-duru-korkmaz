### React Nedir?

* **Tanım:** Kullanıcı arayüzleri (UI) oluşturmak için Meta (Facebook) tarafından geliştirilmiş, açık kaynaklı ve popüler bir JavaScript kütüphanesidir.
* **Bileşen Tabanlı Mimari:** Uygulamayı bağımsız, yeniden kullanılabilir ve izole küçük parçalara (bileşenlere/components) bölerek büyük projeleri yönetmeyi kolaylaştırır.
* **Virtual DOM (Sanal DOM):** Gerçek DOM manipülasyonlarının maliyetli ve yavaş olması nedeniyle, değişiklikleri önce bellekteki sanal DOM üzerinde hesaplar ve sadece değişen kısımları gerçek DOM'a yansıtarak yüksek performans sağlar.
* **Tek Sayfalık Uygulama (SPA):** Sayfa yenilenmesine gerek kalmadan, kullanıcı etkileşimlerine anlık ve dinamik tepkiler veren akıcı web uygulamaları geliştirmeye olanak tanır.

### Frontend Nedir?

* **Tanım:** Kullanıcının bir web sitesi veya uygulamada gözle gördüğü, düğmelere tıkladığı, gezindiği ve doğrudan etkileşime girdiği **istemci tarafı (client-side)** arayüz katmanıdır.
* **Temel Yapı Taşları:** Web sitesinin iskeletini oluşturan **HTML**, tasarımı ve görsel stilini belirleyen **CSS**, kullanıcı etkileşimlerini ve dinamik davranışları sağlayan **JavaScript** teknolojilerine dayanır.
* **Çalışma Prensibi:** Kullanıcının tarayıcısında (Chrome, Safari, Firefox vb.) doğrudan çalışarak sunucudan gelen ham verileri görsel sayfalara ve butonlara dönüştürür.
* **Modern Ekosistem:** Günümüzde saf HTML/CSS/JS yerine, geliştirme sürecini hızlandırmak ve büyük ölçekli projeleri yönetmek için **React**, **Vue** veya **Angular** gibi modern kütüphane ve çatı (framework) sistemleriyle geliştirilir.

### Component (Bileşen) Mantığı Nedir?

* **Tanım:** React uygulamalarının temel yapı taşlarıdır; bir web arayüzünü bağımsız, yeniden kullanılabilir ve kendi başına çalışabilen küçük parçalara böler.
* **Yeniden Kullanılabilirlik (Reusability):** Tek bir component (örneğin bir buton, kart veya navbar) tasarlandıktan sonra uygulamanın farklı yerlerinde tekrar tekrar çağrılarak kod tekrarı önlenir.
* **İzolasyon ve Modülerlik:** Her component kendi HTML yapısını (JSX), stilini ve mantığını (`state` ve `props`) kendi içinde barındırır; bu sayede büyük projeler daha düzenli ve yönetilebilir hale gelir.
* **Hiyerarşi (Parent-Child):** Component'ler birbirini kapsayabilir. Üst (parent) component'ler alt (child) component'lere veri (`props`) aktararak arayüzün dinamik bir şekilde akmasını sağlar.

### JSX Nedir?

* **Tanım:** JavaScript XML kelimelerinin kısaltmasıdır; JavaScript kodu içinde doğrudan HTML benzeri bir yapı yazmamıza olanak tanıyan bir sözdizimi (syntax) uzantısıdır.
* **Amacı ve Avantajı:** Arayüz bileşenlerini oluştururken JavaScript'in tüm gücünü (mantık, döngüler, koşullar) HTML yapısıyla birleştirerek kod yazmayı çok daha sezgisel ve okunabilir hale getirir.
* **Tarayıcı Uyumluluğu:** Doğrudan tarayıcılar tarafından anlaşılamaz; bu nedenle derleme aşamasında Babel gibi araçlar vasıtasıyla standart JavaScript fonksiyonlarına (`React.createElement`) dönüştürülür.
* **Sözdizimi Kuralları:** İçerisinde yazılan etiketler mutlaka kapatılmalı (`<br />`), JavaScript ifadeleri süslü parantez `{}` arasına yazılmalı ve HTML'deki `class` yerine `className` gibi özel nitelikler kullanılmalıdır.

### Props ve State Farkı Nedir?

* **Tanımları:** `Props` (Properties), üst bileşenden alt bileşene veri aktarmak için kullanılan dışsal parametrelerdir; `State` ise bir bileşenin kendi içinde yönettiği, değiştirilebilir dahili hafızasıdır.
* **Değişkenlik (Mutability):** `Props` salt okunurdur (**read-only**), alt bileşen gelen props değerini doğrudan değiştiremez; `State` ise bileşenin kendi içinde güncelleyebileceği (mutable) verilere sahiptir.
* **Kontrol Kaynağı:** `Props` dışarıdan (parent bileşenden) kontrol edilir ve akış tek yönlüdür; `State` ise tamamen bileşenin kendi iç mantığı ve hook'lar (`useState`) aracılığıyla kontrol edilir.
* **Yeniden Render (Rerender) Etkisi:** `Props` değiştiğinde bileşen yeniden çalışabilir ancak bu değişim genellikle üst bileşenin kontrolündedir; `State` doğrudan kendi içinde güncellendiği an bileşenin yeniden render edilmesini tetikler ve arayüzü günceller.

### useState Nedir?

* **Tanım:** Fonksiyonel bileşenlerde (functional components) dinamik veri tutmamızı ve bu verileri zamanla güncellememizi sağlayan temel bir React Hook'udur.
* **Kullanım Sözdizimi:** `const [deger, setDeger] = useState(baslangicDegeri);` şeklinde tanımlanır; burada ilk eleman güncel değeri, ikinci eleman ise bu değeri değiştirmeye yarayan fonksiyonu temsil eder.
* **Tetikleme Mekanizması:** `setDeger` fonksiyonu çağrıldığında React durumu (state) günceller ve ilgili bileşeni otomatik olarak yeniden render ederek yeni verinin arayüze yansıtılmasını sağlar.
* **Sayfa Bağımsızlığı:** Her `useState` tanımı, çağrıldığı bileşene özel izole bir hafıza alanı oluşturur; bu sayede bileşen her çalıştığında ilk değer sıfırlanmaz, güncel hali korunur.

### useEffect Nedir?

* **Tanım:** Fonksiyonel bileşenlerde veri çekme, abonelik başlatma veya DOM'u manuel değiştirme gibi "yan etkileri" (side effects) yönetmemizi sağlayan bir React Hook'udur.
* **Yaşam Döngüsü (Lifecycle) Rolü:** Klasik bileşenlerdeki `componentDidMount`, `componentDidUpdate` ve `componentWillUnmount` yaşam döngüsü metotlarının işlevini tek bir çatı altında birleştirir.
* **Çalışma Mantığı:** `useEffect(callback, dependencies)` şeklinde kullanılır; ikinci parametre olarak verilen bağımlılık dizisinin (dependency array) durumuna göre (boş, dolu veya yok) ne zaman çalışacağı kontrol edilir.
* **Temizlik (Cleanup):** `useEffect` içinde döndürülen bir fonksiyon (cleanup function) aracılığıyla, bileşen ekrandan kaldırıldığında (unmount) bellek sızıntılarını önlemek için timer veya event listener gibi kaynaklar temizlenebilir.

### React Router Nedir?

* **Tanım:** Tek sayfalık uygulamalarda (SPA - Single Page Application) farklı URL adreslerine karşılık gelen farklı bileşenlerin (sayfaların) gösterilmesini ve kullanıcı tarayıcı geçmişinin yönetilmesini sağlayan standart yönlendirme kütüphanesidir.
* **Çalışma Prensibi:** Geleneksel çok sayfalı web sitelerinden farklı olarak, tarayıcının sunucuya her seferinde yeni bir HTML isteği atmasını engeller; bunun yerine URL değişimini yakalayarak ilgili bileşeni dinamik olarak ekrana getirir ve sayfa yenilenme ihtiyacını ortadan kaldırır.
* **Temel Bileşenleri:** Rotaları tanımlamak için `Routes` ve `Route`, sayfalar arası geçiş yapmak için bağlantı kurmak amacıyla `Link` veya `NavLink`, URL içerisindeki parametreleri yakalamak için ise `useParams` gibi özel kancalar (hooks) sunar.
* **Kullanım Amacı:** Kullanıcılara sanki farklı web sayfaları arasında geziniyormuş deneyimi yaşatırken, uygulamanın hızını ve akıcılığını korumayı sağlar.

### Form Yönetimi Nedir?

* **Tanım:** Kullanıcıların arayüzdeki form elemanları (input, select, textarea vb.) aracılığıyla girdiği verilerin toplanması, saklanması, doğrulanması (validation) ve sunucuya gönderilmesi sürecidir.
* **Kontrollü Bileşenler (Controlled Components):** React'te form elemanlarının değerlerinin `useState` hook'u ile state'e bağlanarak her an kontrol altında tutulması ve güncellenmesi yaklaşımıdır.
* **Validasyon (Doğrulama):** Kullanıcının eksik, hatalı veya yanlış formatta veri girmesini engellemek için kurallar (örneğin e-posta formatı, minimum şifre uzunluğu) tanımlama ve hata mesajı üretme sürecidir.
* **Popüler Kütüphaneler:** Büyük projelerde form yönetimini ve validasyonu kolaylaştırmak için `Formik`, `React Hook Form` gibi harici kütüphaneler yaygın olarak tercih edilir.

### API'den Veri Çekme Nedir?

* **Tanım:** Frontend uygulamasının, harici bir sunucu veya veritabanı ile HTTP protokolü üzerinden haberleşerek veri alması (GET) veya sunucuya veri göndermesi (POST, PUT, DELETE) sürecidir.
* **Kullanım Amacı:** Statik uygulamaları dinamik hale getirmek; kullanıcı listesi, ürün katalogları veya hava durumu gibi güncel verileri dış kaynaklardan çekerek arayüzde göstermektir.
* **Modern Yöntemler:** Tarayıcıların yerleşik olarak sunduğu yerel `fetch()` API'si veya geliştirilmiş özellikler sunan harici **Axios** kütüphanesi bu amaçla sıklıkla kullanılır.
* **Asenkron Yapı (Async/Await):** Ağ istekleri zaman aldığından işlemler `async` ve `await` yapılarıyla yürütülür; bu sayede verinin gelmesi beklenirken uygulamanın donması engellenir ve loading durumları yönetilir.

### LocalStorage Mantığı Nedir?

* **Tanım:** Tarayıcının içerisinde yer alan, web sitelerinin kullanıcının tarayıcısında kalıcı olarak anahtar-değer (key-value) ilişkisiyle veri depolamasını sağlayan bir Web Storage API özelliğidir.
* **Kalıcılık:** `localStorage`'a kaydedilen veriler, tarayıcı veya sekme kapatılsa, hatta bilgisayar yeniden başlatılsa bile silinmez; yalnızca kullanıcı tarayıcı verilerini temizlediğinde veya kod aracılığıyla (`removeItem`, `clear`) silindiğinde ortadan kalkar.
* **Veri Tipi Sınırı:** Sadece **string (metin)** türünde veri saklayabilir; bu nedenle nesne (object) veya dizi (array) kaydetmek istendiğinde veriler `JSON.stringify()` ile metne dönüştürülür, okunurken ise `JSON.parse()` ile tekrar orijinal haline getirilir.
* **Kullanım Alanları:** Kullanıcının tema tercihi (koyu/açık mod), dil seçimi veya oturum bilgileri gibi sayfa yenilendiğinde kaybolmaması gereken küçük boyutlu verileri tarayıcıda tutmak için idealdir.

### Kullanıcıya Hata Mesajı Nasıl Gösterilir?

* **Tanım:** Uygulama içinde API isteklerinin başarısız olması, form verilerinin eksik veya hatalı girilmesi gibi beklenmeyen durumlarda, kullanıcının ne yanlış gittiğini anlamasını ve yönlendirilmesini sağlayan bilgilendirme mekanizmasıdır.
* **Koşullu İşleme (Conditional Rendering):** `useState` ile tutulan bir `error` state'i veya boolean kontrolü sayesinde, hata oluştuğu anda ekrandaki ilgili HTML/JSX bloğunun dinamik olarak görünür hale getirilmesi mantığıdır.
* **Form Validasyon Hataları:** Kullanıcı hatalı bir format girdiğinde (örneğin geçersiz e-posta veya kısa şifre), ilgili input alanının hemen altında veya yanında kırmızı renkli uyarı metinleriyle anlık geri bildirim verilmesidir.
* **Bildirim Kütüphaneleri (Toast / Alert):** Ekranın köşesinde belirip birkaç saniye sonra kaybolan şık bildirimler (Toastify, SweetAlert2 veya UI kütüphanelerinin Alert bileşenleri) kullanarak genel sistem hatalarının veya başarı durumlarının kullanıcıya şık bir şekilde iletilmesidir.

### Loading Durumu (Yüklenme Durumu) Nedir?

* **Tanım:** Uygulama içinde API'den veri çekilmesi, büyük dosyaların indirilmesi veya sunucuya form gönderilmesi gibi asenkron ve zaman alan işlemler sürerken, sürecin devam ettiğini kullanıcıya bildiren durum yönetimidir.
* **Kullanım Amacı:** Ağ isteklerinin tamamlanması milisaniyeler veya saniyeler sürebileceğinden, kullanıcının ekranda boş bir sayfa görmesini engeller ve uygulamanın donmadığını, arka planda çalıştığını göstererek kullanıcı deneyimini (UX) iyileştirir.
* **Uygulama Yöntemi:** Genellikle `const [loading, setLoading] = useState(false);` şeklinde bir state tanımlanır; istek atılmadan hemen önce `true` yapılır, veri geldiğinde veya hata oluştuğunda ise `false` olarak güncellenir.
* **Görsel Örnekler:** Bu süreçte ekranda dönen çarklar (spinners), iskelet ekranlar (skeleton loaders) veya "Yükleniyor..." gibi bilgilendirici metinler koşullu render (conditional rendering) yardımıyla gösterilir.

### Responsive Tasarım Nedir?

* **Tanım:** Web sitelerinin ve uygulamaların masaüstü bilgisayarlar, tabletler ve akıllı telefonlar gibi farklı ekran boyutlarına ve çözünürlüklere kusursuz bir şekilde uyum sağlamasını, otomatik olarak yeniden şekillenmesini sağlayan tasarım yaklaşımıdır.
* **Kullanım Amacı:** Kullanıcıların hangi cihazı kullandığından bağımsız olarak (yatay veya dikey tutuş fark etmeksizin) web sitesinde rahatça gezinebilmesini, yazıları okuyabilmesini ve butonlara tıklayabilmesini sağlayarak kullanıcı deneyimini (UX) en üst düzeye çıkarmaktır.
* **Temel Teknikler:** CSS içerisindeki **Media Queries** (Medya Sorguları) yardımıyla ekran genişliklerine göre farklı kurallar tanımlanır; ayrıca modern **Flexbox** ve **Grid** yapıları veya Bootstrap gibi CSS çatıları esnek (fluid) yerleşimler oluşturmayı kolaylaştırır.
* **Mobil Uyumluluk:** Günümüzde internet trafiğinin büyük bir kısmı mobil cihazlardan geldiği için, responsive tasarım yalnızca bir tercih değil, arama motoru optimizasyonu (SEO) ve erişilebilirlik açısından zorunlu bir standarttır.

### Frontend Klasör Yapısı Nasıl Okunur?

* **Tanım:** Bir yazılım projesindeki dosya ve dizinlerin (klasörlerin) mantıksal bir düzene göre organize edilerek projenin okunabilirliğini, sürdürülebilirliğini ve ekip içi uyumu artıran mimari yerleşim düzenidir.
* **Genel Standartlar (React Projeleri):**
  * `node_modules/`: Projenin çalışması için gereken tüm harici paketlerin ve kütüphanelerin bulunduğu klasördür.
  * `public/`: Statik dosyaların (favicon, logo, resimler veya doğrudan sunulan `index.html`) saklandığı alandır.
  * `src/`: Geliştiricinin tüm kodlarını yazdığı ana kaynaktır; bileşenler, sayfalar ve stiller burada yer alır.
* **Alt Dizin Mantığı:**
  * `components/`: Uygulamanın farklı yerlerinde tekrar tekrar kullanılan ortak küçük bileşenlerin (butonlar, kartlar, navbar vb.) toplandığı klasördür.
  * `pages/` veya `views/`: Web sitesindeki her bir sayfaya (Anasayfa, Hakkımızda, İletişim) karşılık gelen ana sayfa bileşenlerini barındırır.
  * `assets/`: Projede kullanılan görsel, ikon, font veya global stil dosyalarının saklandığı yerdir.
  * `services/` veya `api/`: Backend servisleri ile haberleşen, API isteklerinin (GET, POST vb.) merkezi olarak yönetildiği dosyaları içerir.
* **Okuma Stratejisi:** Projeyi incelerken önce `src/` klasörüne bakılır, ana giriş noktası (`App.js` veya `main.jsx`) tespit edilir ve uygulamanın hangi mantıkla bölündüğü (özellik bazlı veya dosya türü bazlı) bu dizin yapısı takip edilerek çözümlenir.

### Eğitim Kayıt Formu ve Örnek JSON Tasarımı

* **Formun Amacı:** Kullanıcıların kişisel bilgilerini, iletişim tercihlerini ve katılmak istedikleri eğitim detaylarını sisteme girmesini sağlamak ve bu verileri backend servisine kurallara uygun bir JSON formatında iletmektir.
* **İstenen Form Alanları:** Ad, Soyad, E-posta, Telefon, Eğitim seçimi, Eğitim seviyesi, Açıklama ve KVKK onayı.
* **Backend'e Gönderilecek Örnek JSON Yapısı:**
```json
{
  "firstName": "Duru",
  "lastName": "Korkmaz",
  "email": "duru@ornekmail.com",
  "phone": "0538 717 13 24",
  "educationName": "Frontend Web Geliştirme Eğitimi",
  "level": "Başlangıç",
  "description": "Eğitim içeriği ve çalışma saatleri hakkında bilgi almak istiyorum.",
  "kvkkApproved": true
}
```
### AIHEXA Projesinde React Nerede Kullanılır?

* **Kullanıcı Arayüzü ve Sayfa Tasarımı:** AIHEXA projesinin web tabanlı arayüzünde, kullanıcıların yapay zeka araçlarıyla etkileşime girdiği, veri girdiip sonuçları izlediği tüm ön yüz (frontend) bileşenlerinin geliştirilmesinde kullanılır.
* **Modüler Bileşen Mimarisi:** Panel içi modüllerin, butonların, formların, veri tablolarının ve menülerin (sidebar/navbar) bağımsız ve yeniden kullanılabilir bileşenler (`components`) olarak tasarlanmasını sağlar.
* **Dinamik Veri Akışı ve State Yönetimi:** Kullanıcının yaptığı seçimlerin, girdi değerlerinin ve API üzerinden gelen yapay zeka yanıtlarının sayfa yenilenmeden anlık olarak arayüze yansıtılmasında (`useState`, `useEffect`) kritik rol oynar.
* **Tek Sayfalık Uygulama (SPA) Deneyimi:** Kullanıcıların farklı analiz ekranları veya paneller arasında hızlı ve akıcı bir şekilde geçiş yapabilmesi için React Router tabanlı yönlendirme altyapısını oluşturur.

