---
title: 'CA1031: Genel özel durum türlerini yakalamayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1031
- DoNotCatchGeneralExceptionTypes
helpviewer_keywords:
- CA1031
- DoNotCatchGeneralExceptionTypes
ms.assetid: cbc283ae-2a46-4ec0-940e-85aa189b118f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c1dc1e5ed18ddcd42d42c96f3f853808c58ade48
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236061"
---
# <a name="ca1031-do-not-catch-general-exception-types"></a>CA1031: Genel özel durum türlerini yakalamayın

|||
|-|-|
|TypeName|DoNotCatchGeneralExceptionTypes|
|CheckId|CA1031|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
<xref:System.Exception?displayProperty=fullName> `catch()` Ya dagibigenelbirözeldurumyadagibibirgenelcatchyantümcesikullanılır.<xref:System.SystemException?displayProperty=fullName> `catch`

## <a name="rule-description"></a>Kural açıklaması
Genel özel durum yakalanmamalı.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, daha belirli bir özel durumu yakalayın veya `catch` bloktaki son deyimle genel özel durumu yeniden oluşturun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın. Genel özel durum türlerini yakalama, kitaplık kullanıcısının çalışma zamanı sorunlarını gizleyebilir ve hata ayıklamayı daha zor hale getirebilirsiniz.

> [!NOTE]
> .NET Framework 4 ' te başlayarak, ortak dil çalışma zamanı (CLR) artık işletim sisteminde oluşan bozulmuş durum özel durumlarını ve yönetilen kod tarafından işlenmek üzere, içindeki [!INCLUDE[TLA#tla_mswin](../code-quality/includes/tlasharptla_mswin_md.md)]erişim ihlalleri gibi yönetilen kodu teslim eder. .NET Framework 4 veya sonraki sürümlerde bir uygulama derlemek ve bozulmuş durum özel durumlarının işlenmesini sürdürmek istiyorsanız, <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliği bozuk durum özel durumunu işleyen yönteme uygulayabilirsiniz.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralı ihlal eden bir türü ve `catch` bloğu doğru bir şekilde uygulayan bir türü gösterir.

[!code-cpp[FxCop.Design.ExceptionAndSystemException#1](../code-quality/codesnippet/CPP/ca1031-do-not-catch-general-exception-types_1.cpp)]
[!code-vb[FxCop.Design.ExceptionAndSystemException#1](../code-quality/codesnippet/VisualBasic/ca1031-do-not-catch-general-exception-types_1.vb)]
[!code-csharp[FxCop.Design.ExceptionAndSystemException#1](../code-quality/codesnippet/CSharp/ca1031-do-not-catch-general-exception-types_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA2200 Yığın ayrıntılarını korumak için yeniden throw](../code-quality/ca2200-rethrow-to-preserve-stack-details.md)