---
title: 'CA2138: Saydam yöntemler SuppressUnmanagedCodeSecurity özniteliğine sahip yöntemleri değil çağırmalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2138
ms.assetid: a14c4d32-f079-4f3a-956c-a1657cde0f66
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 4e9a9e10f928efe6bcff6fb3d49c1b1cd7b1bd1c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68154291"
---
# <a name="ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute"></a>CA2138: Saydam metotlar SuppressUnmanagedCodeSecurity özniteliğine sahip metotları çağırmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods|
|CheckId|CA2138|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Saydam güvenlik yöntemi ile işaretlenmiş bir yöntemi çağıran <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliği.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural tetikler kullanarak örneğin, yerel kod içinde doğrudan çağıran herhangi bir saydam yöntem üzerinde bir P/Invoke aracılığıyla (platform çağırma) çağırın. İle işaretlenmiş P/Invoke ve COM birlikte çalışma yöntemlerini <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliği karşı çağıran Metoda yapılan bir LinkDemand sonuçlanır. Güvenliği saydam kod LinkDemands gerçekleştiremiyor çünkü kod da SuppressUnmanagedCodeSecurity özniteliği ile işaretlenmiş yöntemler veya SuppressUnmanagedCodeSecurity özniteliği ile işaretlenmiş sınıf yöntemlerini çağıramazsınız. Yöntemi başarısız olur ya da isteğe bağlı tam bir talebi karşılamak için dönüştürülür.

 Bu kural ihlalleri neden bir <xref:System.MethodAccessException> için talepte bulunur ve Düzey 2 güvenlik saydamlık modeli içindeki <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> düzey 1 saydamlık modeli içindeki.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için kaldırmak <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute> özniteliği ve yöntemi işaretlemek <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 [!code-csharp[FxCop.Security.CA2138.TransparentMethodsMustNotCallSuppressUnmanagedCodeSecurityMethods#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2138.transparentmethodsmustnotcallsuppressunmanagedcodesecuritymethods/cs/ca2138.cs#1)]
