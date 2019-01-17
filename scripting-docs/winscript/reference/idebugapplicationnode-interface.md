---
title: Idebugapplicationnode arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationNode interface
ms.assetid: 30be3a97-8191-45ac-8706-3f7056c163d6
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d7bd38a0fbbdd596f6a1f6bb040190dddca78bf9
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349003"
---
# <a name="idebugapplicationnode-interface"></a>IDebugApplicationNode Arabirimi
`IDebugApplicationNode` Arabirimi işlevselliğini genişleten `IDebugDocumentProvider` proje ağacı içinde bir bağlam sağlayarak arabirimi.  
  
 Devralınan yöntemleri yanı sıra `IDebugDocumentProvider`, `IDebugApplicationNode` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplicationNode::EnumChildren](../../winscript/reference/idebugapplicationnode-enumchildren.md)|Bu uygulama düğümünün alt düğümleri numaralandırır.|  
|[IDebugApplicationNode::GetParent](../../winscript/reference/idebugapplicationnode-getparent.md)|Bu uygulama düğümü üst düğümünün döndürür.|  
|[IDebugApplicationNode::SetDocumentProvider](../../winscript/reference/idebugapplicationnode-setdocumentprovider.md)|Bu uygulama düğümü için belge sağlayıcısı ayarlar.|  
|[IDebugApplicationNode::Close](../../winscript/reference/idebugapplicationnode-close.md)|Tüm başvuruları bırakın ve etkin olmayan bir duruma girmek bu uygulamanın neden olur.|  
|[IDebugApplicationNode::Attach](../../winscript/reference/idebugapplicationnode-attach.md)|Bu uygulama düğümü belirtilen projeyi ağacına ekler.|  
|[IDebugApplicationNode::Detach](../../winscript/reference/idebugapplicationnode-detach.md)|Bu uygulama düğümü proje ağacından kaldırır.|