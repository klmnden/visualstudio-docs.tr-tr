---
title: 'DA0013: Yüksek oranda String.Split veya String.Substring kullanımı | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.13
- vs.performance.rules.DAAvoidStringSubstr
- vs.performance.DA0013
- vs.performance.rules.DA0013
helpviewer_keywords:
- vs.performance.13
- vs.performance.rules.DA0013
ms.assetid: f501f423-bef9-4e08-bf96-c9ac9957e5a2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 83ddc7462b703ef28a52b531aa379b46198516df
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56608209"
---
# <a name="da0013-high-usage-of-stringsplit-or-stringsubstring"></a>DA0013: Yüksek oranda String.Split veya String.Substring kullanımı

|||
|-|-|
|Kural Kimliği|DA0013|
|Kategori|.NET framework Kullanım Kılavuzu|
|Profil oluşturma yöntemleri|Örnekleme|
|İleti|String.Split ve String.Substring işlevlerin kullanımını azaltmayı deneyin.|
|Kural türü|Uyarı|

## <a name="cause"></a>Sebep
 System.String.Split veya System.String.Substring yöntemlere yapılan çağrılar, profil oluşturma verilerinin önemli bir parçasıdır. Bir dizedeki bir alt dizenin bulunup bulunmadığını test ediyorsanız System.String.IndexOf veya System.String.IndexOfAny kullanmayı düşünün.

## <a name="rule-description"></a>Kural açıklaması
 Split yöntemini bir dize nesnesi üzerinde çalışır ve alt dizeler özgün tutan yeni bir dizi dize döndürür. İşlevi, döndürülen dizi nesnesi için bellek ayırır ve bulduğu her dizi öğesi için yeni bir dize nesnesi ayırır. Benzer şekilde, Substr yöntemi, bir dize nesnesi üzerinde çalışır ve istenen alt dize için eşdeğer bir gruba yeni bir dize döndürür.

 Bellek ayırmalarını yönetmek, uygulamanızda önemliyse, alternatifler String.Split ve String.Substr yöntemlerine göz önünde bulundurun. Örneğin, dize sınıfının yeni bir örneğini oluşturmadan bir karakter dizesi içinde belirli bir alt dizeyi bulmak için IndexOf veya IndexOfAny yöntemi kullanabilirsiniz.

## <a name="how-to-investigate-a-warning"></a>Bir uyarı araştırma
 İletide çift **hata listesi** gitmek için pencere [işlev Ayrıntıları görünümü](../profiling/function-details-view.md) örnekleme, profil verileri. En sık rastlanan System.String.Split veya System.String.Substr yöntemleri kullanabilmesine programın bölümlerini bulmak için arama işlevleri inceleyin. Mümkünse, dize sınıfının yeni bir örneğini oluşturmadan bir karakter dizesi içinde belirli bir alt dizeyi bulmak için IndexOf veya IndexOfAny yöntemi kullanın.