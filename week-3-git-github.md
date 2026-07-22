# 3. Hafta: Git, GitHub ve Proje Dosya Disiplini Araştırması

## 1. Git Nedir?
Git, yazılım projelerinin kaynak kod geçmişini, versiyonlarını ve yapılan değişiklikleri takip etmeyi sağlayan dağıtık bir sürüm kontrol sistemidir. Geliştiricilerin kodlarını güvenle saklamasına, eski sürümlere dönebilmesine ve hatalı kodları ayıklayabilmesine olanak tanır.

## 2. GitHub Nedir?
Git ile takip edilen projelerin bulut ortamında depolandığı, ekip çalışmalarına, kod paylaşımlarına, sürüm takibine ve açık kaynak projelerine ev sahipliği yapan küresel bir platformdur.

## 3. Repository Nedir?
Repository (kısaca "repo"), bir projenin tüm dosyalarının, klasörlerinin ve bu dosyalara ait geçmiş tüm versiyon değişikliklerinin saklandığı depo alanıdır. Yerel bilgisayarda (local) veya bulutta (remote) bulunabilir.

## 4. Commit Nedir?
Commit, projede yapılan kod değişikliklerinin Git veritabanına kalıcı ve açıklayıcı bir notla kaydedildiği anlık bir fotoğraftır. Her commit, projenin o anki durumunun bir kaydıdır.

## 5. Branch Nedir?
Branch (dal), ana projeyi (`main` veya `master`) bozmadan yeni bir özellik geliştirmek, hata düzeltmek veya deneysel çalışmalar yapmak için açılan bağımsız çalışma kollarıdır.

## 6. Pull Request Nedir?
Pull Request (PR), bir geliştiricinin kendi branch'inde yazdığı kodları ana projeye dahil etmek için ekip liderine veya diğer geliştiricilere sunduğu inceleme ve onay talebidir.

## 7. Merge Conflict Nedir?
Merge conflict (birleşme çakışması), aynı dosyanın aynı satırında iki farklı geliştirici zıt değişiklikler yaptığında Git'in hangisinin geçerli olduğuna karar veremeyip kullanıcı müdahalesi istemesi durumudur.

## 8. .gitignore Nedir?
.gitignore, Git'in takip etmemesini (versiyonlamamasını) istediğimiz şifreler, veritabanı bağlantı bilgileri, derlenmiş geçici dosyalar veya `node_modules` gibi ağır klasörlerin belirtildiği özel bir konfigürasyon dosyasıdır.

## 9. README.md Dosyası Neden Önemlidir?
README.md, bir repository'nin ana sayfasında yer alan; projenin ne işe yaradığını, nasıl kurulacağını, hangi teknolojilerin kullanıldığını ve nasıl çalıştırılacağını anlatan projenin ilk ımza kılavuz dosyasıdır.

## 10. Issue Nedir?
Issue, yazılım projelerindeki yapılacak görevleri, özellik taleplerini veya karşılaşılan hataları (bug) takip etmek ve ekip içinde tartışmak için kullanılan bir görev yönetim sistemidir.

## 11. Bir Yazılım Ekibinde GitHub Nasıl Kullanılır?
Bir yazılım ekibinde herkes projeyi kendi bilgisayarına klonlar. Yeni bir özellik için ayrı branch açılır. Kod yazılıp commit edildikten sonra GitHub'a gönderilir ve `Pull Request` açılarak kod incelemesinden (code review) geçirildikten sonra ana koda (`main`) dahil edilir.

## 12. Commit Mesajı Nasıl Yazılmalıdır?
Commit mesajları rastgele veya geçiştirme olmamalıdır ("123", "düzelttim" gibi). Net, açıklayıcı ve geçmişe dönük incelendiğinde ne yapıldığını anlatan formatta olmalıdır (Örn: `feat: kullanıcı kayıt formu validasyonları eklendi`).

## 13. Proje Klasör Yapısı Neden Önemlidir?
Düzenli bir klasör yapısı (örn: frontend, backend, database, docs ayrımı), kodların okunabilirliğini artırır, yeni dahil olan geliştiricilerin projeye adapte olmasını hızlandırır ve sürdürülebilirliği sağlar.

## 14. Bu Konular AIHEXA Projesinde Nerede Kullanılır?
AIHEXA yazılım ve eğitim şirketinde; geliştiriciler ve stajyerler ortak bir modül geliştirirken Git branch yapısını kullanır. Hazırlanan kodlar `pull request` süreçleriyle sisteme eklenir, `.gitignore` ile gizli veriler korunur ve README dosyaları ile projelerin dökümantasyonu profesyonel düzeyde yönetilir.
