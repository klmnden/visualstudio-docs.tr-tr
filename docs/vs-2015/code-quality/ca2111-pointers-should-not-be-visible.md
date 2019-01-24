---
title: 'CA2111: İşaretçiler görünür olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- PointersShouldNotBeVisible
- CA2111
helpviewer_keywords:
- CA2111
- PointersShouldNotBeVisible
ms.assetid: b3a8d466-895b-43bc-a2df-5d7058fe915f
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 8497433088e4c49868a76dd3281d02a5e79babe5
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54794969"
---
# <a name="ca2111-pointers-should-not-be-visible"></a>CA2111: İşaretçiler görünür olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|PointersShouldNotBeVisible|
|CheckId|CA2111|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı bir <xref:System.IntPtr?displayProperty=fullName> veya <xref:System.UIntPtr?displayProperty=fullName> alanı salt okunur değildir.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.IntPtr> ve <xref:System.UIntPtr> işaretçi türleri, yönetilmeyen bellek erişmek için kullanılır. Bir işaretçi özel, içsel veya salt okunur durumda değilse, kötü amaçlı kod işaretçinin, potansiyel olarak bellekte rastgele konumlara erişmesine izin vermek veya uygulama ya da sistem hatalarına neden değerini değiştirebilirsiniz.

 İşaretçi alan içeren tür güvenli erişim yapmak istiyorsanız, bkz. [CA2112: Güvenli türler alanları kullanıma](../code-quality/ca2112-secured-types-should-not-expose-fields.md).

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 İşaretçi salt okunur, iç veya özel hale getirerek güvenli hale getirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 İşaretçi değeri temel kullanmayın, bu kuraldan bir uyarıyı gizler.

## <a name="example"></a>Örnek
 Aşağıdaki kod, ihlal ve kural karşılamak işaretçileri gösterir. Özel olmayan işaretçileri de kuralı ihlal bildirimi [CA1051: Görünür örnek alanlarını bildirmeyin](../code-quality/ca1051-do-not-declare-visible-instance-fields.md).

 [!code-csharp[FxCop.Security.PointersArePrivate#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.PointersArePrivate/cs/FxCop.Security.PointersArePrivate.cs#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2112: Güvenli türler alanları açığa çıkarmamalıdır](../code-quality/ca2112-secured-types-should-not-expose-fields.md)

 [CA1051: Görünür örnek alanlarını bildirmeyin](../code-quality/ca1051-do-not-declare-visible-instance-fields.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.IntPtr?displayProperty=fullName><xref:System.UIntPtr?displayProperty=fullName>
