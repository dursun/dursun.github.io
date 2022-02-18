---
layout: post
title: Araç Gereç
---

Sayın Recai hocam (roktas) derdi ki: "Bizim meslek araç kullanım bakımından terziliğin zıttıdır; terziler yıllardır hep aynı araçlar ile çalışırken bizde sürekli kullanılan araçlar değişir". Recai hocam bunu daha havalı söylemiştir ama ben aklımda kaldığı şekilde aktardım. Çift tırnak arasına almama bakmayın çünkü bazı dilbilgisi kurallarında zorlanıyorum; garanti yolu seçiyorum.

Mesela dilbilgisi dedim ya, birtakım işaretler falan var ve sen onu cümlede bir yere yerleştirmek zorundasın. Yani yine bir kurallar manzumesi ile karşı karşıyasın. Ama bazı kurallar var mesela, onlar senin içindeki hayvana seslendiği için o kuralları bilmesen de anlayabiliyorsun. Özellikle tehlike anında verilen işaretler/sesler seni ister istemez yönlendiriyor. Mesela geçtiğimiz günlerde bulunduğumuz sitede yangın çıktı, yangın alarmı bi başladı var ya ... Öyle bir bağırıyor ki anlatamam. Her yerde ışıklar yanıp sönüyor, yanıp sönüyor. İster istemez "hareket etmeliyim, evi terk etmeliyim" diyorsun. Gerçi üç-beş gün sonra bir kere daha yangın çıktı, bu sefer ota boka yangın alarmı ötebileceğini anladığım için sağa sola bakıp duman görmediğimden, yangın alarmının üzerine yastık bastırmayı tercih ettim. Yani içindeki hayvanı bi şekilde eğitebiliyorsun, bu işin bir kötü yanı da bu. Ne kadar iyi kural koyarsan koy, kişi o kurala uymak istemeyebilir. İyi kuraldan kastım, tabii ki uyulan kuraldır zira kurallar uyulmak için vardır.

Bir de bu kuralların anlaşılır olması da önemlidir ki kolay öğrenebilesiniz. Mesela kırmızı, sarı, yeşil ışık, bence gayet anlaşılır. Bir yönden içindeki hayvana da sesleniyor. Bir kere öğrensen kolay kolay unutmazsın. Bir de bazı kurallar var, günlük hayatından çıktığında tekrar unutabilirsin. Ona da örnek olarak C dilindeki işaretçi (pointer) kullanımını vereceğim: 

~~~~
#define _POSIX_C_SOURCE 200809L

#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <stdint.h>

typedef struct person_s {
    uint8_t age;
    char* name;
} person_t;

void person_initialize (person_t *person)
{
    person = (person_t *) calloc(1, sizeof(person_t));
    person->name = strndup("dursun", strlen("dursun"));
    person->age = 34;
    printf("%s: name: %s, age: %u\n", __func__, person->name, person->age);
}

int main (void)
{
    person_t *person = NULL;

    person_initialize(person);
    printf("%s: name: %s, age: %u\n", __func__, person->name, person->age);

    return 0;
}
~~~~

Size yardımcı olacak birtakım açıklamalar sunuyorum:

- person, person_t türündeki verinin olduğu adresi gösterir.
- \*person, bu adresteki veriyi temsil eder. 
- **->** operatörünün (arrow operator) manası şudur: person->age, aslında (\*person).age demektir.

Bu açıklamaların hepsi doğrudur. Şimdi bu bilgiler ışığında bakıldığında bu kodun beklenildiği gibi çalışıyor olması lazım ve her iki printf'te de *person* değişkeninin değerleri basılıyor olması gerekmektedir. Fakat öyle olmamaktadır.

Özellikle high-level dillerle uğraşmış kişiler, C'nin bu durumu karşısında epey şaşırmaktadırlar 😲 Çünkü onlara "abi işte metoda pointer geçirirsen pass-by-reference gibi davranır" diye öğretilmiştir. C öğrenenler ise (vakti zamanında kendim de dahil olmak üzere; hatta itiraf ediyorum uzun süre kullanmayınca da bir kere başıma gelmişti) yukarıda yaptığım tanımlamalar üzerinden düşündükleri için hata yapmaktadırlar.

