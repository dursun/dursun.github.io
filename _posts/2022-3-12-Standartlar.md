---
layout: post
title: Standartlar
---

Yazılım işiyle ilgilenen biri olarak standartlar hayatımın merkezinde bulunuyor diyebilirim. Bir iş yapacaksam ve standardı varsa, temel kaynak olarak onu kabul ederim zira standart üzerinden ilerlemek sizi doğru yola ileteceği gibi, aynı zamanda sunduğu bakış açısıyla ufkunuzu açacaktır. Tabii eğer bu son model bir C veya C++ standardı değilse 😃 Bu yazıyı yazmaya beni iten dert, C11 ile gelen threads kütüphanesine öylesine bakarken karşılaştığım abidik gubidik durumlardır. Şimdi mamını mamını mikrofon şov yaparak sövmenin zamanıdır ama sakin kalmaya çalışacağım 😃

Öncelikle sevgili kardeşlerim, şunu söylemek isterim ki siz madem standart koyucusunuz, o halde sözünüzün geçmesi lazımdır. Sözünüzün geçmesi için de sözünüzü detaylandırmanız lazım ki aracı geliştirenler sözünüzden çıkamasın.

C11 standardını geliştiren kardeşlerim! Ya bi thread kütüphanesi desteği getirmişsiniz, tam evlere şenlik. Altı üstü şu fonksiyonu kullanarak "remaining" (T. kalan) süreyi alabileceğim bir kod yazayım dedim, bir türlü beklediğim sonucu alamadım:

    int thrd_sleep(const struct timespec *duration, struct timespec *remaining);

Benim gibi uğraşanlar da [olmuş](https://forum.pellesc.de/index.php?topic=9914.0){:target="_blank"}. Ben GCC ile denedim ama bir türlü "remaining" değerini alacağım senaryoyu gerçekleştiremedim. C standardını geliştiren komitede olan bu abimiz bile vakti zamanında C11 threads kütüphanesine [isyan etmiş](https://gustedt.wordpress.com/2012/10/14/c11-defects-c-threads-are-not-realizable-with-posix-threads/){:target="_blank"}. Ben de her böyle bir durumla karşılaştığımda standardı geliştirenlere [bu abimiz gibi isyan ediyorum](https://youtu.be/sjpSU5Ar7Z0){:target="_blank"}.

C++ zaten "benim yeni dillerden neyim eksik, bende de tüm o özellikler olsun" diye diye coşmuş gitmiş. Millet yeni standardın sunduğu özellikleri kullanacağım derken programını bug manyağı yaptı. Etraf "yaa bu uygulama neden beklediğim gibi çalışmıyor" diyenler ile doldu taştı. Özellikle oyun geliştiricilerinin makalelerinde, videolarında denk geliyorum "gözünüzün yağını yiyeyim yapmayın etmeyin eskisi gibi takılmaya devam edin" diyorlar.

Yeni standartları kullanmak isteyenlere hak veriyorum, ben de çoğu zaman merak eder, ne var ne yok diye bakarım. C11 threads örneğinde de olduğu gibi, kullanmaya da çalışırım. Fakat kullanmaya çalışırken cebelleşmeye başlarsam sinirlerim bozuluyor. C11 ile gelen "Designated initializers", "Type-generic expressions", "Anonymous structures and unions" özellikleri gayet güzel, kullanışlı olduğu durumlar mevcut. Fakat işte bu bahsettiğim thread desteği gibi olmamış işler de standarda sokulunca insanın siniri bozuluyor. O zaman "yak bütün standartları" diyesiniz geliyor.

Kısacası, bir standart çıkarıyorsanız oluşabilecek tüm durumları kapsamanız lazım. Kapsamıyorsanız da "unspecified", "undefined" veya "implementation-defined" olarak bu durumları belirtmelisiniz ki standardınızı kullanacak kişi ona göre karar versin. Altı üstü kıçı kırık bi "thrd_sleep" fonksiyonunun çalıştığı thread'e sinyal geldiğinde uygulamanın devam edip sleep'ten ne zaman çıktığımı görmek istedim, resmen maymuna döndüm. Yani kıçı kırık bir fonksiyon için okyanusun derinliklerine, yeraltı dehlizlerine falan girip çıkmayayım. İstirham ediyorum efendim, lütfen!