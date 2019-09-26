---
title: "CA2205: Win32 API'sinin yönetilen eşdeğerlerini kullanın"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- UseManagedEquivalentsOfWin32Api
- CA2205
helpviewer_keywords:
- UseManagedEquivalentsOfWin32Api
- CA2205
ms.assetid: 1c65ab59-3e50-4488-a727-3969c7f6cbe4
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: ad26dcbbbef5a34796ca0aa134653c3c9df5d763
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253265"
---
# <a name="ca2205-use-managed-equivalents-of-win32-api"></a>CA2205: Win32 API'sinin yönetilen eşdeğerlerini kullanın

|||
|-|-|
|TypeName|UseManagedEquivalentsOfWin32Api|
|CheckId|CA2205|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Platform çağırma yöntemi tanımlanmıştır ve .NET 'te eşdeğer işlevselliğe sahip bir yöntem vardır.

## <a name="rule-description"></a>Kural açıklaması

Bir platform çağırma yöntemi, yönetilmeyen bir DLL işlevini çağırmak için kullanılır ve <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName> özniteliği `Declare` veya Visual Basic anahtar sözcüğü kullanılarak tanımlanır. Yanlış tanımlanmış bir platform çağırma yöntemi, yanlış adlandırılmış bir işlev, parametre ve dönüş değeri veri türlerinin hatalı eşlemesi ve çağırma kuralı ve karakteri gibi yanlış alan belirtimleri nedeniyle çalışma zamanı özel durumlarına yol açabilir. kurmak. Varsa, daha basit ve yönetilmeyen yöntemi doğrudan çağırdığından, eşdeğer yönetilen yöntemi çağırmak daha basit ve daha az hataya açıktır. Platform çağırma yöntemini çağırmak, giderilmesi gereken ek güvenlik sorunlarına da yol açabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için yönetilmeyen işleve yapılan çağrıyı, yönetilen eşdeğeri çağrısıyla değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Önerilen değiştirme yöntemi gerekli işlevselliği sağlamıyorsa bu kuraldan bir uyarı gizleyin.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralı ihlal eden bir platform çağırma yöntemi tanımını gösterir. Ayrıca, platform çağırma yöntemine yapılan çağrılar ve eşdeğer yönetilen yöntem gösterilir.

[!code-csharp[FxCop.Usage.ManagedEquivalents#1](../code-quality/codesnippet/CSharp/ca2205-use-managed-equivalents-of-win32-api_1.cs)]
[!code-vb[FxCop.Usage.ManagedEquivalents#1](../code-quality/codesnippet/VisualBasic/ca2205-use-managed-equivalents-of-win32-api_1.vb)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1404 P/Invoke sonrasında GetLastError 'yi çağırın](../code-quality/ca1404-call-getlasterror-immediately-after-p-invoke.md)
- [CA1060 P/Invoke öğesini NativeMethods sınıfına taşı](../code-quality/ca1060-move-p-invokes-to-nativemethods-class.md)
- [CA1400 P/Invoke giriş noktaları bulunmalıdır](../code-quality/ca1400-p-invoke-entry-points-should-exist.md)
- [CA1401 P/Invoke görünür olmamalıdır](../code-quality/ca1401-p-invokes-should-not-be-visible.md)
- [CA2101 P/Invoke dize bağımsız değişkenleri için sıralama belirtin](../code-quality/ca2101-specify-marshaling-for-p-invoke-string-arguments.md)