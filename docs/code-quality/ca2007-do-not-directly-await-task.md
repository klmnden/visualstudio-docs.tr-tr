---
title: 'CA2007: Doğrudan bir Görevi beklemeyin'
ms.date: 03/08/2019
ms.topic: reference
f1_keywords:
- CA2007
- DoNotDirectlyAwaitATaskAnalyzer
helpviewer_keywords:
- CA2007
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.openlocfilehash: cf07c997f933e6aacf3eff29ae204ecd0bedb036
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233068"
---
# <a name="ca2007-do-not-directly-await-a-task"></a>CA2007: Doğrudan bir Görevi beklemeyin

|||
|-|-|
|TypeName|Donotdirectlyawa, Taskanalyzer|
|CheckId|CA2007|
|Kategori|Microsoft. güvenilirliği|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Zaman uyumsuz bir [](/dotnet/csharp/language-reference/keywords/await) Yöntem <xref:System.Threading.Tasks.Task> doğrudan bekler.

## <a name="rule-description"></a>Kural açıklaması

Zaman uyumsuz bir yöntem <xref:System.Threading.Tasks.Task> doğrudan bekler, görevi oluşturan aynı iş parçacığında devamlılık oluşur. Bu davranış, performans açısından maliyetli olabilir ve Kullanıcı arabirimi iş parçacığında kilitlenmeye neden olabilir. Devamlılığını <xref:System.Threading.Tasks.Task.ConfigureAwait(System.Boolean)?displayProperty=nameWithType> sağlamak için çağırmayı düşünün.

Bu kural [FxCop çözümleyicileri](install-fxcop-analyzers.md) ile tanıtılmıştı ve eski FxCop analizinde yok.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

İhlalleri onarmak için, bekletildi <xref:System.Threading.Tasks.Task.ConfigureAwait%2A> <xref:System.Threading.Tasks.Task>üzerinde çağrı yapın. Parametresi için `true` `false` veya ' i geçirebilirsiniz. `continueOnCapturedContext`

- Görevde `ConfigureAwait(true)` çağırmak, açıkça çağrılmayan <xref:System.Threading.Tasks.Task.ConfigureAwait%2A>aynı davranışa sahiptir. Bu yöntemi açık bir şekilde çağırarak, okuyucuların özgün eşitleme bağlamında devamlılığını bilerek gerçekleştirmek istediğinizi öğrenmiş olursunuz.

- İş `ConfigureAwait(false)` parçacığı havuzunda devamlılıkları zamanlamak için görevde çağrı yapın, böylece kullanıcı arabirimi iş parçacığında kilitlenmelerden kaçının. Geçirme `false` , uygulamayla bağımsız kitaplıklar için iyi bir seçenektir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Tüketicinin bir grafik kullanıcı arabirimi (GUI) uygulaması olmadığını veya tüketicinin bir <xref:System.Threading.SynchronizationContext>öğesine sahip olmadığını biliyorsanız, bu uyarıyı gizleyebilirsiniz.

## <a name="example"></a>Örnek

Aşağıdaki kod parçacığı uyarı oluşturur:

```csharp
public async Task Execute()
{
    Task task = null;
    await task;
}
```

<xref:System.Threading.Tasks.Task.ConfigureAwait%2A> İhlalin<xref:System.Threading.Tasks.Task>giderilmesi için, beklenen:

```csharp
public async Task Execute()
{
    Task task = null;
    await task.ConfigureAwait(false);
}
```

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuraldan bir değer döndürmeyen zaman uyumsuz yöntemleri dışlamak isteyip istemediğiniz yapılandırabilirsiniz. Bu tür yöntemleri dışlamak için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
# Package version 2.9.0 and later
dotnet_code_quality.CA2007.exclude_async_void_methods = true

# Package version 2.6.3 and earlier
dotnet_code_quality.CA2007.skip_async_void_methods = true
```

Ayrıca, bu kuralın hangi çıkış derleme türlerini uygulanacağını de yapılandırabilirsiniz. Örneğin, bu kuralı yalnızca bir konsol uygulaması veya dinamik olarak bağlı bir kitaplık (yani, bir UI uygulaması değil) üreten koda uygulamak için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.CA2007.output_kind = ConsoleApplication, DynamicallyLinkedLibrary
```

Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="see-also"></a>Ayrıca bkz.

- [ConfigureAwait (false) ile bir görevi beklemem gerekir mi?](https://github.com/Microsoft/vs-threading/blob/master/doc/cookbook_vs.md#should-i-await-a-task-with-configureawaitfalse)
- [Visual Studio 'da FxCop çözümleyicileri 'ni yükler](install-fxcop-analyzers.md)