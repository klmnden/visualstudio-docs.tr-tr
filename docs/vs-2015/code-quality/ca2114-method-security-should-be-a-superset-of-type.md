---
title: 'CA2114: Yöntem güvenliği türün bir üst kümesi olmalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- MethodSecurityShouldBeASupersetOfType
- CA2114
helpviewer_keywords:
- CA2114
- MethodSecurityShouldBeASupersetOfType
ms.assetid: 663f7aa4-8be5-4bd5-be92-4e9444f07077
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b1a360ee4ad35fd48a46f6d866912a05a584a54c
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65687311"
---
# <a name="ca2114-method-security-should-be-a-superset-of-type"></a>CA2114: Metot güvenliği türün bir üst kümesi olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MethodSecurityShouldBeASupersetOfType|
|CheckId|CA2114|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bildirim temelli güvenlik türünde yöntemlerinden birine sahip aynı güvenlik eylemi için bildirime dayalı güvenlik ve güvenlik eylem [bağlantı talepleri](https://msdn.microsoft.com/library/a33fd5f9-2de9-4653-a4f0-d9df25082c4d) veya [devralma taleplerini](https://msdn.microsoft.com/28b9adbb-8f08-4f10-b856-dbf59eb932d9)ve izinleri işaretli tür tarafından yöntemi tarafından iade izinler kümesini değildir.

## <a name="rule-description"></a>Kural Tanımı
 Hem yöntem düzeyine hem de tür düzeyine bir bildirim temelli güvenlik aynı eylem için bir yöntem olmamalıdır. İki denetimleri birleştirilmez; yöntem düzeyi isteğe uygulanır. Örneğin, bir tür izin talep ederse `X`, ve yöntemlerinden birini talepleri izni `Y`, kod izni yok `X` metodunu yürütmek için.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Her iki eylem gerekli olduğundan emin olmak için kodunuzu gözden geçirin. Her iki eylem gerekiyorsa, yöntem düzeyi eylem tür düzeyindeki güvenlik içerdiğinden emin olun. Örneğin türüne izin talep ederse `X`, ve onun yöntemi de izin talep gerekir `Y`, yöntemi açıkça talep `X` ve `Y`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Yöntem türü tarafından belirtilen güvenliği gerektirmiyorsa, bu kuraldan bir uyarıyı bastırmak güvenlidir. Ancak, sıradan bir senaryo değildir ve dikkatli bir tasarım incelemesi için bir gereksinimi olduğunu gösteriyor olabilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bu kuralın ihlali tehlikeleri göstermek için ortam izinleri kullanır. Bu örnekte, uygulama kodu türü tarafından gerekli izni reddetme önce güvenli türün bir örneğini oluşturur. Tehdit gerçek dünya senaryosunda, uygulama nesnesinin bir örneği elde etmek için başka bir yolu olması gerekir.

 Aşağıdaki örnekte, kitaplık taleplerini yazma izni bir tür için ve bir yöntem için okuma izni.

 [!code-csharp[FxCop.Security.MethodLevelSecurity#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.MethodLevelSecurity/cs/FxCop.Security.MethodLevelSecurity.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki uygulama kodu, güvenlik gereksinimleri karşılamıyor olsa bile yöntemi çağırarak Kitaplığı'nın güvenlik açığı gösterir.

 [!code-csharp[FxCop.Security.TestMethodLevelSecurity#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.TestMethodLevelSecurity/cs/FxCop.Security.TestMethodLevelSecurity.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **[Tüm izinleri] Kişisel bilgileri: 6/16/1964 12:00:00 AM'den**
 **[yazma izni (talep türüne göre)] kişisel bilgileri: 6/16/1964 12:00:00 AM'den**
 **[(yöntemi tarafından talep) okuma izni yok], kişisel bilgi erişilemedi: İstek başarısız oldu.**
## <a name="see-also"></a>Ayrıca Bkz.
 [Güvenli kodlama yönergeleri](https://msdn.microsoft.com/library/4f882d94-262b-4494-b0a6-ba9ba1f5f177) [devralma taleplerini](https://msdn.microsoft.com/28b9adbb-8f08-4f10-b856-dbf59eb932d9) [bağlantı talepleri](https://msdn.microsoft.com/library/a33fd5f9-2de9-4653-a4f0-d9df25082c4d) [veri ve modelleme](https://msdn.microsoft.com/library/8c37635d-e2c1-4b64-a258-61d9e87405e6)
