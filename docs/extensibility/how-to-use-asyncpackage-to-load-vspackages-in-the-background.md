---
title: 'Nasıl yapılır: Arka planda VSPackage AsyncPackage sayfanızdaki | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: dedf0173-197e-4258-ae5a-807eb3abc952
author: madskristensen
ms.author: madsk
ms.workload:
- vssdk
ms.openlocfilehash: 64514a6d43d580fbda142dfa65bb3a2d384dff4e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66324779"
---
# <a name="how-to-use-asyncpackage-to-load-vspackages-in-the-background"></a>Nasıl yapılır: Arka planda VSPackage yükleme için AsyncPackage kullanın
Yükleme ve VS paket başlatma disk g/ç neden olabilir. Böyle g/ç UI iş parçacığı üzerinde olursa bu yanıt hızını sorunlarına yol açabilir. Bunu ele almak için Visual Studio 2015 kullanıma sunulan <xref:Microsoft.VisualStudio.Shell.AsyncPackage> paketi yükleme arka plan iş parçacığında sağlayan sınıf.

## <a name="create-an-asyncpackage"></a>Bir sınıfta oluşturma
 Bir VSIX projesi oluşturarak başlayın (**dosya** > **yeni** > **proje** > **Visual C#**   >  **Genişletilebilirlik** > **VSIX projesi**) ve bir VSPackage'ı projeye ekleniyor (projeye sağ tıklayın ve **Ekle**  >  **Yeni öğe**  >   **C# öğesi** > **genişletilebilirlik**  >   **Visual Studio paket**). Ardından, hizmetlerinizi oluşturup bu hizmetler, pakete ekleyin.

1. Paketten türetilen <xref:Microsoft.VisualStudio.Shell.AsyncPackage>.

2. Hizmetleri sorgulamak, yüklemek, paket neden olabilir sağlıyorsanız:

    Visual Studio için paketinizi arka planda yükleme için güvenli olduğunu belirtmek için ve bu davranışı geri çevirmek için <xref:Microsoft.VisualStudio.Shell.PackageRegistrationAttribute> ayarlamalısınız **AllowsBackgroundLoading** özelliği true olarak öznitelik Oluşturucusu.

   ```csharp
   [PackageRegistration(UseManagedResourcesOnly = true, AllowsBackgroundLoading = true)]

   ```

    Visual Studio için hizmetinizde bir arka plan iş parçacığı oluşturmak güvenli olduğunu belirtmek için ayarlamalısınız <xref:Microsoft.VisualStudio.Shell.ProvideServiceAttributeBase.IsAsyncQueryable%2A> özelliği true olarak <xref:Microsoft.VisualStudio.Shell.ProvideServiceAttribute> Oluşturucusu.

   ```csharp
   [ProvideService(typeof(SMyTestService), IsAsyncQueryable = true)]

   ```

3. UI bağlamı yüklenen sonra belirtmeniz gerekir **PackageAutoLoadFlags.BackgroundLoad** için <xref:Microsoft.VisualStudio.Shell.ProvideAutoLoadAttribute> bayrak değeri (0x2) paketinizin otomatik yükle giriş değeri olarak yazılamaz veya okunamaz.

   ```csharp
   [ProvideAutoLoad(UIContextGuid, PackageAutoLoadFlags.BackgroundLoad)]

   ```

4. Zaman uyumsuz başlatma iş yapmak için varsa, geçersiz kılmalıdır <xref:Microsoft.VisualStudio.Shell.AsyncPackage.InitializeAsync%2A>. Kaldırma `Initialize()` VSIX şablonuyla sağlanan yöntemi. ( `Initialize()` Yönteminde **AsyncPackage** korumalı). Herhangi birini kullanabilmeniz için <xref:Microsoft.VisualStudio.Shell.AsyncPackage.AddService%2A> paketiniz için zaman uyumsuz bir hizmet eklemek için yöntemleri.

    NOT: Çağrılacak `base.InitializeAsync()`, kaynak kodunuzu değiştirebilirsiniz:

   ```csharp
   await base.InitializeAsync(cancellationToken, progress);
   ```

5. RPC (uzak yordam çağrısı) yapmamak için zaman uyumsuz başlatma kodunuzdan ilgileniriz gerekir (içinde **InitializeAsync**). Çağırdığınızda bu oluşabilir <xref:Microsoft.VisualStudio.Shell.Package.GetService%2A> doğrudan veya dolaylı olarak.  Eşitleme yükleri gerekli olduğunda, UI iş parçacığı kullanan engeller <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory>. Varsayılan engelleme modelini RPC devre dışı bırakır. Bu, zaman uyumsuz görevleri bir RPC kullanmayı denerseniz, kullanıcı Arabirimi iş parçacığı kendisi, paketi yüklemek bekleyen ise, kilitlenme, anlamına gelir. Kodunuzu UI iş parçacığına benzer bir şey kullanarak gerekirse sıralamakta genel alternatiftir **birleştirilebilir görev fabrikasını**'s <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory.SwitchToMainThreadAsync%2A> veya bir RPC kullanmaz başka bir mekanizma.  Kullanmayın **ThreadHelper.Generic.Invoke** veya genellikle UI iş parçacığına almak için bekliyor çağıran iş parçacığını engeller.

    NOT: Kullanmaktan kaçınmalısınız **GetService** veya **QueryService** içinde `InitializeAsync` yöntemi. Bu kullanmanız gerekiyorsa, kullanıcı Arabirimi iş parçacığına geçmeniz gerekir. Alternatif kullanmaktır <xref:Microsoft.VisualStudio.Shell.AsyncServiceProvider.GetServiceAsync%2A> gelen, **AsyncPackage** (için atama tarafından <xref:Microsoft.VisualStudio.Shell.Interop.IAsyncServiceProvider>.)

   C#: Bir sınıfta oluşturun:

```csharp
[PackageRegistration(UseManagedResourcesOnly = true, AllowsBackgroundLoading = true)]
[ProvideService(typeof(SMyTestService), IsAsyncQueryable = true)]
public sealed class TestPackage : AsyncPackage
{
    protected override Task InitializeAsync(System.Threading.CancellationToken cancellationToken, IProgress<ServiceProgressData> progress)
    {
        this.AddService(typeof(SMyTestService), CreateService, true);
        return Task.FromResult<object>(null);
    }
}
```

## <a name="convert-an-existing-vspackage-to-asyncpackage"></a>Mevcut bir VSPackage AsyncPackage için Dönüştür
 İşin çoğunu yeni oluşturma aynıdır **AsyncPackage**. 1 ile 5 yukarıdaki adımları izleyin. Aşağıdaki öneriler ek dikkatli olması gerekir:

1. Kaldırmayı unutmayın `Initialize` geçersiz kılma paketinizdeki vardı.

2. Kilitlenmeler kaçının: Olabilir, kodunuzda RPC gizli. artık bir arka plan iş parçacığında gerçekleşir. Bir RPC yapıyorsanız emin olun (örneğin, **GetService**), ana iş parçacığı (1) ya da geç yapmanız veya var (2) zaman uyumsuz bir API sürümünü kullanın (örneğin, **Asyncpackage'dan**).

3. Çok sık iş parçacıkları arasında geçiş. Yükleme zamanını azaltmak için arka plan iş parçacığında oluşabilir iş yerelleştirmek deneyin.

## <a name="querying-services-from-asyncpackage"></a>AsyncPackage hizmetlerinden sorgulama
 Bir **AsyncPackage** olabilir veya zaman uyumsuz olarak bağlı olarak çağıran yüklenmeyebilir. Örneğin,

- Çağıranın çağrılırsa **GetService** veya **QueryService** (hem zaman uyumlu API) veya

- Çağıranın çağrılırsa **IVsShell::LoadPackage** (veya **IVsShell5::LoadPackageWithContext**) veya

- Yükleme kullanıcı Arabirimi bağlam tarafından tetiklenir, ancak UI bağlamı mekanizması, zaman uyumsuz olarak yükleyebilirsiniz belirtmedi

  Ardından, paket zaman uyumlu olarak yüklenir.

  UI iş parçacığı için söz konusu iş tamamlama engellenecek olsa paketinizi UI iş parçacığından, çalışmaya devam (zaman uyumsuz başlangıç aşamasında) fırsatına sahiptir. Çağıranın kullanıyorsa **IAsyncServiceProvider** hizmetiniz için zaman uyumsuz olarak sorgu için sonra yükleme ve başlatma zaman uyumsuz olarak bunlar yok hemen engelleme elde edilen görev nesnesinde varsayılarak yapılır.

  C#: Hizmet zaman uyumsuz olarak sorgulayıp nasıl:

```csharp
using Microsoft.VisualStudio.Shell;
using Microsoft.VisualStudio.Shell.Interop;

IAsyncServiceProvider asyncServiceProvider = Package.GetService(typeof(SAsyncServiceProvider)) as IAsyncServiceProvider;
IMyTestService testService = await asyncServiceProvider.GetServiceAsync(typeof(SMyTestService)) as IMyTestService;
```
