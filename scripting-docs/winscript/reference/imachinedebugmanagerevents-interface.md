---
title: Imachinedebugmanagerevents arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IMachineDebugManagerEvents interface
ms.assetid: 468de2f4-49e0-4f6f-ba0c-0f5f6832c092
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fcfcc2aed0fedefdc149b83e911d33cd3b54cdef
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58153129"
---
# <a name="imachinedebugmanagerevents-interface"></a>IMachineDebugManagerEvents Arabirimi
Sinyalleri çalışmasını değişiklikleri uygulama listesi Makine Hata Ayıklama Yöneticisi tarafından korunur. Bu arabirim, uygulamaların dinamik bir listesini görüntülemek için IDE hata ayıklayıcı tarafından kullanılabilir.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IMachineDebugManagerEvents` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IMachineDebugManagerEvents::onAddApplication](../../winscript/reference/imachinedebugmanagerevents-onaddapplication.md)|Çalışan bir uygulama eklendiğinde, olayı işleyen uygulama listesi.|  
|[IMachineDebugManagerEvents::onRemoveApplication](../../winscript/reference/imachinedebugmanagerevents-onremoveapplication.md)|Bir uygulamanın çalışmasını kaldırıldığında olayı işleyen uygulama listesi.|