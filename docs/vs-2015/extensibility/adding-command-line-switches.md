---
title: Komut satırı anahtarları ekleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- command-line switches, adding
- command-line switches, retrieving
- IVsAppCommandLine::GetOption method
- command line, switches
ms.assetid: 8bbbd87e-76fe-4fb5-8ef9-65f5e31967cf
caps.latest.revision: 22
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e28a3f303849458a407b212d3aad1a8c198f6d25
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54781344"
---
# <a name="adding-command-line-switches"></a>Komut Satırı Anahtarları Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Devenv.exe yürütüldüğünde, VSPackage için geçerli olan komut satırı anahtarları ekleyebilirsiniz. Kullanım <xref:Microsoft.VisualStudio.Shell.ProvideAppCommandLineAttribute> adını anahtar ve özelliklerini bildirmek için. Bu örnekte, MySwitch anahtar VSPackage adlı bir alt sınıfı için eklenen **AddCommandSwitchPackage** bağımsız değişken olmadan ile otomatik olarak yüklenecek VSPackage'ı.  
  
```csharp  
[ProvideAppCommandLine("MySwitch", typeof(AddCommandSwitchPackage), Arguments = "0", DemandLoad = 1)]  
```  
  
 Adlandırılmış parametreler aşağıdaki tabloda gösterilmiştir.  
  
 Arguments  
 Anahtar için bağımsız değişken sayısı. Olabilir "*", veya bağımsız değişkenlerinin listesi.  
  
 DemandLoad  
 Bu 1, aksi durumda 0 olarak ayarlayın, ayarlanırsa VSPackage'ı otomatik olarak yükleyin.  
  
 HelpString  
 Görüntülemek için Yardım dizesi veya kaynak kimliği dizesi **devenv /?**.  
  
 Ad  
 Anahtar.  
  
 PackageGuid  
 Paket GUID'si.  
  
 İlk bağımsız değişken genellikle 0 veya 1 değeridir. Özel bir değeri ' *' tüm kalan komut satırı bağımsız değişkeni olduğunu göstermek için kullanılabilir. Bu, bir kullanıcı bir hata ayıklayıcı komut dizesi burada geçmelidir senaryoları hata ayıklama için yararlı olabilir.  
  
 DemandLoad değeri geçerli `true` (1) veya `false` (0) VSPackage'ı otomatik olarak yüklenmesi gerektiğini belirtir.  
  
 HelpString değerdir devenv içinde görünen dize kaynak kimliği /? Yardım görüntüleme. Bu değer, "#nnn nnn bir tamsayı olduğu" biçiminde olmalıdır. Kaynak dosyadaki dize değeri bir yeni satır karakteri ile bitmelidir.  
  
 Anahtar adı değerdir.  
  
 Bu anahtar uygulayan paket GUID'i PackageGuid değerdir. IDE bu GUID VSPackage'ı komut satırı anahtarı uygulandığı kayıt defterinde bulmak için kullanır.  
  
## <a name="retrieving-command-line-switches"></a>Komut satırı anahtarları alma  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A>   
 [Devenv komut satırı anahtarları](../ide/reference/devenv-command-line-switches.md)   
 [CreatePkgDef yardımcı programı](../extensibility/internals/createpkgdef-utility.md)   
 [.Pkgdef Dosyaları](../extensibility/modifying-the-isolated-shell-by-using-the-dot-pkgdef-file.md)
