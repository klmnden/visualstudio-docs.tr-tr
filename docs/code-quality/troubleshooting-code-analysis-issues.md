---
title: Kod Çözümleme Sorunlarını Giderme
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: troubleshooting
ms.assetid: 61c7e44d-2780-4df5-9bcb-49e40c1152fc
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 34fce91db15d484b140aee291f9abd915d9399d2
ms.sourcegitcommit: 159ed9d4f56cdc1dff2fd19d9dffafe77e46cd4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53738799"
---
# <a name="troubleshooting-code-analysis-issues"></a>Kod Çözümleme Sorunlarını Giderme
Bu konu aşağıdaki Visual Studio Kod Analizi sorunlarına yönelik sorun giderme bilgileri içerir.

-   [Bir Visual Studio 2010 kural kümesi olan önceki Visual Studio sürümlerinde yansıtılan olmayan değişiklikler](#ChildRuleSetChangesInPreviousVersions)

##  <a name="ChildRuleSetChangesInPreviousVersions"></a> Bir Visual Studio 2010 kural kümesi olan önceki Visual Studio sürümlerinde yansıtılan olmayan değişiklikler
 Bir kural kümesi oluşturduğunuzda [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] bir alt kural kümesi içeren, bir değişiklik alt kural kümesi için Kod Analizi yürütmeleri Visual Studio'nun önceki bir sürümünü kullanan bilgisayarlarda uygulanmayabilir. Bu sorunu çözmek için bir yeniden yazma alt kural kümesini içeren kural kümesi olan üst kural kümesinin zorlaması gerekir.

1. Açık üst kural kümesinde [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)].

2. Ekleme veya bir kuralı kaldırma gibi bir değişiklik yapın ve sonra kural kümesi kaydedin.

3. Kural kümesi yeniden, değişikliğini tersine çevirebilir ve kural kümesi yeniden kaydedin.

## <a name="see-also"></a>Ayrıca Bkz.
 [Uygulama kalitesini analiz etme](../code-quality/analyzing-application-quality-by-using-code-analysis-tools.md) [yönetilen kod kalitesini analiz etme](../code-quality/code-analysis-for-managed-code-overview.md) [kural kümeleri kullanma Kod Analizi kurallarını gruplandırmak için](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)