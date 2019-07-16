---
title: Betik hata ayıklamasında sınırlamalar | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- ASPX breakpoint mapping, limitations
- script debugging, limitations
- breakpoint mapping, limitations
ms.assetid: 280eead5-693c-47af-967f-dfe9d23f84db
caps.latest.revision: 25
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5ea088eadc09d45d576dd3c9cd33e5d9e2d79fc8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68160625"
---
# <a name="limitations-on-script-debugging"></a>Betik Hata Ayıklamasında Sınırlamalar
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Bu konudaki sınırlamalar istemci tarafı komut dosyası hata ayıklamayı destekler.  
  
## <a name="limitations-on-breakpoint-mapping-with-client-side-script"></a>Kesme noktası eşleme istemci tarafı komut dosyası ile ilgili sınırlamalar  
 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] istemci tarafı dosya çalışma zamanında dönüştürülür bir sunucu tarafı ASPX veya HTML dosyasında bir kesme noktası ayarlamak sağlar. [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Sunucu tarafı dosyadan kesme noktası aşağıdaki sınırlamalara tabi istemci tarafındaki dosyada karşılık gelen bir kesme noktasıyla eşler:  
  
- Kesme noktaları ayarlayın, içinde `<script>` engeller. Satır içi betik kesme noktaları veya `<% %>` blokları eşleştirilemez.  
  
- Sayfa için tarayıcı URL sayfa adı içermelidir. Örneğin: http://microsoft.com/default.apsx. Kesme noktası eşleme tanıyamıyor bir adresinden bir yeniden yönlendirme gibi http://microsoft.com varsayılan sayfasına.  
  
- Kesme noktası ayarlayın veya bu sayfa tarafından eklenen diğer dosya tarayıcı URL değil bir ASPX denetimi (ascx) dosyası içinde belirtilen sayfasında Yöneticisi. Dahil edilen sayfaları'nda ayarlanan kesme noktaları eşlenemez.  
  
- Kesme noktaları ayarlayın `<script defer=true>` blokları eşleştirilemez.  
  
- Kesme noktaları ayarlayın `<script id="">` blokları, kesme noktası eşleme yoksayar `id` özniteliği.  
  
## <a name="breakpoint-mapping-and-duplicate-lines"></a>Kesme noktası eşleme ve yinelenen satırlar  
 Sunucu tarafı ve istemci tarafı komut dosyasında karşılık gelen konum bulmak için kod her satırda bir kesme noktası eşleştirme algoritmasını inceler. Algoritma, her bir satırı benzersiz olduğunu varsayar. İki veya daha fazla satır aynı kodu içeren ve yinelenen satırlar biri üzerinde bir kesme noktası ayarlayın, kesme noktası eşleme algoritması istemci tarafı dosyasında yanlış yinelenen seçebilirsiniz. Bunu önlemek için kesme noktası burada ayarladığınız satırı için bir açıklama ekleyin. Örneğin:  
  
```  
i++ ;  
i ++; // I added a comment, so this line is now unique  
i ++;  
```
