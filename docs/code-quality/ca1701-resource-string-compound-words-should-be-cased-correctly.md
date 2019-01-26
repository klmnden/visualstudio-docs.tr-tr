---
title: 'CA1701: Kaynak dizesi bileşik sözcüklerin büyük küçük harfleri doğru olmalıdır'
ms.date: 03/28/2018
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- ResourceStringCompoundWordsShouldBeCasedCorrectly
- CA1701
helpviewer_keywords:
- CA1701
- ResourceStringCompoundWordsShouldBeCasedCorrectly
ms.assetid: 4ddbe09f-24b8-4c47-9373-a06f4487ca0d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bf671e8c948f4554225278982c4db794fedb974d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55023385"
---
# <a name="ca1701-resource-string-compound-words-should-be-cased-correctly"></a>CA1701: Kaynak dizesi bileşik sözcüklerin büyük küçük harfleri doğru olmalıdır

|||
|-|-|
|TypeName|ResourceStringCompoundWordsShouldBeCasedCorrectly|
|CheckId|CA1701|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Kaynak dizesi, büyük küçük harfleri doğru için görünmeyen bir bileşik sözcük içerir.

## <a name="rule-description"></a>Kural açıklaması

Kaynak dizedeki her sözcüğün büyük/küçük harf üzerinde temel belirteçler içinde bölünür. Her bir bitişik ikili-işaret kombinasyonu Microsoft yazım kitaplığı tarafından denetlenir. Tanınırsa, kelime kural ihlali üretir. "CheckSum" ve "Checksum" ve "Multipart" sırasıyla yazılmalıdır "MultiPart" bir ihlaline neden bileşik sözcüklerin örnekleridir. Önceki ortak kullanımı nedeniyle kurala birkaç özel durum oluşturulur ve "Araç çubuğu" ve "iki ayrı sözcükleri yazılmalıdır Filename" gibi birden fazla tek sözcük işaretlenir. Bu örnekte, "Araç çubuğu" ve "Dosya adı" bayrak eklenmiş.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Word'ün bu sözcüklerden şekilde değiştirin.

## <a name="change-the-dictionary-language"></a>Sözlük dilini değiştirme

Varsayılan olarak, yazım denetimcisi (TR) İngilizce sürümü kullanılır. Yazım dilini değiştirmek istiyorsanız, ekleyerek aşağıdakilerden birini özniteliklerini şekilde bunu yapabilirsiniz, *AssemblyInfo.cs* veya *AssemblyInfo.vb* dosyası:

- Kullanım <xref:System.Reflection.AssemblyCultureAttribute> kaynaklarınızın bir uydu derlemesine varsa kültürü belirtmek için.
- Kullanım <xref:System.Resources.NeutralResourcesLanguageAttribute> belirtmek için *bağımsız kültür* derlemenizin kaynaklarınızı aynı bütünleştirilmiş kod bulunuyorsa.

> [!IMPORTANT]
> İngilizce-tabanlı bir kültür dışında bir kültürü ayarlarsanız, bu kod çözümleme kural sessiz bir şekilde devre dışı bırakıldı.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bileşik sözcük kısımlarını yazım sözlüğüyle tanınır ve amacı iki kelimeye kullanmaktır. Bu kuraldan bir uyarıyı bastırmak güvenlidir.

Özel sözlük yazım denetimi için bileşik sözcüklerin ekleyebilirsiniz. Özel sözlük sözcükleri ihlallerine neden olmaz. Daha fazla bilgi için [nasıl yapılır: Kod çözümleme dizinini özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md).

## <a name="related-rules"></a>İlgili kuralları

- [CA1702: Bileşik sözcüklerin doğru yazılmalıdır](../code-quality/ca1702-compound-words-should-be-cased-correctly.md)
- [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Büyük/Küçük Harf Kuralları](/dotnet/standard/design-guidelines/capitalization-conventions)
- [Adlandırma Kuralları](/dotnet/standard/design-guidelines/naming-guidelines)