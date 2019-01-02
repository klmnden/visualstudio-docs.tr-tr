---
title: 'CA1053: Statik tutucu türlerinde oluşturucular bulunmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- StaticHolderTypesShouldNotHaveConstructors
- CA1053
helpviewer_keywords:
- CA1053
- StaticHolderTypesShouldNotHaveConstructors
ms.assetid: 10302b9a-fa5e-4935-a06a-513d9600f613
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 998d941d0dd0ec06ff7d0f8a727ad3bf50718065
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53928525"
---
# <a name="ca1053-static-holder-types-should-not-have-constructors"></a>CA1053: Statik tutucu türlerinde oluşturucular bulunmamalıdır

|||
|-|-|
|TypeName|StaticHolderTypesShouldNotHaveConstructors|
|CheckId|CA1053|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya iç içe geçmiş ortak tür yalnızca statik üyeleri bildirir ve ortak veya korumalı varsayılan bir oluşturucu vardır.

## <a name="rule-description"></a>Kural açıklaması
 Statik üyeleri çağırma bir tür örneği gerektirmediğinden kurucu gereksizdir. Statik olmayan üye türüne sahip olmadığından, ayrıca, bir örneği oluşturma erişim herhangi bir türün üyeleri için sağlamaz.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için varsayılan oluşturucu kaldırın veya özel yapın.

> [!NOTE]
>  Türünü hiçbir oluşturucu tanımlamıyorsa bazı derleyiciler, ortak varsayılan oluşturucusu otomatik olarak oluşturun. Türünüz Durum buysa, ihlalin ortadan kaldırmak için özel varsayılan bir oluşturucu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Oluşturucu varlığını türü statik bir tür değil önerir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir. Kaynak kodunda varsayılan oluşturucu yok olduğuna dikkat edin. Bu kod bir derlemeye derlendiğinde, C# Derleyici bu kuralı ihlal varsayılan bir oluşturucu ekler. Bunu düzeltmek için özel bir oluşturucu bildirin.

 [!code-csharp[FxCop.Design.StaticTypes#1](../code-quality/codesnippet/CSharp/ca1053-static-holder-types-should-not-have-constructors_1.cs)]