---
title: 'CA1048: Korumalı türlerde sanal üyeleri bildirmeyin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotDeclareVirtualMembersInSealedTypes
- CA1048
helpviewer_keywords:
- DoNotDeclareVirtualMembersInSealedTypes
- CA1048
ms.assetid: 5dcf4a30-6f98-48a8-b8cc-7b89ea757262
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 36ee787ca9762766f8c563ab4b5081ee47355a56
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54774417"
---
# <a name="ca1048-do-not-declare-virtual-members-in-sealed-types"></a>CA1048: Sealed türlerde virtual üyeler bildirmeyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotDeclareVirtualMembersInSealedTypes|
|CheckId|CA1048|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak tür, korumalı ve hem de bir yöntem `virtual` (`Overridable` Visual Basic'te) ve son değil. Bu kural ihlalleri bu deseni izlemelidir temsilci türleri raporlamaz.

## <a name="rule-description"></a>Kural Tanımı
 Türler yöntemi sanal olarak bildirir, böylece devralan türler sanal yöntemin uygulanmasını geçersiz kılabilir. Tanımı gereği, sanal yöntemi mühürlenmiş bir türde anlamsız hale getirme sealed türünden devralınamaz.

 Visual Basic .NET ve C# Derleyicileri türleri bu kuralı ihlal edilmesine izin vermez.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için yöntemi sanal olmayan veya türü devralınabilir.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Geçerli durumunda türü bırakarak bakım sorunlarına neden olabilir ve herhangi bir avantaj sağlamaz.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir.

 [!code-cpp[FxCop.Design.SealedVirtual#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.SealedVirtual/cpp/FxCop.Design.SealedVirtual.cpp#1)]
