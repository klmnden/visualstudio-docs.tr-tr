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
ms.openlocfilehash: 3f35e450f17a671b800d003b94ceb5ebc2321c90
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65841419"
---
# <a name="ca2007-do-not-directly-await-a-task"></a>CA2007: Doğrudan bir Görevi beklemeyin

|||
|-|-|
|TypeName|DoNotDirectlyAwaitATaskAnalyzer|
|CheckId|CA2007|
|Kategori|Microsoft.Reliability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Zaman uyumsuz bir yöntem [bekler](/dotnet/csharp/language-reference/keywords/await) bir <xref:System.Threading.Tasks.Task> doğrudan.

## <a name="rule-description"></a>Kural açıklaması

Zaman zaman uyumsuz bir yöntem bekler bir <xref:System.Threading.Tasks.Task> doğrudan, devamlılık görevi oluşturan aynı iş parçacığında oluşur. Bu davranış, performans açısından pahalı olabilir ve kullanıcı Arabirimi iş parçacığında bir kilitlenmeye neden olabilir. Arama göz önünde bulundurun <xref:System.Threading.Tasks.Task.ConfigureAwait(System.Boolean)?displayProperty=nameWithType> amacınız devamlılık için sinyal.

Bu kural ile sunulan [FxCop Çözümleyicileri](install-fxcop-analyzers.md) ve "eski" (statik kod çözümleme)'içinde yok FxCop.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

İhlallerini düzeltmek için çağrı <xref:System.Threading.Tasks.Task.ConfigureAwait%2A> beklenen üzerinde <xref:System.Threading.Tasks.Task>. Geçirebilirsiniz `true` veya `false` için `continueOnCapturedContext` parametresi.

- Çağırma `ConfigureAwait(true)` görevi açıkça çağırma olarak aynı davranışa sahip <xref:System.Threading.Tasks.Task.ConfigureAwait%2A>. Açıkça bu yöntemi çağırarak kasıtlı olarak devamlılığın özgün eşitleme kapsamının üzerinde gerçekleştirmek istediğiniz okuyuculara izin vererek.

- Çağrı `ConfigureAwait(false)` görevi iş parçacığı havuzu devamlılıklarının zamanlamak için böylece kullanıcı Arabirimi iş parçacığında bir kilitlenme önleme. Geçirme `false` uygulama bağımsız kitaplıkları için iyi bir seçenektir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Tüketici bir grafik kullanıcı arabirimi (GUI) uygulaması değil veya tüketici sahip değil biliyorsanız, bu uyarının gösterilmemesi bir <xref:System.Threading.SynchronizationContext>.

## <a name="example"></a>Örnek

Aşağıdaki kod parçacığı, uyarıyı üretir:

```csharp
public async Task Execute()
{
    Task task = null;
    await task;
}
```

İhlali gidermek için çağrı <xref:System.Threading.Tasks.Task.ConfigureAwait%2A> beklenen üzerinde <xref:System.Threading.Tasks.Task>:

```csharp
public async Task Execute()
{
    Task task = null;
    await task.ConfigureAwait(false);
}
```

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan bir değer döndürmez zaman uyumsuz yöntemler hariç tutmak isteyip istemediğinizi yapılandırabilirsiniz. Bu tür yöntemler tutmak için projenizin bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
# Package version 2.9.0 and later
dotnet_code_quality.CA2007.exclude_async_void_methods = true

# Package version 2.6.3 and earlier
dotnet_code_quality.CA2007.skip_async_void_methods = true
```

Ayrıca, hangi derleme türleri bu kuralın uygulanacağı çıktı yapılandırabilirsiniz. Örneğin, yalnızca bu kural bir konsol uygulaması veya dinamik olarak bağlı bir kitaplığı (diğer bir deyişle, olmayan bir kullanıcı Arabirimi uygulaması) oluşturan koda uygulamak için projenizin bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.CA2007.output_kind = ConsoleApplication, DynamicallyLinkedLibrary
```

Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Ben bir görevle ConfigureAwait(false) await?](https://github.com/Microsoft/vs-threading/blob/master/doc/cookbook_vs.md#should-i-await-a-task-with-configureawaitfalse)
- [Visual Studio'da FxCop Çözümleyicileri yükleyin](install-fxcop-analyzers.md)