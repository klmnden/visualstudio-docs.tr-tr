---
title: 'CA2002: Zayıf kimliği olan nesneleri kilitlemeyin'
ms.date: 01/31/2018
ms.topic: reference
f1_keywords:
- DoNotLockOnObjectsWithWeakIdentity
- CA2002
helpviewer_keywords:
- CA2002
- DoNotLockOnObjectsWithWeakIdentity
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: fc4504e917daeadc93963c6d6870c00515a5065a
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233170"
---
# <a name="ca2002-do-not-lock-on-objects-with-weak-identity"></a>CA2002: Zayıf kimliği olan nesneleri kilitlemeyin

|||
|-|-|
|TypeName|DoNotLockOnObjectsWithWeakIdentity|
|CheckId|CA2002|
|Kategori|Microsoft. güvenilirliği|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir iş parçacığı, zayıf bir kimliğe sahip bir nesne üzerinde kilit edinmeye çalışır.

## <a name="rule-description"></a>Kural açıklaması

Bir nesneye uygulama etki alanları arasından erişilebiliyorsa o nesnenin zayıf bir kimliğe sahip olduğu söylenir. Zayıf kimliğe sahip bir nesne üzerinde kilit almayı deneyen iş parçacığı aynı nesne üzerinde bir kilide sahip olan farklı uygulama etki alanı içindeki ikinci iş parçacığı tarafından engellenebilir.

Aşağıdaki türlerin zayıf bir kimliği vardır ve kurala göre işaretlenir:

- <xref:System.String>

- [İntegral türleri](/dotnet/csharp/language-reference/keywords/integral-types-table), [kayan nokta türleri](/dotnet/csharp/language-reference/keywords/floating-point-types-table)ve <xref:System.Boolean>dahil olmak üzere değer türlerinin dizileri.

- <xref:System.MarshalByRefObject>

- <xref:System.ExecutionEngineException>

- <xref:System.OutOfMemoryException>

- <xref:System.StackOverflowException>

- <xref:System.Reflection.MemberInfo>

- <xref:System.Reflection.ParameterInfo>

- <xref:System.Threading.Thread>

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, açıklama bölümündeki listede yer alan bir türden bir nesne kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kurallar

[CA2213 Atılabilir alanlar atılmalıdır](../code-quality/ca2213-disposable-fields-should-be-disposed.md)

## <a name="example"></a>Örnek

Aşağıdaki örnekte, kuralı ihlal eden bazı nesne kilitleri gösterilmektedir.

[!code-vb[FxCop.Reliability.LockWeakObjects#1](../code-quality/codesnippet/VisualBasic/ca2002-do-not-lock-on-objects-with-weak-identity_1.vb)]
[!code-csharp[FxCop.Reliability.LockWeakObjects#1](../code-quality/codesnippet/CSharp/ca2002-do-not-lock-on-objects-with-weak-identity_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Threading.Monitor>
- <xref:System.AppDomain>
- [Lock deyimleri (C#)](/dotnet/csharp/language-reference/keywords/lock-statement)
- [SyncLock ekstresi (Visual Basic)](/dotnet/visual-basic/language-reference/statements/synclock-statement)