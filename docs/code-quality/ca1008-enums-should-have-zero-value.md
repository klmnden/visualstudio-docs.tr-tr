---
title: 'CA1008: Sabit listelerinin sıfır değeri olmalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1008
- EnumsShouldHaveZeroValue
helpviewer_keywords:
- CA1008
- EnumsShouldHaveZeroValue
ms.assetid: 3503a73c-360c-416d-8ee4-c2aa44365a05
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 4bb79d2944bdb49c59fd53fb30e1497c57c5c516
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62779658"
---
# <a name="ca1008-enums-should-have-zero-value"></a>CA1008: Sabit listelerinin sıfır değeri olmalıdır

|||
|-|-|
|TypeName|EnumsShouldHaveZeroValue|
|CheckId|CA1008|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Eklemek için istendiğinde bölünemez - bir **hiçbiri** bayrağı olmayan bir sabit listesi değeri. Yeniden adlandırmakta ya da tüm sabit listesi değerleri kaldırmak isteyip istemediğiniz sorulduğunda - kesiliyor.|

## <a name="cause"></a>Sebep

Numaralandırmaya uygulanan bir olmadan <xref:System.FlagsAttribute?displayProperty=fullName> sıfır değerine sahip bir üye tanımlamıyor. Veya, bir uygulanan olan bir numaralandırma <xref:System.FlagsAttribute> bir üyeyi tanımlayan bir değeri sıfır olan ancak adını 'None' değil. Ya da birden çok sabit listesi tanımlar sıfır değerli üyeleri.

Varsayılan olarak, bu kural yalnızca dışarıdan görünen bir numaralandırma sırasında görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Diğer değer türleri gibi başlatılmamış bir numaralandırmanın varsayılan değeri sıfırdır. Bayrakları öznitelikli sabit listesi, böylece varsayılan değer geçerli bir numaralandırma değeri sıfır değerine sahip bir üye tanımlamanız gerekir. Uygunsa, üye 'None' olarak adlandırın. Aksi takdirde, sıfır en sık kullanılan bir üyeye atayın. Değerin ilk sabit listesi üyesi bildiriminde ayarlanmazsa varsayılan olarak, değeri sıfırdır.

Sahip bir sabit listesi varsa <xref:System.FlagsAttribute> uygulanan bir sıfır değerli üyeyi tanımlayan adı numaralandırmada hiçbir değer ayarlandığını göstermek için ' None' olmalıdır. Aykırı kullanımını başka bir amaç için sıfır değerli bir üyeyi kullanarak <xref:System.FlagsAttribute> içeren ve ve veya bit düzeyinde işleçler üyesiyle gereksiz. Bu, yalnızca bir üyenin değeri sıfır atanması anlamına gelir. Sıfır değerine sahip birden çok üye bayrakları öznitelikli numaralandırmada, gerçekleşirse `Enum.ToString()` sıfır olmayan üyeler için hatalı sonuçlar verir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Numaralandırma bayraklarını öznitelikli için bu kural ihlalini düzeltmek için sıfır değerine sahip bir üye tanımlayın. Bu bir hataya neden olmayan değişikliktir. Sıfır değerli bir üyeyi tanımlayan bayraklar öznitelikli numaralandırmalar bu üye 'None' olarak adlandırın ve sıfır değerine sahip herhangi bir üye silin; bir değişiklik budur.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Daha önce sevk bayrakları öznitelikli numaralandırmalar dışında bu kuraldan bir uyarıyı bastırmayın.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1008.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, kural karşılayan iki sabit listeleri ve bir numaralandırma gösterir `BadTraceOptions`, bu kuralı ihlal ediyor.

[!code-cpp[FxCop.Design.EnumsZeroValue#1](../code-quality/codesnippet/CPP/ca1008-enums-should-have-zero-value_1.cpp)]
[!code-csharp[FxCop.Design.EnumsZeroValue#1](../code-quality/codesnippet/CSharp/ca1008-enums-should-have-zero-value_1.cs)]
[!code-vb[FxCop.Design.EnumsZeroValue#1](../code-quality/codesnippet/VisualBasic/ca1008-enums-should-have-zero-value_1.vb)]

## <a name="related-rules"></a>İlgili kuralları

- [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)
- [CA1700: Numaralandırma değerlerini 'Reserved' olarak adlandırmayın](../code-quality/ca1700-do-not-name-enum-values-reserved.md)
- [CA1712: Enum değerleri için tür adıyla önek kullanmayın](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)
- [CA1028: Numaralandırma depolaması Int32 olmalıdır](../code-quality/ca1028-enum-storage-should-be-int32.md)
- [CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Enum?displayProperty=fullName>