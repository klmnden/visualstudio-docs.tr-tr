---
title: Komut satırı anahtarları ekleme | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- command-line switches, adding
- command-line switches, retrieving
- IVsAppCommandLine::GetOption method
- command line, switches
ms.assetid: 8bbbd87e-76fe-4fb5-8ef9-65f5e31967cf
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 0f8349cc71bf0541d726a47bf5b875724c89bcc6
ms.sourcegitcommit: 159ed9d4f56cdc1dff2fd19d9dffafe77e46cd4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53738595"
---
# <a name="add-command-line-switches"></a>Komut satırı anahtarları ekleme
Uygulamak için VSPackage'ı komut satırı anahtarları eklediğiniz zaman *devenv.exe* yürütülür. Kullanım <xref:Microsoft.VisualStudio.Shell.ProvideAppCommandLineAttribute> adını anahtar ve özelliklerini bildirmek için. Bu örnekte, MySwitch anahtar VSPackage adlı bir alt sınıfı için eklenen **AddCommandSwitchPackage** bağımsız değişken olmadan ile otomatik olarak yüklenecek VSPackage'ı.  
  
```csharp  
[ProvideAppCommandLine("MySwitch", typeof(AddCommandSwitchPackage), Arguments = "0", DemandLoad = 1)]  
```  
  
 Aşağıdaki açıklamalarda adlandırılmış parametreleri gösterilmektedir.

||||
|-|-|-|-|
| Parametre | Açıklama|
| Arguments | Anahtar için bağımsız değişken sayısı. Olabilir "*", veya bağımsız değişkenlerinin listesi. |
| DemandLoad | Bu 1, aksi durumda 0 olarak ayarlayın, ayarlanırsa VSPackage'ı otomatik olarak yükleyin. |  
| HelpString | Görüntülemek için Yardım dizesi veya kaynak kimliği dizesi **devenv /?**. |
| Ad | Anahtar. |
| PackageGuid | Paket GUID'si. |  
  
 İlk bağımsız değişken genellikle 0 veya 1 değeridir. Özel bir değeri ' *' tüm kalan komut satırı bağımsız değişkeni olduğunu göstermek için kullanılabilir. Bu, bir kullanıcı bir hata ayıklayıcı komut dizesi burada geçmelidir senaryoları hata ayıklama için yararlı olabilir.  
  
 DemandLoad değeri geçerli `true` (1) veya `false` (0) VSPackage'ı otomatik olarak yüklenmesi gerektiğini belirtir.  
  
 Görünen dize kaynak kimliği HelpString değerdir **devenv /?** Yardım görüntüleme. Bu değer, "#nnn nnn bir tamsayı olduğu" biçiminde olmalıdır. Kaynak dosyadaki dize değeri bir yeni satır karakteri ile bitmelidir.  
  
 Anahtar adı değerdir.  
  
 Bu anahtar uygulayan paket GUID'i PackageGuid değerdir. IDE bu GUID VSPackage'ı komut satırı anahtarı uygulandığı kayıt defterinde bulmak için kullanır.  
  
## <a name="retrieve-command-line-switches"></a>Komut satırı anahtarları alma  
 Paketiniz yüklendiğinde, aşağıdaki adımları tamamlayarak komut satırı anahtarları alabilirsiniz.  
  
1. İçinde VSPackage'nın <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A> uygulaması, çağrı `QueryService` üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.SVsAppCommandLine> almak için <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine> arabirimi.  
  
2. Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine.GetOption%2A> kullanıcı girilen komut satırı anahtarları alınamadı.  
  
   Aşağıdaki kod MySwitch komut satırı anahtarı olup kullanıcı tarafından girilen kullanıma nasıl gösterir:  
  
```csharp  
IVsAppCommandLine cmdline = (IVsAppCommandLine)GetService(typeof(SVsAppCommandLine));  
  
int isPresent = 0;  
string optionValue = "";  
  
cmdline.GetOption("MySwitch", out isPresent, out optionValue);  
```  
  
 Bu, paket her yüklendiğinde, komut satırı anahtarları için denetlenecek sizin sorumluluğunuzdur.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A>   
 [Devenv komut satırı anahtarları](../ide/reference/devenv-command-line-switches.md)   
 [CreatePkgDef yardımcı programı](../extensibility/internals/createpkgdef-utility.md)   
 [. Pkgdef dosyaları](/visualstudio/extensibility/shell/modifying-the-isolated-shell-by-using-the-dot-pkgdef-file)