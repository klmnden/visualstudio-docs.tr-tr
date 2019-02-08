---
title: 'CA1703: Kaynak dizeleri doğru yazılmalıdır'
ms.date: 03/28/2018
ms.topic: reference
f1_keywords:
- ResourceStringsShouldBeSpelledCorrectly
- CA1703
helpviewer_keywords:
- CA1703
- ResourceStringsShouldBeSpelledCorrectly
ms.assetid: 693f4970-f512-40cb-ae3b-a0f3a5c6d6f1
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2643ff7cb8ce401462be7e5c1e52d5f985896f3a
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55915732"
---
# <a name="ca1703-resource-strings-should-be-spelled-correctly"></a>CA1703: Kaynak dizeleri doğru yazılmalıdır

|||
|-|-|
|TypeName|ResourceStringsShouldBeSpelledCorrectly|
|CheckId|CA1703|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Kaynak dizesi, Microsoft Yazım kitaplığı tarafından tanınmayan bir veya birkaç sözcük içerir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural kaynak dizesi (bileşik sözcüklerin) kelimelere ayrıştırır ve her kelimenin/belirtecin yazımını denetler. Ayrıştırma algoritma hakkında daha fazla bilgi için bkz. [CA1704: Tanımlayıcıları yazıldığından](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md).

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için sözcüklerin bir özel sözlüğüne ekleyin ya da doğru yazıldığından tam sözcük kullanın. Özel sözlükler kullanma hakkında daha fazla bilgi için bkz: [CA1704: Tanımlayıcıları yazıldığından](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md).

## <a name="change-the-dictionary-language"></a>Sözlük dilini değiştirme

Varsayılan olarak, yazım denetimcisi (TR) İngilizce sürümü kullanılır. Yazım dilini değiştirmek istiyorsanız, ekleyerek aşağıdakilerden birini özniteliklerini şekilde bunu yapabilirsiniz, *AssemblyInfo.cs* veya *AssemblyInfo.vb* dosyası:

- Kullanım <xref:System.Reflection.AssemblyCultureAttribute> kaynaklarınızın bir uydu derlemesine varsa kültürü belirtmek için.
- Kullanım <xref:System.Resources.NeutralResourcesLanguageAttribute> belirtmek için *bağımsız kültür* derlemenizin kaynaklarınızı aynı bütünleştirilmiş kod bulunuyorsa.

> [!IMPORTANT]
> İngilizce-tabanlı bir kültür dışında bir kültürü ayarlarsanız, bu kod çözümleme kural sessiz bir şekilde devre dışı bırakıldı.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın. Doğru bir şekilde yazılmış kelimeler yeni yazılım kitaplıkları öğrenmek için gereken süreyi azaltın.

## <a name="related-rules"></a>İlgili kuralları

- [CA1701: Kaynak dize bileşik sözcüklerinin doğru yazılmalıdır](../code-quality/ca1701-resource-string-compound-words-should-be-cased-correctly.md)
- [CA1704: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)
- [CA2204: Değişmez değerler doğru yazılmalıdır](../code-quality/ca2204-literals-should-be-spelled-correctly.md)