---
title: 'CA2208: Bağımsız değişken özel durumlarını doğru örnekleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2208
- InstantiateArgumentExceptionsCorrectly
helpviewer_keywords:
- InstantiateArgumentExceptionsCorrectly
- CA2208
ms.assetid: e2a48939-d9fa-478c-b2f9-3bdbce07dff7
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: d82b1884336b314e8fcede3c6041030a878b999c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62806777"
---
# <a name="ca2208-instantiate-argument-exceptions-correctly"></a>CA2208: Bağımsız değişken özel durumlarını doğru örnekleyin

|||
|-|-|
|TypeName|InstantiateArgumentExceptionsCorrectly|
|CheckId|CA2208|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Aşağıdaki durumlarda olası nedenler:

- Varsayılan (parametresiz) kurucu, veya ondan türetilmiş bir özel durum türü için bir çağrı yapılır <xref:System.ArgumentException>.

- Bir hatalı dize bağımsız değişkeni parametreli bir kurucu, veya ondan türetilmiş bir özel durum türü iletilir <xref:System.ArgumentException>.

## <a name="rule-description"></a>Kural açıklaması

Varsayılan oluşturucuyu çağırmak yerine sağlanması daha anlamlı bir özel durum iletisi veren oluşturucu aşırı yüklemeleri birini çağırın. Özel durum iletisi, geliştirici hedef ve hata durumu ve düzeltin veya özel durumdan kaçınmak nasıl NET bir şekilde açıklayın.

Bir ve iki dize oluşturucular imzaları <xref:System.ArgumentException> ve türetilmiş türlerini ilişkilendirilebilmesi için tutarlı olmayan `message` ve `paramName` parametreleri. Bu oluşturucular doğru dize bağımsız değişkenlerle çağrılır emin olun. İmzaları aşağıdaki gibidir:

 <xref:System.ArgumentException>(string `message`)

 <xref:System.ArgumentException>(string `message`, dize `paramName`)

 <xref:System.ArgumentNullException>(string `paramName`)

 <xref:System.ArgumentNullException>(string `paramName`, dize `message`)

 <xref:System.ArgumentOutOfRangeException>(string `paramName`)

 <xref:System.ArgumentOutOfRangeException>(string `paramName`, dize `message`)

 <xref:System.DuplicateWaitObjectException>(string `parameterName`)

 <xref:System.DuplicateWaitObjectException>(string `parameterName`, dize `message`)

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için bir ileti, bir parametre adı veya her ikisini de alan bir oluşturucu çağırmak ve bağımsız değişken türü için uygun olduğundan emin olun <xref:System.ArgumentException> çağrılan.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Parametreli bir kurucu doğru dize bağımsız değişkenleri ile yalnızca çağrılması halinde bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example-1"></a>Örnek 1
 Aşağıdaki örnek, yanlış ArgumentNullException türün bir örneğini başlatan bir oluşturucu gösterir.

 [!code-cpp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#1](../code-quality/codesnippet/CPP/ca2208-instantiate-argument-exceptions-correctly_1.cpp)]
 [!code-csharp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#1](../code-quality/codesnippet/CSharp/ca2208-instantiate-argument-exceptions-correctly_1.cs)]
 [!code-vb[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#1](../code-quality/codesnippet/VisualBasic/ca2208-instantiate-argument-exceptions-correctly_1.vb)]

## <a name="example-2"></a>Örnek 2
 Aşağıdaki örnek, oluşturucu bağımsız geçerek yukarıdaki ihlali düzeltir.

 [!code-cpp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#2](../code-quality/codesnippet/CPP/ca2208-instantiate-argument-exceptions-correctly_2.cpp)]
 [!code-csharp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#2](../code-quality/codesnippet/CSharp/ca2208-instantiate-argument-exceptions-correctly_2.cs)]
 [!code-vb[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#2](../code-quality/codesnippet/VisualBasic/ca2208-instantiate-argument-exceptions-correctly_2.vb)]