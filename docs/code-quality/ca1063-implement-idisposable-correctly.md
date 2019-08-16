---
title: "CA1063: IDisposable'ı doğru uygulayın"
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- ImplementIDisposableCorrectly
- CA1063
helpviewer_keywords:
- CA1063
- ImplementIDisposableCorrectly
ms.assetid: 12afb1ea-3a17-4a3f-a1f0-fcdb853e2359
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: 837659ca24eb66995626668185500db7bc32bbd7
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69547379"
---
# <a name="ca1063-implement-idisposable-correctly"></a>CA1063: IDisposable'ı doğru uygulayın

|||
|-|-|
|TypeName|ImplementIDisposableCorrectly|
|CheckId|CA1063|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

<xref:System.IDisposable?displayProperty=nameWithType> Arabirim doğru bir şekilde uygulanmadı. Bunun olası nedenleri şunlardır:

- <xref:System.IDisposable>, sınıfında yeniden uygulanır.

- `Finalize`yeniden geçersiz kılındı.

- `Dispose()`geçersiz kılındı.

- Yöntem ortak, korumalı veya adlandırılmış **Dispose**değil. [](/dotnet/csharp/language-reference/keywords/sealed) `Dispose()`

- `Dispose(bool)`korunmaz, sanal veya korumasız değildir.

- Korumasız türlerde, `Dispose()` `Dispose(true)`çağrılmalıdır.

- Korumasız türler için, `Finalize` uygulama ya da her ikisini `Dispose(bool)` veya temel sınıf sonlandırıcısını çağırmaz.

Bu desenlerden herhangi birinin ihlali, uyarı CA1063 tetikler.

<xref:System.IDisposable> Arabirimini bildiren ve uygulayan her korumasız tür kendi `protected virtual void Dispose(bool)` metodunu sağlamalıdır. `Dispose()`çağrılmalıdır ve sonlandırıcının çağırmalıdır `Dispose(false)`. `Dispose(true)` <xref:System.IDisposable> Arabirimini bildiren ve uygulayan korumasız bir tür oluşturursanız, onu tanımlamanız `Dispose(bool)` ve çağırmanız gerekir. Daha fazla bilgi için bkz. [yönetilmeyen kaynakları temizleme (.net Kılavuzu)](/dotnet/standard/garbage-collection/unmanaged) ve [Dispose model](/dotnet/standard/design-guidelines/dispose-pattern).

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Tüm <xref:System.IDisposable> türler [Dispose modelini](/dotnet/standard/design-guidelines/dispose-pattern) doğru uygulamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Kodunuzu inceleyin ve aşağıdaki çözümlerden hangisinin bu ihlalin düzelceğini saptayın:

- Türü <xref:System.IDisposable> tarafından uygulanan arabirimlerin listesinden kaldırın ve bunun yerine temel sınıf Dispose uygulamasını geçersiz kılın.

- Bu sonlandırıcıyı türden kaldırın, Dispose (bool disposing) öğesini geçersiz kılın ve sonlandırma mantığını ' disposing ' değeri false olan kod yoluna koyun.

- Dispose (bool disposing) öğesini geçersiz kılın ve Dispose mantığını ' disposing ' in true olduğu kod yoluna koyun.

- Dispose () public ve [Sealed](/dotnet/csharp/language-reference/keywords/sealed)olarak bildirildiği için emin olun.

- Dispose yönteminizi **Dispose** olarak yeniden adlandırın ve Public ve [Sealed](/dotnet/csharp/language-reference/keywords/sealed)olarak bildirildiği şekilde ayarlandığından emin olun.

- Dispose (bool) korumalı, sanal ve korumasız olarak bildirildiği için emin olun.

- Dispose () öğesini, Dispose (true) yöntemini çağıracak şekilde değiştirin, sonra <xref:System.GC.SuppressFinalize%2A> geçerli nesne örneğinde (`this`veya `Me` Visual Basic) çağırır ve sonra döndürür.

- Sonlandırıcıyı, Dispose (false) yöntemini çağıracak ve ardından döndüren bir şekilde değiştirin.

- <xref:System.IDisposable> Arabirimini bildiren ve uygulayan korumasız bir tür oluşturursanız, uygulamasının <xref:System.IDisposable> uygulamanın bu bölümde daha önce açıklanan modele uyduğundan emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1063.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="pseudo-code-example"></a>Sözde kod örneği

Aşağıdaki sözde kod, Dispose (bool) ' ın yönetilen ve yerel kaynakları kullanan bir sınıfta nasıl uygulanması gerektiği hakkında genel bir örnek sağlar.

```csharp
public class Resource : IDisposable
{
    private IntPtr nativeResource = Marshal.AllocHGlobal(100);
    private AnotherResource managedResource = new AnotherResource();

    // Dispose() calls Dispose(true)
    public void Dispose()
    {
        Dispose(true);
        GC.SuppressFinalize(this);
    }

    // NOTE: Leave out the finalizer altogether if this class doesn't
    // own unmanaged resources, but leave the other methods
    // exactly as they are.
    ~Resource()
    {
        // Finalizer calls Dispose(false)
        Dispose(false);
    }

    // The bulk of the clean-up code is implemented in Dispose(bool)
    protected virtual void Dispose(bool disposing)
    {
        if (disposing)
        {
            // free managed resources
            if (managedResource != null)
            {
                managedResource.Dispose();
                managedResource = null;
            }
        }
        // free native resources if there are any.
        if (nativeResource != IntPtr.Zero)
        {
            Marshal.FreeHGlobal(nativeResource);
            nativeResource = IntPtr.Zero;
        }
    }
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [Dispose kriteri (çerçeve tasarım yönergeleri)](/dotnet/standard/design-guidelines/dispose-pattern)
- [Yönetilmeyen kaynakları temizleme (.NET Kılavuzu)](/dotnet/standard/garbage-collection/unmanaged)