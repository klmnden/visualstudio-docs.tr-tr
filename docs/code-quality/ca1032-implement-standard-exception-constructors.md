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
ms.openlocfilehash: 7baf13eb9125b273ad8fb1265a65eb7b053238a1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62779130"
---
# <a name="ca1032-implement-standard-exception-constructors"></a>CA1032: Standart özel durum oluşturucularını uygulayın

|||
|-|-|
|TypeName|ImplementStandardExceptionConstructors|
|CheckId|CA1032|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir türü genişleten <xref:System.Exception?displayProperty=fullName> gerekli tüm oluşturucular değil ancak.

## <a name="rule-description"></a>Kural açıklaması

Özel durum türleri, aşağıdaki üç oluşturucular uygulamanız gerekir:

- Genel NewException()

- Genel NewException(string)

- Genel NewException (dize, özel durum)

Eski FxCop statik kod analizi olarak çalıştırıyorsanız, ayrıca, çalışmanın aksine [Roslyn tabanlı FxCop Çözümleyicileri](../code-quality/roslyn-analyzers-overview.md), dördüncü Oluşturucu olmaması, aynı zamanda bir ihlali oluşturur:

- korumalı veya özel NewException (SerializationInfo, StreamingContext)

Yapıcıların tüm ayarlamasını sağlamaktaki başarısızlık, istisnalarla başa çıkmayı zorlaştırabilir. Örneğin, bir imzaya sahip Oluşturucu `NewException(string, Exception)` diğer özel durumların neden olduğu bir özel durum oluşturmak için kullanılır. Bu oluşturucu, oluşturabilir ve böyle bir durumda hangi yönetilen kod yapmalısınız olan bir iç (yuvalanmış) özel içeren, özel durum örneği harekete.

Kural gereği, ilk üç özel durum oluşturucuları ortaktır. Dördüncü Oluşturucu, mühürsüz sınıflar olarak korumalı ve korumalı sınıflardaki özel. Daha fazla bilgi için [CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için eksik oluşturucular özel durumu ekleyin ve doğru erişilebilirlik sahip olduğunuzdan emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Genel oluşturucular için farklı erişim düzeyi kullanarak ihlali neden olduğunda bu kuraldan bir uyarıyı bastırmak güvenlidir. Ayrıca, uyarı için uygun olup `NewException(SerializationInfo, StreamingContext)` taşınabilir sınıf kitaplığı (PCL) derliyorsanız Oluşturucusu.

## <a name="example"></a>Örnek

Aşağıdaki örnek bu kuralı ihlal eden bir özel durum türünü ve doğru bir şekilde uygulandığından bir özel durum türü içerir.

[!code-csharp[FxCop.Design.ExceptionMultipleCtors#1](../code-quality/codesnippet/CSharp/ca1032-implement-standard-exception-constructors_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

[CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)