---
title: Eski dil hizmetinde otomatik biçimlendirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- language services, automatic formatting
ms.assetid: c210fc94-77bd-4694-b312-045087d8a549
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 89345c7cd466211292a21ec4ca99276ebf95d67a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53873554"
---
# <a name="automatic-formatting-in-a-legacy-language-service"></a>Eski dil hizmetinde otomatik biçimlendirme
Bir kullanıcı bir bilinen kod yapısı türüne başladığında otomatik biçimlendirme bir dil hizmeti otomatik olarak bir kod parçacığı ekler.  
  
## <a name="automatic-formatting-behavior"></a>Otomatik biçimlendirme davranışı  
 Örneğin, yazarken *varsa*dil hizmeti eşleşen küme ayraçlarını otomatik olarak ekler veya ENTER tuşuna basın, dil hizmeti noktasını yeni satırda uygun girinti düzeyine bağlı olarak, zorlar olup yeni bir kapsam önceki satır açılır.  
  
 Dil hizmeti geri kalanı için kullanılan komut filtresi, otomatik biçimlendirme için de kullanılabilir. Çağırarak eşleşen küme ayraçlarını vurgulayabilirsiniz <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.HighlightMatchingBrace%2A>.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Eski dil hizmeti geliştirme](../../extensibility/internals/developing-a-legacy-language-service.md)