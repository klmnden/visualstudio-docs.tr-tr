---
title: "Nasıl yapılır: Metin arabelleği olayları eski API'si ile kaydolma | Microsoft Docs"
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - register for text buffer events
ms.assetid: 5fc00ced-882c-4b48-b46c-1fa5a2469f94
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ce88836b8162da76e8b4ef330a179680af24f992
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56702479"
---
# <a name="how-to-register-for-text-buffer-events-with-the-legacy-api"></a>Nasıl yapılır: Metin arabelleği olayları eski API'si ile kaydolun
Metin arabelleği eski API'si aracılığıyla erişiyorsanız aşağıdaki yordamda gösterildiği gibi metin arabelleği olayları kaydolmalıdır.

## <a name="to-advise-text-buffer-events"></a>Metin arabelleği olayları bildirmek için

1.  Arabirimlerde birine bir işaretçiden <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>, çağrı `QueryInterface` işaretçisi için <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer>.

2.  Çağrı <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer.FindConnectionPoint%2A> yöntemi ve kaydetmek istediğiniz olayların arabirimi kimliği geçirin.

     Örneğin, kaydolmak istiyorsanız <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLinesEvents>, ardından bir arabirim kimliği, IID_IVsTextLinesEvents geçirin.

     Metin arabelleği için bir işaretçi döndürür <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint> uygun bir bağlantı noktası nesne için arabirim.

3.  Bu işaretçinin kullanarak, çağrı <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint.Advise%2A> yöntemi, bir işaretçiyi istediğiniz kaydetmek örneğin olaylar arabirimi uygulamanıza geçirmeden `IVsTextLinesEvents` arabirimi.

     Ardından çağırarak olayları dinleyecek şekilde kullanabileceğiniz bir tanımlama bilgisi ortam döndürür <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint.Unadvise%2A> yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [Metin arabelleği olayları eski API](../extensibility/text-buffer-events-in-the-legacy-api.md)