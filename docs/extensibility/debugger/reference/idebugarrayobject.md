---
title: IDebugArrayObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugArrayObject
helpviewer_keywords:
- IDebugArrayObject method
ms.assetid: a1c8e77e-dee1-4748-a516-6ab032a8f54f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a35aa8dd85cbcd6d04e30fc88b0595151624ba42
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55037661"
---
# <a name="idebugarrayobject"></a>IDebugArrayObject
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Bu arabirim, bir dizi nesnesi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugArrayObject : IDebugObject  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 İfade değerlendirici bir diziyi temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) kullanarak arabirimi bu arabirim edinebilirsiniz [QueryInterface](/cpp/atl/queryinterface) nesne dizisi temsil ediyorsa.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemlere ek olarak `IDebugObject` arabirimi aşağıdaki yöntemleri üzerinde uygulanır `IDebugArrayObject` arabirimi.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetCount](../../../extensibility/debugger/reference/idebugarrayobject-getcount.md)|Dizideki öğe sayısını alır.|  
|[GetElement](../../../extensibility/debugger/reference/idebugarrayobject-getelement.md)|Bir dizideki öğe alır.|  
|[GetElements](../../../extensibility/debugger/reference/idebugarrayobject-getelements.md)|Dizinin tüm öğeleri alır.|  
|[GetRank](../../../extensibility/debugger/reference/idebugarrayobject-getrank.md)|Dizi boyut sayısını alır.|  
|[GetDimensions](../../../extensibility/debugger/reference/idebugarrayobject-getdimensions.md)|Dizinin boyut sayısını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 İfade değerlendiricisi, ayrıştırma ağacı dizilerde temsil etmek için bu arabirimi kullanır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: ee.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)