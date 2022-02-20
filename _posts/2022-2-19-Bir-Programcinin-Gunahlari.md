---
layout: post
title: Programcının En Büyük Günahları
---

Dünkü "Yaptığım Yanlışlar" başlıklı yazımda, bir programcının günahlarından biri olan "bir konuyu anlamak için yeterince uğraşmadan ona bok atmak" konusuna değinmiştim. Bugün de onun kardeşi bir günaha değinmek istiyorum: "Birinin bir konu hakkındaki değerlendirmesinden yola çıkarak, kolayına da geldiği için, o konuyu göz ardı etmek".

Bu konuya örnek olarak *debugger kullanımını* vermek istiyorum. Linus Torvalds biliyorsunuz haklı haksız çıkışları ile meşhur birisi. Debugger (T. hata ayıklayıcı) kullanımına, hem çevremde kullanımını çok görmediğim için hem de kendisinin lafına kandığım için, ben de karşıydım. Sadece *core dump* analiz ederken kullanırdım; yazılım geliştirme sürecinde kullanmazdım. Bug (T. hata) çıktığında bile çoğu zaman log alarak veya kodu inceleyerek hatayı bulmaya çalışırdım, ta ki debugger'ların detaylı kullanımı ile haşır neşir olana kadar. Debugger'lar çoğu zaman zaruri olarak kullanılırken, kimi zaman da geliştirme sürecini hızlandıran bir araç olarak kullanılabiliyor. Zira log/çıktı alıp incelemek daha zahmetli bir süreç ve çalışma zamanı içerisinde yazılımın durumunu her yönüyle incelemeye imkan sağlamıyor. Doğru noktaları *print* ettirene kadar, çalışma zamanında yazılım içerisinde rahatlıkla inceleme yapabilmek, gerektiğinde değişkeni veya akışı değiştirmek, frame'ler arası dolanabilmek gibi imkanlar yönünden debugger'lar, log almak ile kıyaslanamaz bile. Fakat Linus Torvalds ve kendini çok zeki sanan abilerimiz yüzünden önyargılı davranıyoruz. Ayrıca zaten o zamana kadar işimizi kendi yöntemimizle çözdüğümüz ve de debugger kullananların ota boka debugger kullandığını gördüğümüz için de o abilerimizin sözüne inancımız daha da güçleniyor. Özellikle makine dili seviyesinde inceleme yapılan dillerde, debugger kullanımı çoğu zaman yanlış pratiklerle kullanılıyor. E bir de üstüne tembellik eklenince, "ne yapacaksın yeaa debugger'ı" diyorsun hem kendine hem de millete.

Ne yazık ki bu yönde yönlendirdiğim insanlar da oldu ama büyük ihtimal beni umursamayıp yönelmemişlerdir, o yüzden üzülmüyorum 😃 Papaz efendi, günahım affoldu mu?

---

Linus Torvalds'ın ilgili çıkışı: [Availability of kdb, 6 Sep 2000](https://lkml.org/lkml/2000/9/6/65){:target="_blank"}

Zaten hatalı olduğunu zaman ispatlamış oluyor zira günümüzde kernel geliştirmede debugger kullanılmaktadır: [Using kgdb, kdb and the kernel debugger internals](https://docs.kernel.org/dev-tools/kgdb.html){:target="_blank"}