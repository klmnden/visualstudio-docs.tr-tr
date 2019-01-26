---
title: IDebugProgramEngines2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgramEngines2
helpviewer_keywords:
- IDebugProgramEngines2 interface
ms.assetid: 53d648f0-6c11-4337-badd-c43f3872b62c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a383dc55b42fe8baad8df31628d0a182d50d554e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55025676"
---
# <a name="idebugprogramengines2"></a>IDebugProgramEngines2
Bu arabirim tarafından program düğümleri bu programda hata ayıklamak tüm olası hata ayıklama altyapısı (DE) belirtmek için kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProgramEngines2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bir DE veya özel bağlantı noktası sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) belirli bir program için kullanılacak belirli bir DE oluşturma desteklemek için.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugProgramNode2` arabirimi bu arabirim elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramEngines2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[EnumPossibleEngines](../../../extensibility/debugger/reference/idebugprogramengines2-enumpossibleengines.md)|Bu programda hata ayıklamak olası DEs gösterir.|  
|[SetEngine](../../../extensibility/debugger/reference/idebugprogramengines2-setengine.md)|Bu program hata ayıklama için kullanılacak DE seçer.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir DE kullanıcı tarafından seçilen sonra bu seçimi program düğümle çağırarak kayıtlı [SetEngine](../../../extensibility/debugger/reference/idebugprogramengines2-setengine.md). Seçili olan altyapı tarafından döndürülen altyapısı olur [GetEngineInfo](../../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [GetEngineInfo](../../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md)