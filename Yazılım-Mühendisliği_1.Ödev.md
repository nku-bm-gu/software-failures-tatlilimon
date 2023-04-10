# Apple Maps Yazılımının 2012'deki Başarısızlığının Kapsamlı Analizi

<ins>**Proje Konusu**</ins>: Apple Haritalar - 2012'deki lansmanı üzerine Apple Haritalar uygulaması, gezinme hatalarına ve kullanıcı hayal kırıklığına neden olan yanlış ve eksik veriler içeriyordu.

<ins>**Ders Adı**</ins>: Yazılım Mühendisliği

<ins>**Akademisyen**</ins>: Rabia Korkmaz

### <ins>Proje Ekibi:</ins>

Gökberk Tatar - 2180656021

Gül Berfin Yücel - 2190656061

Metin Seferli - 2200656609

### <ins>İçindekiler</ins>:

- Giriş
- Yazılım Başarısızlığı: Genel Bir Bakış
- Geliştirme Süreci ve Başarısızlık Nedenleri
- Alternatif Yönetim Yaklaşımları
- Sonuç
- Kaynakça

# Özet

Bu rapor, Apple Maps'in 2012 yılında piyasaya sürülmesinin ardından yaşanan yazılım başarısızlığını, geliştirme sürecine, başarısızlığın ardındaki nedenlere ve yazılım mühendisliği uygulamalarında daha iyi sonuçlara yol açabilecek olası iyileştirmelere odaklanarak incelemektedir. Raporda ayrıca projenin yönetilmesine yönelik potansiyel alternatif yaklaşımlar da tartışılmaktadır.

<img src="/_resources/5dd6b3ebfd9db251de742917.jpg" alt="5dd6b3ebfd9db251de742917.jpg" width="498" height="374" class="jop-noMdConv">

# Giriş

2012'de piyasaya sürülen Apple Maps, iOS cihazlarda varsayılan harita uygulaması olarak Google Maps'in yerini almayı amaçlıyordu. Ancak uygulama yanlış ve eksik veriler içerdiğinden navigasyon hatalarına ve kullanıcı hayal kırıklığına yol açtı. Bu rapor yazılımın başarısızlığını, geliştirme sürecini ve başarısızlığın nedenlerini analiz etmeyi amaçlamaktadır. Ayrıca, yazılım mühendisliği uygulamaları ve yönetim stratejilerinde başarısızlığı hafifletebilecek olası iyileştirmelerine de  değineceğiz.

# Yazılım Başarısızlığı: Genel Bir Bakış

Yazılım arızası, bir yazılım sistemi veya uygulaması beklendiği veya amaçlandığı gibi çalışmadığında ortaya çıkar ve tatmin edici olmayan kullanıcı deneyimlerine, mali kayıplara ve hatta güvenlik tehlikelerine yol açar. Apple Maps arızasının geliştirme süreci, veri toplama, işleme ve görselleştirme dahil olmak üzere çeşitli teknik süreçleri içermektedir. Yazılım uygulaması kullanıcılara navigasyon, haritalama ve konum tabanlı arama gibi hizmetler sunmak üzere tasarlanmıştır. Ancak yazılımın doğru ve eksiksiz veri sağlayamaması, navigasyon hatalarına ve kullanıcı hayal kırıklığına yol açmıştır.

<img src="/_resources/8ab0aee5b76498e9da9d222cf94b2330.png" alt="8ab0aee5b76498e9da9d222cf94b2330.png" width="371" height="277" class="jop-noMdConv">

# Geliştirme Süreci ve Başarısızlık Nedenleri

Apple sözcüsü Trudy Muller 2012 IOS 6 lansmanında şu konuşmayı yaptı:

> Dünyanın dört bir yanındaki müşterilerimiz, ilk harita hizmetimiz olan Apple Maps de dahil olmak üzere 200'den fazla yeni özelliğe sahip iOS 6'ya geçiş yapıyor. Flyover ve Siri entegrasyonu ve ücretsiz adım adım navigasyon gibi yenilikçi özelliklere sahip bu hizmeti sunmaktan heyecan duyuyoruz. Bu yeni harita hizmetini, bunun büyük bir girişim olduğunu ve daha yeni başladığımızı bilerek başlattık. Sürekli olarak geliştiriyoruz ve Haritalar bulut tabanlı bir çözüm olduğu için ne kadar çok kişi kullanırsa o kadar iyi olacak. Ayrıca App Store'daki bazı harika transit uygulamalarını iOS Haritalar'a entegre etmek için geliştiricilerle birlikte çalışıyoruz. Tüm müşteri geri bildirimlerini değerlendirmeye alıyoruz ve müşteri deneyimini daha da iyi hale getirmek için çok çalışıyoruz.

