---
title: 'DA0002: VSPerfCorProf.dll yok | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0002
- vs.performance.2
- vs.performance.rules.DAVsPerfCorProfMissing
- vs.performance.rules.DA0002
ms.assetid: 76e614b3-ad7e-4b92-b7be-88dc1329be1d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: aa263f6ceab515627fd33070517e3393aeec419d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62936739"
---
# <a name="da0002-vsperfcorprofdll-is-missing"></a>DA0002: VSPerfCorProf.dll eksik

|||
|-|-|
|Kural Kimliği|DA0002|
|Kategori|Profil oluşturma araçları kullanım|
|Profil oluşturma yöntemleri|VSPerfCmd ve VSPerfASPNETCmd komut satırı araçlarını kullanarak profil oluşturma|
|İleti|Dosya ortam değişkenlerini doğru ayarlamadan toplanmış görünüyor *VSPerfCLREnv.cmd*. Yönetilen ikililerin sembolleri çözülemiyor olabilir.|
|Kural türü|Bilgiler|

## <a name="cause"></a>Sebep
 Profil oluşturucu bulunamadı *VSPerfCorProf.dll* profil oluşturma çalışması sırasında. Profil Oluşturucu veri koleksiyonu için komut satırı araçlarını kullanarak olmadan kullanıldığında, bu uyarı oluşur *VSPerfCLREnv.cmd* gerekli ortam değişkenlerini başlatmak üzere. Başka bir profil oluşturucu profil oluşturma araçları başlattığınızda çalışıyorsa uyarı da tetikleyebilir.

## <a name="rule-description"></a>Kural açıklaması
 .NET Framework ikili dosyaları sembolleri çözümlemek profil oluşturucu için profil oluşturma yürütmesine önce belirli ortam değişkenlerini ayarlamanız gerekir. Bu uyarı öneren *VSPerfCLREnv.cmd* aracı profil oluşturma verilerinin toplandığı önce değil çalıştırıldı. Yönetilen ikililerin sembolleri çözebilir değil. Komut satırından profil oluşturma araçlarını kullanma hakkında daha fazla bilgi için bkz. [komut satırından profil oluşturma](../profiling/using-the-profiling-tools-from-the-command-line.md)

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Zaman profil yönetilen uygulamaların komut satırı araçları kullanarak [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma, çalıştırma Araçları [VSPerfCLREnv](../profiling/vsperfclrenv.md) veri toplama başlamadan önce komut satırı aracı.