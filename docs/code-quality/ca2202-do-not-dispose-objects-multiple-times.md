---
title: 'CA2202: Nesneleri birden çok kez atmayın'
ms.date: 07/16/2019
ms.topic: reference
f1_keywords:
- CA2202
- Do not dispose objects multiple times
- DoNotDisposeObjectsMultipleTimes
helpviewer_keywords:
- CA2202
ms.assetid: fa85349a-cf1e-42c8-a86b-eacae1f8bd96
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b5fb70baa17bee484dc3c31d7c6ce9b302019403
ms.sourcegitcommit: 2bbcba305fd0f8800fd3d9aa16f7647ee27f3a4b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2019
ms.locfileid: "68300594"
---
# <a name="ca2202-do-not-dispose-objects-multiple-times"></a>CA2202: Nesneleri birden çok kez atmayın

|||
|-|-|
|TypeName|DoNotDisposeObjectsMultipleTimes|
|CheckId|CA2202|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Yöntem uygulama, aynı nesne üzerinde, bazı türlerde bir Close ( <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> ) yöntemi gibi birden çok çağrıya veya bir Dispose eşdeğerine neden olabilecek kod yollarını içerir.

## <a name="rule-description"></a>Kural açıklaması

Doğru şekilde uygulanan <xref:System.IDisposable.Dispose%2A> bir yöntem, özel durum oluşturmadan birden çok kez çağrılabilir. Ancak, bu garanti edilmez ve bir <xref:System.ObjectDisposedException?displayProperty=fullName> nesne üzerinde birden fazla kez çağırmamalıdır. <xref:System.IDisposable.Dispose%2A>

## <a name="related-rules"></a>İlgili kurallar

- [CA2000 Kapsamı kaybetmeden önce nesneleri atma](../code-quality/ca2000-dispose-objects-before-losing-scope.md)

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, uygulamayı kod yolundan bağımsız olarak, <xref:System.IDisposable.Dispose%2A> nesne için yalnızca bir kez çağırılabilecek şekilde değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. <xref:System.IDisposable.Dispose%2A> Nesnenin güvenli bir şekilde birden çok kez çağrılabilir olduğu bilinse bile, uygulama gelecekte değişebilir.

## <a name="example"></a>Örnek

İç `using` içe geçmiş`Using` deyimler (Visual Basic) CA2202 uyarı ihlallerine neden olabilir. İç içe geçmiş iç `using` deyimin IDisposable kaynağı dıştaki `using` deyimin kaynağını içeriyorsa, `Dispose` iç içe kaynak yöntemi içerilen kaynağı serbest bırakır. Bu durum oluştuğunda, `Dispose` dış `using` deyimin yöntemi kaynağı ikinci bir kez atmayı dener.

Aşağıdaki örnekte, bir dış using <xref:System.IO.Stream> ifadesinde oluşturulan bir nesne, `stream` nesneyi içeren <xref:System.IO.StreamWriter> nesnenin Dispose yönteminde Inner using ifadesinin sonunda serbest bırakılır. Dış `using` deyimin sonunda `stream` , nesne ikinci kez serbest bırakılır. İkinci sürüm, CA2202 ihlaline neden olur.

```csharp
using (Stream stream = new FileStream("file.txt", FileMode.OpenOrCreate))
{
    using (StreamWriter writer = new StreamWriter(stream))
    {
        // Use the writer object...
    }
}
```

## <a name="example"></a>Örnek

Bu `try` sorunu çözmek için dış / `finally` deyiminyerinebirblokkullanın`using` . Bloğunda, `stream` kaynağın null olmadığından emin olun. `finally`

```csharp
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
    stream?.Dispose();
}
```

> [!TIP]
> Yukarıdaki sözdizimi null [koşullu işleçtir.](/dotnet/csharp/language-reference/operators/member-access-operators#null-conditional-operators--and-) `?.`

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IDisposable?displayProperty=fullName>
- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)