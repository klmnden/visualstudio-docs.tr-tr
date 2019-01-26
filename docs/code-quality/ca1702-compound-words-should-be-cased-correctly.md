---
title: 'CA1702: Bileşik sözcüklerin büyük küçük harfleri doğru olmalıdır'
ms.date: 03/28/2018
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1702
- CompoundWordsShouldBeCasedCorrectly
helpviewer_keywords:
- CA1702
- CompoundWordsShouldBeCasedCorrectly
ms.assetid: 05481245-7ad8-48c3-a456-3aa44b6160a6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 67d697ac5c441efaf78fa7382b9efdead647eec8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54996512"
---
# <a name="ca1702-compound-words-should-be-cased-correctly"></a>CA1702: Bileşik sözcüklerin büyük küçük harfleri doğru olmalıdır

|||
|-|-|
|TypeName|CompoundWordsShouldBeCasedCorrectly|
|CheckId|CA1702|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|En son ne zaman derlemelerini tetiklenir.<br /><br /> Bölünemez - tür parametrelerinde tetiklendiğinde.|

## <a name="cause"></a>Sebep

Tanımlayıcının adı birden çok sözcük içerir ve bu sözcüklerden en az biri büyük harf kullanımı hatasına maruz kalmış birleşik kelime olarak görülür.

## <a name="rule-description"></a>Kural açıklaması

Tanımlayıcı adı büyük/küçük harf üzerinde dayalı sözcükler bölündüğünü. Bitişik her iki word birleşimi, Microsoft Yazım kitaplığı tarafından denetlenir. Tanımlıysa, tanımlayıcı bir kural ihlali üretir. "CheckSum" ve "Checksum" ve "Multipart" sırasıyla yazılmalıdır "MultiPart" bir ihlaline neden bileşik sözcüklerin örnekleridir. Önceki yaygın kullanım nedeniyle, kurala birkaç özel durum oluşturulur ve birden fazla tek sözcük işaretlenmiş, "Araç çubuğu" ve "Dosya adı" gibi büyük/küçük harfleri olarak iki ayrı sözcükleri (Bu durumda, "Araç çubuğu" ve "Dosya adı").

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Böylece bu sözcüklerden adını değiştirin.

## <a name="language"></a>Dil

Yazım denetleyicisi şu anda yalnızca İngilizce tabanlı kültürü sözlükleri karşı denetler. Proje dosyası projenize kültürü ekleyerek değiştirebilirsiniz **CodeAnalysisCulture** öğesi.

Örneğin:

```xml
<Project ...>
  <PropertyGroup>
    <CodeAnalysisCulture>en-AU</CodeAnalysisCulture>
```

> [!IMPORTANT]
> İngilizce-tabanlı bir kültür dışında bir kültürü ayarlarsanız, bu kod çözümleme kural sessiz bir şekilde devre dışı bırakıldı.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bileşik sözcük kısımlarını yazım sözlüğüyle tanınır ve amacı iki kelimeye kullanmaktır. Bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları

- [CA1701: Kaynak dize bileşik sözcüklerinin doğru yazılmalıdır](../code-quality/ca1701-resource-string-compound-words-should-be-cased-correctly.md)
- [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Adlandırma Kuralları](/dotnet/standard/design-guidelines/naming-guidelines)
- [Büyük/Küçük Harf Kuralları](/dotnet/standard/design-guidelines/capitalization-conventions)