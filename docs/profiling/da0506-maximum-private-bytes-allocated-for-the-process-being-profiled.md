---
title: 'DA0506: Maksimum özel bayt profil oluşturulan işlem için ayrılan | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DA0506
- vs.performance.DA0506
- vs.performance.506
ms.assetid: e9c43554-9a85-4d98-9fa4-3b19986e7b62
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f09066fc66570f0de700959509327476f6fc4665
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54961708"
---
# <a name="da0506-maximum-private-bytes-allocated-for-the-process-being-profiled"></a>DA0506: Maksimum özel bayt profil oluşturulan işlem için ayırılmış

|||  
|-|-|  
|Kural Kimliği|DA0506|  
|Kategori|Kaynak İzleme|  
|Profil oluşturma yöntemi|Tümü|  
|İleti|Bu bilgiler yalnızca bilgi toplanmıştır. İşlem özel baytlar sayacı, profil bir işlem tarafından sanal belleği ölçer. Bildirilen değer tüm ölçüm aralıklarında gözlemlenen en yüksek.|  
|Kural türü|Bilgiler|  

 Örnekleme, .NET bellek ve kaynak çekişmesi yöntemleri kullanılarak profili, bu kural tetiklemek için en az 10 örnekleri toplamanız gerekir.  

## <a name="rule-description"></a>Kural açıklaması  
 Bu ileti, en fazla bayt (özel baytlar) işlem ayrılmış bir sanal bellek miktarını bildirir. Özel baytlar yalnızca işlem içinde çalışan iş parçacığı tarafından erişilebilir bir işlem tarafından ayrılan sanal bellek konumları temsil eder.  

 Bir 32-bit makine üzerinde çalışan 32 bitlik işlemler için işlem adres alanı özel bölümünü sayısı üst sınırı 2 GB'dir. Kullanarak [3 GB](http://go.microsoft.com/fwlink/?LinkId=177831) Boot.ini anahtarı 32 bitlik işlemler 3 GB'a kadar sanal belleğin elde. Bir 64 bit makine üzerinde çalışan bir 32-bit işlem en fazla 4 GB özel sanal bellek elde edebilirsiniz.  

 Bir 64 bit makine üzerinde çalışan bir 64-bit işlem, özel sanal bellek, 8 TB'a kadar elde edebilirsiniz.  

 Bildirilen değeri, profil oluşturulan işlem etkin olduğu tüm ölçüm aralıklarında en yüksek değer.  

 İşlem adres alanları hakkında daha fazla bilgi için bkz. [sanal adres alanı](http://go.microsoft.com/fwlink/?LinkId=177832) Windows bellek yönetimi belgelerinde.  

## <a name="how-to-use-rule-data"></a>Kural verileri kullanma  
 Bildirilen değeri farklı sürümlerini performansını veya programın yapıları karşılaştırmak veya farklı bir profil oluşturma senaryoları altında uygulama performansını anlamak için kullanır.  

 Ne kadar büyük bir işlemin adres alanı büyüyebilir, mimari sınırına yaklaştı en fazla işleme özel bayt sayısı değerini bellek özel durumları out neden olabilir. Daha fazla bilgi için [bellek sorunlarını araştırma](http://go.microsoft.com/fwlink/?LinkID=177833) MSDN magazine'de.