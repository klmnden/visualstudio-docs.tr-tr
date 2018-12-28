---
title: Kod Ölçümleri Sorunlarını Giderme
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: troubleshooting
ms.assetid: f2fdb995-4888-4246-85dc-7bacadd45968
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9575020135846edc9cb86bd89ff72682500d8a9d
ms.sourcegitcommit: 159ed9d4f56cdc1dff2fd19d9dffafe77e46cd4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53739568"
---
# <a name="troubleshooting-code-metrics-issues"></a>Kod Ölçümleri Sorunlarını Giderme
Kod ölçümleri toplarken aşağıdaki sorunlardan bazılarını karşılaşabilirsiniz:

-   [Visual Studio 2010 kod karmaşıklığı hesaplamalar değişiklikleri](#Changes_in_Visual_Studio_2010_code_complexity_calculations)

##  <a name="Changes_in_Visual_Studio_2010_code_complexity_calculations"></a> Visual Studio 2010 kod karmaşıklığı hesaplamalar değişiklikleri
 Aynı işlev için Kod Karmaşıklığı ölçüm hesaplanır [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] önceki sürümleri tarafından hesaplanan ölçüyü farklı olabilir [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] aşağıdaki durumlar için:

- Bir veya daha fazla catch blokları bir işlevi içeriyor. Önceki sürümlerinde [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)], catch blokları hesaplamaya eklenmez. İçinde [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)], her bir catch bloğu karmaşıklığını işlevi karmaşıklığını eklenir.

- İşlev (Select Case vb'de) switch deyimi içerir. Derleyici farkları arasında [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] ve önceki sürümleri, başarısızlık servis taleplerini içerir bazı switch deyimleri için farklı MSIL kodu oluşturabilir.

## <a name="see-also"></a>Ayrıca Bkz.
 [Yönetilen Kodun Ölçüm Karmaşıklığı ve Bakımı](../code-quality/code-metrics-values.md)