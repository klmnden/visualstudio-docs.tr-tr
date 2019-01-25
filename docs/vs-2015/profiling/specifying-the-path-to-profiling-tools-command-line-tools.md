---
title: Profil oluşturma yolunu belirterek Araçları komut satırı araçları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 7047bf18-5779-4f6e-872c-66e2fc47c969
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 209c2263e35bc4e6c5bfffb03b4a760e8cc15a45
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54791758"
---
# <a name="specifying-the-path-to-profiling-tools-command-line-tools"></a>Profil Oluşturma Araçları Komut Satırı Araçları Yolunu Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yolu [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Profil Araçları komut satırı araçları, PATH ortam değişkenine eklenmez. 32-bit bilgisayarlarda, tek bir dizinde araçlardır. Profil oluşturma araçlarından 64-bit bilgisayarlarda 32 bit ve 64-bit sürümleri vardır.  
  
## <a name="32-bit-computers"></a>32-bit bilgisayarlar  
 Varsayılan profil oluşturucu Araçlar Dizin 32-bit bilgisayarlarda, *sürücü*\Program Visual Studio 11.0\Team Araçlar\Performans araçları.  
  
## <a name="64-bit-computers"></a>64 bit bilgisayarlar  
 64-bit bilgisayarlarda, profili oluşturulan uygulamanın hedef platformu göre yolu belirtin.  
  
-   32-bit uygulamalar için varsayılan profil oluşturucu Araçlar dizindir:  
  
     *Sürücü*\Program dosyaları (x86) \Microsoft Visual Studio 11.0\Team Araçlar\Performans araçları  
  
-   64-bit uygulamalar için varsayılan profil oluşturucu Araçlar dizindir:  
  
     *Sürücü*\Program dosyaları (x86) \Microsoft Visual Studio 11.0\Team Araçlar\Performans Tools\x64
