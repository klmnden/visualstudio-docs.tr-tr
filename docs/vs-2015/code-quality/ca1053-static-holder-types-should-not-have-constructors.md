---
title: 'CA1053: Statik tutucu türlerinde oluşturucular olmamalıdır | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- StaticHolderTypesShouldNotHaveConstructors
- CA1053
helpviewer_keywords:
- CA1053
- StaticHolderTypesShouldNotHaveConstructors
ms.assetid: 10302b9a-fa5e-4935-a06a-513d9600f613
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 10f9f1547c550505935b19b548e1db2589133c7b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53988426"
---
# <a name="ca1053-static-holder-types-should-not-have-constructors"></a>CA1053: Statik tutucu türlerinde oluşturucular bulunmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|StaticHolderTypesShouldNotHaveConstructors|
|CheckId|CA1053|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya iç içe geçmiş ortak tür yalnızca statik üyeleri bildirir ve ortak veya korumalı varsayılan bir oluşturucu vardır.

## <a name="rule-description"></a>Kural Tanımı
 Statik üyeleri çağırma bir tür örneği gerektirmediğinden kurucu gereksizdir. Statik olmayan üye türüne sahip olmadığından, ayrıca, bir örneği oluşturma erişim herhangi bir türün üyeleri için sağlamaz.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için varsayılan oluşturucu kaldırın veya özel yapın.

> [!NOTE]
>  Türünü hiçbir oluşturucu tanımlamıyorsa bazı derleyiciler, ortak varsayılan oluşturucusu otomatik olarak oluşturun. Türünüz Durum buysa, ihlalin ortadan kaldırmak için özel varsayılan bir oluşturucu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Oluşturucu varlığını türü statik bir tür değil önerir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir. Kaynak kodunda varsayılan oluşturucu yok olduğuna dikkat edin. Bu kod bir derlemeye derlendiğinde, C# Derleyici bu kuralı ihlal varsayılan bir oluşturucu ekler. Bunu düzeltmek için özel bir oluşturucu bildirin.

 [!code-csharp[FxCop.Design.StaticTypes#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.StaticTypes/cs/FxCop.Design.StaticTypes.cs#1)]
