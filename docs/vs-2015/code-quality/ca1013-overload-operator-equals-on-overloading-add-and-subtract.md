---
title: 'CA1013: Aşırı yükleme aşırı eşittir işlecini ekleme ve çıkarmayı | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- OverrideOperatorEqualsOnOverridingAddAndSubtract
- OverrideOperatorEqualsOnOverloadingAddAndSubtract
- CA1013
- OverloadOperatorEqualsOnOverloadingAddAndSubtract
helpviewer_keywords:
- OverrideOperatorEqualsOnOverloadingAddAndSubtract
- OverrideOperatorEqualsOnOverridingAddAndSubtract
- CA1013
- OverloadOperatorEqualsOnOverloadingAddAndSubtract
ms.assetid: 5bd28d68-c179-49ff-af47-5250b8b18a10
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1b70085c83d842ccb5f8addc661af9109b5a5976
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65695616"
---
# <a name="ca1013-overload-operator-equals-on-overloading-add-and-subtract"></a>CA1013: Toplama ve çıkarmayı aşırı yüklediğinizde eşittir işlecini aşırı yükleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|OverloadOperatorEqualsOnOverloadingAddAndSubtract|
|CheckId|CA1013|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir genel ya da korumalı tür eşitlik imlecini uygulamadan ekleme ya da çıkarma işleçlerini uygular.

## <a name="rule-description"></a>Kural Tanımı
 Toplama ve çıkarma gibi işlemleri kullanarak bir türün örneklerinin birleştirilebilir, neredeyse her zaman eşitlik tanımlamalıdır `true` bağlı değerlerine sahip iki tüm örnekler için.

 Eşitlik işleci aşırı yüklenmiş bir uygulamada varsayılan eşitlik işlecini kullanamazsınız. Bunun yapılması, yığın taşmasına neden olur. Eşitlik işleci uygulamak için uygulamanızda Object.Equals yöntemi kullanın. Aşağıdaki örnekte bakın.

```vb
If (Object.ReferenceEquals(left, Nothing)) Then
    Return Object.ReferenceEquals(right, Nothing)
Else
    Return left.Equals(right)
End If
```

```csharp
if (Object.ReferenceEquals(left, null))
    return Object.ReferenceEquals(right, null);
return left.Equals(right);
```

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için matematiksel olarak toplama ve çıkarma işleçleri ile tutarlı olması eşitlik işlecini uygular.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Eşitlik işleci varsayılan uygulama türü için doğru davranışı sağladığında bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür tanımlar (`BadAddableType`), bu kuralı ihlal ediyor. Bu tür test alan değerlerine sahip herhangi iki örnekleri yapmak için eşitlik işlecini uygulamalıdır `true` eşitlik için. Türü `GoodAddableType` düzeltilmiş uygulamasını gösterir. Bu tür da eşitsizlik işleci uygular ve geçersiz kılmalar Not <xref:System.Object.Equals%2A> diğer kurallarını karşılamak için. Tam bir uygulama da uygulamak <xref:System.Object.GetHashCode%2A>.

 [!code-csharp[FxCop.Design.AddAndSubtract#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.AddAndSubtract/cs/FxCop.Design.AddAndSubtract.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, varsayılan ve doğru davranışı için eşitlik operatörünün göstermek için bu konuda daha önceden tanımlanan türlerin örneklerini kullanarak eşitlik için test eder.

 [!code-csharp[FxCop.Design.TestAddAndSubtract#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.TestAddAndSubtract/cs/FxCop.Design.TestAddAndSubtract.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **Yanlış tür: {2,2} {2,2} eşitse? Hayır**
**iyi türü: {3,3} {3,3} eşitse? Evet**
**iyi türü: {3,3} {3,3} == misiniz?   Evet**
**yanlış tür: {2,2} {9,9} eşitse? Hayır**
**iyi türü: {3,3} {9,9} == misiniz?   Yok**
## <a name="see-also"></a>Ayrıca Bkz.
 [Eşitlik İşleçleri](https://msdn.microsoft.com/library/bc496a91-fefb-4ce0-ab4c-61f09964119a)
