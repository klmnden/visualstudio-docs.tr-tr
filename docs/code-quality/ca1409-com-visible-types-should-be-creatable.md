---
title: 'CA1409: COM görünebilir türler oluşturulabilmelidir'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5fd168c5174dcc403a38c6eb3e443c3711fce537
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53821694"
---
# <a name="ca1409-com-visible-types-should-be-creatable"></a>CA1409: COM görünebilir türler oluşturulabilmelidir

|||
|-|-|
|TypeName|ComVisibleTypesShouldBeCreatable|
|CheckId|CA1409|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Özel Bileşen Nesne Modeli (COM) görünür olarak işaretlenmiş bir başvuru türü, parametreli ortak kurucu içeriyorsa ancak genel varsayılan (parametresiz) bir oluşturucu içermiyor.

## <a name="rule-description"></a>Kural açıklaması
 Genel bir varsayılan oluşturucu olmadan tür COM istemcileri tarafından oluşturulamıyor. Ancak, başka bir yöntem türü oluşturup istemciye (örneğin, üzerinden bir yöntem çağrısının dönüş değerini) geçirmek kullanılabilir durumdaysa türü hala COM istemcileri tarafından erişilebilir.

 Öğesinden türetilen türler kural yoksayar <xref:System.Delegate?displayProperty=fullName>.

 Varsayılan olarak, COM görünür şunlardır: derlemeleri, genel tür, genel türlerde ortak örnek üyeleri ve tüm ortak türlerin üyeleri.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için ortak varsayılan oluşturucusu ekleme veya kaldırma <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> yazın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Yollar oluşturma ve nesneyi COM istemcisi geçirin sağlandıysa bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1017: Derlemeleri ComVisibleAttribute ile işaretleyin](../code-quality/ca1017-mark-assemblies-with-comvisibleattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Birlikte Çalışma için .NET Türlerini Niteleme](/dotnet/framework/interop/qualifying-net-types-for-interoperation)
- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)