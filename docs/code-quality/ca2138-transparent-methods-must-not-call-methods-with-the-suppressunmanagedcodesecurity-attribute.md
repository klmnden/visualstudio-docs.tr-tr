---
title: 'CA2138: Saydam metotlar SuppressUnmanagedCodeSecurity özniteliğine sahip metotları çağırmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2138
ms.assetid: a14c4d32-f079-4f3a-956c-a1657cde0f66
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 2c211ac7c0e7e8793d8bae6d24753716bec0d12c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54970454"
---
# <a name="ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute"></a>CA2138: Saydam metotlar SuppressUnmanagedCodeSecurity özniteliğine sahip metotları çağırmamalıdır

|||
|-|-|
|TypeName|TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods|
|CheckId|CA2138|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Saydam güvenlik yöntemi ile işaretlenmiş bir yöntemi çağıran <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliği.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural tetikler P/Invoke'ı kullanarak örneğin, yerel kod içinde doğrudan çağıran herhangi bir saydam yöntemi (platform çağırma) çağırın. İle işaretlenmiş P/Invoke ve COM birlikte çalışma yöntemlerini <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliği karşı çağıran Metoda yapılan bir LinkDemand sonuçlanır. Güvenliği saydam kod LinkDemands gerçekleştiremiyor çünkü kod da SuppressUnmanagedCodeSecurity özniteliği ile işaretlenmiş yöntemler veya SuppressUnmanagedCodeSecurity özniteliği ile işaretlenmiş sınıf yöntemlerini çağıramazsınız. Yöntemi başarısız olur ya da isteğe bağlı tam bir talebi karşılamak için dönüştürülür.

 Bu kural ihlalleri neden bir <xref:System.MethodAccessException> için talepte bulunur ve Düzey 2 güvenlik saydamlık modeli içindeki <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> düzey 1 saydamlık modeli içindeki.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için kaldırmak <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliği ve yöntemi işaretlemek <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 [!code-csharp[FxCop.Security.CA2138.TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods#1](../code-quality/codesnippet/CSharp/ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute_1.cs)]