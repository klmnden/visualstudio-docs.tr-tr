---
title: 'CA1700: Sabit listesi değerlerini adlandırmayın &#39;ayrılmış&#39;'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 27372856d8984a1c16741142a4affec757670b32
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53914640"
---
# <a name="ca1700-do-not-name-enum-values-39reserved39"></a>CA1700: Sabit listesi değerlerini adlandırmayın &#39;ayrılmış&#39;

|||
|-|-|
|TypeName|DoNotNameEnumValuesReserved|
|CheckId|CA1700|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir numaralandırma üyesinin adı "ayrılmış" sözcüklerini içerir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, "ayrılmış" içeren bir ada sahip numaralandırma üyesi şu anda kullanılmamaktadır ancak yeniden adlandırılabilir veya gelecekteki bir sürüme kaldırıldığını varsayar. Üye kaldırma veya yeniden adlandırma bölünmesi farklıdır. Kullanıcıların bir üyesi olduğundan, yalnızca "ayrılmış" adını içerir ya da kullanıcılara Okuma veya belge tarafından uymayı güvenebilirsiniz yoksay beklememeniz gerekir. Ayrıca, nesne tarayıcılar ve akıllı bir tümleşik geliştirme ortamları ayrılmış üyeleri görünür olduğundan, bunlar hakkında gerçekten üyeleri kullanıldığını karışıklığa neden olabilir.

Ayrılmış bir üye kullanmak yerine, sabit listesi gelecek sürümünde yeni bir üye ekleyin. Eklenmesini değiştirmek için özgün üyelerinin değerlerini neden olmaz sürece çoğu durumda, yeni üyenin toplama bozucu bir değişiklik değil.

Bile özgün değerlerine özgün üyelerini korumak, çalışmaları sınırlı bir süre içinde bir üyenin bir değişiklik ektir. Öncelikle, yeni üye var olan kod yolları kullanan çağıranlar bozmadan döndürülemez bir `switch` (`Select` içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) ifadesi, kapsayan tüm üye listesi ve bu bir özel durum oluşturur dönüş değeri Varsayılan durumda. İstemci kodu yansıma yöntemleri davranış değişikliği gibi işleyebilir değil, bir ikincil arz ettiği <xref:System.Enum.IsDefined%2A?displayProperty=fullName>. Buna uygun olarak, mevcut yöntemlerden döndürülecek yeni üyenin veya bilinen uygulama uyumsuzluğu nedeniyle zayıf yansıma kullanım gerçekleşir, yalnızca bölünemez çözümdür:

1. Özgün ve yeni üyelerini içeren yeni bir sabit listesi ekleyin.

2. Özgün numaralandırması ile işaretle <xref:System.ObsoleteAttribute?displayProperty=fullName> özniteliği.

   Herhangi bir dışarıdan görülebilen türler ve özgün numaralandırma kullanıma üyeleri için aynı yordamı izleyin.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için kaldırmak veya üye yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Daha önce sevk kitaplıkları veya şu anda kullanılan bir üye için bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları

[CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

[CA1712: Enum değerleri için tür adıyla önek kullanmayın](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)

[CA1028: Numaralandırma depolaması Int32 olmalıdır](../code-quality/ca1028-enum-storage-should-be-int32.md)

[CA1008: Numaralandırmalar sıfır değerine sahip olmalıdır](../code-quality/ca1008-enums-should-have-zero-value.md)

[CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)