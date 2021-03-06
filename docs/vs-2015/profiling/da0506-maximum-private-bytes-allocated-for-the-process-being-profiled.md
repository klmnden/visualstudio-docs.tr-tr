---
title: 'DA0506: Maksimum özel bayt profil oluşturulan işlem için ayrılan | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.rules.DA0506
- vs.performance.DA0506
- vs.performance.506
ms.assetid: e9c43554-9a85-4d98-9fa4-3b19986e7b62
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 97d1cacccc2fdd6abbd13aace1de71b28975779e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68158050"
---
# <a name="da0506-maximum-private-bytes-allocated-for-the-process-being-profiled"></a>DA0506: Profili oluşturulan İşlem için ayırılmış En Yüksek Sayıda Özel Bayt
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA0506 |  
| Kategori | Kaynak İzleme |  
| Profil oluşturma yöntemi | Tüm |  
| İleti | Bu bilgiler yalnızca bilgi toplanmıştır. İşlem özel baytlar sayacı, profil bir işlem tarafından sanal belleği ölçer. Bildirilen değer olan en yüksek tüm ölçüm aralıklarında gözlemlenen. |  
| Kural türü | Bilgi |  
  
 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Bu ileti, en fazla bayt (özel baytlar) işlem ayrılmış bir sanal bellek miktarını bildirir. Özel baytlar yalnızca işlem içinde çalışan iş parçacığı tarafından erişilebilir bir işlem tarafından ayrılan sanal bellek konumları temsil eder.  
  
 Bir 32-bit makine üzerinde çalışan 32 bitlik işlemler için işlem adres alanı özel bölümünü sayısı üst sınırı 2 GB'dir. Kullanarak [3 GB](http://go.microsoft.com/fwlink/?LinkId=177831) Boot.ini anahtarı 32 bitlik işlemler 3 GB'a kadar sanal belleğin elde. Bir 64 bit makine üzerinde çalışan bir 32-bit işlem en fazla 4 GB özel sanal bellek elde edebilirsiniz.  
  
 Bir 64 bit makine üzerinde çalışan bir 64-bit işlem, özel sanal bellek, 8 TB'a kadar elde edebilirsiniz.  
  
 Bildirilen değeri, profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında en yüksek değer.  
  
 İşlem adres alanları hakkında daha fazla bilgi için bkz. [sanal adres alanı](http://go.microsoft.com/fwlink/?LinkId=177832) Windows bellek yönetimi belgelerinde.  
  
## <a name="how-to-use-rule-data"></a>Kural verileri kullanma  
 Bildirilen değeri farklı sürümlerini performansını veya programın yapıları karşılaştırmak veya farklı bir profil oluşturma senaryoları altında uygulama performansını anlamak için kullanır.  
  
 Ne kadar büyük bir işlemin adres alanı büyüyebilir, mimari sınırına yaklaştı en fazla işleme özel bayt sayısı değerini bellek özel durumları out neden olabilir. Daha fazla bilgi için [bellek sorunlarını araştırma](http://go.microsoft.com/fwlink/?LinkID=177833) MSDN magazine'de.
