---
title: 'DA0001: Birleştirmeler için StringBuilder kullanın | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0001
- vs.performance.rules.DAUseStringBuilder
- vs.performance.1
- vs.performance.rules.DA0001
ms.assetid: a7cc7613-ad5f-48c8-bd2b-56372cc12dfc
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 823b6e32675f036e4e077fc0b17e5e1c2f9adbb0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53967793"
---
# <a name="da0001-use-stringbuilder-for-concatenations"></a>DA0001: Birleştirmeler için StringBuilder kullanın

|||  
|-|-|  
|Kural Kimliği|DA0001|  
|Kategori|.NET framework kullanımı|  
|Profil oluşturma yöntemleri|Örnekleme<br /><br /> İzleme|  
|İleti|Dize birleştirmeleri için StringBuilder kullanmayı düşünün|  
|İleti türü|Uyarı|  

## <a name="cause"></a>Sebep  
 System.String.Concat çağrıları, profil oluşturma verilerinin önemli bir kısmı aynıdır. Kullanmayı <xref:System.Text.StringBuilder> birden çok kesimi dizeleri oluşturmak için sınıf.  

## <a name="rule-description"></a>Kural açıklaması  
 A <xref:System.String> nesne değişmez. Bu nedenle, yeni bir dize nesnesi ve çöp toplama özgün dize değişiklik oluşturur. String.Concat açıkça çağırmak ya da dize birleştirme işleçleri kullanın Bu aynı, davranıştır + veya +=... Program performansı düşebilir, ne zaman karakter dizesine sıkı bir döngüde eklenir gibi bu yöntemleri sık denir.  

 StringBuilder sınıfını değişebilir bir nesne olan ve System.String, bu sınıfın bir örneği değiştiren StringBuilder yöntemlerin çoğu, aynı örneğe bir başvuru döndürür. Karakterleri eklemek veya bir StringBuilder örneği için metin ekleyin ve kaldırın veya karakter örneğinde yeni bir örneğini tahsis etme ve özgün örneği silme gerek kalmadan değiştirin.  

## <a name="how-to-investigate-a-warning"></a>Bir uyarı araştırma  
 İletide çift **hata listesi** gitmek için pencere [işlev Ayrıntıları görünümü](../profiling/function-details-view.md) örnekleme, profil verileri. Dize birleştirme en sık kullanılan olarak kullanabilmesine programın bölümlerini bulur. StringBuilder sınıfını sık dize birleştirme işlemleri dahil olmak üzere, karmaşık dize işlemeleri için kullanın.  

 Dizeler ile çalışma hakkında daha fazla bilgi için [dize işlemleri](http://go.microsoft.com/fwlink/?LinkId=177816) bölümünü [bölüm 5 - yönetilen kod performansını iyileştirme](http://go.microsoft.com/fwlink/?LinkId=177817) Microsoft Patterns and Practices Kitaplığı'nda.