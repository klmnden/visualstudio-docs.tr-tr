---
title: 'DA0002: VSPerfCorProf.dll yok | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.DA0002
- vs.performance.2
- vs.performance.rules.DAVsPerfCorProfMissing
- vs.performance.rules.DA0002
ms.assetid: 76e614b3-ad7e-4b92-b7be-88dc1329be1d
caps.latest.revision: 19
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5723506415a0ddbf816b896e23e93eaa706bf7e7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68158721"
---
# <a name="da0002-vsperfcorprofdll-is-missing"></a>DA0002: VSPerfCorProf.dll eksik
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA0002 |  
| Kategori | Profil oluşturma araçları kullanım |  
| Profil oluşturma yöntemlerini | VSPerfCmd ve VSPerfASPNETCmd komut satırı araçlarını kullanarak profil oluşturma |  
| İleti | Dosya ortam değişkenleri VSPerfCLREnv.cmd ile düzgün şekilde ayarlamadan toplanmış görünür. Yönetilen ikililerin sembolleri olmayan çözebilir. |  
| Kural türü | Bilgi |  
  
## <a name="cause"></a>Sebep  
 Profil Oluşturucu, profil oluşturma çalışması süresince VSPerfCorProf.dll bulunamadı. Profil Oluşturucu veri koleksiyonu için komut satırı araçları gerekli ortam değişkenlerini başlatmak için VSPerfCLREnv.cmd Aracı'nı kullanarak olmadan kullanıldığında, bu uyarı oluşur. Başka bir profil oluşturucu profil oluşturma araçları başlattığınızda çalışıyorsa uyarı da tetikleyebilir.  
  
## <a name="rule-description"></a>Kural Tanımı  
 .NET Framework ikili dosyaları sembolleri çözümlemek profil oluşturucu için profil oluşturma yürütmesine önce belirli ortam değişkenlerini ayarlamanız gerekir. Bu uyarı, profil oluşturma verilerinin toplandığı önce VSPerfCLREnv.cmd aracı çalıştırılmadı önerir. Yönetilen ikililerin sembolleri çözebilir değil. Komut satırından profil oluşturma araçlarını kullanma hakkında daha fazla bilgi için bkz. [komut satırından profil oluşturma](../profiling/using-the-profiling-tools-from-the-command-line.md)  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Zaman profil yönetilen uygulamaların komut satırı araçları kullanarak [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma, çalıştırma Araçları [VSPerfCLREnv](../profiling/vsperfclrenv.md) veri toplama başlamadan önce komut satırı aracı.
