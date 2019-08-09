---
title: 'CA1047: Sealed türlerde protected üyeler bildirmeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotDeclareProtectedMembersInSealedTypes
- CA1047
helpviewer_keywords:
- CA1047
- DoNotDeclareProtectedMembersInSealedTypes
ms.assetid: 829033b5-a9d8-4f26-a719-45494c9dd035
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 5ab7cf2c5a4f17966ed5b4da30657e05a4683738
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922642"
---
# <a name="ca1047-do-not-declare-protected-members-in-sealed-types"></a>CA1047: Sealed türlerde protected üyeler bildirmeyin

|||
|-|-|
|TypeName|DoNotDeclareProtectedMembersInSealedTypes|
|CheckId|CA1047|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Ortak bir tür `sealed` (`NotInheritable` Visual Basic 'te) ve korumalı bir üye ya da korumalı bir iç içe tür bildirir. Bu kural yöntemler için <xref:System.Object.Finalize%2A> ihlalleri raporlamaz, bu da bu düzene uymalıdır.

## <a name="rule-description"></a>Kural açıklaması
Türler, devralmasına erişebileceğiniz veya üyeyi geçersiz kılmak için korunan üyelerin türlerini bildirir. Tanım olarak, korumalı türler üzerinde korunan yöntemlerin çağrılabilmesi için korumalı bir türden devralma yapılamaz.

C# Derleyici bu hata için bir uyarı verir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için üyenin erişim düzeyini özel olarak değiştirin veya türü devralınabilir yapın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın. Türü geçerli durumunda bırakmak, bakım sorunlarına neden olabilir ve herhangi bir avantaj sağlamaz.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralı ihlal eden bir türü gösterir.

[!code-vb[FxCop.Design.SealedNoProtected#1](../code-quality/codesnippet/VisualBasic/ca1047-do-not-declare-protected-members-in-sealed-types_1.vb)]
[!code-csharp[FxCop.Design.SealedNoProtected#1](../code-quality/codesnippet/CSharp/ca1047-do-not-declare-protected-members-in-sealed-types_1.cs)]