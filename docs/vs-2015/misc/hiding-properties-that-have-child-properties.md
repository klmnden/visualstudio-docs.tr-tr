---
title: Alt özellikleri olan özellikleri gizleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- properties [Visual Studio SDK], hiding
- Properties window, hiding properties that have child properties
ms.assetid: 6003607e-fc19-4bf9-a299-9f6adf8e92eb
caps.latest.revision: 13
manager: jillfra
ms.openlocfilehash: 1d20b865c6f07d76320a7df8402810c82869ddfb
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60052369"
---
# <a name="hiding-properties-that-have-child-properties"></a>Alt özellikleri olan özellikleri gizleme
Alt özellikleri taşıyan özellikler gizlemek isteyebilirsiniz:  
  
- Burada ana proje bazı yönlerini alt projeyi program aracılığıyla denetimleri iç içe projeler varsa.  
  
- Varsa bir denetimi ile özel bir tasarımcı kullanın ve geliştiriciler, denetimin tüm özelliklerini tam erişim vermek istiyor musunuz.  
  
- Varsa bir nesnenin kapsamı sahiplik ve özellikleri görünümünü sınırlamak istiyorsunuz.  
  
### <a name="to-hide-properties-that-have-child-properties"></a>Alt özellikleri taşıyan özellikler gizlemek için  
  
1. Ayarlama `pfDisplay` parametresinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.DisplayChildProperties%2A> için `FALSE`.  
  
2. Ayarlama `pfHide` parametresinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.HideProperty%2A> için `TRUE`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özellikler Görüntü Kılavuzu](../extensibility/internals/properties-display-grid.md)