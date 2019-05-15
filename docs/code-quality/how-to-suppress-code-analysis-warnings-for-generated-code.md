---
title: Üretilen kod için Kod Analizi ihlallerini gösterme
ms.date: 05/13/2019
ms.topic: conceptual
ms.assetid: 3a96434e-d419-43a7-81ba-95cccac835b8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6a7990f5e9fa1893d8813b1307ab6a0a7fee46be
ms.sourcegitcommit: 77b4ca625674658d5c5766e684fa0e2a07cad4da
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65613562"
---
# <a name="how-to-suppress-code-analysis-warnings-for-generated-code"></a>Nasıl yapılır: Üretilen kod için kod analizi uyarılarını gizleme

Oluşturulan kod projenize yönetilen kod derleyicilerini veya üçüncü taraf araçları tarafından eklenen kodu içerir. Kod Analizi üretilen kodda bulur kural ihlalleri görmek isteyebilirsiniz. Ancak, görüntüleyin ve ihlalleri içerdiği kodu tutmak olduğundan, bunları görmek istemeyebilirsiniz.

**Üretilen koddan gelen sonuçları Gizle** onay kutusunu Kod Analizi özellik sayfasında projenin Kod Analizi uyarıları bir üçüncü taraf araç tarafından oluşturulan kodu gösterilip gösterilmeyeceğini seçmenize imkan tanır.

> [!NOTE]
> Bu seçenek hataları ve Uyarıları formları ve şablonlar görüntülendiğinde kod çözümleme hataları ve Uyarıları üretilen koddan gelen engellemez. Hem görüntüleyebilir ve bir form veya şablon için kaynak kodunu korumak.

### <a name="to-suppress-warnings-for-generated-code-in-a-project"></a>Bir projedeki üretilen kod için uyarıları bastırmak için

1. Projeye sağ **Çözüm Gezgini** ve ardından **özellikleri**.

2. Seçin **Kod Analizi** sekmesi.

3. Seçin **üretilen koddan gelen sonuçları Gizle** onay kutusu.

> [!NOTE]
> Yalnızca gelen statik kod analizi uyarıları gösterilmemesini sağlayabilirsiniz. Şu anda, kod çözümleme Uyarıları'ndan başlatmayı önleyemez [Çözümleyicileri](roslyn-analyzers-overview.md).