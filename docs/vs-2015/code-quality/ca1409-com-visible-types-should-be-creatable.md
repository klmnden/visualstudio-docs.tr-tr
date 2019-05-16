---
title: 'CA1409: COM görünebilir türler oluşturulabilir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- ComVisibleTypesShouldBeCreatable
- CA1409
helpviewer_keywords:
- ComVisibleTypesShouldBeCreatable
- CA1409
ms.assetid: 9f59569b-de15-4a38-b7cb-cff152972243
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 7bd52ad75c67f9c8faa80e84eb5ae09c22c25280
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65678871"
---
# <a name="ca1409-com-visible-types-should-be-creatable"></a>CA1409: COM görünebilir türler oluşturulabilir olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ComVisibleTypesShouldBeCreatable|
|CheckId|CA1409|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Özel Bileşen Nesne Modeli (COM) görünür olarak işaretlenmiş bir başvuru türü, parametreli ortak kurucu içeriyorsa ancak genel varsayılan (parametresiz) bir oluşturucu içermiyor.

## <a name="rule-description"></a>Kural Tanımı
 Genel bir varsayılan oluşturucu olmadan tür COM istemcileri tarafından oluşturulamıyor. Ancak, başka bir yöntem türü oluşturup istemciye (örneğin, üzerinden bir yöntem çağrısının dönüş değerini) geçirmek kullanılabilir durumdaysa türü hala COM istemcileri tarafından erişilebilir.

 Öğesinden türetilen türler kural yoksayar <xref:System.Delegate?displayProperty=fullName>.

 Varsayılan olarak, COM görünür şunlardır: derlemeleri, genel tür, genel türlerde ortak örnek üyeleri ve tüm ortak türlerin üyeleri.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için ortak varsayılan oluşturucusu ekleme veya kaldırma <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> yazın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Yollar oluşturma ve nesneyi COM istemcisi geçirin sağlandıysa bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1017: Derlemeleri ComVisibleAttribute ile işaretleyin](../code-quality/ca1017-mark-assemblies-with-comvisibleattribute.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Birlikte çalışma için .NET türlerini niteleme](https://msdn.microsoft.com/library/4b8afb52-fb8d-4e65-b47c-fd82956a3cdd) [yönetilmeyen kod ile birlikte](https://msdn.microsoft.com/library/ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258)
