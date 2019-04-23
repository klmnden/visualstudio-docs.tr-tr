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
ms.openlocfilehash: 7fadcff84c4b927a7718d7d4ad1311918ae0f18a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60066942"
---
# <a name="specifying-the-path-to-profiling-tools-command-line-tools"></a>Profil Oluşturma Araçları Komut Satırı Araçları Yolunu Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yolu [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Profil Araçları komut satırı araçları, PATH ortam değişkenine eklenmez. 32-bit bilgisayarlarda, tek bir dizinde araçlardır. Profil oluşturma araçlarından 64-bit bilgisayarlarda 32 bit ve 64-bit sürümleri vardır.  
  
## <a name="32-bit-computers"></a>32-bit bilgisayarlar  
 Varsayılan profil oluşturucu Araçlar Dizin 32-bit bilgisayarlarda, *sürücü*\Program Visual Studio 11.0\Team Araçlar\Performans araçları.  
  
## <a name="64-bit-computers"></a>64 bit bilgisayarlar  
 64-bit bilgisayarlarda, profili oluşturulan uygulamanın hedef platformu göre yolu belirtin.  
  
- 32-bit uygulamalar için varsayılan profil oluşturucu Araçlar dizindir:  
  
     *Sürücü*\Program dosyaları (x86) \Microsoft Visual Studio 11.0\Team Araçlar\Performans araçları  
  
- 64-bit uygulamalar için varsayılan profil oluşturucu Araçlar dizindir:  
  
     *Sürücü*\Program dosyaları (x86) \Microsoft Visual Studio 11.0\Team Araçlar\Performans Tools\x64