Lakin Apple Maps ile alakalı dediklerinin hiçbiri gerçek çıkmadı. Kullanıcılar her geçen gün şirkete şikayetlerini bıraktılar. Hatta şikayetlerin boyutu o kadar büyüktü ki kullanıcılar artık durumu dalga geçerek izah etmeye başladılar.

<img src="/_resources/45388ec2bf76acb7f25df1f918d5cfdc.png" alt="45388ec2bf76acb7f25df1f918d5cfdc.png" width="409" height="491" class="jop-noMdConv"> <img src="/_resources/39236e01003ca6590b8c445b73c0aff3.png" alt="39236e01003ca6590b8c445b73c0aff3.png" width="455" height="143" class="jop-noMdConv">

Geliştirme sürecindeki belirli başarısızlıkları 4 ana sebepte toparlayabiliriz. Bunlar:

### <ins>**a)**</ins> <ins>**Yetersiz Veri Toplama**</ins>:

Apple'ın TomTom ve OpenStreetMap gibi birden fazla veri kaynağına dayanması, haritalama verilerinde tutarsızlıklara ve yanlışlıklara yol açtı. Apple Haritalar için veri toplama süreci, üçüncü taraf veri sağlayıcıları, uydu görüntüleri ve kitle kaynaklı veriler dahil olmak üzere çeşitli veri kaynaklarını içeriyordu. Ancak veri toplama süreci yeterince kapsamlı değildi ve bu da hatalı ve eksik verilere yol açıyordu. Üçüncü taraf veri sağlayıcılarının ve kitle kaynaklı verilerin kullanılması, verilerin doğruluğu ve eksiksizliği açısından önemli riskler oluşturmuştur. Ayrıca, kullanılan veri işleme ve görselleştirme teknikleri yetersizdi ve bu da verilerin yanlış temsil edilmesine yol açtı.

<img src="/_resources/7849c03cc32096ea496b054503f5a22a.png" alt="7849c03cc32096ea496b054503f5a22a.png" width="642" height="228" class="jop-noMdConv"> <img src="/_resources/9798a1e344078ea05c61a424f15703a3.png" alt="9798a1e344078ea05c61a424f15703a3.png" width="642" height="211" class="jop-noMdConv"><img src="/_resources/1034c1c5f7e75c93ab44bd497cb953d6.png" alt="1034c1c5f7e75c93ab44bd497cb953d6.png" width="642" height="229" class="jop-noMdConv">

### <ins>**b)**</ins> <ins>**Yetersiz Kalite Güvencesi**</ins>:

Apple'ın iOS 6 haritalarının kalite güvencesi sürecinde yeterince test edilmemesi ve kullanıcılardan geri bildirim alınmamasıydı. Apple, uygulamanın piyasaya sürülmesi için acele etti ve yeterli kalite kontrolü gerektiği kadar yapılmadan kullanıma sunuldu.

### <ins>**c)**</ins> <ins>**Gerçekçi Olmayan Teslim Tarihleri**</ins>:

Apple'ın iOS cihazlarında Google Maps'i Apple Maps ile değiştirme kararı, uygulamanın hızlı bir şekilde piyasaya sürülmesi için baskı yarattı ve potansiyel olarak geliştirme ve test süreçlerini tehlikeye attı. Bu tür büyük projelerde gerekli hesaplamaların yapılıp projenin aşamalarının ne zaman geliştirilip test edileceği ile alakalı detaylı bir rapor hazırlanması gereklidir.

### **<ins>d)</ins>** <ins>**Kullanıcı Geri Bildirimi Eksikliği**</ins>:

Apple, geliştirme sürecinde kullanıcıları veya harici test uzmanlarını sürece yeterince dahil etmedi ve lansmandan önce sorunları belirleme ve ele alma fırsatını sınırladı.Apple Maps'in lansmanından hemen sonra, kullanıcılar bazı yerlerin yanlış adlarının veya adreslerinin göründüğünü fark ettiler. Ayrıca, bazı yerlerin yanlış konumlandırıldığı veya hiç listelenmediği rapor edildi. Bu, Apple'ın işletmeler ve lokasyonlar için veri doğruluğunu kontrol etme konusunda yeterli bir çalışma yapmadığını göstermektedir.

