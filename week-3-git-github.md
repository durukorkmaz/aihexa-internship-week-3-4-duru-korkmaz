##  Git Nedir ve Ne İşe Yarar?  
Git, yazılım geliştirme süreçlerinde projelerin geçmişini takip etmek, değişiklikleri yönetmek ve birden fazla geliştiricinin aynı proje üzerinde eş zamanlı çalışmasını sağlamak için kullanılan dağıtık (distributed) bir sürüm kontrol sistemidir.

Linus Torvalds tarafından 2005 yılında geliştirilen Git, dosyalarınızın zaman içindeki tüm değişimlerini kayda alır. Böylece projenizin herhangi bir eski versiyonuna dilediğiniz zaman geri dönebilir, kimin neyi ne zaman değiştirdiğini kolayca görebilirsiniz.

## Git'in Temel Özellikleri  
**Dağıtık Mimari (Distributed):** Merkezi sistemlerin aksine Git'te her geliştiricinin bilgisayarında projenin tüm geçmişi ve deposu (repository) eksiksiz olarak bulunur. İnternet bağlantısı olmasa bile yerelde commit atabilir, geçmişi inceleyebilirsiniz.

**Hız ve Performans:** Tasarımı sayesinde dosya işlemlerini, versiyon karşılaştırmalarını ve dallanma (branching) işlemlerini çok hızlı gerçekleştirir.

**Veri Güvenliği ve Bütünlüğü:** Git, içerdiği her veriyi (dosya, commit vb.) SHA-1 hash adı verilen benzersiz bir mekanizmayla şifreler. Bilginin izinsiz değiştirilmesi veya bozulması bu sayede engellenir.

**Dallanma (Branching) Kolaylığı:** Projenin ana koduna zarar vermeden yeni özellikler denemek veya hata ayıklamak için izole çalışma alanları oluşturmayı son derece pratik hale getirir.

## GitHub Nedir?
GitHub, Git altyapısını kullanan, bulut tabanlı bir depo (repository) barındırma ve ortak çalışma platformudur.

Git yerel bilgisayarınızda çalışıp dosya geçmişini yönetmenizi sağlarken, GitHub bu projeleri internet üzerinde (bulutta) saklamanıza, yedeklemenize ve diğer geliştiricilerle kolayca paylaşmanıza olanak tanır.

## GitHub Ne İşe Yarar? Temel Özellikleri Nelerdir?
Bulut Tabanlı Yedekleme: Yerel bilgisayarınızda yaşanabilecek teknik sorunlara karşı projelerinizin güvenli bir şekilde bulutta saklanmasını sağlar.

**Ekip Çalışması ve İş Birliği:** Birden fazla geliştiricinin aynı proje üzerinde çakışma yaşamadan, eş zamanlı ve koordineli bir şekilde çalışmasına imkan tanır.

**Açık Kaynak (Open Source) Desteği:** Dünyanın dört bir yanından yazılımcıların ortak projeler geliştirmesine, başkalarının kodlarını incelemesine ve projelere katkı (Pull Request ile) sağlamasına zemin hazırlar.

**Kod İncelemesi (Code Review):** Projeye eklenmek istenen değişikliklerin ana koda girmeden önce ekip arkadaşları tarafından incelenmesini, yorumlanmasını ve onaylanmasını sağlar.

**Portfolyo Oluşturma:** Yazılımcıların geliştirdikleri projeleri sergileyerek dijital bir özgeçmiş/portfolyo oluşturmasına olanak tanır.

**Proje ve Hata Yönetimi (Issue Tracking):** Projedeki görevlerin takip edilmesi, hataların (bug) raporlanması ve süreç yönetiminin yapılması için araçlar sunar.

## Repository Nedir?
Repository, yazılım geliştirme dünyasında bir projenin tüm dosyalarının, klasörlerinin ve bu dosyalara ait geçmişteki tüm değişiklik kayıtlarının (sürüm geçmişinin) saklandığı depo veya alan anlamına gelir.

Bir repository, projenizin doğuşundan itibaren geçirdiği evrim sürecini, kimin hangi satırı ne zaman değiştirdiğini ve farklı sürümleri bünyesinde barındırır.

### Repository Çeşitleri Nelerdir?
Local Repository (Yerel Depo): Kendi bilgisayarınızda bulunan ve üzerinde çalıştığınız projenin yerel kopyasıdır. İnternet bağlantısı gerektirmez; değişikliklerinizi yerelde commit'leyerek bu depoda saklarsınız.

**Remote Repository (Uzak Depo):** GitHub, GitLab veya Bitbucket gibi bulut tabanlı sunucularda barındırılan depodur. Projenin ekiple paylaşılmasını ve güvenli bir şekilde yedeklenmesini sağlar.

## Commit Nedir?
Commit, Git versiyon kontrol sisteminde projenizde yaptığınız değişikliklerin kalıcı olarak kaydedildiği an veya bu kayıt paketinin kendisidir.

Yazılım geliştirirken kodlarınızda değişiklikler yaparsınız. Bu değişiklikleri anlık olarak Git veritabanına kaydetmek istediğinizde bir commit atarsınız.

### Commit'in Temel Özellikleri ve Yapısı
Anlık Görüntü (Snapshot): Her commit, projenizin o andaki tam halinin bir anlık görüntüsünü alır ve saklar.

**Benzersiz Kimlik (Hash):** Her commit, sistem tarafından otomatik olarak üretilen SHA-1 tabanlı uzun ve benzersiz bir kimlik numarasına (hash) sahiptir. Bu sayede geçmişteki herhangi bir commit'e kolayca referans verilebilir.

