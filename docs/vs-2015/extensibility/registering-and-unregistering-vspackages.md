---
title: Kaydetme ve kaydını VSPackages | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- registration, VSPackages
- VSPackages, registering
ms.assetid: e25e7a46-6a55-4726-8def-ca316f553d6b
caps.latest.revision: 36
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f5f43dd44dde41de4ecf3e34fa5e895ee0f4711f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49187622"
---
# <a name="registering-and-unregistering-vspackages"></a>VSPackage Kaydetme ve Kaydını Kaldırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Öznitelik bir VSPackage'ı kaydetmek için kullandığınız ancak  
  
## <a name="registering-a-vspackage"></a>VSPackage kaydetme  
 Yönetilen VSPackages kaydını denetlemek için öznitelikleri kullanabilirsiniz. Tüm kayıt bilgileri .pkgdef dosyasında yer alır. Dosya tabanlı kayıt hakkında daha fazla bilgi için bkz. [CreatePkgDef yardımcı programı](../extensibility/internals/createpkgdef-utility.md).  
  
 Aşağıdaki kod, VSPackage'ı kaydetmek için standart kayıt öznitelikleri kullanmayı gösterir.  
  
```csharp  
[PackageRegistration(UseManagedResourcesOnly = true)]  
[Guid("0B81D86C-0A85-4f30-9B26-DD2616447F95")]  
public sealed class BasicPackage : Package  
{. . .}  
```  
  
## <a name="unregistering-an-extension"></a>Bir uzantı kaydı siliniyor  
 Çok sayıda farklı VSPackage'ları ile denemeler ve bunları deneysel örneği kaldırmak istiyorsanız, yalnızca çalıştırabilirsiniz **sıfırlama** komutu. Aranacak **Visual Studio Deneysel örneğini sıfırlama** başlangıç sayfasında, bilgisayarın veya komut satırından şu komutu çalıştırın:  
  
```vb  
<location of Visual Studio 2015 install>\"Microsoft Visual Studio 14.0\VSSDK\VisualStudioIntegration\Tools\Bin\CreateExpInstance.exe" /Reset /VSInstance=14.0 /RootSuffix=Exp  
```  
  
 Git, Visual Studio geliştirme örneğinde yüklü olduğu bir uzantıyı kaldırmak istiyorsanız, **araçları / Uzantılar ve güncelleştirmeler**uzantısını bulun ve tıklayın **kaldırma**.  
  
 Bazı nedenlerden dolayı bu yöntemlerin hiçbiri uzantısını kaldırmayı en başarılı olursa komut satırından VSPackage derleme gibi kaydını kaldırabilirsiniz:  
  
```  
<location of Visual Studio 2015 install>\"Microsoft Visual Studio 14.0\VSSDK\VisualStudioIntegration\Tools\Bin\regpkg” /unregister <pathToVSPackage assembly>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPackage’lar](../extensibility/internals/vspackages.md)

