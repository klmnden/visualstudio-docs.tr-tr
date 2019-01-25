---
title: 'CA2101: P-Invoke dize bağımsız değişkenleri için hazırlama belirtin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- SpecifyMarshalingForPInvokeStringArguments
- CA2101
helpviewer_keywords:
- CA2101
- SpecifyMarshalingForPInvokeStringArguments
ms.assetid: 9d1abfc3-d320-41e0-9f6e-60cefe6ffe1b
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 11916609f2efa9c0b6e208548ba51795bd276015
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764079"
---
# <a name="ca2101-specify-marshaling-for-pinvoke-string-arguments"></a>CA2101: P/Invoke dize bağımsız değişkenleri için sıralama belirtin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|SpecifyMarshalingForPInvokeStringArguments|
|CheckId|CA2101|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir platform çağırma üyesi kısmen güvenilmeyen çağrıcılara izin verir. bir dize parametresine sahiptir ve dize açıkça sıralanmaz.

## <a name="rule-description"></a>Kural Tanımı
 ANSI-Unicode dönüştürme yaptığınızda, tüm Unicode karakterleri belirli bir ANSI kod sayfasında temsil edilebilmesi mümkündür. *En iyi uyan eşlemeyi* temsil edilemeyen bir karakter için bir karakter değiştirerek bu sorunu çözmek çalışır. Bu özelliğin kullanımı, seçilen karakter denetleyemeyeceğiniz için olası bir güvenlik açığına neden olabilir. Örneğin, kötü amaçlı kod gibi dosya sistemi için özel karakterler dönüştürülen bir belirli kod sayfasında bulunan karakter içeren bir Unicode dize kasıtlı olarak oluşturabilirsiniz '..' veya '/'. Ayrıca dize için ANSI dönüştürülmeden önce özel karakterler için güvenlik denetimleri sık gerçekleşmesini unutmayın.

 En iyi uyan eşlemeyi WChar MB için yönetilmeyen dönüştürme için varsayılandır. En iyi uyan eşlemeyi açıkça devre dışı sürece kodunuzun Bu sorun nedeniyle bir açıklardan güvenlik açığı içerebilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için açıkça dizesi veri türleriyle hazırlama.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal ediyor ve ihlali gidermek nasıl daha sonra gösterir bir yöntemi gösterir.

 [!code-csharp[FxCop.Security.PinvokeAnsiUnicode#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.PinvokeAnsiUnicode/cs/FxCop.Security.PinvokeAnsiUnicode.cs#1)]
