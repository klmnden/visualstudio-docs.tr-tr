---
title: "CA1404: P-Invoke'un ardından hemen GetLastError çağırın"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CallGetLastErrorImmediatelyAfterPInvoke
- CA1404
helpviewer_keywords:
- CallGetLastErrorImmediatelyAfterPInvoke
- CA1404
ms.assetid: 52ae9eff-50f9-4b2f-8039-ca7e49fba88e
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: ab789e578dd8603f604cdb00aa5d236250d13670
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235049"
---
# <a name="ca1404-call-getlasterror-immediately-after-pinvoke"></a>CA1404: P/Invoke ardından hemen GetLastError çağırın

|||
|-|-|
|TypeName|CallGetLastErrorImmediatelyAfterPInvoke|
|CheckId|CA1404|
|Kategori|Microsoft. çalışabilirliği|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

<xref:System.Runtime.InteropServices.Marshal.GetLastWin32Error%2A?displayProperty=fullName> Yöntemine veya eşdeğer Win32 `GetLastError` işlevine çağrı yapılır ve hemen önce gelen çağrı bir platform çağırma yöntemine değildir.

## <a name="rule-description"></a>Kural açıklaması
Platform çağırma yöntemi yönetilmeyen koda erişir ve içinde `Declare` [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] veya <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName> özniteliğinde anahtar sözcüğü kullanılarak tanımlanır. Genellikle, hata durumunda yönetilmeyen işlevler, hata ile ilişkili `SetLastError` bir hata kodu ayarlamak için Win32 işlevini çağırır. Başarısız işlevi çağıran, hata kodunu almak ve hatanın `GetLastError` nedenini öğrenmek için Win32 işlevini çağırır. Hata kodu iş parçacığı başına temelinde tutulur ve sonraki çağrısıyla `SetLastError`üzerine yazılır. Başarısız platform çağırma yöntemine yapılan çağrıdan sonra, yönetilen kod <xref:System.Runtime.InteropServices.Marshal.GetLastWin32Error%2A> yöntemini çağırarak hata kodunu alabilir. Hata kodu diğer yönetilen sınıf kitaplığı metotlarından gelen iç çağrılar tarafından üzerine yazılabildiğinden, `GetLastError` veya <xref:System.Runtime.InteropServices.Marshal.GetLastWin32Error%2A> yöntemi platform çağırma yöntemi çağrısından hemen sonra çağrılmalıdır.

Kural, platform çağırma yöntemine yapılan çağrı ve çağrısı <xref:System.Runtime.InteropServices.Marshal.GetLastWin32Error%2A>arasında gerçekleştiklerinde, aşağıdaki yönetilen üyelere yapılan çağrıları yoksayar. Bu Üyeler hata kodunu değiştirmez ve bazı platform çağırma yöntemi çağrılarının başarısını belirlemek için faydalıdır.

- <xref:System.IntPtr.Zero?displayProperty=fullName>

- <xref:System.IntPtr.op_Equality%2A?displayProperty=fullName>

- <xref:System.IntPtr.op_Inequality%2A?displayProperty=fullName>

- <xref:System.Runtime.InteropServices.SafeHandle.IsInvalid%2A?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için çağrıyı, platform çağırma yöntemine yapılan <xref:System.Runtime.InteropServices.Marshal.GetLastWin32Error%2A> çağrıyı hemen takip eden öğesine taşıyın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Platform çağırma yöntemi çağrısı ve <xref:System.Runtime.InteropServices.Marshal.GetLastWin32Error%2A> Yöntem çağrısı arasındaki kod, açıkça veya örtük olarak hata kodunun değişmesine neden değilse, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ve kuralını karşılayan bir yöntemi ihlal eden bir yöntemi gösterir.

[!code-vb[FxCop.Interoperability.LastErrorPInvoke#1](../code-quality/codesnippet/VisualBasic/ca1404-call-getlasterror-immediately-after-p-invoke_1.vb)]
[!code-csharp[FxCop.Interoperability.LastErrorPInvoke#1](../code-quality/codesnippet/CSharp/ca1404-call-getlasterror-immediately-after-p-invoke_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1060 P/Invoke öğesini NativeMethods sınıfına taşı](../code-quality/ca1060-move-p-invokes-to-nativemethods-class.md)

[CA1400 P/Invoke giriş noktaları bulunmalıdır](../code-quality/ca1400-p-invoke-entry-points-should-exist.md)

[CA1401 P/Invoke görünür olmamalıdır](../code-quality/ca1401-p-invokes-should-not-be-visible.md)

[CA2101 P/Invoke dize bağımsız değişkenleri için sıralama belirtin](../code-quality/ca2101-specify-marshaling-for-p-invoke-string-arguments.md)

[CA2205 Win32 API yönetilen eşdeğerlerini kullanın](../code-quality/ca2205-use-managed-equivalents-of-win32-api.md)