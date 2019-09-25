---
title: 'CA1700: Ayrılmış Enum değerlerini &#39;adlandırma&#39;'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1700
- DoNotNameEnumValuesReserved
helpviewer_keywords:
- DoNotNameEnumValuesReserved
- CA1700
ms.assetid: 7a7e01c3-ae7d-4c82-a646-91b58864a749
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5171123827481c99bbc35c10b04aaf942a15fabb
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234384"
---
# <a name="ca1700-do-not-name-enum-values-39reserved39"></a>CA1700: Ayrılmış Enum değerlerini &#39;adlandırma&#39;

|||
|-|-|
|TypeName|DoNotNameEnumValuesReserved|
|CheckId|CA1700|
|Kategori|Microsoft. Naming|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir numaralandırma üyesinin adı "ayrılmış" sözcüğünü içerir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, "ayrılmış" içeren bir ada sahip numaralandırma üyesi şu anda kullanılmamaktadır ancak yeniden adlandırılabilir veya gelecekteki bir sürüme kaldırıldığını varsayar. Üye kaldırma veya yeniden adlandırma bölünmesi farklıdır. Kullanıcıların, adı "ayrılmış" içerdiğinden veya belgelere göre okumak veya onları okumak için kullanıcılara güvenebilmesi için, yalnızca bir üyeyi yok saymasını beklememelisiniz. Ayrıca, ayrılmış Üyeler nesne tarayıcılarında ve akıllı tümleşik geliştirme ortamlarında göründüğünden, gerçekte hangi üyelerin kullanıldığı hakkında karışıklık oluşmasına neden olabilirler.

Ayrılmış bir üye kullanmak yerine gelecekteki sürümde numaralandırmaya yeni bir üye ekleyin. Çoğu durumda, ek olarak özgün üyelerin değerlerinin değişmesine neden olmadığı sürece yeni üyenin eklenmesi bir son değişiklik değildir.

Sınırlı sayıda durumda, özgün Üyeler orijinal değerlerini korusa bile bir üyenin eklenmesi Son değişiklik olur. Birincil olarak, yeni üye, tüm üye listesini kapsayan ve içinde bir özel durum oluşturan dönüş değerindeki `switch` bir`Select` ( [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]ın) bildiriminde bir (ın) ifadesini kullanan mevcut kod yollarından geri döndürülemez. Varsayılan durum. İkincil bir sorun, istemci kodunun gibi <xref:System.Enum.IsDefined%2A?displayProperty=fullName>yansıma yöntemlerinden davranış değişikliğini işleyemeyebilir. Buna uygun olarak, yeni üyenin mevcut metotlardan döndürülmesi gerekiyorsa veya kötü yansıma kullanımı nedeniyle bilinen bir uygulama uyumsuzluğu oluşursa, tek bölünemez çözüm şu şekilde olur:

1. Özgün ve yeni üyeleri içeren yeni bir sabit listesi ekleyin.

2. Özgün numaralandırmayı <xref:System.ObsoleteAttribute?displayProperty=fullName> özniteliğiyle işaretleyin.

   Tüm dışarıdan görünen türler veya özgün numaralandırmayı kullanıma sunan Üyeler için aynı yordamı izleyin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için üyeyi kaldırın veya yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Şu anda kullanılan bir üyenin veya daha önce sevk edilen kitaplıklarda bu kuraldan bir uyarının görüntülenmesini güvenlidir.

## <a name="related-rules"></a>İlgili kurallar

[CA2217 Numaralandırmaları FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

[CA1712 Tür adı ile Enum değerlerini önek olarak kullanmayın](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)

[CA1028 Sabit Listesi depolaması Int32 olmalıdır](../code-quality/ca1028-enum-storage-should-be-int32.md)

[CA1008 Numaralandırmalar sıfır değerine sahip olmalıdır](../code-quality/ca1008-enums-should-have-zero-value.md)

[CA1027 Numaralandırmaları FlagsAttribute ile işaretle](../code-quality/ca1027-mark-enums-with-flagsattribute.md)