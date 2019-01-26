---
title: 'CA1711: Tanımlayıcılar yanlış sonek içermemelidir'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1711
- IdentifiersShouldNotHaveIncorrectSuffix
helpviewer_keywords:
- CA1711
- IdentifiersShouldNotHaveIncorrectSuffix
ms.assetid: a63359ab-386d-44ae-b381-ee3a983aca29
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a612aa39899336eda4802e849529ae61faf192be
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54935650"
---
# <a name="ca1711-identifiers-should-not-have-incorrect-suffix"></a>CA1711: Tanımlayıcılar yanlış sonek içermemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotHaveIncorrectSuffix|
|CheckId|CA1711|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tanımlayıcı yanlış bir son eke sahip.

## <a name="rule-description"></a>Kural açıklaması

Kural gereği, yalnızca, belirli temel türleri genişleten veya bazı arabirimleri ya da bu türlerden türetilmiş türleri uygulayan tür adları, belirli ayrılmış soneklerle bitmelidir. Diğer tür adları aşağıdaki ayrılmış sonekleri kullanmamalı.

Aşağıdaki tabloda, ayrılmış sonekler ve ilişkili oldukları temel türler ve arabirimler listelenmiştir.

|Son eki|Temel tür arabirimi|
|------------|--------------------------|
|Öznitelik|<xref:System.Attribute?displayProperty=fullName>|
|Koleksiyon|<xref:System.Collections.ICollection?displayProperty=fullName><br /><br /> <xref:System.Collections.IEnumerable?displayProperty=fullName><br /><br /> <xref:System.Collections.Queue?displayProperty=fullName><br /><br /> <xref:System.Collections.Stack?displayProperty=fullName><br /><br /> <xref:System.Collections.Generic.ICollection%601?displayProperty=fullName><br /><br /> <xref:System.Data.DataSet?displayProperty=fullName><br /><br /> <xref:System.Data.DataTable?displayProperty=fullName>|
|Sözlük|<xref:System.Collections.IDictionary?displayProperty=fullName><br /><br /> <xref:System.Collections.Generic.IDictionary%602?displayProperty=fullName>|
|EventArgs|<xref:System.EventArgs?displayProperty=fullName>|
|EventHandler|Bir olay işletici temsilcisi|
|Özel Durum|<xref:System.Exception?displayProperty=fullName>|
|İzin|<xref:System.Security.IPermission?displayProperty=fullName>|
|Sıra|<xref:System.Collections.Queue?displayProperty=fullName>|
|Yığın|<xref:System.Collections.Stack?displayProperty=fullName>|
|Akış|<xref:System.IO.Stream?displayProperty=fullName>|

Ayrıca, aşağıdaki sonekler **değil** kullanılabilir:

- `Delegate`

- `Enum`

- `Impl` (kullanın `Core` yerine)

- `Ex` veya benzer sonek aynı türde önceki bir sürümünden ayırmak için

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Tür adından soneki kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Sonekte uygulama etki alanında açık bir anlama sahip olmadığı sürece bu kuraldan bir uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kuralları

- [CA1710: Tanımlayıcılar doğru soneke sahip olmalıdır](../code-quality/ca1710-identifiers-should-have-correct-suffix.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Öznitelikler](/dotnet/standard/design-guidelines/attributes)
- [Olaylar oluşturma ve işleme](/dotnet/standard/events/index)