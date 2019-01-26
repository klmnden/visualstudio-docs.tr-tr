---
title: IPropertyProxyEESide | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IPropertyProxyEESide
helpviewer_keywords:
- IPropertyProxyEESide interface
ms.assetid: cf227cf8-39d9-4758-8f7e-a697aebb1926
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 69f67bcba200d5b2a12544f7405fca04f5106e5f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54954078"
---
# <a name="ipropertyproxyeeside"></a>IPropertyProxyEESide
Bu arabirim, ilişkili nesne verilerini görüntülemek için yöntemler sağlar. Bu arabirim tür görselleştiricileri desteğinin bir parçasıdır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IPropertyProxyEESide : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 İfade değerlendiricisi tür görselleştiricileri desteklemek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [GetPropertyProxy](../../../extensibility/debugger/reference/ipropertyproxyprovider-getpropertyproxy.md) bu arabirimi elde edilir. Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) almak için arabirimi [IPropertyProxyProvider](../../../extensibility/debugger/reference/ipropertyproxyprovider.md) arabirimi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki yöntemleri bu arabirim tarafından uygulanır:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[InitSourceDataProvider](../../../extensibility/debugger/reference/ipropertyproxyeeside-initsourcedataprovider.md)|Böylece nesnenin verilere erişilebilir bir veri kaynağı sağlayıcı başlatır.|  
|[GetManagedViewerCreationData](../../../extensibility/debugger/reference/ipropertyproxyeeside-getmanagedviewercreationdata.md)|Nesnenin derleme hakkındaki bilgileri alır.|  
|[GetInitialData](../../../extensibility/debugger/reference/ipropertyproxyeeside-getinitialdata.md)|Nesne için ilk veri alır.|  
|[CreateReplacementObject](../../../extensibility/debugger/reference/ipropertyproxyeeside-createreplacementobject.md)|Mevcut bir veri deposunun kopyasını oluşturur.|  
|[InPlaceUpdateObject](../../../extensibility/debugger/reference/ipropertyproxyeeside-inplaceupdateobject.md)|Mevcut bir veri depolama için bir başvuru oluşturur.|  
|[ResolveAssemblyRef](../../../extensibility/debugger/reference/ipropertyproxyeeside-resolveassemblyref.md)|Bu nesneyi içeren derlemenin bağlam içinde belirli bir derleme hakkındaki bilgileri alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tür görselleştiricisi bu arabirimi bu arabirim, bir parçasıdır nesneyle ilişkili değerlere erişmek için kullanır. Üzerinden erişilen verileri [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) veri salt okunur bir görünümünü sunan arabirimi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [Tür görselleştiricisi ve özel Görüntüleyici](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)