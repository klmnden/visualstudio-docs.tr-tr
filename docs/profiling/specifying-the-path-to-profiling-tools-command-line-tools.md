---
title: Profil oluşturma yolunu belirterek Araçları komut satırı araçları | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 7047bf18-5779-4f6e-872c-66e2fc47c969
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7ef2434cdea3183fc55ad72fafb36175a726c58e
ms.sourcegitcommit: 34840a954ed3446c789e80ee87da6cbf1203cbb5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/18/2018
ms.locfileid: "53592904"
---
# <a name="specify-the-path-to-profiling-tools-command-line-tools"></a>Profil oluşturma araçları komut satırı araçları yolunu belirtme
Yolu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profil Araçları komut satırı araçları, PATH ortam değişkenine eklenmez. 32-bit bilgisayarlarda, tek bir dizinde araçlardır. Profil oluşturma araçlarından 64-bit bilgisayarlarda 32 bit ve 64-bit sürümleri vardır.  
  
## <a name="32-bit-computers"></a>32-bit bilgisayarlar  
 Yerel kod için Visual Studio profil oluşturma API'leri bulunan *VSPerf.dll*. Üstbilgi dosyası *VSPerf.h*ve içeri aktarma kitaplığını *VSPerf.lib*, bulunan *Microsoft Visual Studio\2017\Team Araçlar\Performans Tools\PerfSDK* Dizin.
  
 Yönetilen kod için profil oluşturucu API bulunan *Microsoft.VisualStudio.Profiler.dll*. Bu DLL bulunan *Microsoft Visual Studio\Shared\Common\VSPerfCollectionTools* dizin.
  
## <a name="64-bit-computers"></a>64 bit bilgisayarlar  
 64-bit bilgisayarlarda, profili oluşturulan uygulamanın hedef platformu göre yolu belirtin.  
  
-   32-bit uygulamalar için varsayılan profil oluşturucu Araçlar dizindir:  
  
     (yerel) *Microsoft Visual Studio\2017\Team Araçlar\Performans Tools\PerfSDK* (yönetilen) *Microsoft Visual Studio\Shared\Common\VSPerfCollectionTools*  
  
-   64-bit uygulamalar için varsayılan profil oluşturucu Araçlar dizindir:  
  
     (yerel) *Microsoft Visual Studio\2017\Team Araçlar\Performans Tools\x64\PerfSDK* (yönetilen) *Microsoft Visual Studio\Shared\Common\VSPerfCollectionTools\x64*