---
title: Bağlam menüleri | Microsoft Docs
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
- editors [Visual Studio SDK], legacy - context menus
ms.assetid: 44fd9e6a-6d42-4aba-80ba-f37fa0070f1d
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e4b53174776b93d94c38982a430db3213ba184b9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49207735"
---
# <a name="context-menus"></a>Bağlam Menüleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bağlam menüleri kullanıcı etkin bir istemci alanını bölgesinde tıkladığında görüntülenir ve farenin sağ düğmesi bırakıldığında temizleyin.  
  
## <a name="editor-context-menus"></a>Düzenleyici Bağlam Menüleri  
 Kesintiye tarafından `ECMD_SHOWCONTEXTMENU`, düzenleyicide görüntülenir bağlam menüleri, dil hizmeti denetleyebilirsiniz. Kendi bağlam menüsünü görüntülemek için oturum geçirildiğinde bu komutu işlemek, <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> çağırarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.ShowContextMenu%2A>. Bu komut işlememesi IDE düzenleyici için sağlanan standart bağlam menüsü görüntülenir. Bağlam menüsü işaret başına temelinde içeriğini de denetleyebilirsiniz. Bu konu hakkında daha fazla bilgi için bkz. [kullanarak metin işaretçileri eski API'siyle](../extensibility/using-text-markers-with-the-legacy-api.md) ve [kesintiye eski dil hizmeti komutlarını](../extensibility/internals/intercepting-legacy-language-service-commands.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski dil hizmeti geliştirme](../extensibility/internals/developing-a-legacy-language-service.md)   
 [Menüleri ve Komutlari Genişletme](../extensibility/extending-menus-and-commands.md)

