---
title: Komut satırı anahtarları ekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- command-line switches, adding
- command-line switches, retrieving
- IVsAppCommandLine::GetOption method
- command line, switches
ms.assetid: 8bbbd87e-76fe-4fb5-8ef9-65f5e31967cf
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9c44864285f3e5701604379a110292c29d3f9b78
ms.sourcegitcommit: 90c3187d804ad7544367829d07ed4b47d3f8a72d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68821525"
---
# <a name="add-command-line-switches"></a>Komut satırı anahtarları Ekle
*Devenv. exe* yürütüldüğünde VSPackage 'a uygulanan komut satırı anahtarlarını ekleyebilirsiniz. Anahtarın <xref:Microsoft.VisualStudio.Shell.ProvideAppCommandLineAttribute> adını ve özelliklerini bildirmek için kullanın. Bu örnekte, bir bağımsız değişken içermeyen ve VSPackage otomatik olarak yüklenen VSPackage adlı VSPackage alt sınıfı Için mySwitch anahtarı eklenir.

```csharp
[ProvideAppCommandLine("MySwitch", typeof(AddCommandSwitchPackage), Arguments = "0", DemandLoad = 1)]
```

 Adlandırılmış parametreler aşağıdaki açıklamalarda gösterilmiştir.

||||
|-|-|-|-|
| Parametre | Açıklama|
| Arguments | Anahtar için bağımsız değişkenlerin sayısı. "*" Veya bağımsız değişken listesi olabilir. |
| Isteğsiz yük | Bu 1 olarak ayarlanırsa VSPackage 'ı otomatik olarak yükleyin, aksi takdirde 0 olarak ayarlayın. |
| HelpString | **Devenv/?** ile görüntülenecek dizenin Yardım dizesi veya kaynak kimliği. |
| Ad | Anahtar. |
| PackageGuid | Paketin GUID 'SI. |

 Bağımsız değişkenlerin ilk değeri genellikle 0 veya 1 ' dir. Komut satırının tüm geri kalanın bağımsız değişken olduğunu göstermek için ' * ' özel değeri kullanılabilir. Bu, kullanıcının bir hata ayıklayıcı komut dizesinde geçmesi gereken hata ayıklama senaryolarında yararlı olabilir.

 Kullanılan yük değeri (1) `true` ya `false` da (0) VSPackage 'ın otomatik olarak yüklenmesi gerektiğini gösterir.

 HelpString değeri, **devenv/?** içinde görüntülenen DIZENIN kaynak kimliğidir. Yardım görüntüleme. Bu değer, nnn ' in bir tamsayı olduğu "#nnn" biçiminde olmalıdır. Kaynak dosyasındaki dize değeri yeni bir satır karakteriyle bitmelidir.

 Ad değeri, anahtarın adıdır.

 PackageGuid değeri, bu anahtarı uygulayan paketin GUID 'sidir. IDE, komut satırı anahtarının uygulandığı kayıt defterindeki VSPackage 'ı bulmak için bu GUID 'yi kullanır.

## <a name="retrieve-command-line-switches"></a>Komut satırı anahtarlarını alma
 Paketiniz yüklendiğinde, aşağıdaki adımları tamamlayarak komut satırı anahtarlarını alabilirsiniz.

1. VSPackage <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A> uygulamanızda, <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine> arabirimini almak <xref:Microsoft.VisualStudio.Shell.Interop.SVsAppCommandLine> için öğesini `QueryService` çağırın.

2. Kullanıcının <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine.GetOption%2A> girdiği komut satırı anahtarlarını almak için çağırın.

   Aşağıdaki kod, MySwitch komut satırı anahtarının Kullanıcı tarafından girilip girilmediğini nasıl bulacağınızı göstermektedir:

```csharp
IVsAppCommandLine cmdline = (IVsAppCommandLine)GetService(typeof(SVsAppCommandLine));

int isPresent = 0;
string optionValue = "";

cmdline.GetOption("MySwitch", out isPresent, out optionValue);
```

 Paketinizin her yüklenilişinde komut satırı anahtarlarınızın denetlenmesi sizin sorumluluğunuzdadır.

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A>
- [Devenv komut satırı anahtarları](../ide/reference/devenv-command-line-switches.md)
- [CreatePkgDef yardımcı programı](../extensibility/internals/createpkgdef-utility.md)
- [. Pkgdef dosyaları](https://devblogs.microsoft.com/visualstudio/whats-a-pkgdef-and-why/)