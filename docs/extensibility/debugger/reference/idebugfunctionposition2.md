---
title: IDebugFunctionPosition2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugFunctionPosition2
helpviewer_keywords:
- IDebugFunctionPosition2 interface
ms.assetid: a835f65b-91b0-48ad-8485-04534c814b1b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 61fd298b1bbbf28f7a7fe514a01dc5707c35e04b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53840940"
---
# <a name="idebugfunctionposition2"></a>IDebugFunctionPosition2
Bu arabirim, kaynak belgedeki bir işlevin soyut bir konumu temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugFunctionPosition2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE), bir işlevin bir kaynak belge içindeki konumunu göstermek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirimin bir parçası olarak sağlanan bir [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) birleşim (özellikle bir [BP_LOCATION_CODE_FUNC_OFFSET](../../../extensibility/debugger/reference/bp-location-code-func-offset.md) yapısı) sırayla parçası olan [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) bekleyen kesme noktası oluşturmak için kullanılan yapısı.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugFunctionPosition2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetFunctionName](../../../extensibility/debugger/reference/idebugfunctionposition2-getfunctionname.md)|Bu konumun göreli olduğu işlevin adını alır.|  
|[GetOffset](../../../extensibility/debugger/reference/idebugfunctionposition2-getoffset.md)|İşlev başından uzaklık alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim tarafından temsil edilen konumu, özellikle, metin tabanlı bir [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) yapısı.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [BP_LOCATION_CODE_FUNC_OFFSET](../../../extensibility/debugger/reference/bp-location-code-func-offset.md)   
 [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)   
 [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)