<img src="/_resources/ea5e03810c1ee175a00d1fc91f813d8f.png" alt="ea5e03810c1ee175a00d1fc91f813d8f.png" width="359" height="247" class="jop-noMdConv"> <img src="/_resources/02169104a983fa6e51ce53ae36b14c2d.png" alt="02169104a983fa6e51ce53ae36b14c2d.png" width="440" height="247" class="jop-noMdConv"><img src="/_resources/e207793b31ae9d56263bb8c5dd6dba4b.png" alt="e207793b31ae9d56263bb8c5dd6dba4b.png" width="341" height="245" class="jop-noMdConv">

# Alternatif Yönetim Yaklaşımları

Apple Maps'in başarısızlığıyla ilgili olarak gereksinim mühendisliği, yazılım testi ve kullanıcı arayüzü tasarımı dahil olmak üzere çeşitli yazılım mühendisliği süreçleri tanımlanabilir. Gereksinim mühendisliği, kullanıcı ihtiyaçlarının ve gereksinimlerinin ortaya çıkarılmasını ve belirlenmesini içermektedir. Ancak bu süreç yetersizdi ve yazılımın kullanıcıların ihtiyaçlarını karşılamasını sağlamak için kullanıcıların aktif katılımını içermiyordu. Yazılım testi, yazılımdaki hataların ve kusurların tespit edilmesini ve giderilmesini içermektedir. Ancak test süreci yetersizdi, çok çeşitli senaryoları ve uç durumları kapsamıyordu ve gerçek dünya senaryoları ve kullanıcı testleri yoktu. Kullanıcı arayüzü tasarımı, kullanıcı dostu ve özelleştirilebilir bir arayüzün tasarlanmasını ve uygulanmasını içermektedir. Ancak tasarım yetersizdi, farklı kullanıcıların ihtiyaçlarını karşılayamıyordu.

Aynı yazılım projesini yönetiyor olsaydık, aşağıdaki alternatif yaklaşımlar uygulanırdı:

1.  Gereksinim mühendisliği süreci daha kapsamlı olmalı ve yazılımın kullanıcıların ihtiyaçlarını karşıladığından emin olmak için kullanıcıların aktif katılımını içermelidir.
2.  Verilerin doğruluğunu ve eksiksizliğini sağlamak için veri toplama süreci kurum içinde veya güvenilir ortaklarla yapılmalıdır.
3.  yazılım test süreci, gerçek dünya senaryolarını ve kullanıcı testlerini içeren daha geniş bir senaryo ve uç durum yelpazesini kapsamalıdır.Ürün lansmanından önce hataları tespit etmek ve düzeltmek için otomatik test, manuel test ve veri doğrulama dahil olmak üzere sağlam bir kalite güvence sürecinin uygulanması.
4.  Kullanıcı arayüzü tasarımı daha kullanıcı dostu ve özelleştirilebilir olmalı, farklı kullanıcıların ihtiyaçlarını karşılamalı ve Siri gibi diğer Apple ürünleriyle entegre edilmelidir.
5.  Haritalama verilerinde tutarlılığı ve doğruluğu korumak için birden fazla kaynaktan kapsamlı veri doğrulaması ve entegrasyonunun sağlanması.
6.  Uygulamanın geliştirilmesi ve piyasaya sürülmesi için gerçekçi bir zaman çizelgesinin benimsenmesi, olası sorunların ele alınması ve yüksek kaliteli bir ürün elde edilmesi için yeterli zamanın tanınması.
7.  Aşamalı geliştirmeye olanak tanıyacak çevik yazılım geliştirme metodolojileri uygulanması.
8.  Kullanıcıdan belirli aralıklarda bulunduğu konumu doğrulaması için bildirim gönderilmesinin uygulanması. Bu uygulama sayesinde kendi veritabanımızı, gerçek dünya ile doğrulamış oluruz.

# Sonuç

Sonuç olarak, Apple Maps'in başarısızlığı, yetersiz veri toplama, yetersiz test ve zayıf kullanıcı arayüzü tasarımı gibi teknik faktörlerin bir araya gelmesinden kaynaklanmıştır. Gereksinim mühendisliği, yazılım testi ve kullanıcı arayüzü tasarımı dahil olmak üzere başarısızlıkla ilgili çeşitli yazılım mühendisliği süreçleri tanımlanabilir. Gelecekte bu tür başarısızlıkları önlemek için, yazılım geliştirme süreçleri kullanıcıların aktif katılımını da içerecek şekilde daha kapsamlı olmalı ve testler daha geniş bir senaryo ve uç durum yelpazesini kapsamalıdır. Daha sağlam veri toplama, işleme ve görselleştirme tekniklerinin uygulanması da verilerin doğruluğunu ve eksiksizliğini artırmaya yardımcı olabilir. Ayrıca, güvenilir veri sağlayıcıların ve veri doğrulama içeren kitle kaynak tekniklerinin kullanılması veri kalitesini artırabilir.

