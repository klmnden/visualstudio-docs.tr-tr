---
title: 'CA1409: COM görünebilir türler oluşturulabilir olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ComVisibleTypesShouldBeCreatable
- CA1409
helpviewer_keywords:
- ComVisibleTypesShouldBeCreatable
- CA1409
ms.assetid: 9f59569b-de15-4a38-b7cb-cff152972243
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 54630b7fba69ef96a2c08486e535ae45d8e614b8
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234758"
---
# <a name="ca1409-com-visible-types-should-be-creatable"></a>CA1409: COM görünebilir türler oluşturulabilir olmalıdır

|||
|-|-|
|TypeName|ComVisibleTypesShouldBeCreatable|
|CheckId|CA1409|
|Kategori|Microsoft. çalışabilirliği|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Özellikle bileşen nesne modeli (COM) tarafından görünür olarak işaretlenen bir başvuru türü ortak parametreli bir Oluşturucu içerir ancak ortak bir varsayılan (parametresiz) Oluşturucu içermez.

## <a name="rule-description"></a>Kural açıklaması
Ortak varsayılan oluşturucusu olmayan bir tür COM istemcileri tarafından oluşturulamaz. Ancak, tür oluşturmak ve istemciye geçirmek (örneğin, bir yöntem çağrısının dönüş değeri aracılığıyla) için başka bir anlamı varsa, bu tür COM istemcileri tarafından yine de erişilebilir.

Kural öğesinden <xref:System.Delegate?displayProperty=fullName>türetilmiş türleri yoksayar.

Varsayılan olarak, aşağıdakiler COM 'a görünür: derlemeler, ortak türler, ortak türlerdeki ortak örnek üyeleri ve tüm ortak değer türleri üyeleri.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, genel bir varsayılan oluşturucu ekleyin veya türünden kaldırın <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> .

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Nesneyi oluşturmak ve COM istemcisine geçirmek için başka yollar sağlanmışsa, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="related-rules"></a>İlgili kurallar
[CA1017 Derlemeleri ComVisibleAttribute ile işaretleyin](../code-quality/ca1017-mark-assemblies-with-comvisibleattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Birlikte Çalışma için .NET Türlerini Niteleme](/dotnet/framework/interop/qualifying-net-types-for-interoperation)
- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)