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
ms.openlocfilehash: dac1f5840f7a3c80cd5c5c6e3544ddcb301e3966
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55915809"
---
# <a name="ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute"></a>CA2139: Saydam metotlar HandleProcessCorruptingExceptions özniteliğini kullanamaz

|||
|-|-|
|TypeName|TransparentMethodsMustNotHandleProcessCorruptingExceptions|
|CheckId|CA2139|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Saydam bir yöntem ile işaretlenmiş <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliği.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural, saydam olan ve bir işlem kullanarak özel durumu bozan herhangi bir yöntemi tetikler <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliği. Özel durumu bozan bu işlem bir CLR 4.0 sürümü özel durum tür özel durumların sınıflandırılmasıdır <xref:System.AccessViolationException>. HandleProcessCorruptedStateExceptionsAttribute özniteliği, sadece kritik güvenlik yöntemleri tarafından kullanılır ve saydam bir yöntem uygulanırsa yoksayılır. İşlem bozulan özel durumları işlemek için bu yöntem güvenlik açısından kritik veya güvenlik güvenli kritik hale gelmelidir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için kaldırmak <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliği veya yöntemi işaretlemek <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Bu örnekte, saydam bir yöntem ile işaretlenmiş <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliği ve kuralı başarısız olur. Yöntemi de ile işaretlenmelidir <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği.

 [!code-csharp[FxCop.Security.CA2139.TransparentMethodsMustNotHandleProcessCorruptingExceptions#1](../code-quality/codesnippet/CSharp/ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute_1.cs)]