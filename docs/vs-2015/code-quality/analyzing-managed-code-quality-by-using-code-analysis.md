---
title: Kod çözümlemesi ile yönetilen kod kalitesini analiz etme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- code analysis,managed code
- managed code analyis
ms.assetid: 68510a55-da51-4381-81a5-0feba76b8b4f
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 5d8740b79b026ade7f3da19aa4a89cacd94df17d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68157131"
---
# <a name="analyzing-managed-code-quality-by-using-code-analysis"></a>Kod Çözümlemesi ile Yönetilen Kod Kalitesini Çözümleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Güvenli olmayan veri erişimi ve kullanım ihlallerine tasarım sorunları gibi kodunuzdaki olası sorunları bulmak için Visual Studio'da kod çözümleme araçları kullanabilirsiniz. Kod Analizi, .NET Framework, yerel (C ve C++) ve veritabanı uygulamaları üzerinde çalışır. Yönetilen kod için Kod Analizi kuralları düzenler *kural kümeleri* hedefleyen belirli sorunları kodlama.  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Ortak Görevler|Destekleyici İçerik|  
|------------------|------------------------|  
|**Uygulamalı alıştırma alın:** Basit bir .NET Framework uygulamasında hataları düzelterek kod analysis temellerini öğrenin.|-   [İzlenecek yol: Kod kusurları için yönetilen kodu analiz etme](../code-quality/walkthrough-analyzing-managed-code-for-code-defects.md)|  
|**Bir proje için Kod Analizi yapılandırın:** Yönetilen kod için kuralları, güvenlik ve tasarım gibi belirli alanları hedef kural kümeleri halinde düzenlenir. Microsoft Standart kural ayarlar veya kendinizinkini oluşturun birini kullanabilirsiniz.|-   [Yönetilen kod genel bakış için Kod Analizi](../code-quality/code-analysis-for-managed-code-overview.md)<br />-   [Kod Analizi kurallarını gruplandırmak için kural kullanarak ayarlar](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)<br />-   [SuppressMessage özniteliğini kullanarak uyarıları bastırma](../code-quality/suppress-warnings-by-using-the-suppressmessage-attribute.md)|  
|**Kod analizini çalıştır:** Bir proje yapılandırması oluşturulan her zaman otomatik olarak çalıştırılacak Kod Analizi belirtebilirsiniz ve Kod Analizi proje üzerinde el ile çalıştırabilirsiniz.|-   [Nasıl Yapılır: Etkinleştirme ve otomatik kod analizini devre dışı](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md)<br />-   [Nasıl Yapılır: Kod çözümlemesini elle çalıştırma](../code-quality/how-to-run-code-analysis-manually-for-managed-code.md)|  
|**Kod Analizi sonuçlarını çözümleyin:** Kod Analizi uyarıları ve hataları Kod Analizi penceresinde listelenir. Bir uyarı veya hata başlığı, uyarı hakkında ek bilgi görüntülemek ve görüntülemek ve kural harekete geçirilen kaynak kod satırı vurgulamak için seçebilirsiniz. Bilgileri ve sorunu çözmek örnekleri içerir MSDN Kitaplığı'nda ayrıntılı bilgileri görüntülemek için uyarı kimliği seçebilirsiniz.|-   [Nasıl Yapılır: Yönetilen kod kusurlarını görüntüleme](../code-quality/how-to-view-managed-code-defects.md)<br />-   [Yönetilen kod uyarıları için Kod Analizi](../code-quality/code-analysis-for-managed-code-warnings.md)<br />-   [Checkıd uyarıları](../code-quality/code-analysis-warnings-for-managed-code-by-checkid.md)<br />-   [Anonim metotlar ve kod çözümleme](../code-quality/anonymous-methods-and-code-analysis.md)|  
|**Kod analizini, geliştirme yaşam döngüsü ile tümleştirme:** İade ilkelerini [!INCLUDE[esprscc](../includes/esprscc-md.md)] etkinleştir geliştirme ekipleri tüm iade kod emin olmak için Kod Analizi standartları ortak bir dizi karşılamak. Kod Analizi kural ihlali için iş öğesi oluşturma Hata Listesi penceresindeki yapabilmek için basit bir yordamdır.|-   [Takım projesi iade ilkeleri ile kod kalitesini arttırma](../code-quality/enhancing-code-quality-with-team-project-check-in-policies.md)<br />-   [Nasıl Yapılır: İade takım projesi ilkesiyle kod proje kural kümelerini eşitleme](../code-quality/how-to-synchronize-code-project-rule-sets-with-team-project-check-in-policy.md)<br />-   [Nasıl Yapılır: Yönetilen kod hatası için iş öğesi oluşturma](../code-quality/how-to-create-a-work-item-for-a-managed-code-defect.md)|
