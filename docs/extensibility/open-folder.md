---
title: Visual Studio açık klasör genişletilebilirlik genel bakış | Microsoft Docs
ms.date: 02/21/2018
ms.topic: conceptual
ms.assetid: 94c3f8bf-1de3-40ea-aded-7f40c4b314c7
author: vukelich
ms.author: svukel
manager: viveis
ms.workload:
- vssdk
ms.openlocfilehash: 2bb74703f639848d643f536edf620e30b1836310
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62806498"
---
# <a name="open-folder-extensibility"></a>Açık klasör genişletilebilirliği

[Klasörünü Aç](../ide/develop-code-in-visual-studio-without-projects-or-solutions.md) özelliği sağlar, kullanıcıların proje veya çözüm dosyaları gerek kalmadan Visual Studio'da codebase herhangi. Klasör Aç özellikler kullanıcılar Visual Studio'dan gibi bekler sağlar:

* Çözüm Gezgini tümleştirmesi ve arama
* Düzenleyici renklendirme
* Gezinti Git
* Dosya arama bulun

Hem .NET hem de C++ geliştirme gibi iş yükleri ile kullanıldığında, kullanıcılar ayrıca Al:

* Zengin IntelliSense
* Dile özgü işlevi

Açık klasör ile uzantı yazarları Zengin özellikleri herhangi bir dil için oluşturabilirsiniz. API'ları, bir kullanıcı herhangi bir dosyada kod tabanına oluşturma, hata ayıklama ve sembol arama desteği vardır. Geçerli Genişleticileri destekleyen proje veya çözüm olmadan kod anlamak için mevcut Visual Studio özellikleri güncelleştirebilirsiniz.

## <a name="an-api-without-project-systems"></a>Proje sistemleri olmadan bir API

Tarihsel olarak, Visual Studio, yalnızca bir çözüm ve proje sistemleri kullanarak projeleri dosyalarında anladım. Proje sistemi yüklü bir proje için işlevselliği ve kullanıcı etkileşimlerini sorumludur. Görsel temsilini proje içeriği, diğer projeleri, bağımlılıkları, proje dosyaları, içerir ve arka plandaki değişiklik proje dosyası anlar. Bu, bu hiyerarşiler ve diğer bileşenleri kullanıcı adına çalışan özellikleri aracılığıyla olur. Tüm kod tabanlarında bir proje ve çözüm yapısında de temsil edilir. Komut dosyası dilleri ve Linux için C++ dilinde yazılmış açık kaynaklı kod için iyi örneklerdir. Açık klasör ile Visual Studio, kullanıcılara kendi kaynak kod ile etkileşim için yeni bir yolunu sağlar.

Açık klasör altında apı'lerdir `Microsoft.VisualStudio.Workspace.*` ad alanı oluşturmak ve verileri veya açık klasördeki dosyaları geçici bir çözüm eylemleri Genişleticileri için kullanılabilir. Uzantılar da dahil olmak üzere çok sayıda alanlar için işlevselliği sağlamak için bu API'leri kullanabilirsiniz:

- [Çalışma alanları](workspaces.md) - çalışma alanı ve API'lerini olan açık klasör noktası genişletilebilirlik başlatılıyor.
- [Dosya bağlamları ve Eylemler](workspace-file-contexts.md) -dosya dosya bağlamları sağlanan özel kod gösterimi.
- [Dizin oluşturma](workspace-indexing.md) - toplamak ve klasör Aç çalışma alanları hakkında daha fazla veriyi kalıcı olarak.
- [Dil Hizmetleri](workspace-language-services.md) -Klasör Aç çalışma alanları halinde dil Hizmetleri tümleştirin.
- [Derleme](workspace-build.md) -derleme klasörü aç çalışma alanları için destek.

Aşağıdaki türleri kullanan özellikler, açık klasör desteklemek için yeni API'ler benimsemeye gerekir:

- `IVsHierarchy`
- `IVsProject`
- `DTE`

## <a name="feedback-comments-issues"></a>Geri bildirim, yorumlar, sorunları

Klasör Aç ve `Microsoft.VisualStudio.Workspace.*` etkin geliştirilme apı'lerdir. Beklenmeyen davranışı görürseniz, daha sonra ilgilendiğiniz sürüm için bilinen sorunlar bakın. [Geliştirici topluluğu](https://developercommunity.visualstudio.com) oylamak ve herhangi bir sorun oluşturmak için önerilen yerdir. Her görüş için ayrıntılı sorun açıklamasını öneririz. Geliştirmekte Visual Studio sürümü, (hem ne uyguladık ve ile etkileşim) kullandığınız API'leri, beklenen sonuç ve gerçek sonuç içerir. Mümkünse, döküm devenv.exe işleminin ekleyin. Geri bildirim bu vermek için GitHub'ın sorun kullanın ve ilgili belgeleri.

## <a name="next-steps"></a>Sonraki adımlar

* [Çalışma alanları](workspaces.md) -API Klasör Aç çalışma hakkında bilgi edinin.