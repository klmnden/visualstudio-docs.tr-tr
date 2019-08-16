---
title: 'CA2214: Geçersiz kılınabilir metotları oluşturucular içinde çağırmayın'
ms.date: 05/29/2016
ms.topic: reference
f1_keywords:
- DoNotCallOverridableMethodsInConstructors
- CA2214
helpviewer_keywords:
- CA2214
- DoNotCallOverridableMethodsInConstructors
ms.assetid: 335b57ca-a6e8-41b4-a20e-57ee172c97c3
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: a59346cb70269d4d2b405279fc9ea5573a879b1e
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69547013"
---
# <a name="ca2214-do-not-call-overridable-methods-in-constructors"></a>CA2214: Geçersiz kılınabilir metotları oluşturucular içinde çağırmayın

|||
|-|-|
|TypeName|DoNotCallOverridableMethodsInConstructors|
|CheckId|CA2214|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Korumasız bir türün Oluşturucusu sınıfında tanımlanmış sanal bir yöntemi çağırır.

## <a name="rule-description"></a>Kural açıklaması

Bir sanal yöntem çağrıldığında, yöntemi yürüten gerçek tür çalışma zamanına kadar seçili değildir. Bir Oluşturucu sanal bir yöntemi çağırdığında, yöntemi çağıran örnek için olan oluşturucunun yürütülmemiş olması mümkündür.

> [!NOTE]
> Bu kuralın eski analiz uygulamasının farklı bir tanılama iletisi " **\[Oluşturucu adı], sınıf tarafından tanımlanan bir sanal yönteme çağrı ile sonuçlanan bir çağrı zinciri içeriyor. İstenmeyen sonuçlar**için aşağıdaki çağrı yığınını gözden geçirin. Bu kuralın [FxCop çözümleyicileri](install-fxcop-analyzers.md) uygulamasının "**kurucularda geçersiz kılınabilir yöntemleri çağırma**" tanılama iletisi vardır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, türün oluşturucularının içinden bir türün sanal yöntemlerini çağırmayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Sanal yöntem çağrısını ortadan kaldırmak için oluşturucunun yeniden tasarlanması gerekir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kuralı ihlal eden etkisini gösterir. Test uygulaması `DerivedType`, kendi temel sınıf (`BadlyConstructedType`) oluşturucusunun yürütülmesine neden olan bir örneği oluşturur. `BadlyConstructedType`oluşturucusunun sanal yöntemi `DoSomething`yanlış bir şekilde çağırır. Çıktıda gösterildiği gibi, `DerivedType.DoSomething()` Oluşturucu yürütmeden önce `DerivedType`yürütülür.

[!code-csharp[FxCop.Usage.CtorVirtual#1](../code-quality/codesnippet/CSharp/ca2214-do-not-call-overridable-methods-in-constructors_1.cs)]
[!code-vb[FxCop.Usage.CtorVirtual#1](../code-quality/codesnippet/VisualBasic/ca2214-do-not-call-overridable-methods-in-constructors_1.vb)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
Calling base ctor.
Derived DoSomething is called - initialized ? No
Calling derived ctor.
```