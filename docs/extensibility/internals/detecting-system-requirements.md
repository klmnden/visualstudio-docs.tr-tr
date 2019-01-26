---
title: Sistem gereksinimlerini algılama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- setup, VSPackages
- launch conditions
ms.assetid: 0ba94acf-bf0b-4bb3-8cca-aaac1b5d6737
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f4df7ec753f1d636a74dfce74b451ecaf5557c53
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55021682"
---
# <a name="detect-system-requirements"></a>Sistem gereksinimlerini algılama
VSPackage Visual Studio'nun yüklü olduğu sürece çalışamaz. Microsoft Windows Installer, VSPackage'ı yüklemesini yönetmek için kullandığınız zaman, Visual Studio yüklü olup olmadığını algılamak için yükleyici yapılandırabilirsiniz. Ayrıca, örneğin sistemin diğer gereksinimleri denetlemek üzere, belirli bir Windows sürümü veya belirli bir RAM miktarını yapılandırabilirsiniz.  
  
## <a name="detect-visual-studio-editions"></a>Visual Studio sürümleri algılayın  
 Visual Studio sürümü yüklü olup olmadığını belirlemek için aşağıdakileri doğrulayın değerini **yükleme** kayıt defteri anahtarı *(REG_DWORD) 1* uygun klasöründe, aşağıdaki tabloda listelendiği gibi. Visual Studio sürümleri hiyerarşisini olduğuna dikkat edin:  
  
1.  Enterprise  
  
2.  Professional  
  
3.  Topluluk  
      
Daha yeni bir sürümü yüklü olduğunda, bu sürüm için kayıt defteri anahtarlarını önceki sürümlerinde olduğu gibi de eklenir. Diğer bir deyişle, Enterprise edition yüklü değilse, **yükleme** anahtarı ayarlanır *1* Professional ve Community sürümlerinde yanı sıra, kuruluş için. Bu nedenle, gereksinim duyduğunuz yalnızca en son sürümü için denetlenecek gerekir.  
  
> [!NOTE]
>  Kayıt Defteri Düzenleyicisi'ni 64-bit sürümünde 32 bit anahtarlar altında görüntülenen **HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\\**. Visual Studio anahtarları altındadır **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\DevDiv\vs\Servicing\\**.  
  
|Ürün|Anahtar|  
|-------------|---------|  
|Visual Studio Enterprise 2015|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\enterprise|  
|Visual Studio Professional 2015|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\professional|  
|Visual Studio Community 2015|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\community|  
|Visual Studio 2015 (tümleşik ve yalıtılmış) Kabuğu|HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DevDiv\vs\Servicing\14.0\isoshell|  
  
## <a name="detect-when-visual-studio-is-running"></a>Visual Studio çalışırken Algıla  
 Vspackage'i yüklediğinizde Visual Studio çalışıyorsa, VSPackage'ı doğru kaydedilemez. Yükleyici, Visual Studio çalışırken algılamak ve programı yüklemek geri çevir. Windows Installer gibi algılamayı etkinleştirmek için tablo girişleri kullanmanıza izin vermez. Bunun yerine, özel bir eylem şu şekilde oluşturmanız gerekir: Kullanım `EnumProcesses` algılamak için işlev *devenv.exe* işlemek ve ardından ya da koşullu olarak Visual Studio'yu kapatın kullanıcının isteyen bir iletişim kutusu görüntüler veya başlatma koşulunda kullanılan bir yükleyici özelliğini ayarlayın.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Windows Installer ile VSPackage yükleme](../../extensibility/internals/installing-vspackages-with-windows-installer.md)