---
title: 'CA1064: Özel durumlar genel olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1064
- ExceptionsShouldBePublic
helpviewer_keywords:
- ExceptionsShouldBePublic
- CA1064
ms.assetid: 83eb224c-2456-4368-acf4-3b3378e67759
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0ffc12d8d047be1bb13fcac133a61b047152ce3d
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235328"
---
# <a name="ca1064-exceptions-should-be-public"></a>CA1064: Özel durumlar genel olmalıdır

|||
|-|-|
|TypeName|ExceptionsShouldBePublic|
|CheckId|CA1064|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Genel olmayan bir özel durum doğrudan, <xref:System.Exception> <xref:System.SystemException>, veya <xref:System.ApplicationException>' den türetilir.

## <a name="rule-description"></a>Kural açıklaması
İç özel durum yalnızca kendi iç kapsamı içinde görülebilir. İç kapsam dışında kalan özel durumlardan sonra, sadece basit istisnalar istisna yakalamak için kullanılabilir. İç özel durum öğesinden devralınan <xref:System.Exception>, <xref:System.SystemException>, veya <xref:System.ApplicationException>, harici kod özel durum ne olduğunu bilmek yeterli bilgiye sahip değildir.

Ancak, kodun daha sonra iç özel durum için temel olarak kullanıldığı ortak bir özel durum varsa, kodun daha fazla çıkış için temel özel durumla akıllı bir şey yapabildiğini varsaymak mantıklı olur. Genel özel durum, veya <xref:System.Exception> <xref:System.ApplicationException>tarafından <xref:System.SystemException>sağlandıkından daha fazla bilgiye sahip olacaktır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Özel durumu genel yapın veya iç özel durumu, <xref:System.Exception> <xref:System.SystemException>veya <xref:System.ApplicationException>olmayan genel bir özel durumdan türetebilirsiniz.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Özel özel durumun kendi iç kapsamı içinde yakalanıp tüm durumlarda emin değilseniz, bu kuraldan bir ileti gizleyin.

## <a name="example"></a>Örnek
Özel durum sınıfı doğrudan özel durumdan türetildiğinden ve iç iş olduğundan, bu kural ilk örnek yöntemi ' FirstCustomException ' de ateşlenir. Sınıf, doğrudan özel durumdan türediğinden, sınıf genel olarak bildirildiği için, bu kural SecondCustomException sınıfında başlatılmıyor. Üçüncü sınıf aynı zamanda, <xref:System.Exception?displayProperty=fullName> <xref:System.SystemException?displayProperty=fullName>veya <xref:System.ApplicationException?displayProperty=fullName>' den türemediği için kuralı tetiklemez.

[!code-csharp[FxCop.Design.ExceptionsShouldBePublic.CA1064#1](../code-quality/codesnippet/CSharp/ca1064-exceptions-should-be-public_1.cs)]
