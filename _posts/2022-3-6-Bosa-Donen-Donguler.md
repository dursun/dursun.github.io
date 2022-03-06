---
layout: post
title: Boşa Dönen Döngüler
---

Bilgisayarların neden olduğu elektrik israfına engel olabilmek için "Gereksizse söndürünüz", "Boşa Akıtmayın" gibi vurucu sloganlar gerekmektedir. Bu yazımızda bunun üzerine kafa yoralım.

Öncelikle tasarruf nasıl sağlanır sorusunu yanıtlamamız lazım. 

İnsanların kullanımını kısıtlayamazsınız. Adam tuvalette kullanıyor; hacet giderirken elinden telefonu alacak haliniz yok. 

İnsanların telefonlarını kendi ürettikleri elektrikle şarj etmelerini sağlayabilirsiniz fakat bu da pek efektik olmaz. Kendi ürettikleri elektrik derken Matrix filmindeki gibi enerji çiftliklerinden bahsetmiyorum tabii ki. Vakti zamanında bu amaca hizmet eden bi proje demosu yapmıştım. Kamusal alanlarda, parklarda bahçelerde, bulunan sabit bisikletleri insanlar çevirdikçe telefonları şarj oluyordu, aynı zamanda kişilerin ne kadar karbon salınımına engel olduğu da sunucu tarafına iletiliyordu. Bu tür araçlar geliştirilip insanların kullanımına sunulabilir ve insanlar teşvik edilebilir.

Ortak kullanımdaki bilgisayarlar ile birtakım hesaplamalar yapmak da iyi bir tasarruf yöntemi zira bu sayede daha önce başkasının yaptığı bir işlemi, siz de kullanabilir oluyorsunuz. Bu konuda birden çok örnek mevcuttur. Dağıtık çalışan bilgisayar sistemleri de bu tasarruf yöntemine örnektir. Gömülü sistemler ile ilgilendiğim için "build farm" (Açıklama. derleme işlemi için özelleştirilmiş bilgisayar topluluğundan oluşan, genellikle uzaktan erişime açık, sistemler) güç tasarrufu için güzel bir örnek fakat ne yazık ki günümüzde halka açık olanı pek bulunmuyor. Hayırseverlik ölmüş 😐 Sadece Raspberry Pi için Yocto ile yapılan derlemeleri ele alsak bile epey bir enerji eder. Halbuki ortak alan olsa, aynı dosyaları tekrar tekrar kimse sıfırdan derlemek zorunda kalmazdı. RPi4 için, Yocto varsayılan recipe'sini (Açıklama. (T. reçete) hangi paketlerin nasıl derleneceğini belirleyen tanımlamalar) derlemek benim bilgisayarım ile yaklaşık 5-6 saat sürüyordu diye hatırlıyorum. Boşa harcanan enerjiyi buradan hesap edebilirsiniz. Zaten derleme işlemi işlemciyi sömürdüğü için o sırada kolay kolay başka bir iş de yapamıyorsunuz; yani bilgisayarınız sadece 5-6 saat paket derlemek ile uğraşıyor.

---

**sivri zekalılar için açıklama -normal insanlar burayı geçebilir**

Burada, "kardeşim sen de o kadar paket derleme" diyen sivri zekalılar çıkacaktır. Birincisi konu ben değilim, herkes. İkincisi emin olun derleme işleminden daha fazla enerji tüketen bir sürü iş (evet, mesela "coin mining") zaten var; ben bunu sadece örnek olarak verdim. Üçüncüsü de "imajını indirsinler kardeşim" deme çünkü zaten bunlar build sistemi; yani herkes kendine göre imaj oluşturulabilsin diye geliştirilmiş yazılımlar. Yani amaç aynı imajı kullanmak değil, özelleştirmek.

**açıklama bitti**

---

Bir diğer tasarruf yöntemine ise piyasa yeni yeni uyanıyor ve akademik alanda da bu konuda çalışmalar görüyoruz. Yazılımı mümkün mertebe optimize etme ve bilgisayarın kaynaklarını en az "bottleneck" (Açıklama. darboğaz yani bir işlem sırasında, ilgili donanımın işlem kapasitesi dolduğu için diğer işlemleri de yavaşlatması) oluşacak şekilde pay etme. Bu konu özellikle HPC (High Performance Computing) alanında incelenmektedir. Kısacası, kaynaklardan en çok verim alınmaya çalışılmaktadır. Bu sayede işlemcilerin her bir döngüsünün/anının (tick) dolu dolu geçmesi amaçlanmaktadır.

Dünyamızdaki kullanılabilir enerji ihtiyacı için kan ve gözyaşı dökülüyor. Bilgisayarların harcadığı enerji belki diğer harcamaların yanında devede kulak fakat bizim de çorbada bir tuzumuz olsun derseniz işe öncelikle güzel bir slogan bularak başlayabilirsiniz. Lütfen slogan önerilerinizi yorumlarda iletiniz. Dünyamız size minnettardır.

Bir diğer önerim de insanlardaki kinetik enerjiyi elektriğe çevirip kısa sürede kullanılmak üzere depolamaktır. Hamster gibi bisiklet çevirelim, enerji üretelim. Hızlı çevirmeyene kırbaç vuralım, yemek vermeyelim. Günlük kotasını doldurmayana su bile vermeyelim. İşte insanlık böyle böyle yükseletecektir. Yaşasın insanlık, yaşasın medeniyet! Atalarımız elektrik olmadan nasıl yaşıyormuş be kardeşim! Zavallı dedelerimiz 🥺 Sahip çıkamadık dedeye 😐 Dedeee, dedeeciiim 😃