---
title: 'Nasıl yapılır: Yönetilen kod projesi için kod çözümlemesini yapılandırma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.propertypages.csvb
helpviewer_keywords:
- code analysis, selecting rule sets
- code analysis, rule sets
ms.assetid: 618f6ff3-db0e-46cb-b08d-dfa35e62c9e7
caps.latest.revision: 35
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a37ededab38cf27a002117f874d17d6a340000d9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63429163"
---
# <a name="how-to-configure-code-analysis-for-a-managed-code-project"></a>Nasıl yapılır: Yönetilen Kod Projesi İçin Kod Analizini Yapılandırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İçinde [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)] ve [!INCLUDE[vsPro](../includes/vspro-md.md)], Kod Analizi listesinden seçtiğiniz *kural kümeleri* yönetilen kod projesi için uygulanacak. Varsayılan kuralı Microsoft en az önerilen kurallar kümesidir. Başka bir kural bir proje veya Çözümdeki tüm projeleri kümesi uygulayabilirsiniz.  
  
> [!NOTE]
> ASP.NET Web uygulamaları için bir kural yapılandırma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Bir ASP.NET Web uygulaması için kod çözümlemesini yapılandırma](../code-quality/how-to-configure-code-analysis-for-an-aspnet-web-application.md).  
  
### <a name="to-configure-a-rule-set-for-a-net-framework-project"></a>.NET Framework projesi için bir kural yapılandırmak için  
  
1. İçinde **Çözüm Gezgini**, projeye tıklayın.  
  
2. Üzerinde **Çözümle** menüsünde tıklatın **için Kod Analizi yapılandırma** *ProjectName*.  
  
3. İçinde **yapılandırma** ve **Platform** listeleri, derleme yapılandırması ve hedef platform'a tıklayın.  
  
4. Seçili yapılandırma kullanarak proje oluşturulan her zaman, Kod Analizi çalıştırmak için seçin **etkinleştir (code_analysıs sabitini tanımlar) derlemede kod analizini** onay kutusu. Ayrıca kod analizini el ile açıp çalıştırabilirsiniz **Çözümle** menü ve tıklayarak **kod çözümlemeyi Çalıştır** *ProjectName*.  
  
5. Varsayılan olarak, Kod Analizi uyarıları otomatik olarak dış araçları tarafından oluşturulan kodu raporlamaz. Üretilen koddan gelen uyarıları görüntülemek için temizleyin **üretilen koddan gelen sonuçları Gizle** onay kutusu.  
  
    > [!NOTE]
    > Bu seçenek hataları ve Uyarıları formları ve şablonlar görüntülendiğinde kod çözümleme hataları ve Uyarıları üretilen koddan gelen engellemez. Hem görüntüleyebilir ve bir form veya şablon için kaynak kodunu korumak.  
  
6. İçinde **bu kural kümesini Çalıştır** listesinde, aşağıdakilerden birini yapın:  
  
    - Kullanmak istediğiniz bir kural kümesi tıklayın.  
  
    - Tıklayın  **\<Gözat … >** var olan bir özel kural kümesini belirlemek için listesinde değil.  
  
    - Bir özel kural kümesi tanımlar.  
  
         Daha fazla bilgi için [özel kural kümeleri oluşturma](../code-quality/creating-custom-code-analysis-rule-sets.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İzlenecek yol: Yapılandırma ve bir özel kural kullanarak ayarlayın](../code-quality/walkthrough-configuring-and-using-a-custom-rule-set.md)
