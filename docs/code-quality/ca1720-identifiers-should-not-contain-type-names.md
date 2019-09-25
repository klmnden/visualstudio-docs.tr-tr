---
title: 'CA1720: Tanımlayıcılar tür adları içermemelidir'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1720
- IdentifiersShouldNotContainTypeNames
helpviewer_keywords:
- IdentifiersShouldNotContainTypeNames
- CA1720
ms.assetid: c95ee48f-f23a-45f0-ac9e-a3c1ecfabdea
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a2677c2ef5342b795bb684f3ab06bc7cf5195cf7
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233890"
---
# <a name="ca1720-identifiers-should-not-contain-type-names"></a>CA1720: Tanımlayıcılar tür adları içermemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotContainTypeNames|
|CheckId|CA1720|
|Kategori|Microsoft. Naming|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir üye içindeki bir parametrenin adı bir veri türü adı içerir.

veya

Üyenin adı dile özgü bir veri türü adı içerir.

Bu kural varsayılan olarak yalnızca dışarıdan görünür üyelere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Parametrelerin ve üyelerin adları, geliştirme araçları tarafından sağlanması beklenen, kendi türlerini tanımlamaya kıyasla anlamını iletmek için daha iyi kullanılır. Üye adları için, bir veri türü adı kullanılması gerekiyorsa dile özgü bir ad kullanın. Örneğin, C# tür adı `int`yerine dilden bağımsız veri türü adı ' nı `Int32`kullanın.

Parametre veya üyenin adındaki her bir ayrık belirteç, büyük/küçük harfe duyarsız bir şekilde aşağıdaki dile özgü veri türü adlarına göre denetlenir:

- Bool
- WChar
- Int8
- UInt8
- Kısa
- UShort
- int
- U
- Tamsayı
- UInteger
- Uzun
- 'Tur
- İşaretlenmemiş
- İmza
- Float
- Float32
- Float64

Ayrıca, bir parametrenin adları, büyük/küçük harf duyarsız bir şekilde aşağıdaki dilden bağımsız veri türü adlarına karşı de denetlenir:

- Nesne
- Nesnesi
- Boole değeri
- Char
- Dize
- SByte
- Bayt
- Ubde
- Int16
- UInt16
- Int32
- UInt32
- Int64
- UInt64
- IntPtr
- kaydetmeye
- Çağrısı
- Uıınptr
- UPtr
- UPointer
- Tek
- Çift
- Ondalık
- Guid

## <a name="how-to-fix-violations"></a>İhlalleri çözme

**Bir parametreye göre tetiklendiğinde:**

Parametresinin adı içindeki veri türü tanımlayıcısını, anlamını daha iyi açıklayan bir terim veya ' Value ' gibi daha genel bir terim ile değiştirin.

**Bir üyeye karşı harekete geçirildiğinde:**

Üyenin adında dile özgü veri türü tanımlayıcısını, anlamını daha iyi açıklayan bir terim, dilden bağımsız bir eşdeğer veya ' Value ' gibi daha genel bir terim ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Tür tabanlı parametre ve üye adlarının zaman zaman kullanımı uygun olabilir. Bununla birlikte, yeni geliştirme için, bu kuraldan bir uyarıyı bastırdığınızda bilinen senaryolar oluşmaz. Daha önce sevk edilen kitaplıklar için, bu kuraldan bir uyarıyı bastırdığınızda kalabilirsiniz.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1720.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (adlandırma) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="related-rules"></a>İlgili kurallar

- [CA1709 Tanımlayıcılar doğru şekilde yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708 Tanımlayıcılar, büyük/küçük harf bakımından farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
- [CA1707 Tanımlayıcılar alt çizgi içermemelidir](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)
- [CA1719 Parametre adları üye adlarıyla eşleşmemelidir](../code-quality/ca1719-parameter-names-should-not-match-member-names.md)