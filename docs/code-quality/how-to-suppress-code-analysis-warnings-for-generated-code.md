---
title: 'Nasıl yapılır: Üretilen Kod İçin Kod Analizi Uyarılarını Gizleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 3a96434e-d419-43a7-81ba-95cccac835b8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c2d58ea5d23ed8b302b6ec2a0352f23b0eeeff66
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60066526"
---
# <a name="how-to-suppress-code-analysis-warnings-for-generated-code"></a>Nasıl yapılır: Üretilen Kod İçin Kod Analizi Uyarılarını Gizleme
Yönetilen kod derleyiciler genellikle hızlı kod geliştirilmesini sağlamak üzere bir projeye eklenen kod oluşturur. Ayrıca, geliştiriciler genellikle üçüncü taraf araçları uygulamaları hızla geliştirmenizi yardımcı olması için kullanın. Bu araçlar ayrıca projesine eklenen kod oluşturur.

 Kod Analizi üretilen kodda bulur kural ihlalleri görmek isteyebilirsiniz. Ancak, görüntülemek ve ihlalin içerdiği kodu korumak görmek istemeyebilirsiniz.

 **Üretilen koddan gelen sonuçları Gizle** Kod Analizi özellik sayfasında projenin onay kutusu, bir üçüncü taraf araç tarafından üretilen koddan Kod Analizi uyarıları görmek isteyip istemediğinizi seçmenizi sağlar.

> [!NOTE]
>  Bu seçenek hataları ve Uyarıları formları ve şablonlar görüntülendiğinde Kod Analizi hataları ve Uyarıları üretilen koddan gelen engellemez. Hem görüntüleyebilir ve bir form veya şablon için kaynak kodunu korumak.

### <a name="to-suppress-warnings-for-generated-code-in-a-project"></a>Bir projedeki üretilen kod için uyarıları bastırmak için

1. Çözüm Gezgini'nde projeye sağ tıklayın ve ardından **özellikleri**.

2. Tıklayın **Kod Analizi**.

3. Seçin **üretilen koddan gelen sonuçları Gizle** onay kutusu.