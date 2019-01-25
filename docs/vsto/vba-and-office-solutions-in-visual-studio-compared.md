---
title: Visual Studio'da karşılaştırılan VBA ve Office çözümleri
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- VBA code, managed code extensions
- managed code extensions [Office development in Visual Studio], VBA compared to
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 313af1a48b4c8fac6281fd8250ed36104a5276b6
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54866889"
---
# <a name="vba-and-office-solutions-in-visual-studio-compared"></a>Visual Studio'da karşılaştırılan VBA ve Office çözümleri
  Microsoft Visual Basic for Applications (VBA), Office uygulamaları ile tümleşiktir, yönetilmeyen kod kullanır. Visual Studio kullanılarak oluşturulan Microsoft Office projeleri .NET Framework ve Visual Studio Tasarım araçları avantajlarından yararlanmanıza olanak tanır.  
  
 Visual Studio kullanarak oluşturabileceğiniz Office çözümleri türleri hakkında daha fazla bilgi için bkz [Office çözümleri geliştirmesine genel bakış &#40;VSTO&#41;](../vsto/office-solutions-development-overview-vsto.md).  
  
## <a name="comparison"></a>Karşılaştırma  
 Aşağıdaki tabloda Office çözümlerini Visual Studio'da VBA çözümleri arasındaki temel bir karşılaştırma sağlar.  
  
|VBA çözümleri|Visual Studio'da Office çözümleri|  
|-------------------|---------------------------------------|  
|Belirli bir belge ile bağlı ve kalıcı kodu kullanır.|Belgedeki (için belge düzeyinde özelleştirmeler), ayrı olarak depolanan kod veya derlemedeki (VSTO eklentileri için) uygulama tarafından yüklenir.|  
|Office nesne modelleri ve VBA API'ler ile çalışır.|Hem de Office nesne modelleri için erişim sağlar ve [!INCLUDE[dnprdnshort](../sharepoint/includes/dnprdnshort-md.md)] API'leri.|  
|Makro kaydı ve Basitleştirilmiş bir geliştirici deneyimi için tasarlanmıştır.|Güvenlik, daha kolay bir şekilde kod bakımı ve tam Visual Studio tümleşik geliştirme ortamı (IDE) kullanma olanağı için tasarlanmıştır.|  
|İyi Office uygulamalarıyla sıkı bir tümleştirme yararlı çözümleri için çalışır.|İyi Visual Studio'nun tam kaynaklardan yararlanan çözümler için çalışır ve [!INCLUDE[dnprdnshort](../sharepoint/includes/dnprdnshort-md.md)].|  
|Kuruluşlar için güvenlik ve dağıtım alanlarda özellikle sınırlamalar uygulanır.|Kurumsal kullanım için tasarlanmıştır.|  
  
 Bazı şeyler VBA kullanarak hızlı bir şekilde yapmak yine de kolaydır. Özellikle, VBA kullanmaya devam etmek isteyebilirsiniz:  
  
-   Özel çalışma işlevleri.  
  
-   Makro kaydetme.  
  
## <a name="combine-vba-solutions-and-office-solutions-created-by-using-visual-studio"></a>VBA çözümlerini ve Visual Studio kullanılarak oluşturulan Office çözümlerini birleştirin  
 Visual Studio kullanılarak oluşturulan Office Çözümlerinden VBA kodu çağırabilir ve VBA'dan Visual Studio kullanılarak oluşturulan Office çözümlerinde kod çağırabilir. Belirli teknik Office çözümünüzü VSTO eklentisi veya belge düzeyi özelleştirmesi olup bağlı olarak farklılık gösterir. Daha fazla bilgi için [çağrı kod VSTO eklentileri diğer Office Çözümlerinden](../vsto/calling-code-in-vsto-add-ins-from-other-office-solutions.md) ve [birleştirmek VBA ve belge düzeyi özelleştirmeleri](../vsto/combining-vba-and-document-level-customizations.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Office çözümleri geliştirmesine genel bakış &#40;VSTO&#41;](../vsto/office-solutions-development-overview-vsto.md)   
 [VSTO eklentilerinde diğer Office Çözümlerinden kod arama](../vsto/calling-code-in-vsto-add-ins-from-other-office-solutions.md)   
 [VBA ve belge düzeyi özelleştirmelerini birleştirme](../vsto/combining-vba-and-document-level-customizations.md)   
 [Belge düzeyi özelleştirmeler mimarisi](../vsto/architecture-of-document-level-customizations.md)   
 [VSTO eklentileri mimarisi](../vsto/architecture-of-vsto-add-ins.md)   
 [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)   
 [Başlama &#40;Visual Studio'da Office geliştirme&#41;](../vsto/getting-started-office-development-in-visual-studio.md)  
