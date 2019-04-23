---
title: Kod ölçümleri sorunlarını giderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: troubleshooting
ms.assetid: f2fdb995-4888-4246-85dc-7bacadd45968
caps.latest.revision: 6
author: erickson-doug
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d8a3ccfa22ba248ba094b99f25ea1478ec378f4d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60094625"
---
# <a name="troubleshooting-code-metrics-issues"></a>Kod Ölçümleri Sorunlarını Giderme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kod ölçümleri toplarken aşağıdaki sorunlardan bazılarını karşılaşabilirsiniz:  
  
- [Visual Studio 2010 kod karmaşıklığı hesaplamalar değişiklikleri](#Changes_in_Visual_Studio_2010_code_complexity_calculations)  
  
## <a name="Changes_in_Visual_Studio_2010_code_complexity_calculations"></a> Visual Studio 2010 kod karmaşıklığı hesaplamalar değişiklikleri  
 Aynı işlev için Kod Karmaşıklığı ölçüm hesaplanır [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] önceki sürümleri tarafından hesaplanan ölçüyü farklı olabilir [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)] aşağıdaki durumlar için:  
  
- Bir veya daha fazla catch blokları bir işlevi içeriyor. Önceki sürümlerinde [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)], catch blokları hesaplamaya eklenmez. İçinde [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)], her bir catch bloğu karmaşıklığını işlevi karmaşıklığını eklenir.  
  
- İşlev (Select Case vb'de) switch deyimi içerir. Derleyici farkları arasında [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] ve önceki sürümleri, başarısızlık servis taleplerini içerir bazı switch deyimleri için farklı MSIL kodu oluşturabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönetilen Kodun Ölçüm Karmaşıklığı ve Bakımı](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)
