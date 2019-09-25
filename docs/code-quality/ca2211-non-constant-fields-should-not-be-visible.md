---
title: 'CA2211: Sabit olmayan alanlar görünür olmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2211
- NonConstantFieldsShouldNotBeVisible
helpviewer_keywords:
- NonConstantFieldsShouldNotBeVisible
- CA2211
ms.assetid: e1e42c40-0acd-4312-af29-70133739a304
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 11ff4ca3a3146c1080e26fd3ab50af7f7cf0e4e6
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231758"
---
# <a name="ca2211-non-constant-fields-should-not-be-visible"></a>CA2211: Sabit olmayan alanlar görünür olmamalıdır

|||
|-|-|
|TypeName|NonConstantFieldsShouldNotBeVisible|
|CheckId|CA2211|
|Kategori|Microsoft. Usage|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir statik alan sabit değildir ve salt okunurdur.

## <a name="rule-description"></a>Kural açıklaması
Ne sabitler, ne de salt okunur olan statik alanlar güvenli iş parçacığı değildir. Bu tür bir alana erişimin dikkatle denetlenmesi ve sınıf nesnesine erişimin eşitlenmesi için gelişmiş programlama teknikleri olması gerekir. Bunlar öğrenmek ve ana öğe hakkında zor beceriler olduğundan, bu tür bir nesnenin test edilmesi, kendi zorluk sergilediğinin yanı sıra, değişmeyen verileri depolamak için en iyi şekilde kullanılır. Bu kural kitaplıklar için geçerlidir; uygulamalar herhangi bir alanı kullanıma sunmamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için statik alanı sabit veya salt okunurdur yapın. Bu mümkün değilse, temel alana iş parçacığı açısından güvenli erişimi yöneten iş parçacığı güvenli özelliği gibi alternatif bir mekanizma kullanmak için türü yeniden tasarlayabiliriz. Kilit çakışması ve kilitlenmeleri gibi sorunların, kitaplığın performansını ve davranışını etkileyebileceğini fark edebilirsiniz.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bir uygulama geliştiriyorsanız bu kuraldan bir uyarıyı gizlemek güvenlidir ve bu nedenle statik alanı içeren türe erişim üzerinde tam denetime sahip olursunuz. Kitaplık tasarımcıları bu kuraldan bir uyarı göstermemelidir; sabit olmayan statik alanları kullanmak, geliştiricilerin doğru bir şekilde kullanması için kitaplık kullanımını zorlaştırır.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralı ihlal eden bir türü gösterir.

[!code-vb[FxCop.Usage.AvoidStaticNonConstants#1](../code-quality/codesnippet/VisualBasic/ca2211-non-constant-fields-should-not-be-visible_1.vb)]
[!code-csharp[FxCop.Usage.AvoidStaticNonConstants#1](../code-quality/codesnippet/CSharp/ca2211-non-constant-fields-should-not-be-visible_1.cs)]