---
title: 'DA0505: Ortalama özel baytlar profil oluşturulan işlem için ayrılan | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0505
- vs.performance.rules.DA0505
- vs.performance.505
ms.assetid: 32c612ea-d077-44ba-8e6f-3a96333bad00
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 26a3678bb47a27152daa46488d756fe7d51abfa8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54929971"
---
# <a name="da0505-average-private-bytes-allocated-for-the-process-being-profiled"></a>DA0505: Ortalama özel baytlar profil oluşturulan işlem için ayırılmış

|||  
|-|-|  
|Kural Kimliği|DA0505|  
|Kategori|Kaynak Yönetimi|  
|Profil oluşturma yöntemi|Tümü|  
|İleti|Bu bilgiler yalnızca bilgi toplanmıştır. İşlem özel baytlar sayacı, profil bir işlem tarafından sanal belleği ölçer. Bildirilen değer tüm ölçüm aralıklarında ortalaması hesaplanır.|  
|Kural türü|Bilgiler|  

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  

## <a name="rule-description"></a>Kural açıklaması  
 Bu ileti, ortalama bayt (özel baytlar) işlem ayrılmış bir sanal bellek miktarını bildirir. Özel baytlar yalnızca işlem içinde çalışan iş parçacığı tarafından erişilebilir bir işlem tarafından ayrılan sanal bellek konumları temsil eder.  

 Bir 32-bit makine üzerinde çalışan 32 bitlik işlemler için işlem adres alanı özel bölümünü sayısı üst sınırı 2 GB'dir. Kullanarak [3 GB](http://go.microsoft.com/fwlink/?LinkId=177831) Boot.ini anahtarı 32 bitlik işlemler 3 GB'a kadar sanal belleğin elde. Bir 64 bit makine üzerinde çalışan bir 32-bit işlem en fazla 4 GB özel sanal bellek elde edebilirsiniz.  

 Bir 64 bit makine üzerinde çalışan bir 64-bit işlem, özel sanal bellek, 8 TB'a kadar elde edebilirsiniz.  

 Bildirilen değeri, profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında ortalamadır.  

 İşlem adres alanları hakkında daha fazla bilgi için bkz. [sanal adres alanı](http://go.microsoft.com/fwlink/?LinkId=177832) Windows bellek yönetimi belgelerinde.  

## <a name="how-to-use-rule-data"></a>Kural verileri kullanma  
 Bildirilen değeri farklı sürümlerini performansını veya programın yapıları karşılaştırmak veya farklı bir profil oluşturma senaryoları altında uygulama performansını anlamak için kullanır.