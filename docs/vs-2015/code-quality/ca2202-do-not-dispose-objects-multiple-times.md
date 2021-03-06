---
title: 'CA2202: Nesneleri birden çok kez atmayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2202
- Do not dispose objects multiple times
- DoNotDisposeObjectsMultipleTimes
helpviewer_keywords:
- CA2202
ms.assetid: fa85349a-cf1e-42c8-a86b-eacae1f8bd96
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 3dfe606e3083c937db3ba3d1e6cd49d34bace853
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697976"
---
# <a name="ca2202-do-not-dispose-objects-multiple-times"></a>CA2202: Nesneleri birden çok kez atmayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotDisposeObjectsMultipleTimes|
|CheckId|CA2202|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Birden çok çağrı neden olabilecek kod yolları bir yöntemi uygulaması içeren <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> veya aynı nesne üzerinde bazı türleri üzerinde Close() yöntemi gibi bir Dispose eşdeğer.

## <a name="rule-description"></a>Kural Tanımı
 Düzgün uygulanan bir <xref:System.IDisposable.Dispose%2A> yöntemi çağrıldığında birden çok kez bir özel durum olmadan. Ancak, bu kesin değildir ve oluşturmaktan kaçınmak için bir <xref:System.ObjectDisposedException?displayProperty=fullName> değil, çağırmalıdır <xref:System.IDisposable.Dispose%2A> bir nesne üzerinde birden fazla kez.

## <a name="related-rules"></a>İlgili kuralları
 [CA2000: Kapsamı kaybetmeden önce verileri nesneleri dispose](../code-quality/ca2000-dispose-objects-before-losing-scope.md)

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için kod yolunun, bu nedenle bu bakılmaksızın uygulamasını değiştirin <xref:System.IDisposable.Dispose%2A> nesne için yalnızca bir kez çağrılır.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Bile <xref:System.IDisposable.Dispose%2A> nesne birden çok kez güvenli bir şekilde çağrılabilir olduğunun bilindiği için uygulama gelecekte değişebilir.

## <a name="example"></a>Örnek
 İç içe geçmiş `using` deyimleri (`Using` Visual Basic'te) CA2202 uyarı ihlalleri neden olabilir. İç içe geçmiş iç IDisposable kaynağın `using` deyimi içeren kaynak dış `using` deyimi `Dispose` yöntemi iç içe kaynak kapsanan kaynak serbest bırakır. Bu durum ortaya çıktığında `Dispose` yöntemi dış `using` deyimi için ikinci bir zaman kaynağı dispose dener.

 Aşağıdaki örnekte, bir <xref:System.IO.Stream> bir dış oluşturulan nesne using deyimi içinde Dispose yöntemini using deyimi iç sonunda yayımlanır <xref:System.IO.StreamWriter> içeren nesne `stream` nesne. Dış sonunda `using` deyimi `stream` nesne ikinci kez yayımlanır. İkinci Sürüm CA2202 ihlal eder.

```
using (Stream stream = new FileStream("file.txt", FileMode.OpenOrCreate))
{
    using (StreamWriter writer = new StreamWriter(stream))
    {
        // Use the writer object...
    }
}
```

## <a name="example"></a>Örnek
 Bu sorunu gidermek için bir `try` / `finally` bloğu dış yerine `using` deyimi. İçinde `finally` emin olun, block `stream` kaynağı null değil.

```
Stream stream = null;
try
{
    stream = new FileStream("file.txt", FileMode.OpenOrCreate);
    using (StreamWriter writer = new StreamWriter(stream))
    {
        stream = null;
        // Use the writer object...
    }
}
finally
{
    if(stream != null)
        stream.Dispose();
}
```

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.IDisposable?displayProperty=fullName> [Dispose deseni](https://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)
