---
title: 'CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- IdentifiersShouldDifferByMoreThanCase
- CA1708
helpviewer_keywords:
- CA1708
- IdentifiersShouldDifferByMoreThanCase
ms.assetid: dac0f01d-dd21-484d-add1-c8cd2bf6969f
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4fd2ac35d5c6df5e1ffc3d49ea3089bb4ee3ea77
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53833251"
---
# <a name="ca1708-identifiers-should-differ-by-more-than-case"></a>CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır

|||
|-|-|
|TypeName|IdentifiersShouldDifferByMoreThanCase|
|CheckId|CA1708|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 İki tür, üye, parametre veya tam ad alanları adları, küçük harfe dönüştürüldüğünde aynıdır.

## <a name="rule-description"></a>Kural açıklaması
 Ortak dil çalışma zamanı hedef dilleri büyük/küçük harf duyarlı olması gerekmediğinden ad alanları, türler, üyeler ve parametreler için tanımlayıcılar yalnızca büyük/küçük harfe göre farklılık göstermeyebilir. Örneğin, [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] yaygın olarak kullanılan bir büyük küçük harf duyarsız dilidir.

 Bu kural yalnızca herkese görünür üyelere tetikler.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Büyük küçük harf duyarlı bir şekilde diğer tanımlayıcılarla karşılaştırılır, benzersiz bir ad seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Kitaplığı, .NET Framework içindeki kullanılabilir tüm dillerde kullanılabilir olmayabilir.

## <a name="example-of-a-violation"></a>Bir ihlali örneği
 Aşağıdaki örnek, bu kural ihlalini gösterir.

 [!code-csharp[FxCop.Naming.IdentifiersShouldDifferByMoreThanCase#1](../code-quality/codesnippet/CSharp/ca1708-identifiers-should-differ-by-more-than-case_1.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)