---
title: 'CA1715: Tanımlayıcılar doğru öneke sahip olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1715
- IdentifiersShouldHaveCorrectPrefix
helpviewer_keywords:
- IdentifiersShouldHaveCorrectPrefix
- CA1715
ms.assetid: cf45f8df-6855-4cb6-a4e2-7cfed714cf2f
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 7c7abdaa2356bdf622f0892e9b027047fc021096
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53912931"
---
# <a name="ca1715-identifiers-should-have-correct-prefix"></a>CA1715: Tanımlayıcılar doğru öneke sahip olmalıdır

|||
|-|-|
|TypeName|IdentifiersShouldHaveCorrectPrefix|
|CheckId|CA1715|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|-Arabirimlerde tetiklendiğinde kesiliyor.<br /><br /> Bölünemez - genel tür parametrelerinde oluştuğunda.|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir arabirimin adını bir büyük harf 'ı' başlamıyor.

 -veya-

 Genel tür parametresi dışarıdan görünen tür veya yöntem adı ile bir büyük harf 'T başlamıyor '.

## <a name="rule-description"></a>Kural açıklaması
 Kural gereği, programlama öğelerinin adlarını belirli bir önek ile başlayın.

 Arabirim adına 'I' başka bir büyük harf tarafından izlenen büyük harf ile başlamalıdır. Bu kural ihlalleri için arabirim adına 'MyInterface' ve 'IsolatedInterface' gibi bildirir.

 Genel tür parametresi adlarına başlamalıdır bir büyük harf ile 'T' ve isteğe bağlı olarak başka bir büyük harf tarafından izlenebilir. Bu kural ihlalleri için 'V' ve 'Type' gibi genel tür parametre adları bildirir.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Tanımlayıcı doğru önek yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 **Aşağıdaki örnek, yanlış adlandırılmış bir arabirimi gösterir.**

 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_1.cpp)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_1.vb)]
 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_1.cs)]

## <a name="example"></a>Örnek
 **Aşağıdaki örnek, önceki ihlali 'I' arabirimi koyarak düzeltir.**

 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_2.cs)]
 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_2.cpp)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_2.vb)]

## <a name="example"></a>Örnek
 **Aşağıdaki örnek, bir yanlış adlandırılmış genel tür parametresi gösterir.**

 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_3.cpp)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_3.vb)]
 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_3.cs)]

## <a name="example"></a>Örnek
 **Aşağıdaki örnek önceki ihlali 'T genel tür parametre ekleyerek düzeltmeleri '.**

 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_4.cpp)]
 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_4.cs)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_4.vb)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1722: Tanımlayıcıların önekleri yanlış olmamalıdır](../code-quality/ca1722-identifiers-should-not-have-incorrect-prefix.md)