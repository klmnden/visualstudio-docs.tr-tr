---
title: 'CA2219: Özel durum yan tümceleri içinde özel durum harekete geçirmeyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- DoNotRaiseExceptionsInExceptionClauses
- CA2219
helpviewer_keywords:
- DoNotRaiseExceptionsInExceptionClauses
- CA2219
ms.assetid: 7b9b0bee-4e8e-49a4-8c40-52142b49061f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f4159dd1b7ff7ba878e851649597d8d3a8908783
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54934016"
---
# <a name="ca2219-do-not-raise-exceptions-in-exception-clauses"></a>CA2219: Özel durum yan tümceleri içinde özel durum harekete geçirmeyin

|||
|-|-|
|TypeName|DoNotRaiseExceptionsInExceptionClauses|
|CheckId|CA2219|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan bölme|

## <a name="cause"></a>Sebep
 Bir özel durum bir `finally`, filtre ya da arıza yan tümcesi.

## <a name="rule-description"></a>Kural açıklaması
 Bir özel durum yan tümcesinde bir özel durum oluştuğunda, hata ayıklamayı büyük ölçüde artırır.

 Ne zaman bir neden bir `finally` ya da arıza yan tümcesine yeni istisna aktif istisnayı, varsa. Bu özgün hata algılama ve hata ayıklamayı sabit hale getirir.

 Filtre yan tümcesinde bir özel durum oluştuğunda, çalışma zamanı sessizce özel durumu yakalar ve filtre false olarak değerlendirilecek neden olur. False ve filtresi throw olan bir özel durum filtresi değerlendirme arasındaki farkı bildirmek için hiçbir yolu yoktur. Bu algılama ve filtre mantığındaki hataların hata ayıklamayı zorlaştırır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kuralın ihlalini düzeltmek için açıkça adresinden bir özel durum harekete geçirmeyin bir `finally`, filtre ya da arıza yan tümcesi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kural için bir uyarıyı bastırmayın. Altında oluşturulan bir özel durum yan tümcesinde bir özel durum kodu yürütürken bir avantaj sağlayan senaryo vardır.

## <a name="related-rules"></a>İlgili kuralları
 [CA1065: Beklenmedik konumlarda özel durumlar harekete geçirmeyin](../code-quality/ca1065-do-not-raise-exceptions-in-unexpected-locations.md)

## <a name="see-also"></a>Ayrıca bkz.
 [Tasarım Uyarıları](../code-quality/design-warnings.md)