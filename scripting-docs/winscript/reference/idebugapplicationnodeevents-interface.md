---
title: Idebugapplicationnodeevents arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationNodeEvents interface
ms.assetid: 02e0bb17-84ce-458b-bae6-608a9899e535
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7412e258c7f67f44bde6f69b593a1eecb1d84e07
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62822281"
---
# <a name="idebugapplicationnodeevents-interface"></a>IDebugApplicationNodeEvents Arabirimi
Olay arabirimi sağlayan `IDebugApplicationNode` arabirimi.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugApplicationNodeEvents` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplicationNodeEvents::onAddChild](../../winscript/reference/idebugapplicationnodeevents-onaddchild.md)|Bir hata ayıklama uygulama düğüm nesnesi için bir alt düğüm eklendiğinde olayını işler.|  
|[IDebugApplicationNodeEvents::onRemoveChild](../../winscript/reference/idebugapplicationnodeevents-onremovechild.md)|Hata ayıklama uygulama düğüm nesnesinden bir alt düğüm kaldırıldığında olayını işler.|  
|[IDebugApplicationNodeEvents::onDetach](../../winscript/reference/idebugapplicationnodeevents-ondetach.md)|Hata ayıklama uygulama düğüm nesnesi bir üst düğümden kullanımdan çıkarılmamış gösteren bir olayını işler.|  
|[IDebugApplicationNodeEvents::onAttach](../../winscript/reference/idebugapplicationnodeevents-onattach.md)|Hata ayıklama uygulama düğüm nesnesi bir üst düğüme iliştirildiği gösteren bir olayını işler.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationNode Arabirimi](../../winscript/reference/idebugapplicationnode-interface.md)