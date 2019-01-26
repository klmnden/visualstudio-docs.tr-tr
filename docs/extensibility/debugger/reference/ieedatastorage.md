---
title: IEEDataStorage | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEEDataStorage
helpviewer_keywords:
- IEEDataStorage interface
ms.assetid: 704e932d-2325-410e-89c4-ce88c6ec19da
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2bc409f455d93b84b12b9630a5f72f8e82a752d7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54930978"
---
# <a name="ieedatastorage"></a>IEEDataStorage
Bu arabirim, bayt dizisini temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEEDataStorage : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 İfade değerlendirici (EE) bayt dizisini temsil etmek için bu arabirimi uygulayan (tür görselleştiricilerde almak ve verileri aracılığıyla değiştirmek için kullanılan [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) arabirimi). EE genellikle dış tür görselleştiricileri desteklemek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Yöntemlerde `IPropertyProxyEESide` tüm arabirimi bu arabirim döndürür. Çağrı [GetPropertyProxy](../../../extensibility/debugger/reference/ipropertyproxyprovider-getpropertyproxy.md) edinme [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) arabirimi. Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) almak için arabirimi [IPropertyProxyProvider](../../../extensibility/debugger/reference/ipropertyproxyprovider.md) arabirimi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 `IEEDataStorage` Arabirimi aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md)|Belirtilen arabellek için sağlanan veri bayt sayısını alır.|  
|[GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md)|Kullanılabilir veri bayt sayısını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, belirli bir nesne tarafından tutulan verilere erişmek için bir tür görselleştiricisi tarafından kullanılır. Veri yolu kullanıcıya sunmak için gerekli olan işlemek tür görselleştiricisi sağlayan bir bayt dizisi olarak değerlendirilir.  
  
 Genellikle özel Görüntüleyici özel bir arabirim kullanır ancak özel Görüntüleyici de bu arabirimi isterseniz kullanabilirsiniz [GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md) veya [GetStringChars](../../../extensibility/debugger/reference/idebugproperty3-getstringchars.md) (için dize odaklı veriler).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [Tür Görselleştiricisi ve Özel Görüntüleyici](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)