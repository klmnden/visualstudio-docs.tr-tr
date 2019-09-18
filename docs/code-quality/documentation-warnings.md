---
title: Belge uyarıları
ms.date: 09/16/2019
ms.topic: reference
f1_keywords:
- vs.codeanalysis.documentationrules
helpviewer_keywords:
- documentation warnings
- managed code analysis warnings, documentation warnings
- warnings, documentation
author: mavasani
ms.author: mavasani
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 00b42dc20b228e30a9b2632a0525a1ec8a9ddbb1
ms.sourcegitcommit: 541a0556958201ad6626bc8638406ad02640f764
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2019
ms.locfileid: "71079200"
---
# <a name="documentation-warnings"></a>Belge uyarıları

Belge uyarıları, dışarıdan görülebilen API 'Ler için doğru [XML belge açıklamalarını](https://docs.microsoft.com/dotnet/csharp/codedoc) kullanarak iyi belgelenmiş kitaplıklar yazmayı destekler.

## <a name="in-this-section"></a>Bu bölümde

| Kural | Açıklama |
| - | - |
| [CA1200: Ön ek ile cref etiketlerini kullanmaktan kaçının](../code-quality/ca1200.md) | XML belgesi etiketindeki [cref](https://docs.microsoft.com/dotnet/csharp/programming-guide/xmldoc/cref-attribute) özniteliği "kod başvurusu" anlamına gelir. Etiketin iç metninin tür, yöntem veya özellik gibi bir kod öğesi olduğunu belirtir. Derleyicinin başvuruları doğrulamasını önlediği için ön ekleri olan etiketlerikullanmaktankaçının.`cref` Ayrıca, Visual Studio tümleşik geliştirme ortamının (IDE) yeniden düzenlemeler sırasında bu sembol başvurularını bulmasını ve güncelleştirmesini de önler. |

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Analizi uyarıları](../code-quality/code-analysis-for-managed-code-warnings.md)
