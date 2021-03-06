---
title: VSPackage yükleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, autoloading
- VSPackages, loading
ms.assetid: f4c3dcea-5051-4065-898f-601269649d92
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2c7c2a558abc928524813419df6b7848d34f0f3e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309568"
---
# <a name="load-vspackages"></a>VSPackage yükleme
İşlevleri gerekli olduğunda VSPackages Visual Studio'ya yüklenir. Örneğin, Visual Studio bir proje fabrikası ya da VSPackage'ı uygulayan bir hizmet kullanırken bir VSPackage yüklenir. Bu özellik, mümkün olduğunda performansını artırmak kullanılan Gecikmeli yüklemeyi çağrılır.

> [!NOTE]
> Visual Studio VSPackage'ı yüklemeden VSPackage sunan komutlar gibi belirli bir VSPackage bilgileri belirleyebilirsiniz.

 Bir çözümü açtığınızda VSPackages sorsorgu belirli kullanıcı arabirimi (UI) bağlamında gibi olarak ayarlanabilir. <xref:Microsoft.VisualStudio.Shell.ProvideAutoLoadAttribute> Özniteliği bu bağlamda ayarlar.

### <a name="autoload-a-vspackage-in-a-specific-context"></a>Otomatik belirli bir bağlamda VSPackage yükleme

- Ekleme `ProvideAutoLoad` özniteliği VSPackage öznitelikleri:

    ```csharp
    [DefaultRegistryRoot(@"Software\Microsoft\VisualStudio\14.0")]
    [PackageRegistration(UseManagedResourcesOnly = true)]
    [ProvideAutoLoad(UIContextGuids80.SolutionExists)]
    [Guid("00000000-0000-0000-0000-000000000000")] // your specific package GUID
    public class MyAutoloadedPackage : Package
    {. . .}
    ```

     Numaralandırılmış alanlarını bkz <xref:Microsoft.VisualStudio.Shell.Interop.UIContextGuids80> UI bağlamı ve GUID değerlerinin listesi.

- Bir kesim noktası <xref:Microsoft.VisualStudio.Shell.Package.Initialize%2A> yöntemi.

- VSPackage'ı oluşturun ve hata ayıklamaya başlayın.

- Bir çözümü yüklemek veya bir tane oluşturabilirsiniz.

     VSPackage'ı yükler ve kesme noktasında durur.

## <a name="force-a-vspackage-to-load"></a>VSPackage'ı yüklemek için zorlama
 Bazı koşullar altında bir VSPackage yüklenecek başka bir VSPackage zorlamanız gerekebilir. Örneğin, basit bir VSPackage'ı bir CMDUIContext kullanılamayan bir bağlamda daha büyük bir VSPackage yükleyebilir.

 Kullanabileceğiniz <xref:Microsoft.VisualStudio.Shell.Interop.IVsShell.LoadPackage%2A> VSPackage'ı yüklemeye zorlamak için yöntemi.

- Bu koda Ekle <xref:Microsoft.VisualStudio.Shell.Package.Initialize%2A> yüklemek için başka bir VSPackage zorlar VSPackage'ı yöntemi:

    ```csharp
    IVsShell shell = GetService(typeof(SVsShell)) as IVsShell;
    if (shell == null) return;

    IVsPackage package = null;
    Guid PackageToBeLoadedGuid =
        new Guid(Microsoft.PackageToBeLoaded.GuidList.guidPackageToBeLoadedPkgString);
    shell.LoadPackage(ref PackageToBeLoadedGuid, out package);

    ```

     VSPackage'ı başlatıldığında zorlayacak `PackageToBeLoaded` yüklenemedi.

     Zorla yüklenmesini VSPackage iletişimi için kullanılmaması gerekir. Kullanım [kullanın ve hizmetleri sağlamak](../extensibility/using-and-providing-services.md) yerine.

## <a name="see-also"></a>Ayrıca bkz.
- [VSPackage’lar](../extensibility/internals/vspackages.md)
