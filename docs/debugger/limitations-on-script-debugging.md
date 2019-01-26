---
title: Betik hata ayıklamasında sınırlamalar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- ASPX breakpoint mapping, limitations
- script debugging, limitations
- breakpoint mapping, limitations
ms.assetid: 280eead5-693c-47af-967f-dfe9d23f84db
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a4c74a698a07718d99036ee4fc23c5b45123b9dc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55021565"
---
# <a name="limitations-on-script-debugging"></a>Betik Hata Ayıklamasında Sınırlamalar
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Bu konudaki sınırlamalar istemci tarafı komut dosyası hata ayıklamayı destekler.  
  
## <a name="limitations-on-breakpoint-mapping-with-client-side-script"></a>Kesme noktası eşleme istemci tarafı komut dosyası ile ilgili sınırlamalar  
 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] istemci tarafı dosya çalışma zamanında dönüştürülür bir sunucu tarafı ASPX veya HTML dosyasında bir kesme noktası ayarlamak sağlar. [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Sunucu tarafı dosyadan kesme noktası aşağıdaki sınırlamalara tabi istemci tarafındaki dosyada karşılık gelen bir kesme noktasıyla eşler:  
  
-   Kesme noktaları ayarlayın, içinde `<script>` engeller. Satır içi betik kesme noktaları veya `<% %>` blokları eşleştirilemez.  
  
-   Sayfa için tarayıcı URL sayfa adı içermelidir. Örneğin: http://microsoft.com/default.apsx Kesme noktası eşleme tanıyamıyor bir adresinden bir yeniden yönlendirme gibi http://microsoft.com varsayılan sayfasına.  
  
-   Kesme noktası ayarlayın veya bu sayfa tarafından eklenen diğer dosya tarayıcı URL değil bir ASPX denetimi (ascx) dosyası içinde belirtilen sayfasında Yöneticisi. Dahil edilen sayfaları'nda ayarlanan kesme noktaları eşlenemez.  
  
-   Kesme noktaları ayarlayın `<script defer=true>` blokları eşleştirilemez.  
  
-   Kesme noktaları ayarlayın `<script id="">` blokları, kesme noktası eşleme yoksayar `id` özniteliği.  
  
## <a name="breakpoint-mapping-and-duplicate-lines"></a>Kesme noktası eşleme ve yinelenen satırlar  
 Sunucu tarafı ve istemci tarafı komut dosyasında karşılık gelen konum bulmak için kod her satırda bir kesme noktası eşleştirme algoritmasını inceler. Algoritma, her bir satırı benzersiz olduğunu varsayar. İki veya daha fazla satır aynı kodu içeren ve yinelenen satırlar biri üzerinde bir kesme noktası ayarlayın, kesme noktası eşleme algoritması istemci tarafı dosyasında yanlış yinelenen seçebilirsiniz. Bunu önlemek için kesme noktası burada ayarladığınız satırı için bir açıklama ekleyin. Örneğin:  
  
```csharp
i++ ;  
i ++; // I added a comment, so this line is now unique  
i ++;  
```
