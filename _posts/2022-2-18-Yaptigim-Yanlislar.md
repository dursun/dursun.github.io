---
layout: post
title: Yaptığım Yanlışlar
---

Bir yazılımcı olarak yaptığım yanlışlardan birine değineceğim: Bir konuyu anlamak için yeterince uğraşmadan ona bok atmak.

Özellikle bazı araçlar ve programlama dilleri, insanı uyuz edecek derecede antin kuntin oluyorlar. Bu yazıyı yazmama da sebep olan Autotools, buna bir örnektir.

İhtiyacımız olan altı üstü bir paket yöneticisi ama elimizde birbirinden çirkin sözdizimine (syntax) sahip dosyalar ve birden çok program mevcut. Aslında Autotools yazılımcıdan ziyade son kullanıcının yazılımı kurmasını kolaylaştırmak için geliştirilmiş bir araç seti fakat kardeşim insan biraz da yazılımcıyı düşünür 😃 Büyük konuşmak istemiyorum, sadece tahmin yapıyorum; herhalde eski zihniyetin ürünü olduğu için tasarım kararları da ona göre alınmıştır. Bi npm bi cargo yanında Autotools nasıl kalıyor, kararı size bırakıyorum. Tabii şimdi C için de janti paket yöneticileri çıkıyor fakat henüz istenen seviyede olduğunu düşünmüyorum.

Neyse, arada sıkıldıkça bazı eksik olduğumu hissettiğim alanlarda kitap okurum. Bu sayede hem bilgilerimi tazeliyorum hem de bilmediklerimi öğreniyorum. Bugün de 7 çocuklu John Calcote'nin yazdığı **Autotools - A Practitioner's Guide to ...** kitabını okuyordum. Orada şöyle bir paragraf gördüm, hoşuma gitti. Yazarın izni olmadan paylaşıyorum, kusura bakmasın. Yani bunun için de izin almamız gerekmiyordur herhalde:

`... You need to take the time to understand the open source software distribution, build, test, and installation philosophies embodied by—in many cases even enforced by—these tools, or you’ll find yourself fighting against the system.`

Yani diyor ki; kardeşim eğer sen sistemi anlamak için çaba harcamazsan bu sefer de sisteme bok atmak için çaba harcayacaksın. Yapma böyle şeyler kardeeeş diyor. Bence de doğru diyor. İtiraf etmeliyim ki bunu benim de yapmışlığım var. Allah hepimizi böyle yanlışlara düşmekten muhafaza eylesin.