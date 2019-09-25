---
title: 'CA1701: Kaynak dizesi bileşik sözcüklerin büyük küçük harfleri doğru olmalıdır'
ms.date: 03/28/2018
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
ms.openlocfilehash: ed5ae8c0845755fe626e7e801f500389f9263cf5
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234357"
---
# <a name="ca1701-resource-string-compound-words-should-be-cased-correctly"></a>CA1701: Kaynak dizesi bileşik sözcüklerin büyük küçük harfleri doğru olmalıdır

|||
|-|-|
|TypeName|ResourceStringCompoundWordsShouldBeCasedCorrectly|
|CheckId|CA1701|
|Kategori|Microsoft. Naming|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Kaynak dizesi, doğru şekilde görünmeyen bir bileşik sözcük içerir.

## <a name="rule-description"></a>Kural açıklaması

Kaynak dizesindeki her sözcük büyük küçük harfe dayalı belirteçlere bölünür. Her bir bitişik ikili-işaret kombinasyonu Microsoft yazım kitaplığı tarafından denetlenir. Tanınırsa, kelime kural ihlali üretir. İhlalin oluşmasına neden olan Birleşik kelimelerin örnekleri, sırasıyla "Checksum" ve "multipart" olarak, "Checksum" ve "multipart" şeklinde olmalıdır. Önceki yaygın kullanım nedeniyle, birkaç özel durum kuralda yerleşik olarak bulunur ve "araç çubuğu" ve "dosya adı" gibi birkaç tek sözcük işaretlenir, bu da iki ayrı sözcük olarak kullanılabilir. Bu örnekte, "araç çubuğu" ve "dosya adı" işaretlenir.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıklar için ortak bir görünüm sağlar. Bu, yeni yazılım kitaplıkları için gerekli olan öğrenme eğrisini azaltır ve müşterinin, kitaplığın yönetilen kod geliştirme konusunda uzmanlığa sahip olan birisi tarafından geliştirildiğini arttırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Kelimeyi doğru bir şekilde olacak şekilde değiştirin.

## <a name="change-the-dictionary-language"></a>Sözlük dilini değiştirme

Varsayılan olarak, yazım denetleyicisinin Ingilizce (en) sürümü kullanılır. Yazım denetleyicisinin dilini değiştirmek istiyorsanız, *AssemblyInfo.cs* veya *AssemblyInfo. vb* dosyanıza aşağıdaki özniteliklerden birini ekleyerek bunu yapabilirsiniz:

- Kaynaklarınızın <xref:System.Reflection.AssemblyCultureAttribute> uydu derlemesinde olması durumunda kültürü belirtmek için kullanın.
- Kaynaklarınızın <xref:System.Resources.NeutralResourcesLanguageAttribute> kodunuzla aynı derlemede olması halinde derlemelerinizin *bağımsız kültürünü* belirtmek için kullanın.

> [!IMPORTANT]
> Kültürü, Ingilizce tabanlı kültür dışında bir şeye ayarlarsanız, bu kod analizi kuralı sessizce devre dışıdır.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bileşik sözcüğün her iki bölümü de yazım sözlüğü tarafından tanınıyorsa ve amaç iki sözcükten birini kullanıyorsa, bu kuraldan bir uyarıyı gizlemek güvenlidir.

Ayrıca, yazım denetleyicisi için özel bir sözlüğe bileşik sözcükler ekleyebilirsiniz. Özel Sözlükteki sözcükler ihlallere neden olmaz. Daha fazla bilgi için [nasıl yapılır: Kod Analizi sözlüğünü](../code-quality/how-to-customize-the-code-analysis-dictionary.md)özelleştirin.

## <a name="related-rules"></a>İlgili kurallar

- [CA1702 Bileşik sözcüklerin doğru şekilde küçük harf olması gerekir](../code-quality/ca1702-compound-words-should-be-cased-correctly.md)
- [CA1709 Tanımlayıcılar doğru şekilde yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708 Tanımlayıcılar, büyük/küçük harf bakımından farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Büyük/Küçük Harf Kuralları](/dotnet/standard/design-guidelines/capitalization-conventions)
- [Adlandırma Kuralları](/dotnet/standard/design-guidelines/naming-guidelines)