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
ms.openlocfilehash: e9746119c746679817076c86e3d5a9080cec30d9
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66744694"
---
# <a name="ca1031-do-not-catch-general-exception-types"></a>CA1031: Genel özel durum türlerini yakalamayın

|||
|-|-|
|TypeName|DoNotCatchGeneralExceptionTypes|
|CheckId|CA1031|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Genel bir özel durum gibi <xref:System.Exception?displayProperty=fullName> veya <xref:System.SystemException?displayProperty=fullName> , yakalanan bir `catch` deyimi veya bir genel bir catch yan tümcesi gibi `catch()` kullanılır.

## <a name="rule-description"></a>Kural açıklaması
 Genel özel durum yakalanmamalı.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için daha özel istisnaları yakalayın veya son ifade olarak genel özel durumu yeniden `catch` blok.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Genel özel durum türlerini yakalamak çalışma zamanı sorunlarını kitaplık kullanıcısından gizleyebilir ve hata ayıklama daha zor hale getirebilir.

> [!NOTE]
> .NET Framework 4 ile başlayarak, ortak dil çalışma zamanı (CLR) artık erişim ihlali gibi yönetilen kod ve işletim sistemi ortaya bozuk durum özel durumları sunuyor [!INCLUDE[TLA#tla_mswin](../code-quality/includes/tlasharptla_mswin_md.md)], yönetilen kod tarafından işlenecek. Derleme bir uygulama .NET Framework 4 veya sonraki sürümler için istediğiniz ve bozuk durumda özel durumların işlenmesiyle korumak, uygulayabilirsiniz <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> öznitelik bozuk durum özel durumu işleyen yöntem.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür ve doğru bir şekilde uygulayan bir tür gösterir `catch` blok.

 [!code-cpp[FxCop.Design.ExceptionAndSystemException#1](../code-quality/codesnippet/CPP/ca1031-do-not-catch-general-exception-types_1.cpp)]
 [!code-vb[FxCop.Design.ExceptionAndSystemException#1](../code-quality/codesnippet/VisualBasic/ca1031-do-not-catch-general-exception-types_1.vb)]
 [!code-csharp[FxCop.Design.ExceptionAndSystemException#1](../code-quality/codesnippet/CSharp/ca1031-do-not-catch-general-exception-types_1.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2200: Yığın ayrıntılarını korumak için yeniden fırlatma](../code-quality/ca2200-rethrow-to-preserve-stack-details.md)