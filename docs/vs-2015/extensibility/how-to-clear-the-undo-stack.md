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
ms.openlocfilehash: db77f93fd7f6af16b5358b75b6ffcd5927430653
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62549187"
---
# <a name="how-to-clear-the-undo-stack"></a>Nasıl yapılır: Geri alma yığını Temizle
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki yordam, geri alma yığını temizlemek açıklanmaktadır.  
  
### <a name="to-clear-the-undo-stack"></a>Geri alma yığını temizlemek için  
  
1. Geri alma yığını kullanımını temizlemek için [IOleUndoManager::DiscardFrom](/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-discardfrom) yöntemi. Bunun bir örneği verilmiştir:  
  
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
 [Nasıl yapılır: Geri Alma Yönetimi Uygulama](../extensibility/how-to-implement-undo-management.md)
