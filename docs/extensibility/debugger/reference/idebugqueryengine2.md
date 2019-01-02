---
title: IDebugQueryEngine2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugQueryEngine2
helpviewer_keywords:
- IDebugQueryEngine2 interface
ms.assetid: 8f0e1838-a818-4459-9138-a3dceb7408de
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 0c16ae17f8914ee07662a3cd5580963de43f8b0d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53960034"
---
# <a name="idebugqueryengine2"></a>IDebugQueryEngine2
Bu arabirim, hata ayıklama Yöneticisi (SDM) hata ayıklama altyapısı (DE) temsil eden bir arabirim almak oturum sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugQueryEngine2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE en yaygın DE arabirimleri uygulayan nesneler üzerinde bu arabirimi uygulayan (gibi [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md), [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md), ve [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)) içinde erişime izin vermek için sipariş [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) DE arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [QueryInterface](/cpp/atl/queryinterface) bu arabirimi almak için tipik bir DE arabiriminde.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugQueryEngine2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetEngineInterface](../../../extensibility/debugger/reference/idebugqueryengine2-getengineinterface.md)|Özel hata ayıklama altyapısı (DE) arabirimini alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirimi uygulayan nesne genel uygulanır [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) nedensellik ilişkilerini zamana göre sıralı işlevleri aracılığıyla Adımlama; diğer bir deyişle, hata ayıklayıcı, bir işlev dışında olduğunda Adımlama desteklemek için arabirimi yürütülecek sonraki işlevi yığında önceki işlev ancak başka bir iş parçacığı bir işlevde tamamen olmayabilir. "Nedensellik ilişkilerini" tanımı için bkz [Visual Studio hata ayıklayıcısı sözlüğü](../../../extensibility/debugger/reference/visual-studio-debugger-glossary.md).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)