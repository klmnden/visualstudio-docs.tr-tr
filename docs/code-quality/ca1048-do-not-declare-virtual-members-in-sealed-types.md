---
title: 'CA1048: Sealed türlerde virtual üyeler bildirmeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotDeclareVirtualMembersInSealedTypes
- CA1048
helpviewer_keywords:
- DoNotDeclareVirtualMembersInSealedTypes
- CA1048
ms.assetid: 5dcf4a30-6f98-48a8-b8cc-7b89ea757262
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 84db1db9061eff1373ee3ad4f0316a1f3dba0474
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55924506"
---
# <a name="ca1048-do-not-declare-virtual-members-in-sealed-types"></a>CA1048: Sealed türlerde virtual üyeler bildirmeyin

|||
|-|-|
|TypeName|DoNotDeclareVirtualMembersInSealedTypes|
|CheckId|CA1048|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak tür, korumalı ve hem de bir yöntem `virtual` (`Overridable` Visual Basic'te) ve son değil. Bu kural ihlalleri bu deseni izlemelidir temsilci türleri raporlamaz.

## <a name="rule-description"></a>Kural açıklaması
 Türler yöntemi sanal olarak bildirir, böylece devralan türler sanal yöntemin uygulanmasını geçersiz kılabilir. Tanımı gereği, sanal yöntemi mühürlenmiş bir türde anlamsız hale getirme sealed türünden devralınamaz.

 Visual Basic ve C# Derleyicileri türleri bu kuralı ihlal edilmesine izin vermez.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için yöntemi sanal olmayan veya türü devralınabilir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Geçerli durumunda türü bırakarak bakım sorunlarına neden olabilir ve herhangi bir avantaj sağlamaz.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir.

 [!code-cpp[FxCop.Design.SealedVirtual#1](../code-quality/codesnippet/CPP/ca1048-do-not-declare-virtual-members-in-sealed-types_1.cpp)]