---
title: 'CA2139: Saydam metotlar HandleProcessCorruptingExceptions özniteliğini kullanamaz'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2139
ms.assetid: 45a0328a-add7-40f9-8934-dff59beb02b3
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f6808c5e9b5d35ab6ec8d4012f08e15cba9a159d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920562"
---
# <a name="ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute"></a>CA2139: Saydam metotlar HandleProcessCorruptingExceptions özniteliğini kullanamaz

|||
|-|-|
|TypeName|TransparentMethodsMustNotHandleProcessCorruptingExceptions|
|CheckId|CA2139|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Saydam bir yöntem, <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliğiyle işaretlenir.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, saydam olan ve <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliği kullanarak bir işlem bozulmasını işlemeye çalışır olan herhangi bir yöntemi harekete geçirilir. İşlem bozulmayan özel durum, özel durumların <xref:System.AccessViolationException>CLR sürüm 4,0 özel durum sınıflandırmasıdır. HandleProcessCorruptedStateExceptionsAttribute özniteliği, sadece kritik güvenlik yöntemleri tarafından kullanılır ve saydam bir yöntem uygulanırsa yoksayılır. İşlem bozulmayan özel durumları işlemek için, bu yöntem güvenlik açısından kritik veya güvenli güvenlik açısından kritik hale gelmelidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliğini kaldırın veya yöntemi <xref:System.Security.SecurityCriticalAttribute> ya <xref:System.Security.SecuritySafeCriticalAttribute> da özniteliğiyle işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Bu örnekte, saydam bir yöntem <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliğiyle işaretlenir ve kuralı başarısız olur. <xref:System.Security.SecurityCriticalAttribute> Yöntemi<xref:System.Security.SecuritySafeCriticalAttribute> veya özniteliğiyle de işaretlenmiş olmalıdır.

[!code-csharp[FxCop.Security.CA2139.TransparentMethodsMustNotHandleProcessCorruptingExceptions#1](../code-quality/codesnippet/CSharp/ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute_1.cs)]