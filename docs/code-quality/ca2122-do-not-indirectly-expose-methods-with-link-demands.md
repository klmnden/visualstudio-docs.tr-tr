---
title: 'CA2122: Bağlantı talepleri olan metotları dolaylı olarak açığa çıkarmayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2122
- DoNotIndirectlyExposeMethodsWithLinkDemands
helpviewer_keywords:
- DoNotIndirectlyExposeMethodsWithLinkDemands
- CA2122
ms.assetid: 3eda58e7-c6ec-41c3-8112-ae0841109c6a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 340d8f0a45506f15cdd9281f7ecda463583c3144
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920819"
---
# <a name="ca2122-do-not-indirectly-expose-methods-with-link-demands"></a>CA2122: Bağlantı talepleri olan metotları dolaylı olarak açığa çıkarmayın

|||
|-|-|
|TypeName|DoNotIndirectlyExposeMethodsWithLinkDemands|
|CheckId|CA2122|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir üyenin [bağlantı talepleri](/dotnet/framework/misc/link-demands) vardır ve herhangi bir güvenlik denetimi gerçekleştirmediğinden bir üye tarafından çağırılır.

## <a name="rule-description"></a>Kural açıklaması
Bağlantı talebi, yalnızca o anki çağırıcı izinlerini denetler. Bir üye `X` , arayanlara güvenlik talebi yapıyorsa ve bir bağlantı talebi tarafından korunan kodu çağırırsa, gerekli izni olmayan bir çağıran, korunan üyeye erişmek için kullanabilir `X` .

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bir güvenlik [verileri ekleyin ve](/dotnet/framework/data/index) isteğe bağlı olarak, bağlantıya talep korumalı üyeye güvenli olmayan erişim sağlamaz.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı güvenle bastırmak için, kodunuzun çağıranlar için bir bozucu şekilde kullanılabilecek işlemlere veya kaynaklara erişimini vermediğinden emin olmanız gerekir.

## <a name="example-1"></a>Örnek 1
Aşağıdaki örneklerde, kuralı ihlal eden bir kitaplık ve kitaplığın zayıflılığını gösteren bir uygulama gösterilmektedir. Örnek kitaplık, birlikte kuralı ihlal eden iki yöntem sağlar. Yöntemi `EnvironmentSetting` , ortam değişkenlerine sınırsız erişim talebi ile korunmuş olur. `DomainInformation` Yöntemi çağrı`EnvironmentSetting`yapmadan önce arayanlara güvenlik talebi yapmaz.

[!code-csharp[FxCop.Security.UnsecuredDoNotCall#1](../code-quality/codesnippet/CSharp/ca2122-do-not-indirectly-expose-methods-with-link-demands_1.cs)]

## <a name="example-2"></a>Örnek 2
Aşağıdaki uygulama, güvenli olmayan kitaplık üyesini çağırır.

[!code-csharp[FxCop.Security.TestUnsecuredDoNot1#1](../code-quality/codesnippet/CSharp/ca2122-do-not-indirectly-expose-methods-with-link-demands_2.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
*Value from unsecured member: seattle.corp.contoso.com
```

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
- [Bağlantı talepleri](/dotnet/framework/misc/link-demands)
- [Veri ve Modelleme](/dotnet/framework/data/index)