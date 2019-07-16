---
title: Eski dil hizmetinde otomatik biçimlendirme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- language services, automatic formatting
ms.assetid: c210fc94-77bd-4694-b312-045087d8a549
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e6183fc47138ebb5108e4fbbd2bfa407e5804a72
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68157265"
---
# <a name="automatic-formatting-in-a-legacy-language-service"></a>Eski Dil Hizmetinde Otomatik Biçimlendirme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir kullanıcı bir bilinen kod yapısı türüne başladığında otomatik biçimlendirme bir dil hizmeti otomatik olarak bir kod parçacığı ekler.  
  
## <a name="automatic-formatting-behavior"></a>Otomatik biçimlendirme davranışı  
 Örneğin, yazarken `if`dil hizmeti eşleşen küme ayraçlarını otomatik olarak ekler veya ENTER tuşuna basın, dil hizmeti noktasını yeni satırda uygun girinti düzeyine bağlı olarak zorlar önceki satırı yeni bir kapsam açılır.  
  
 Dil hizmeti geri kalanı için kullanılan komut filtresi, otomatik biçimlendirme için de kullanılabilir. Çağırarak eşleşen küme ayraçlarını vurgulayabilirsiniz <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.HighlightMatchingBrace%2A>.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski Dil Hizmeti Geliştirme](../../extensibility/internals/developing-a-legacy-language-service.md)
