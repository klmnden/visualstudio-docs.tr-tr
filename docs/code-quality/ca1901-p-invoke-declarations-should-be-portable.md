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
ms.openlocfilehash: 0c4216b52fa4a23848a82548c36c34592deacc0b
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55936917"
---
# <a name="ca1901-pinvoke-declarations-should-be-portable"></a>CA1901: P/Invoke bildirimleri taşınabilir olmalıdır

|||
|-|-|
|TypeName|PInvokeDeclarationsShouldBePortable|
|CheckId|CA1901|
|Kategori|Microsoft.Portability|
|Yeni Değişiklik|P/Invoke derlemenin dışında görünür olup olmadığını - kesiliyor. P/Invoke derlemenin dışında görünür değilse olmayan son -.|

## <a name="cause"></a>Sebep
 Bu kural her parametresinin boyutu ve P/Invoke dönüş değeri değerlendirir ve bunların boyutu, 32-bit ve 64-bit platformlarda, yönetilmeyen kod sıralandığı zaman doğru olduğunu doğrular. Bu kural ihlalini en yaygın bir platforma bağımlı, işaretçi boyutlu değişken gerekli olduğu sabit boyutlu bir tamsayı geçirmektir.

## <a name="rule-description"></a>Kural açıklaması
 Bu kuralı ihlal aşağıdaki senaryolardan biri gerçekleşir:

- Olarak yazılmalıdır, parametre ve dönüş değeri bir sabit boyutlu tamsayı olarak yazılan bir `IntPtr`.

- Parametre ve dönüş değeri olarak yazılmış bir `IntPtr` zaman yazdığınız sabit boyutlu bir tamsayı olarak.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Kullanarak, bu ihlali düzeltebilirsiniz `IntPtr` veya `UIntPtr` yerine tanıtıcılarını temsil etmek için `Int32` veya `UInt32`.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu uyarı göndermeme değil.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bu kural ihlalini gösterir.

```csharp
internal class NativeMethods
{
    [DllImport("shell32.dll", CharSet=CharSet.Auto)]
    internal static extern IntPtr ExtractIcon(IntPtr hInst,
        string lpszExeFileName, IntPtr nIconIndex);
}
```

 Bu örnekte, `nIconIndex` parametresi olarak bildirilmiş bir `IntPtr`, 4 bayt genişliğinde 32-bit bir platforma ve 8 baytlık bir 64-bit platformda geniş olduğu. Görürsünüz izleyen yönetilmeyen bildiriminde `nIconIndex` tüm platformlarda bir 4-bayt işaretsiz tamsayı.

```csharp
HICON ExtractIcon(HINSTANCE hInst, LPCTSTR lpszExeFileName,
    UINT nIconIndex);
```

## <a name="example"></a>Örnek
 İhlali gidermek için bildirimi aşağıdaki gibi değiştirin:

```csharp
internal class NativeMethods{
    [DllImport("shell32.dll", CharSet=CharSet.Auto)]
    internal static extern IntPtr ExtractIcon(IntPtr hInst,
        string lpszExeFileName, uint nIconIndex);
}
```

## <a name="see-also"></a>Ayrıca bkz.
 [Taşınabilirlik Uyarıları](../code-quality/portability-warnings.md)