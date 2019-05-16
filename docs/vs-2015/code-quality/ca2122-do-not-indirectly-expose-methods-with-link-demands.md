---
title: 'CA2122: Bağlantı talepleri olan yöntemleri dolaylı olarak açığa çıkarmayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2122
- DoNotIndirectlyExposeMethodsWithLinkDemands
helpviewer_keywords:
- DoNotIndirectlyExposeMethodsWithLinkDemands
- CA2122
ms.assetid: 3eda58e7-c6ec-41c3-8112-ae0841109c6a
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e0b173378194c099b2014093104f814f3454843d
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65687256"
---
# <a name="ca2122-do-not-indirectly-expose-methods-with-link-demands"></a>CA2122: Bağlantı talepleri olan metotları dolaylı olarak açığa çıkarmayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotIndirectlyExposeMethodsWithLinkDemands|
|CheckId|CA2122|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Ortak veya korumalı bir üyenin bir [bağlantı talepleri](https://msdn.microsoft.com/library/a33fd5f9-2de9-4653-a4f0-d9df25082c4d) ve herhangi bir güvenlik denetimi gerçekleştirmeyen üye tarafından çağrılır.

## <a name="rule-description"></a>Kural Tanımı
 Bağlantı talebi, yalnızca o anki çağırıcı izinlerini denetler. Üye ise `X` hiçbir güvenlik taleplerini çağıranlar ve kod gerekli izne kullanabilirsiniz olmadan bu bağlantı talebi tarafından çağıran korumalı çağrıları yapar `X` korunan üyesine erişmek için.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Güvenlik ekleme [veri ve modelleme](https://msdn.microsoft.com/library/8c37635d-e2c1-4b64-a258-61d9e87405e6) veya artık bağlantı talebi tarafından korunan üyesine güvenli erişim sağlar, böylece üyesine bağlantısını isteğe bağlı.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Güvenli bir şekilde bu kuraldan bir uyarıyı bastırmak için kodunuzu işlemleri veya yıkıcı bir şekilde kullanılabilir kaynaklara erişimi çağıranlarını tanımaz emin olmanız gerekir.

## <a name="example"></a>Örnek
 Aşağıdaki örnekler, kural ihlal eden bir kitaplık ve kitaplığın zayıflık gösteren bir uygulama gösterir. Örnek kitaplığı birlikte bu kuralı ihlal eden iki yöntem sunar. `EnvironmentSetting` Ortam değişkenlerini sınırsız erişim için bir bağlantı talebi tarafından güvenli yöntemi. `DomainInformation` Yöntemi çağırmadan önce hiçbir güvenlik taleplerini çağıranlarını yapar `EnvironmentSetting`.

 [!code-csharp[FxCop.Security.UnsecuredDoNotCall#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.UnsecuredDoNotCall/cs/FxCop.Security.UnsecuredDoNotCall.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki uygulama güvenli olmayan kitaplık üyesini çağırır.

 [!code-csharp[FxCop.Security.TestUnsecuredDoNot1#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.TestUnsecuredDoNot1/cs/FxCop.Security.TestUnsecuredDoNot1.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **Güvenli olmayan bir üye değeri: seattle.corp.contoso.com**
## <a name="see-also"></a>Ayrıca Bkz.
 [Güvenli kodlama yönergeleri](https://msdn.microsoft.com/library/4f882d94-262b-4494-b0a6-ba9ba1f5f177) [bağlantı talepleri](https://msdn.microsoft.com/library/a33fd5f9-2de9-4653-a4f0-d9df25082c4d) [veri ve modelleme](https://msdn.microsoft.com/library/8c37635d-e2c1-4b64-a258-61d9e87405e6)
