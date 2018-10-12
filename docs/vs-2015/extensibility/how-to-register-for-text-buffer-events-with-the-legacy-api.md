---
title: "Nasıl yapılır: metin arabelleği olayları eski API'si ile kaydolma | Microsoft Docs"
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - register for text buffer events
ms.assetid: 5fc00ced-882c-4b48-b46c-1fa5a2469f94
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 76b782e688c567eb3888b2dbc890a360d22e3014
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49232251"
---
# <a name="how-to-register-for-text-buffer-events-with-the-legacy-api"></a>Nasıl yapılır: metin arabelleği olayları eski API'si ile kaydolma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Metin arabelleği eski API'si aracılığıyla erişiyorsanız aşağıdaki yordamda gösterildiği gibi metin arabelleği olayları kaydolmalıdır.  
  
### <a name="to-advise-text-buffer-events"></a>Metin arabelleği olayları bildirmek için  
  
1.  Arabirimlerde birine bir işaretçiden <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>, çağrı `QueryInterface` işaretçisi için <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer>.  
  
2.  Çağrı <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer.FindConnectionPoint%2A> yöntemi ve kaydetmek istediğiniz olayların arabirimi kimliği geçirin.  
  
     Örneğin, kaydolmak istiyorsanız <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLinesEvents>, ardından bir arabirim kimliği, IID_IVsTextLinesEvents geçirin.  
  
     Metin arabelleği için bir işaretçi döndürür <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint> uygun bir bağlantı noktası nesne için arabirim.  
  
3.  Bu işaretçinin kullanarak, çağrı <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint.Advise%2A> yöntemi, bir işaretçiyi istediğiniz kaydetmek örneğin olaylar arabirimi uygulamanıza geçirmeden `IVsTextLinesEvents` arabirimi.  
  
     Ardından çağırarak olayları dinleyecek şekilde kullanabileceğiniz bir tanımlama bilgisi ortam döndürür <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint.Unadvise%2A> yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski API'deki Metin Arabelleği Olayları](../extensibility/text-buffer-events-in-the-legacy-api.md)

