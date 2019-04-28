---
title: Kod Analizi Sorunlarını Giderme
ms.date: 11/04/2016
ms.topic: troubleshooting
ms.assetid: 61c7e44d-2780-4df5-9bcb-49e40c1152fc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 936428b82e721a1df6003a4bb0eecefe5b696b4c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62825357"
---
# <a name="troubleshooting-code-analysis-issues"></a>Kod Analizi Sorunlarını Giderme
Bu konu aşağıdaki Visual Studio Kod Analizi sorunlarına yönelik sorun giderme bilgileri içerir.

- [Bir Visual Studio 2010 kural kümesi olan önceki Visual Studio sürümlerinde yansıtılan olmayan değişiklikler](#ChildRuleSetChangesInPreviousVersions)

## <a name="ChildRuleSetChangesInPreviousVersions"></a> Bir Visual Studio 2010 kural kümesi olan önceki Visual Studio sürümlerinde yansıtılan olmayan değişiklikler
 Bir kural kümesi oluşturduğunuzda [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] bir alt kural kümesi içeren, bir değişiklik alt kural kümesi için Kod Analizi yürütmeleri Visual Studio'nun önceki bir sürümünü kullanan bilgisayarlarda uygulanmayabilir. Bu sorunu çözmek için bir yeniden yazma alt kural kümesini içeren kural kümesi olan üst kural kümesinin zorlaması gerekir.

1. Açık üst kural kümesinde [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)].

2. Ekleme veya bir kuralı kaldırma gibi bir değişiklik yapın ve sonra kural kümesi kaydedin.

3. Kural kümesi yeniden, değişikliğini tersine çevirebilir ve kural kümesi yeniden kaydedin.

## <a name="see-also"></a>Ayrıca Bkz.

- [Uygulama Kalitesini Analiz Etme](../code-quality/code-analysis-for-managed-code-overview.md)
- [Yönetilen Kod Kalitesini Analiz Etme](../code-quality/code-analysis-for-managed-code-overview.md)
- [Kod Analizi Kurallarını Gruplandırmak için Kural Kümeleri Kullanma](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)