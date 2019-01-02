---
title: IDebugPointerObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPointerObject
helpviewer_keywords:
- IDebugPointerObject interface
ms.assetid: 257fa167-b46e-4ffb-9a12-272efbf26702
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ea5c75c1fb2737459107b21652aa43b8ea38e526
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53844701"
---
# <a name="idebugpointerobject"></a>IDebugPointerObject
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Bu arabirim işaretçisi nesnenin temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPointerObject : IDebugObject  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 İfade değerlendirici bir işaretçi nesnesinin temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) kullanarak arabirimi bu arabirim edinebilirsiniz [QueryInterface](/cpp/atl/queryinterface) varsa `IDebugObject` bir işaretçiyi temsil eder.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Devralınan yöntemleri yanı sıra [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md), `IDebugPointerObject` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Dereference](../../../extensibility/debugger/reference/idebugpointerobject-dereference.md)|Arabirim işaret ettiği nesnesini alır.|  
|[GetBytes](../../../extensibility/debugger/reference/idebugpointerobject-getbytes.md)|Arabirim arka arkaya bir bayt serisi işaret ettiği değer alır.|  
|[SetBytes](../../../extensibility/debugger/reference/idebugpointerobject-setbytes.md)|Arabirim arka arkaya bir bayt dizisinden işaret ettiği değer ayarlar.|  
  
## <a name="remarks"></a>Açıklamalar  
 İfade değerlendiricisi, ayrıştırma ağacı bir işaretçiyi göstermek için bu arabirimi kullanır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: ee.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İfade değerlendirme arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)