---
title: 'CA1901: P-Invoke bildirimleri taşınabilir olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1901
- PInvokeDeclarationsShouldBePortable
helpviewer_keywords:
- CA1901
- PInvokeDeclarationsShouldBePortable
ms.assetid: 90361812-55ca-47f7-bce9-b8775d3b8803
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d878572c4391805773a9a711ee88e7b58f507c65
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233291"
---
# <a name="ca1901-pinvoke-declarations-should-be-portable"></a>CA1901: P/Invoke bildirimleri taşınabilir olmalıdır

|||
|-|-|
|TypeName|PInvokeDeclarationsShouldBePortable|
|CheckId|CA1901|
|Kategori|Microsoft. taşınabilirlik|
|Son değişiklik|Parçalama-P/Invoke derlemenin dışında görünüyorsa. Bölünmez olmayan-P/Invoke derlemenin dışında görünür değilse.|

## <a name="cause"></a>Sebep
Bu kural, her parametrenin boyutunu ve bir P/Invoke dönüş değerini değerlendirir ve 32-bit ve 64 bit platformlarındaki yönetilmeyen koda sıralanmış olarak bunların boyutunun doğru olduğunu doğrular. Bu kuralın en yaygın ihlali, platforma bağımlı, işaretçi boyutunda bir değişkenin gerekli olduğu sabit boyutlu bir tamsayıyı iletmektir.

## <a name="rule-description"></a>Kural açıklaması
Aşağıdaki senaryolardan biri bu kuralın oluştuğunu ihlal ediyor:

- Dönüş değeri veya parametresi, olarak `IntPtr`yazılması gerektiğinde sabit boyutlu bir tamsayı olarak yazılır.

- Dönüş değeri veya parametresi, sabit boyutlu bir tamsayı `IntPtr` olarak yazılması gerektiğinde bir olarak yazılır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
`IntPtr` `UIntPtr` Veya yerine`UInt32`tutamaçları temsil etmek için veya kullanarak bu ihlalin düzeltmesini çözebilirsiniz. `Int32`

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu uyarıyı gizmemelisiniz.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralın ihlaline neden olduğunu gösterir.

```csharp
internal class NativeMethods
{
    [DllImport("shell32.dll", CharSet=CharSet.Auto)]
    internal static extern IntPtr ExtractIcon(IntPtr hInst,
        string lpszExeFileName, IntPtr nIconIndex);
}
```

Bu örnekte, `nIconIndex` parametresi, 32 bitlik bir platformda 4 `IntPtr`bayt genişliğinde olan ve 64 bitlik bir platformda 8 bayt genişliğinde olan bir olarak bildirilmiştir. Aşağıdaki yönetilmeyen bildirimde, tüm platformlarda 4 baytlık işaretsiz bir tamsayı `nIconIndex` olduğunu görebilirsiniz.

```csharp
HICON ExtractIcon(HINSTANCE hInst, LPCTSTR lpszExeFileName,
    UINT nIconIndex);
```

## <a name="example"></a>Örnek
İhlalin giderilmesi için bildirimi aşağıdaki şekilde değiştirin:

```csharp
internal class NativeMethods{
    [DllImport("shell32.dll", CharSet=CharSet.Auto)]
    internal static extern IntPtr ExtractIcon(IntPtr hInst,
        string lpszExeFileName, uint nIconIndex);
}
```

## <a name="see-also"></a>Ayrıca bkz.
[Taşınabilirlik Uyarıları](../code-quality/portability-warnings.md)