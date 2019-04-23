---
title: 'Nasıl yapılır: Geri alma yığını clear | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - clear undo stack
ms.assetid: 2200d2d4-7f58-401c-87fc-ddd32d368193
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1d6e7c2536b7c5556139ce7a9b56756e20fd3648
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60072870"
---
# <a name="how-to-clear-the-undo-stack"></a>Nasıl yapılır: Geri alma yığını Temizle
Aşağıdaki yordam, geri alma yığını temizlemek açıklanmaktadır.

## <a name="to-clear-the-undo-stack"></a>Geri alma yığını temizlemek için

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

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Uygulama geri alma yönetimi](../extensibility/how-to-implement-undo-management.md)