---
title: ': Ortalama özel baytlar profil oluşturulan da0505 işlem için | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.DA0505
- vs.performance.rules.DA0505
- vs.performance.505
ms.assetid: 32c612ea-d077-44ba-8e6f-3a96333bad00
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c851015c9f811fc6a15f7b6c2ca037a6a30af113
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49187440"
---
# <a name="da0505-average-private-bytes-allocated-for-the-process-being-profiled"></a>DA0505: İşlem için izin verilen Ortalama Özel Bayt Sayısının profili oluşturuluyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA0505 |  
| Kategori | Kaynak Yönetimi |  
| Profil oluşturma yöntemi | Tüm |  
| İleti | Bu bilgiler yalnızca bilgi toplanmıştır. İşlem özel baytlar sayacı, profil bir işlem tarafından sanal belleği ölçer. Bildirilen değer aralıklarından hesaplanan tüm ölçüm aralıklarında. |  
| Kural türü | Bilgi |  
  
 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Bu ileti, ortalama bayt (özel baytlar) işlem ayrılmış bir sanal bellek miktarını bildirir. Özel baytlar yalnızca işlem içinde çalışan iş parçacığı tarafından erişilebilir bir işlem tarafından ayrılan sanal bellek konumları temsil eder.  
  
 Bir 32-bit makine üzerinde çalışan 32 bitlik işlemler için işlem adres alanı özel bölümünü sayısı üst sınırı 2 GB'dir. Kullanarak [3 GB](http://go.microsoft.com/fwlink/?LinkId=177831) Boot.ini anahtarı 32 bitlik işlemler 3 GB'a kadar sanal belleğin elde. Bir 64 bit makine üzerinde çalışan bir 32-bit işlem en fazla 4 GB özel sanal bellek elde edebilirsiniz.  
  
 Bir 64 bit makine üzerinde çalışan bir 64-bit işlem, özel sanal bellek, 8 TB'a kadar elde edebilirsiniz.  
  
 Bildirilen değeri, profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında ortalamadır.  
  
 İşlem adres alanları hakkında daha fazla bilgi için bkz. [sanal adres alanı](http://go.microsoft.com/fwlink/?LinkId=177832) Windows bellek yönetimi belgelerinde.  
  
## <a name="how-to-use-rule-data"></a>Kural verileri kullanma  
 Bildirilen değeri farklı sürümlerini performansını veya programın yapıları karşılaştırmak veya farklı bir profil oluşturma senaryoları altında uygulama performansını anlamak için kullanır.



