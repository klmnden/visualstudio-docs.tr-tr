---
title: 'CA2139: Saydam yöntemler HandleProcessCorruptingExceptions özniteliğini kullanamaz'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2139
ms.assetid: 45a0328a-add7-40f9-8934-dff59beb02b3
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 48f5e0649b9d59994098622d00c3cf23772a9d81
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53987751"
---
# <a name="ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute"></a>CA2139: Saydam yöntemler HandleProcessCorruptingExceptions özniteliğini kullanamaz

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