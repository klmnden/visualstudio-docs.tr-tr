---
title: Bağlam menüleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - context menus
ms.assetid: 44fd9e6a-6d42-4aba-80ba-f37fa0070f1d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 718afb23896f59acfd7eb4e1af60ba6b474de384
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54966249"
---
# <a name="context-menus"></a>Bağlam menüleri
Bağlam menüleri kullanıcı etkin bir istemci alanını bölgesinde tıkladığında görüntülenir ve farenin sağ düğmesi bırakıldığında temizleyin.  
  
## <a name="editor-context-menus"></a>Düzenleyici bağlam menüleri  
 Kesintiye tarafından `ECMD_SHOWCONTEXTMENU`, düzenleyicide görüntülenir bağlam menüleri, dil hizmeti denetleyebilirsiniz. Kendi bağlam menüsünü görüntülemek için oturum geçirildiğinde bu komutu işlemek, <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> çağırarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.ShowContextMenu%2A>. Bu komut işlememesi IDE düzenleyici için sağlanan standart bağlam menüsü görüntülenir. Bağlam menüsü işaret başına temelinde içeriğini de denetleyebilirsiniz. Bu konu hakkında daha fazla bilgi için bkz. [metin işaretçileri eski API'si ile kullanma](../extensibility/using-text-markers-with-the-legacy-api.md) ve [Intercept eski dil hizmeti komutlarını](../extensibility/internals/intercepting-legacy-language-service-commands.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Eski dil hizmeti geliştirme](../extensibility/internals/developing-a-legacy-language-service.md)   
 [Menüler ve komutlar genişletme](../extensibility/extending-menus-and-commands.md)