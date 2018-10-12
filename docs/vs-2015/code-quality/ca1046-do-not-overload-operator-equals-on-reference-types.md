---
title: 'CA1046: başvuru türlerinde eşittir işlecini aşırı yüklemeyin | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- DoNotOverloadOperatorEqualsOnReferenceTypes
- CA1046
helpviewer_keywords:
- CA1046
- DoNotOverloadOperatorEqualsOnReferenceTypes
ms.assetid: c1dfbfe3-63f9-4005-a81a-890427b77e79
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 05c58c3b136c52ace4e683c3d42d0d6417ff4a08
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49183411"
---
# <a name="ca1046-do-not-overload-operator-equals-on-reference-types"></a>CA1046: Başvuru türlerinde eşittir işleçlerini aşırı yüklemeyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|DoNotOverloadOperatorEqualsOnReferenceTypes|
|CheckId|CA1046|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir ortak veya iç içe geçmiş genel başvuru türü eşitlik işlecini aşırı yüklemeleri.

## <a name="rule-description"></a>Kural Tanımı
 Başvuru türleri için, varsayılan eşitlik işleci neredeyse her zaman doğrudur. Varsayılan olarak, yalnızca aynı nesneye gelirseniz iki başvuru eşit olur.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için eşitlik işlecini uygulamasını kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Başvuru türü davranacağını gibi yerleşik değer türünde olduğunda bu kuraldan bir uyarıyı bastırmak güvenlidir. Ekleme veya çıkarma türü örneklerinde yapmak için anlamlı olması durumunda, eşitlik işlecini uygulamak ve ihlalin bastırmak muhtemelen doğrudur.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, iki başvuru karşılaştırılırken varsayılan davranış gösterir.

 [!code-csharp[FxCop.Design.RefTypesNoEqualityOp#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.RefTypesNoEqualityOp/cs/FxCop.Design.RefTypesNoEqualityOp.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki uygulama bazı başvuruları karşılaştırır.

 [!code-csharp[FxCop.Design.TestRefTypesNoEqualityOp#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.TestRefTypesNoEqualityOp/cs/FxCop.Design.TestRefTypesNoEqualityOp.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **bir yeni (2,2) ve b = = yeni (2,2) eşit? Hayır**
**c ve eşit bir misiniz? Evet**
**b ve bir ==? Hayır**
**c ve bir ==? Evet**
## <a name="related-rules"></a>İlgili kuralları
 [CA1013: Eşittir işlecini ekleme ve çıkarmayı aşırı yükleyerek aşırı yükleyin](../code-quality/ca1013-overload-operator-equals-on-overloading-add-and-subtract.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.Object.Equals%2A?displayProperty=fullName> [Eşitlik işleçleri](http://msdn.microsoft.com/library/bc496a91-fefb-4ce0-ab4c-61f09964119a)



