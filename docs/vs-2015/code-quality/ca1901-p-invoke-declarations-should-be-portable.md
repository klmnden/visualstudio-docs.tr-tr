---
title: 'CA1901: P-Invoke bildirimleri taşınabilir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1901
- PInvokeDeclarationsShouldBePortable
helpviewer_keywords:
- CA1901
- PInvokeDeclarationsShouldBePortable
ms.assetid: 90361812-55ca-47f7-bce9-b8775d3b8803
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ccbbc3178a9f65c15d11a27dee1a625cca729240
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60053955"
---
# <a name="ca1901-pinvoke-declarations-should-be-portable"></a>CA1901: P/Invoke bildirimleri taşınabilir olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|PInvokeDeclarationsShouldBePortable|
|CheckId|CA1901|
|Kategori|Microsoft.Portability|
|Yeni Değişiklik|P/Invoke derlemenin dışında görünür olup olmadığını - kesiliyor. P/Invoke derlemenin dışında görünür değilse olmayan son -.|

## <a name="cause"></a>Sebep
 Bu kural her parametresinin boyutu ve P/Invoke dönüş değeri değerlendirir ve bunların boyutu, 32-bit ve 64-bit platformlarda, yönetilmeyen kod sıralandığı zaman doğru olduğunu doğrular. Bu kural ihlalini en yaygın bir platforma bağımlı, işaretçi boyutlu değişken gerekli olduğu sabit boyutlu bir tamsayı geçirmektir.

## <a name="rule-description"></a>Kural Tanımı
 Bu kuralı ihlal aşağıdaki senaryolardan biri gerçekleşir:

- Olarak yazılmalıdır, parametre ve dönüş değeri bir sabit boyutlu tamsayı olarak yazılan bir `IntPtr`.

- Parametre ve dönüş değeri olarak yazılmış bir `IntPtr` zaman yazdığınız sabit boyutlu bir tamsayı olarak.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Kullanarak, bu ihlali düzeltebilirsiniz `IntPtr` veya `UIntPtr` yerine tanıtıcılarını temsil etmek için `Int32` veya `UInt32`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
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

## <a name="see-also"></a>Ayrıca Bkz.
 [Taşınabilirlik Uyarıları](../code-quality/portability-warnings.md)
