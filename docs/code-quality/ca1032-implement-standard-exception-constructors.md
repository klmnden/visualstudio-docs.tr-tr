---
title: 'CA1032: Standart özel durum oluşturucularını uygulayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1032
- ImplementStandardExceptionConstructors
helpviewer_keywords:
- CA1032
- ImplementStandardExceptionConstructors
ms.assetid: a8623c56-273a-4c95-8d83-95911a042be7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ad062154b8213d021c8c265aaf287d3a9335d0e4
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922874"
---
# <a name="ca1032-implement-standard-exception-constructors"></a>CA1032: Standart özel durum oluşturucularını uygulayın

|||
|-|-|
|TypeName|ImplementStandardExceptionConstructors|
|CheckId|CA1032|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir tür, <xref:System.Exception?displayProperty=fullName> gerekli oluşturucuların tümünü genişletir ancak bildirmiyor.

## <a name="rule-description"></a>Kural açıklaması

Özel durum türleri aşağıdaki üç Oluşturucu gerçekleştirmelidir:

- Ortak NewException ()

- Public NewException (dize)

- Public NewException (dize, özel durum)

Ayrıca, [Roslyn tabanlı FxCop çözümleyicileri](../code-quality/roslyn-analyzers-overview.md)yerine eski FxCop statik Kod analizini çalıştırıyorsanız, dördüncü bir oluşturucunun yokluğu de bir ihlal üretir:

- korumalı veya özel NewException (SerializationInfo, StreamingContext)

Yapıcıların tüm ayarlamasını sağlamaktaki başarısızlık, istisnalarla başa çıkmayı zorlaştırabilir. Örneğin, imzaya `NewException(string, Exception)` sahip Oluşturucu diğer özel durumların neden olduğu özel durumlar oluşturmak için kullanılır. Bu Oluşturucu olmadan, bu tür bir durumda hangi yönetilen kodun yapması gerektiği bir iç (iç içe) özel durumu içeren özel özel durumunuzun bir örneğini oluşturamaz ve oluşturamıyoruz.

İlk üç özel durum Oluşturucusu kurala göre ortaktır. Dördüncü Oluşturucu korumasız sınıflarda korunur ve korumalı sınıflarda özeldir. Daha fazla bilgi için bkz [. CA2229: Serileştirme oluşturucularını](../code-quality/ca2229-implement-serialization-constructors.md)uygulayın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini düzeltmek için, eksik oluşturucuları özel duruma ekleyin ve doğru erişilebilirliğe sahip olduklarından emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

İhlalin genel oluşturucular için farklı bir erişim düzeyi kullanmasından kaynaklanan bu kuraldan bir uyarıyı bastırmak güvenlidir. Ayrıca, taşınabilir bir sınıf kitaplığı (PCL) oluşturuyorsanız, `NewException(SerializationInfo, StreamingContext)` oluşturucunun uyarısını da bastırmak normaldir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kuralı ihlal eden bir özel durum türü ve doğru şekilde uygulanan bir özel durum türü içerir.

[!code-csharp[FxCop.Design.ExceptionMultipleCtors#1](../code-quality/codesnippet/CSharp/ca1032-implement-standard-exception-constructors_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

[CA2229 Serileştirme oluşturucularını Uygula](../code-quality/ca2229-implement-serialization-constructors.md)