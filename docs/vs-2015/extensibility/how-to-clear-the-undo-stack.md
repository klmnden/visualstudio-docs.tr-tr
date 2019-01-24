---
title: 'Nasıl yapılır: Geri alma yığını clear | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - clear undo stack
ms.assetid: 2200d2d4-7f58-401c-87fc-ddd32d368193
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: fca0726d8a85ddcaf3df98d4a34b11d83c9b8183
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753999"
---
# <a name="how-to-clear-the-undo-stack"></a>Nasıl yapılır: Geri alma yığını Temizle
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki yordam, geri alma yığını temizlemek açıklanmaktadır.  
  
### <a name="to-clear-the-undo-stack"></a>Geri alma yığını temizlemek için  
  
1.  Geri alma yığını kullanımını temizlemek için [IOleUndoManager::DiscardFrom](http://msdn.microsoft.com/library/windows/desktop/ms693799) yöntemi. Bunun bir örneği verilmiştir:  
  
    ```  
    HRESULT CCmdWindow::ClearUndoStack()  
    {  
      HRESULT hr = S_OK;  
  
      if (m_pUndoMgr == NULL)  
        {  
        IfFailGo(m_pTextLines->GetUndoManager(&m_pUndoMgr));  
        ASSERT(m_pUndoMgr != NULL, "",;);  
        }  
  
      IfFailGo(m_pUndoMgr->DiscardFrom(NULL));  
  
    Error:  
      return hr;  
    }  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Uygulama geri alma yönetimi](../extensibility/how-to-implement-undo-management.md)
