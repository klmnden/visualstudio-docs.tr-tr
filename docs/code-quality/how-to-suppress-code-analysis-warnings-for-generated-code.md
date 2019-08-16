---
title: Üretilen kod için kod analizi ihlallerini gösterme
ms.date: 05/13/2019
ms.topic: conceptual
ms.assetid: 3a96434e-d419-43a7-81ba-95cccac835b8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6ee4e3df94e46b4d3cc996a23fc1e40401195e21
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551127"
---
# <a name="how-to-suppress-code-analysis-warnings-for-generated-code"></a>Nasıl yapılır: Üretilen kod için kod analizi uyarılarını gizleme

Oluşturulan kod, yönetilen kod derleyicileri veya üçüncü taraf araçları tarafından projenize eklenen kodu içerir. Kod analizinin üretilen kodda bulduğu kural ihlallerini görmek isteyebilirsiniz. Ancak, ihlalleri içeren kodu görüntüleyemediğinden ve koruyabileceğinizden, bunları görmek istemeyebilirsiniz.

Bir projenin kod analizi özelliği sayfasında, **üretilen koddan sonuçları gösterme** onay kutusu, üçüncü taraf bir araç tarafından oluşturulan koddan kod analizi uyarılarını gösterip göstermeyeceğinizi seçmenize olanak sağlar.

> [!NOTE]
> Bu seçenek hataları ve Uyarıları formları ve şablonlar görüntülendiğinde kod çözümleme hataları ve Uyarıları üretilen koddan gelen engellemez. Bir form veya şablon için kaynak kodu görüntüleyebilir ve bakımını yapabilirsiniz.

### <a name="to-suppress-warnings-for-generated-code-in-a-project"></a>Bir projede oluşturulan koda yönelik uyarıları gizlemek için

1. **Çözüm Gezgini** ' de projeye sağ tıklayın ve ardından **Özellikler**' e tıklayın.

2. **Kod Analizi** sekmesini seçin.

3. **Oluşturulan koddan sonuçları bastır** onay kutusunu seçin.

> [!NOTE]
> Yalnızca eski analizden gelen uyarıları gizleyebilirsiniz. Şu anda çözümleyicilerin kod analizi uyarılarını gizlenemez. [](roslyn-analyzers-overview.md)