---
title: IDebugProcessQueryProperties | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugProcessQueryProperties
ms.assetid: ce29a248-81a0-42c0-99a7-1606e8c548ec
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5bfdca9a60061e2e519f0e98db9864ecae06b7c0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55021773"
---
# <a name="idebugprocessqueryproperties"></a>IDebugProcessQueryProperties
Bu arabirim tarafından uygulanan bir uzantı arabirimdir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) uygulayıcılar. Hata ayıklama işlem ortamı hakkında bilgi almak uygulayan sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProcessQueryProperties: IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama işlemi yürütme ortamı hakkında bilgi edinmek için bu arabirimi uygulayın.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProcessQueryProperties`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[QueryProperty](../../../extensibility/debugger/reference/idebugprocessqueryproperties-queryproperty.md)|Bir özellik değeri için sorgular.|  
|[QueryProperties](../../../extensibility/debugger/reference/idebugprocessqueryproperties-queryproperties.md)|Özellik değerleri için sorgular.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim nadiren uygulanır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Portpriv.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)