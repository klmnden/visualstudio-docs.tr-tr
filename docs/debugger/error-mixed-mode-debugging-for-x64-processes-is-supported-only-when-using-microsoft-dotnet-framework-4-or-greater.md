---
title: 'Hata: Karışık mod hata ayıklama için işlemler, yalnızca Microsoft .NET Framework 4 kullanılırken desteklenir x64 veya büyük | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.interop_unsupported_x64
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 1423cbcfcae53948f7b9c9cd52eb90f57251bc24
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62851063"
---
# <a name="error-mixed-mode-debugging-for-x64-processes-is-supported-only-when-using-microsoft-net-framework-4-or-greater"></a>Hata: x64 işlemleri için karışık modda hata ayıklama yalnızca Microsoft .NET Framework 4 veya daha yenisi kullanılırken desteklenir
Bir 64-bit işlem içinde karma yerel ve yönetilen kodda hata ayıklamak için olmalıdır [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] sürüm 4. İle 64-bit işlemlerinin karışık mod hata ayıklama [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] sürümleri daha önce 4 desteklenmez.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

- Aşağıdaki adımlardan birini uygulayın:

  - Yükseltme, [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] sürüm 4.

  - Hata ayıklama için uygulamanızın bir 32-bit sürümünü oluşturun.

## <a name="see-also"></a>Ayrıca Bkz.
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)