Konuyu bilenler bana "saçmalama lan" diyebilir ama ben bunu karıştıran çok kişiye rastladığım için bence pointer kullanımı anlaşılır bir gösterim şekline sahip değildir. Ayrıca C'deki tanımlamaların okunması da milletin kafasını karıştırdığı için, özellikle fonksiyon gösterici (function pointer) tanımlarken yaz babam yaz gittiği için, millet çarpım tablosu öğrenen ilkokul çocuğu veya KPSS'ye hazırlanan memur adayı gibi "right-left" ve "clockwise/spiral" kuralları geliştirmiştir. Üstüne bir de [The Most Expensive One-byte Mistake](https://queue.acm.org/detail.cfm?id=2010365){:target="_blank"} var. Valla yazdıkça yazasım geliyor, o yüzden konuya döneyim 😃

Mesela Rust dili var ki evlere şenlik ... Sanki güzel bir şeymiş gibi, öğrenmesi çok zor diye tanıtıyorlar. Bu kadar yeni bir dilin, bu kadar anlaşılmaz olması cidden bana garip geliyor. Acaba programlama dillerini tasarlayanlar, sosyal bilimlerden uzmanlar ile birlikte çalışsa başarılı olurlar mı?

Girişte terzilerden bahsetmiştim, mesela düşünsenize makas var ama dirseğinle kullanmak zorundasın. İğne var iplik var ama ağzınla dikmek zorundasın. Terzi kardeşimiz, "severim böyle mesleğin ızdırabını" der, çeker gider. Bazı yazılımcı kardeşlerim ise adeta acıdan zevk alır gibi, büyük bir keyifle nerede antin kuntin zaman alıcı bir iş var, ona dalarlar. Sonra patron gelir, iş nerede diye sorar ve kem küm edip gerçek dünyaya dönerler ta ki C++ standardının yeni bir versiyonu çıkana kadar 😃 Ya bir de artık 3 yılda bir standart çıkarıyorlar, milleti deli ettiniz yapmayın gözünüzü seveyim 😃

Velhasılı kelam, bu yaşıma geldim, bulaşmadığım yazılım işi neredeyse kalmadı, hala daha araçlardan yüzüm gülmedi. Python 🐍 dilinin sırrı da bence burada, zira ilk kez kullanan bile okuduğu koddan anlam çıkarabiliyor ve yazarken de "o muydu, bu muydu" diye çok düşünmüyor. Tabii bunda dili kullanırken sunulan araçlar ve dilin standardının da etkisi olduğunu düşünüyorum. Bu konuya başka bir yazıda değineceğim. Şimdilik sadece şunu söyleyeyim: C dilinde herkesin kafasına göre bir coding guideline'ı var, yazım kuralları değişken olduğundan kısıtlayıcı standart bir linter (T. kaynak kod analizi yapan araç) yok, dokümantasyon için de bir standart yok, build (T. derleme) sistemi/paket yönetici zaten yok ki o da ayrı bir bela. Bari paket yöneticisi standart olaydı da birbirinden çirkin paket yöneticileriyle kimse muhatap olmayaydı 😔 Gördüğünüz gibi, C dili ile yazılım geliştirmeye başlayacak adamın bir değil birden çok sorunu var. Günümüzün hızlı dünyasında, herkesin PoC peşinde koştuğu şu dünyada, her ne kadar yazılımcı devşirirsen devşir, kafalar ve araçlar değişmedikçe vakitler tükenmeye devam edecektir. İnsanların para için ömür tükettiğini bilmediğim gençlik yıllarımda cengaver laflarım olurdu belki ama o yıllar geçti gitti be.

Başka bir yazıda tekrardan görüşmek üzere. Ben böyle olumsuz şeyler yazdım diye enseyi karartmayın ya; güzel şeyler yazmak daha zor, o yüzden böyle yapıyorum.