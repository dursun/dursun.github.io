---
layout: post
title: Hızlı Yazılım Geliştirme
---

Yazılım geliştirme sürecinde kodu yazmaktan ziyade yazacağınız kodu formülize etme daha çok vakit almaktadır. En azından benim için bu böyledir. Her ne kadar yeni nesil araçlar ile bazı sorunları düşünmekten kurtuluyor olsanız bile çoğu zaman geliştirme ortamınız o kadar da steril olmayabiliyor. 

Yazılım geliştirme sürecinin bu kadar uzun olmasına kafayı takmış durumdayım zira artık, aynı buraya yazı yazdığım gibi, oturup çatır çatır kod yazmak istiyorum. Her ne kadar tecrübe ve süreklilik ile kod yazma süreci hızlansa da, hala daha istediğim hıza erişebilmiş değilim. Bugünlerde en çok kafa yorduğum konuların başında bu geliyor ve birtakım çalışmalar yapıyorum. Bu çalışmaların sonucunu sosyal medya üzerinden paylaşmayı düşünüyorum; hesaplarımızı takipte kalın.

Detaycılık her ne kadar yazılım işiyle uğraşan kişide bulunması gereken bir haslet olsa da yazılım geliştirme konusunda bu pek faydalı değildir. Şu ana kadar gözlemlediğim kadarıyla, hızlı yazılım geliştiren insanlar genellikle hep aynı dili, kütüphaneleri ve araçları kullanan ve mümkün mertebe bunların dışına çıkmayanlardır. Eğer her konuya hakim olayım, şu detayı da düşüneyim derseniz; bir bakmışsınız tüm gününüz tek bir satır kod yazmadan geçmiş gitmiş.

Yazacağınız kodun hikayesini belirlemek ve bu hikayeyi geliştirmeyi tekrarlayan bir süreç (İng. iterative) ile devam ettirmek en verimli yöntem olarak belirlenmiştir ve bu yöntem "agile" olarak adlandırılmaktadır. Bu yöntemin karşıtı, yani öncelikle projeyi faz faz detaylandırıp, bu fazları sırası ile takip ederek yapılan geliştirmeye de "waterfall" denmektedir.

Kod yazarken kullanıcı gözünden senaryoların tanımlamasını yaparak yazılım davranışlarını belirlerseniz, geliştireceğiniz yazılımın aklınızda (ve başkalarının aklında) canlanmasını sağlayabilirsiniz. Bu yönteme de "behavior-driven development" (BDD) denilmektedir. Yazdığınız kodu test ederek ilerlemeye de "test-driven development" (TDD) denilmektedir.

Kullandığınız programlama dilinin sunduğu temel özelliklere göre yazılım geliştirme yaklaşımınızı belirlemeniz gerekmektedir. Örneğin; C dili nesne yönelimli programlama (OOP) için gereken temel yapıları sunmadığı için, C ile OOP kod geliştirmek mantığa uygun değildir ve bunu yaparsanız gereksiz yere kendinizi zorlamış olursunuz. C dili fonksiyonel programlama paradigmasına uygun olduğu için ona göre kod yazılmalıdır. Fonksiyonel programlama paradigmasına göre, program fonksiyonlardan, fonksiyonlar da deyimlerden (statement) oluşur ve böylece programın çalışma zamanındaki durumu belirlenir. Yani C ile kod geliştirirken fonksiyon bazında düşünmek zorundasınız.

Programlama dilinden dolayı takip edeceğiniz paradigma, sizin düşünce yapınızı bir yönüyle düzenlemektedir. Fonksiyonel dediğinizde farklı, nesne yönelimli dediğinizde farklı düşünür ve programı aklınızda ona göre kurgularsınız. Bu kurgunuzu formülize edip diğer insanlarla paylaşabilmek için de bir notasyon (örneğin; matematiksel deyimler veyahut UML gibi) kullanmanız gerekmektedir. Bu da işin bir başka bacağıdır.

Eğer program geliştirirken, en mükemmelini geliştireceğim diye yola çıkarsanız o yol hiçbir zaman bitmez ve hatta doğru dürüst ilerleyemezsiniz bile. Sizin bu yolda hızla ilerlemenizi sağlayacak, takılıp kalmanızı engelleyen en önemli teşvik paradır. Eğer işin içinde para ve az zaman var ise lambur lumbur kodunuzu yazar, çalıştırırsınız.

Fakat sopanın ucuna havuç bağlamadan da kişi kendi kendine bu koşturmacaya girmelidir ki daha üretken olabilsin. Bu zihin yapısına girmek benim için çok zor çünkü fazlasıyla detaya boğulmaya ve keyfi davranmaya müsaitim. Bu davranışımı değiştirip kendimi en kısa sürede en kapsamlı kodu üretecek şekilde geliştirmeye çalışıyorum. Kapsamdan kastım, detaydan ziyade en çok durumu karşılayandır.

Kısacası, henüz "nasıl yazılım geliştirme sürecimi kısaltabilirim" sorusuna yanıt bulamadım. Bulursam büyük bir keyifle paylaşacağım. Bir de ben beceremediğim konuda ahkam kesmeyi sevmem bundan dolayı hala daha kendimi kaliteli bir yazılımcı olarak görmüyorum zira istediğim hıza erişemiyorum. Ne zaman yüz binlerce satır kod yazarım o zaman ahkam keserim. Henüz yüz bin barajına erişememişimdir diye düşünüyorum. Tek bir projede yazdığım SLOC (Single Line of Code, çev. Kod satırı sayısı) değeri en fazla kod 40 bin satır civarındaydı ve otomasyon olduğundan boilerplate kod fazlacaydı. Bundan dolayı kendimi hala daha hedefimden çok uzakta görmekteyim.

Bu konuda yazı yazmak, bana eğlenceli geldi. Bu konuda daha fazla yazabilirim sanki.