Eylül 2012'de çıkan Apple Maps fiyaskosu, New York borsasına da yansıdı. Şirketin hisse değeri 6 ayda %34lük yaklaşık 30 milyar dolarlık bir düşüş yaşadı. Bu kaybı tamamen haritalardan kaynaklanmıyordu lakin bu tür yazılım başarısızlıkları mutlaka şirketin belirli miktarda maddi kaybı ile sonuçlanır.

IOS 6'nın lansmanının 1 yıl ardından IOS 7 tanıtıldı ve yeni Apple Maps sürümünü çıkardılar. Haritalar uygulamasındaki en önemli gelişme Eylül 2013'te iOS 7 işletim sisteminin piyasaya sürülmesiyle geldi. iOS 7, kullanıcıların önceki sürümde şikayet ettiği birçok sorunu ele alan tamamen yeniden tasarlanmış bir Haritalar uygulaması içeriyordu. Yeni Haritalar uygulaması daha doğru ve güncel veriler, geliştirilmiş arama işlevi ve daha kullanıcı dostu bir arayüz içeriyordu. Ayrıca yeni Haritalar uygulaması, önceki sürümde bulunmayan adım adım yol tarifi ve gerçek zamanlı trafik bilgisi gibi özellikleri de içeriyordu. iOS 7 Haritalar uygulamasındaki en önemli gelişmelerden biri vektör tabanlı haritaların uygulanmasıydı. Bu teknoloji, uygulamanın haritaları raster tabanlı haritalar kullanan önceki sürüme göre çok daha hızlı yüklemesini ve oluşturmasını sağladı. Ayrıca, vektör tabanlı haritalar uygulamanın daha sorunsuz bir şekilde yakınlaşıp uzaklaşmasını sağlayarak kullanıcılara daha kusursuz bir deneyim sundu.

<img src="/_resources/429f05ecb2447a81ad9b71a0cbb20048.png" alt="429f05ecb2447a81ad9b71a0cbb20048.png" width="452" height="302" class="jop-noMdConv"> <img src="/_resources/bd5d0d88642f2951c246b398b8b80165.png" alt="bd5d0d88642f2951c246b398b8b80165.png" width="403" height="302" class="jop-noMdConv">

Genellemek gerekirse, yazılım başarısızlığı yazılım geliştirmede önemli bir risktir ve kullanıcılar ve paydaşlar için ciddi sonuçlar doğurabilir. Apple Maps vakası, veri toplama, işleme, test etme ve kullanıcı arayüzü tasarımı dahil olmak üzere kapsamlı geliştirme süreçlerinin önemini vurgulamaktadır. Daha sağlam yazılım mühendisliği süreçleri uygulanarak bu tür başarısızlıklar önlenebilir ve kullanıcılara ihtiyaçlarını karşılayan yüksek kaliteli yazılım uygulamaları sunulabilir.

# Kaynakça

http://www.innovation-portal.info/wp-content/uploads/Apple-vs-Android-Case.pdf

https://static1.squarespace.com/static/57c8faea8419c2bf60a96fc3/t/59a1e771e3df28ce227053bc/1503782771124/MLM_ADV_1209f.pdf

https://discussions.apple.com

https://archive.nytimes.com/bits.blogs.nytimes.com/2012/11/27/apple-fires-maps-manager

https://www.theguardian.com/technology/blog/2012/oct/01/apple-30-billion-maps-mistake

https://www.iculture.nl/nieuws/ios-6-uitgelicht-apple-maps-kaartendienst-met-grote-nederlandse-invloed/

https://www.cnet.com/tech/tech-industry/ios-6-map-mess-was-no-big-surprise-to-apple

https://www.theverge.com/2012/9/20/3363914/wrong-turn-apple-ios-6-maps-phone-5-buggy-complaints

https://en.wikipedia.org/wiki/Apple_Maps

https://edition.cnn.com/2012/09/20/tech/mobile/apple-maps-complaints/index.html

https://www.techradar.com/news/software/applications/ios-6-maps-what-went-wrong-1118121
