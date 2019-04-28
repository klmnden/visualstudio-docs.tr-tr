---
title: Sistem gereksinimlerini algılama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- setup, VSPackages
- launch conditions
ms.assetid: 0ba94acf-bf0b-4bb3-8cca-aaac1b5d6737
caps.latest.revision: 51
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 467554b8e50878bcdf1029e4792bbf168a09fa11
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63445249"
---
# <a name="detecting-system-requirements"></a>Sistem Gereksinimlerini Algılama
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

VSPackage Visual Studio'nun yüklü olduğu sürece çalışamaz. Microsoft Windows Installer, VSPackage'ı yüklemesini yönetmek için kullandığınız zaman, Visual Studio yüklü olup olmadığını algılamak için yükleyici yapılandırabilirsiniz. Ayrıca, örneğin sistemin diğer gereksinimleri denetlemek üzere, belirli bir Windows sürümü veya belirli bir RAM miktarını yapılandırabilirsiniz.  
  
## <a name="detecting-visual-studio-editions"></a>Visual Studio sürümleri algılama  
 Visual Studio sürümü yüklü olup olmadığını belirlemek için yükleme kayıt defteri anahtarının değerini (REG_DWORD) uygun klasöründe, 1 aşağıdaki tabloda listelendiği gibi olduğunu. Visual Studio sürümleri hiyerarşisini olduğuna dikkat edin:  
  
1. Enterprise  
  
2. Professional  
  
3. Topluluk  
  
   "Yüksek" sürümü yüklendiğinde, kayıt defteri anahtarlarını bu sürümünde de "Düşük" sürümleri gibi eklenir. Diğer bir deyişle, Enterprise edition yüklediyseniz, yükleme anahtar 1 Professional ve Community sürümlerinde yanı sıra, kuruluş için ayarlanır. Bu nedenle, gereksinim duyduğunuz yalnızca "Yüksek" sürümü için denetlemeniz gerekir.  
  
> [!NOTE]
> Kayıt Defteri Düzenleyicisi'ni 64-bit sürümünde 32 bit anahtarlar HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node altında görüntülenen\\. Visual Studio anahtarları HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\DevDiv\vs\Servicing altında olan\\.  
  
|Ürün|Anahtar|  
|-------------|---------|  
|Visual Studio Enterprise 2015|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\enterprise|  
|Visual Studio Professional 2015|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\professional|  
|Visual Studio Community 2015|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\community|  
|Visual Studio 2015 (tümleşik ve yalıtılmış) Kabuğu|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\isoshell|  
  
## <a name="detecting-when-visual-studio-is-running"></a>Visual Studio çalışırken algılama  
 Vspackage'i yüklediğinizde Visual Studio çalışıyorsa, VSPackage'ı doğru kaydedilemez. Yükleyici, Visual Studio çalışırken algılamak ve programı yüklemek geri çevir. Windows Installer gibi algılamayı etkinleştirmek için tablo girişleri kullanmanıza izin vermez. Bunun yerine, özel bir eylem şu şekilde oluşturmanız gerekir: Kullanım `EnumProcesses` işlevi devenv.exe işleminin algılayıp ya da bir başlatma koşulu veya koşullu olarak kullanılan bir yükleyici özelliğini ayarlamak için Visual Studio kullanıcının isteyen bir iletişim kutusu görüntüler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Installer ile VSPackage Yükleme](../../extensibility/internals/installing-vspackages-with-windows-installer.md)
