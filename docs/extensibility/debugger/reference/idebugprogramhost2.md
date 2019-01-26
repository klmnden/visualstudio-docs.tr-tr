---
title: IDebugProgramHost2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgramHost2
helpviewer_keywords:
- IDebugProgramHost2 interface
ms.assetid: 2c37b3aa-97a9-4665-8709-edd917f18cb1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fa165aba25b46cab554517c55eb4e9bc174f7b94
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54990751"
---
# <a name="idebugprogramhost2"></a>IDebugProgramHost2
Bu arabirim bir programla ilgili konak (işlem) bilgi sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProgramHost2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı aynı nesne üzerinde bu arabirimi uygulayan [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) barındırma işlemi hakkında bilgi sağlamak için arabirim. Bu isteğe bağlı bir arabirimdir.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugProgram2` arabirimi bu arabirim elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramHost2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetHostName](../../../extensibility/debugger/reference/idebugprogramhost2-gethostname.md)|Başlık, kolay ad veya bu programın barındırma işlemi dosya adını alır.|  
|[GetHostId](../../../extensibility/debugger/reference/idebugprogramhost2-gethostid.md)|Bu programın barındırma işlemin işlem tanımlayıcısını alır.|  
|[GetHostMachineName](../../../extensibility/debugger/reference/idebugprogramhost2-gethostmachinename.md)|Barındırma işlemi bu programın üzerinde çalıştığı makinenin adını alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)