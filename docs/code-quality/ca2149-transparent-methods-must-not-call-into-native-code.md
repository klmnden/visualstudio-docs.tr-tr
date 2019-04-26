---
title: 'CA2149: Saydam metotlar yerel kod içine çağırmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2149
ms.assetid: 28951bd7-f3db-4871-99aa-bad68d1ead80
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 462ddeebba217e3a129736d1532aeec6b106d0cb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62542150"
---
# <a name="ca2149-transparent-methods-must-not-call-into-native-code"></a>CA2149: Saydam metotlar yerel kod içine çağırmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsMustNotCallNativeCode|
|CheckId|CA2149|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir yöntem aracılığıyla bir metot taslağı P/Invoke gibi yerel bir işlevi çağırır.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural doğrudan yerel kod içine, örneğin, bir P/Invoke çağıran herhangi bir saydam yöntemi tetikler. Bu kural ihlalleri neden bir <xref:System.MethodAccessException> Düzey 2 saydamlık modeli ve tam bir talep <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> düzey 1 saydamlık modeli içindeki.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için yerel kod ile yöntemi işaretlemek <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 [!code-csharp[FxCop.Security.CA2149.TransparentMethodsMustNotCallNativeCode#1](../code-quality/codesnippet/CSharp/ca2149-transparent-methods-must-not-call-into-native-code_1.cs)]