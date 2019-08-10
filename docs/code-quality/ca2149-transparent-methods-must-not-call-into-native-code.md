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
ms.openlocfilehash: 725bf599d8d13d345767f5af4d38db619263c23d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920378"
---
# <a name="ca2149-transparent-methods-must-not-call-into-native-code"></a>CA2149: Saydam metotlar yerel kod içine çağırmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsMustNotCallNativeCode|
|CheckId|CA2149|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Yöntemi, P/Invoke gibi bir yöntem saplaması aracılığıyla yerel bir işlevi çağırır.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, örneğin bir P/Invoke aracılığıyla doğrudan yerel koda çağıran herhangi bir saydam yöntemde ateşlenir. Bu kuralın ihlalleri, düzey 2 saydamlık <xref:System.MethodAccessException> modelinde bir öğesine ve düzey 1 saydamlık modelinde için <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> tam talebe yol açabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle yerel kod çağıran yöntemi işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
[!code-csharp[FxCop.Security.CA2149.TransparentMethodsMustNotCallNativeCode#1](../code-quality/codesnippet/CSharp/ca2149-transparent-methods-must-not-call-into-native-code_1.cs)]