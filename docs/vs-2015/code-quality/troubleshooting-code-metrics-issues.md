---
title: Kod ölçümleri sorunlarını giderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: troubleshooting
ms.assetid: f2fdb995-4888-4246-85dc-7bacadd45968
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 1567715a8f944eb10c2728caa9fc1edd43beda8e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62580604"
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
