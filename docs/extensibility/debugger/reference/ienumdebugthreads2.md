---
title: IEnumDebugThreads2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugThreads2
helpviewer_keywords:
- IEnumDebugThreads2
ms.assetid: 1854f078-3b49-42c2-b65b-33e3b506fd63
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1fbb062f61266595b6dc0ae914341b4e9f1d3610
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53842349"
---
# <a name="ienumdebugthreads2"></a>IEnumDebugThreads2
Geçerli hata ayıklama oturumunda çalışan iş parçacıkları bu interfac numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugThreads2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE), bir programdaki iş parçacıklarının listesini temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [EnumThreads](../../../extensibility/debugger/reference/idebugprocess2-enumthreads.md) programlar bir işlemde çalışan tüm iş parçacıklarının listesini temsil eden bu arabirimi elde edilir. Çağrı [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md) bir programda çalışan iş parçacıklarının listesini temsil eden bu arabirimi elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugThreads2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugthreads2-next.md)|Belirtilen bir numaralandırma sıralı iş parçacıklarının sayısını alır.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugthreads2-skip.md)|Bir numaralandırma sıralı iş parçacıklarında belirtilen sayıda atlar.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugthreads2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugthreads2-clone.md)|Geçerli planla aynı sıralaması durumu içeren bir numaralandırıcı oluşturur.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugthreads2-getcount.md)|İş parçacığı sayısını bir numaralandırıcı alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Visual Studio genellikle güncelleştirmek için bu arabirimi alır **iş parçacıkları** çağırmak için ilk iş parçacığında listenin edinmeniz için de penceresi [yürütme](../../../extensibility/debugger/reference/idebugprocess3-execute.md), [devam](../../../extensibility/debugger/reference/idebugprocess3-continue.md), ve [Adım](../../../extensibility/debugger/reference/idebugprocess3-step.md).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprocess2-enumthreads.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md)   
 [Adım](../../../extensibility/debugger/reference/idebugprocess3-step.md)   
 [Devam et](../../../extensibility/debugger/reference/idebugprocess3-continue.md)   
 [Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)