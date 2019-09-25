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
ms.openlocfilehash: 9f9425ab1ea9eadd3bd06d950118ce83ba5c35f9
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231640"
---
# <a name="ca2208-instantiate-argument-exceptions-correctly"></a>CA2208: Bağımsız değişken özel durumlarını doğru örnekleyin

|||
|-|-|
|TypeName|InstantiateArgumentExceptionsCorrectly|
|CheckId|CA2208|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Olası nedenler aşağıdaki durumları içerir:

- Bir özel durum türünün varsayılan (parametresiz) oluşturucusuna bir çağrı yapılır veya öğesinden <xref:System.ArgumentException>türetilir.

- Yanlış dize bağımsız değişkeni, veya ' <xref:System.ArgumentException>den türetilen bir özel durum türünün parametreli oluşturucusuna geçirilir.

## <a name="rule-description"></a>Kural açıklaması

Varsayılan oluşturucuyu çağırmak yerine, daha anlamlı bir özel durum iletisi sağlanmasını sağlayan Oluşturucu aşırı yüklemelerinin birini çağırın. Özel durum iletisi, geliştiriciyi hedeflemelidir ve hata koşulunu açıkça açıklamalı ve özel durumu nasıl düzeltebileceğiniz veya kaçınmalıdır.

<xref:System.ArgumentException> Ve türetilmiş türlerinin bir ve iki dize Oluşturucusu imzaları, konum `message` ve `paramName` parametrelere göre tutarlı değildir. Bu oluşturucuların doğru dize bağımsız değişkenleriyle çağrıldığından emin olun. İmzalar aşağıdaki gibidir:

- <xref:System.ArgumentException>(dize `message`)
- <xref:System.ArgumentException>(dize `message`, dize `paramName`)
- <xref:System.ArgumentNullException>(dize `paramName`)
- <xref:System.ArgumentNullException>(dize `paramName`, dize `message`)
- <xref:System.ArgumentOutOfRangeException>(dize `paramName`)
- <xref:System.ArgumentOutOfRangeException>(dize `paramName`, dize `message`)
- <xref:System.DuplicateWaitObjectException>(dize `parameterName`)
- <xref:System.DuplicateWaitObjectException>(dize `parameterName`, dize `message`)

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için ileti, parametre adı veya her ikisini de alan bir Oluşturucu çağırın ve bağımsız değişkenlerin <xref:System.ArgumentException> Çağrılmakta olan tür için uygun olduğundan emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Yalnızca parametreli bir oluşturucunun doğru dize bağımsız değişkenleriyle çağrılması durumunda, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek

Aşağıdaki kod, bir örneğini <xref:System.ArgumentNullException>yanlış örnekleyen bir oluşturucuyu gösterir.

[!code-cpp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#1](../code-quality/codesnippet/CPP/ca2208-instantiate-argument-exceptions-correctly_1.cpp)]
[!code-csharp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#1](../code-quality/codesnippet/CSharp/ca2208-instantiate-argument-exceptions-correctly_1.cs?range=3-6)]
[!code-vb[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#1](../code-quality/codesnippet/VisualBasic/ca2208-instantiate-argument-exceptions-correctly_1.vb)]

Aşağıdaki kod, Oluşturucu bağımsız değişkenlerini değiştirerek önceki ihlalin düzeltir.

[!code-cpp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#2](../code-quality/codesnippet/CPP/ca2208-instantiate-argument-exceptions-correctly_2.cpp)]
[!code-csharp[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#2](../code-quality/codesnippet/CSharp/ca2208-instantiate-argument-exceptions-correctly_2.cs?range=3-6)]
[!code-vb[FxCop.Usage.InstantiateArgumentExceptionsCorrectly#2](../code-quality/codesnippet/VisualBasic/ca2208-instantiate-argument-exceptions-correctly_2.vb)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1507: Dize yerine NameOf kullanın](ca1507.md)