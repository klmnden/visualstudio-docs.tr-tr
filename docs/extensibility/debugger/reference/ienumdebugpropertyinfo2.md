---
title: IEnumDebugPropertyInfo2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugPropertyInfo2
helpviewer_keywords:
- IEnumDebugPropertyInfo2
ms.assetid: fdea8262-40b8-473e-88ba-639e4c4648e6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0eecb16ce4eecf4e39163a82c3aed48d35db6af2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54933977"
---
# <a name="ienumdebugpropertyinfo2"></a>IEnumDebugPropertyInfo2
Bu arabirim numaralandırır [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) yapıları.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugPropertyInfo2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE), belirli bir özellik için bilgi göstermek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) belirli bir özellik alt öğelerini temsil eden bu arabirimi elde edilir. Çağrı [EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md) özelliklerini belirli bir yığın çerçevesini temsil eden bu arabirimi elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugPropertyInfo2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2-next.md)|Belirtilen sayıda alır [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) yapıları, bir sabit listesi sırası.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2-skip.md)|Belirtilen sayıda atlar [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) yapıları, bir sabit listesi sırası.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2-getcount.md)|Sayısını alır [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) yapılarda bir numaralandırıcı.|  
  
## <a name="remarks"></a>Açıklamalar  
 Genel olarak, ilişkili özellik nesne veya yığın çerçevesi için uygun diğer bilgilerin yanı sıra, ad, değer, adres ve tür ekleyebilirsiniz bilgi hiyerarşisini özelliğidir. Bkz: [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) daha fazla ayrıntı için.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md)   
 [EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md)