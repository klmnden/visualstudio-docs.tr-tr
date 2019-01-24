---
title: -Yükseltme (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- /upgrade Devenv switch
- Devenv, /upgrade switch
- upgrade Devenv switch
ms.assetid: 3468045c-5cc9-4157-9a9d-622452145d27
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 465c90736f5470f48d47336bc916ca3cb2c09b6a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779352"
---
# <a name="upgrade-devenvexe"></a>/Upgrade (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Çözüm dosyası ve proje dosyalarının ya da proje dosyası, belirtilen geçerli tüm güncelleştirmeleri [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] bu dosyaların biçimleri.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
devenv SolutionFile | ProjectFile /upgrade  
```  
  
## <a name="arguments"></a>Arguments  
 `SolutionFile`  
 Tüm bir çözümü ve projelerini yükseltiyorsanız, gereklidir. Çözüm dosyasının adı ve yolu. Yalnızca çözüm dosyasının veya tam yol adı ve çözüm dosyasının adını girebilirsiniz. Adlandırılmış klasör veya dosya henüz yoksa, oluşturulur.  
  
 `ProjectFile`  
 Tek bir projeyi yükseltiyorsanız gereklidir. Çözüm içindeki bir proje dosyasının adı ve yolu. Yalnızca proje dosyasının veya tam yol adını ve proje dosyasının adını girebilirsiniz. Adlandırılmış klasör veya dosya henüz yoksa, oluşturulur.  
  
## <a name="remarks"></a>Açıklamalar  
 Yedeklemeleri otomatik olarak oluşturulur ve geçerli dizinde oluşturulan Backup adlı dizine kopyalanır.  
  
 Yükseltilebilmesi için önce kaynağı denetlenen çözümlerin veya projelerin kullanıma alınması gerekir.  
  
 Kullanarak `/upgrade` anahtar başlamıyor [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]. Yükseltmenin sonuçları, çözüm veya projenin geliştirme dilinin yükseltme Raporu'nda görülebilir. Hiçbir hata veya kullanım bilgisi döndürülür. Projeleri yükseltme hakkında daha fazla bilgi için [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], bkz: [nasıl yapılır: Başarısız Visual Studio Proje yükseltmelerinde sorun giderme](../../porting/how-to-troubleshoot-unsuccessful-visual-studio-project-upgrades.md).  
  
## <a name="example"></a>Örnek  
 Bu örnek için varsayılan klasörünüzdeki "MyProject.sln" adlı bir çözüm dosyasını yükseltir [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] çözümler.  
  
```  
devenv "MyProject.sln" /upgrade  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Başarısız Visual Studio Proje yükseltmelerinde sorun giderme](../../porting/how-to-troubleshoot-unsuccessful-visual-studio-project-upgrades.md)   
 [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
