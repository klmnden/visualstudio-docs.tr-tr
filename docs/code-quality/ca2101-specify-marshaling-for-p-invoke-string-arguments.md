---
title: 'CA2101: P-Invoke dize bağımsız değişkenleri için sıralama belirtin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- SpecifyMarshalingForPInvokeStringArguments
- CA2101
helpviewer_keywords:
- CA2101
- SpecifyMarshalingForPInvokeStringArguments
ms.assetid: 9d1abfc3-d320-41e0-9f6e-60cefe6ffe1b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 52f7e6e0a09bf4b6b11d5cbdab3ab86cfa79724c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971526"
---
# <a name="ca2101-specify-marshaling-for-pinvoke-string-arguments"></a>CA2101: P/Invoke dize bağımsız değişkenleri için sıralama belirtin

|||
|-|-|
|TypeName|SpecifyMarshalingForPInvokeStringArguments|
|CheckId|CA2101|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir platform çağırma üyesi kısmen güvenilmeyen çağrıcılara izin verir. bir dize parametresine sahiptir ve dize açıkça sıralanmaz.

## <a name="rule-description"></a>Kural açıklaması
 ANSI-Unicode dönüştürme yaptığınızda, tüm Unicode karakterleri belirli bir ANSI kod sayfasında temsil edilebilmesi mümkündür. *En iyi uyan eşlemeyi* temsil edilemeyen bir karakter için bir karakter değiştirerek bu sorunu çözmek çalışır. Bu özelliğin kullanımı, seçilen karakter denetleyemeyeceğiniz için olası bir güvenlik açığına neden olabilir. Örneğin, kötü amaçlı kod gibi dosya sistemi için özel karakterler dönüştürülen bir belirli kod sayfasında bulunan karakter içeren bir Unicode dize kasıtlı olarak oluşturabilirsiniz '..' veya '/'. Ayrıca dize için ANSI dönüştürülmeden önce özel karakterler için güvenlik denetimleri sık gerçekleşmesini unutmayın.

 En iyi uyan eşlemeyi WChar MB için yönetilmeyen dönüştürme için varsayılandır. En iyi uyan eşlemeyi açıkça devre dışı sürece kodunuzun Bu sorun nedeniyle bir açıklardan güvenlik açığı içerebilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için açıkça dizesi veri türleriyle hazırlama.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal ediyor ve ihlali gidermek nasıl daha sonra gösterir bir yöntemi gösterir.

 [!code-csharp[FxCop.Security.PinvokeAnsiUnicode#1](../code-quality/codesnippet/CSharp/ca2101-specify-marshaling-for-p-invoke-string-arguments_1.cs)]