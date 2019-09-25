---
title: "CA1415: P-Invoke'ları doğru bildirin"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1415
- DeclarePInvokesCorrectly
helpviewer_keywords:
- CA1415
- DeclarePInvokesCorrectly
ms.assetid: 42a90796-0264-4460-bf97-2fb4a093dfdc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 99274abee2c05a1bd33e34c9eb02cc928c1b54b0
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234620"
---
# <a name="ca1415-declare-pinvokes-correctly"></a>CA1415: P/Invoke'ları doğru bildirin

|||
|-|-|
|TypeName|DeclarePInvokesCorrectly|
|CheckId|CA1415|
|Kategori|Microsoft. çalışabilirliği|
|Son değişiklik|Bölünmez olmayan-parametreyi bildiren P/Invoke derleme dışında görülemez. Parçalama-parametreyi bildiren P/Invoke, derleme dışında görünebilirler.|

## <a name="cause"></a>Sebep
Platform çağırma yöntemi yanlış bir şekilde bildirilmiştir.

## <a name="rule-description"></a>Kural açıklaması
Platform çağırma yöntemi yönetilmeyen koda erişir ve içindeki veya `Declare` <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] anahtar sözcüğü kullanılarak tanımlanır. Şu anda, bu kural çakışan bir yapı parametresine işaretçi olan Win32 işlevlerini hedefleyen platform çağırma yöntemi bildirimlerini arar ve karşılık gelen yönetilen parametre bir <xref:System.Threading.NativeOverlapped?displayProperty=fullName> yapıya işaretçi değildir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için platform çağırma yöntemini doğru bir şekilde bildirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ihlal eden ve kuralı karşılayan platform çağırma yöntemlerini gösterir.

[!code-csharp[FxCop.Interoperability.DeclarePInvokes#1](../code-quality/codesnippet/CSharp/ca1415-declare-p-invokes-correctly_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.
[Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)