**Commit Mesajı:** Her commit atılırken o kaydın ne amaçla yapıldığını açıklayan zorunlu bir mesaj yazılır. Bu, projenin geçmişine bakıldığında neyin neden değiştirildiğinin anlaşılmasını sağlar.

**Zaman Damgası ve Yazar:** Commit, değişikliği yapan kişinin adını, e-postasını ve işlemin yapıldığı tarih/saat bilgisini otomatik olarak kaydeder.

## Branch Nedir?
Branch (Dal), yazılım geliştirme sürecinde ana kod bloğundan bağımsız olarak yeni özellikler geliştirmek, hataları düzeltmek veya denemeler yapmak için oluşturulan izole çalışma kollarından her biridir.

Branch mantığı sayesinde, ana projenin kararlı halini bozmadan üzerinde güvenle yeni çalışmalar yapabilirsiniz.

## Pull Request Nedir?
Pull Request, bir branch'te yaptığın değişikliklerin projenin ana koduna eklenmesi için ekibinden onay isteme sürecidir.

### Ne İşe Yarar?
Kod İncelemesi: Kodlar ana projeye girmeden önce ekip arkadaşları tarafından incelenir ve hatalar önceden yakalanır.

**Güvenli Entegrasyon:** Test edilmemiş veya hatalı kodların ana projeyi bozmasını engeller.

**Ekip İletişimi:** Değişiklikler üzerinde tartışma ve onay süreci sağlar.

### Süreç Nasıl İşler?
Kendi branch'inde kodu yaz ve uzak depoya gönder (git push).

GitHub üzerinden bir Pull Request (PR) aç ve değişikliklerini açıkla.

Ekip arkadaşların kodu inceleyip onaylasın.

Onaylanan kodu Merge butonuna basarak ana dala dahil et.

## Merge Conflict Nedir?
Merge Conflict (Birleştirme Çakışması), iki kişinin aynı dosyanın aynı satırında farklı değişiklikler yapması ve Git'in hangisinin geçerli olduğuna karar veremediği durumdur.

### Ne İşe Yarar ve Neden Olur?
Git akıllı birleştirme yapar ama aynı satırda çakışma olursa kafası karışır.

Hangi kodun kalacağına otomatik karar veremediği için süreci durdurur ve geliştiricinin manuel müdahale etmesini ister.

### Nasıl Çözülür?
Çakışan dosya açılır ve Git'in eklediği işaretler üzerinden hangi kodun kalacağı seçilerek manuel olarak düzenlenir.

Düzeltilen dosya yeniden sahneye alınır (git add).

Commit atılarak çakışma sonlandırılır ve birleştirme tamamlanır.

## .gitignore Nedir?
.gitignore, Git'in takip etmesini istemediğin, versiyon kontrol sistemine dahil edilmemesi gereken dosyaları ve klasörleri belirttiğin özel bir metin dosyasıdır.

### Ne İşe Yarar?
Gereksiz Dosyaları Engeller: Şifreler/API anahtarları, geçici dosyalar, log kayıtları, veritabanı dosyaları veya editör ayarları gibi projenin ana kodunda yer almaması gereken dosyaların yanlışlıkla GitHub'a yüklenmesini önler.

**Depoyu Temiz Tutar:** Uzak depoda sadece projenin kaynak kodlarının bulunmasını sağlayarak kirliliği önler ve boyutu küçültür.

### Nasıl Kullanılır?
Projenin ana dizinine .gitignore adında bir dosya oluşturulur.

İçine Git'in görmezden gelmesi istenen dosya veya klasör isimleri alt alta yazılır.

## README.md Dosyası Neden Önemlidir?
README.md, bir projenin ana sayfasında yer alan ve projenin ne olduğunu, nasıl kurulacağını ve nasıl kullanılacağını anlatan projenin kılavuz dosyasıdır. İyi yazılmış bir README, projenin düzenli ve profesyonel olduğunu gösterir.

## Issue Nedir?
Issue, GitHub gibi platformlarda bir projede karşılaşılan hataları (bug), eksiklikleri, yeni özellik taleplerini veya yapılacak görevleri takip etmek için kullanılan dijital bir kayıt (ticket) sistemidir.

## Bir Yazılım Ekibinde GitHub Nasıl Kullanılır?
Bir yazılım ekibinde, aynı repository üzerinde çalışılır.

**Görev Takibi:** Yapılacak işler ve hatalar Issue olarak açılır ve ekibe paylaştırılır.

**Ayrı Çalışma:** Kimse ana koda dokunmaz; herkes kendi branch'inde çalışır.

**Kod Gönderimi:** Yazılan kodlar GitHub'a push edilir.

**İnceleme ve Onay:** Kodun ekip tarafından incelenmesi için Pull Request açılır.

**Birleştirme:** Onaylanan kod projeye merge edilir.

## Commit Mesajı Nasıl Yazılmalıdır?
Kısa tutun: Başlık 50 karakteri geçmesin.

**Emir kipi kullanın:** "Ekle" veya "düzelt" deyin.

**Açıklayıcı olun:** Ne yapıldığını net yazın.

**Odaklı olun:** Tek commit'te tek bir iş yapın.

## Proje Klasör Yapısı Neden Önemlidir?
**Düzen ve Okunabilirlik:** Dosyaların nerede olduğunu bulmayı kolaylaştırır ve karmaşayı önler.

**Sürdürülebilirlik:** Proje büyüdüğünde yeni özellikler eklemeyi ve kodları güncellemeyi kolaylaştırır.

**Ekip Çalışması:** Birden fazla kişi çalışırken herkesin aynı mantıkla hızlıca uyum sağlamasını sağlar.

**Hata Yönetimi:** Hataların hangi dosyada olduğunu bulmayı ve çözmeyi hızlandırır.
