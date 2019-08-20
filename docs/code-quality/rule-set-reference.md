---
title: Kod çözümleme kural kümesi başvurusu
ms.date: 04/04/2018
ms.topic: reference
helpviewer_keywords:
- code analysis, rule sets reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0222dab568ce421c3bd87474b956c82aab4d2683
ms.sourcegitcommit: b83fefa8177c5554cbe2c59c4d102cbc534f7cc6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2019
ms.locfileid: "69585245"
---
# <a name="code-analysis-rule-set-reference"></a>Kod analizi kural kümesi başvurusu

Visual Studio 'da yönetilen kod projeleri için eski analizler yapılandırdığınızda, yerleşik *kural kümeleri*listesinden seçim yapabilirsiniz. Bazı kurallar yerleşik kural kümelerinden birine dahildir. Örneğin, temel doğruluk kuralları kural kümesi, Yönetilen Önerilen Kurallar kural kümesindeki kuralları içerir.

> [!NOTE]
> Bu bölümdeki kural kümeleri eski Analize aittir. Kod Çözümleyicisi paketleri için kullanılabilen kural kümeleri hakkında daha fazla bilgi için bkz. [kural kümelerini kod Çözümleyicileri Ile kullanma](analyzer-rule-sets.md).

Ya da bu yerleşik kural kümelerinden birini kullanabilir veya yapabilecekleriniz [bir kural kümesi özelleştirme](../code-quality/how-to-create-a-custom-rule-set.md) proje gereksinimlerinizi karşılayacak şekilde. Özel bir kural kümesinde aynı kuralı içeren birden çok kural kümesi eklerseniz, bu kural özel kural kümesinde yalnızca bir kez görünür.

Bu bölümdeki konular, yerleşik kuralı açıklayın kümeleri ve kurallar (veya uyarılar) içerirler.

| Kural kümesi | Dahil edilen kurallar |
| - | - |
| [Tüm kurallar](all-rules-rule-set.md) | Tüm kullanılabilir yönetilen ve C++ kuralları içerir |
| [Temel doğruluk kuralları](basic-correctness-rules-rule-set-for-managed-code.md) | Mantık hataları ve çerçeve kullanımı için yönetilen önerilen kuralları ve kuralları içerir |
| [Genişletilmiş doğruluk kuralları](extended-correctness-rules-rule-set-for-managed-code.md) | Temel doğruluk kurallarını (Yönetilen Önerilen kuralları içerir) ve mantık hataları ve çerçeve kullanımı için daha fazla kuralı içerir |
| [Temel tasarım kılavuzu kuralları](basic-design-guideline-rules-rule-set-for-managed-code.md) | , Kodun okunmasını, anlaşılmasını ve bakımını kolaylaştırmak için yönetilen önerilen kuralları ve kuralları içerir |
| [Genişletilmiş tasarım yönergeleri kuralları](extended-design-guidelines-rules-rule-set-for-managed-code.md) | Temel tasarım kılavuz kuralları (Yönetilen Önerilen kuralları içerir) ve adlandırmaya odaklanabilecek daha fazla bakım kuralı içerir |
| [Genelleştirme kuralları](globalization-rules-rule-set-for-managed-code.md) | Genelleştirme sorunları için kuralları içerir |
| [Yönetilen minimum kurallar](managed-minimum-rules-rule-set-for-managed-code.md) | Kritik yönetilen kod sorunları için dört kural içerir |
| [Yönetilen Önerilen Kurallar](managed-recommended-rules-rule-set-for-managed-code.md) | Yönetilen minimum kuralların yanı sıra kritik yönetilen kod sorunları için daha fazla kural içerir |
| [Karışık minimum kurallar](mixed-minimum-rules-rule-set.md) | CLR C++ kodunda kritik sorunlara yönelik kurallar içerir |
| [Önerilen karma kurallar](mixed-recommended-rules-rule-set.md) | Karma minimum kuralların yanı sıra CLR C++ kodunda kritik sorunlar için daha fazla kural içerir |
| [Yerel minimum kurallar](native-minimum-rules-rule-set.md) | Yerel koddaki kritik sorunlara yönelik kurallar içerir |
| [Yerel önerilen kurallar](native-recommended-rules-rule-set.md) | Yerel en düşük kuralları ve yerel koddaki kritik sorunlar için daha fazla kuralı içerir |
| [Güvenlik kuralları](security-rules-rule-set-for-managed-code.md) | Güvenlik açıklarını bulmaya yönelik kuralları içerir |