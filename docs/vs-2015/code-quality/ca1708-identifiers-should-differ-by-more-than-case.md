---
title: 'CA1708: Tanımlayıcılar farklı büyük küçük harf | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- IdentifiersShouldDifferByMoreThanCase
- CA1708
helpviewer_keywords:
- CA1708
- IdentifiersShouldDifferByMoreThanCase
ms.assetid: dac0f01d-dd21-484d-add1-c8cd2bf6969f
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a58e40ff973467e9a24a923410ff2f73981ecaab
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54759832"
---
# <a name="ca1708-identifiers-should-differ-by-more-than-case"></a>CA1708: Tanımlayıcılar yalnızca büyük küçük harfle birbirinden farklı olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|IdentifiersShouldDifferByMoreThanCase|
|CheckId|CA1708|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 İki tür, üye, parametre veya tam ad alanları adları, küçük harfe dönüştürüldüğünde aynıdır.

## <a name="rule-description"></a>Kural Tanımı
 Ortak dil çalışma zamanı hedef dilleri büyük/küçük harf duyarlı olması gerekmediğinden ad alanları, türler, üyeler ve parametreler için tanımlayıcılar yalnızca büyük/küçük harfe göre farklılık göstermeyebilir. Örneğin, [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] yaygın olarak kullanılan bir büyük küçük harf duyarsız dilidir.

 Bu kural yalnızca herkese görünür üyelere tetikler.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Büyük küçük harf duyarlı bir şekilde diğer tanımlayıcılarla karşılaştırılır, benzersiz bir ad seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Kitaplık tüm kullanılabilir dilde kullanılabilir olmayabilir [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)].

## <a name="example-of-a-violation"></a>Bir ihlali örneği
 Aşağıdaki örnek, bu kural ihlalini gösterir.

 [!code-csharp[FxCop.Naming.IdentifiersShouldDifferByMoreThanCase#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Naming.IdentifiersShouldDifferByMoreThanCase/cs/FxCop.Naming.IdentifiersShouldDifferByMoreThanCase.cs#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
