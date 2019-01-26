---
title: 'CA1047: Sealed türlerde protected üyeler bildirmeyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 77277c093396ddbfdf458e93f468ad5ce5775bd2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54928405"
---
# <a name="ca1047-do-not-declare-protected-members-in-sealed-types"></a>CA1047: Sealed türlerde protected üyeler bildirmeyin

|||
|-|-|
|TypeName|DoNotDeclareProtectedMembersInSealedTypes|
|CheckId|CA1047|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Genel bir tür `sealed` (`NotInheritable` Visual Basic'te) ve korumalı bir üye veya korumalı iç içe geçmiş bir tür bildirir. Bu kural ihlallerini raporlamaz <xref:System.Object.Finalize%2A> yöntemleri bu deseni izlemelidir.

## <a name="rule-description"></a>Kural açıklaması
 Türler, devralmasına erişebileceğiniz veya üyeyi geçersiz kılmak için korunan üyelerin türlerini bildirir. Tanımı gereği, yöntemi mühürlenmiş türler üzerindeki korunan anlamına çağrılamaz sealed türünden devralınamaz.

 C# Derleyici, bu hata için bir uyarı verir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için üye erişim düzeyini private olarak değiştirin ya da türü devralınabilir yapın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Geçerli durumunda türü bırakarak bakım sorunlarına neden olabilir ve herhangi bir avantaj sağlamaz.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir.

 [!code-vb[FxCop.Design.SealedNoProtected#1](../code-quality/codesnippet/VisualBasic/ca1047-do-not-declare-protected-members-in-sealed-types_1.vb)]
 [!code-csharp[FxCop.Design.SealedNoProtected#1](../code-quality/codesnippet/CSharp/ca1047-do-not-declare-protected-members-in-sealed-types_1.cs)]