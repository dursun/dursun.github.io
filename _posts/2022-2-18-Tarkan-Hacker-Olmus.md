---
layout: post
title: Tarkan Hacker Olmuş
---

Tarkan'ın Geççek şarkısının başında klasik bir "hacker" sekansı var. Oradaki kod tanıdık gelince ((void*)__get_free_page(GFP_USER) ve goto out_undo_p*devamı yok*), bu ne olabilir diye Linux kernel kodunu araştırdım. kernel/groups.c'nin eski bir versiyonu olduğunu gördüm.

Sonra googlelayınca gördüm ki hackertyper diye web uygulamaları varmış, [bu kodu](https://github.com/torvalds/linux/blob/b0e77598f87107001a00b8a4ece9c95e4254ccc4/kernel/groups.c#L35){:target="_blank"} kullanıyormuş. Ben de sevinmiştim bir şeyler keşfettim diye 😐 Millet zaten reddit'te, orada burada eskiden bunun muhabbetini döndürmüş bile. Yani epey bilinen bir şeymiş 😃

Bu kadar araştırdım madem en azından bir işe yarasın, bugünlük yazımı da yazmış olayım.

---

Not: Kodun versiyonu konusunda tam emin değilim. Paylaştığım kod ile yakın zamanlarda başka versiyonlar da olabilir. Meraklısı olursa araştırsın bulsun, benden bu kadar.