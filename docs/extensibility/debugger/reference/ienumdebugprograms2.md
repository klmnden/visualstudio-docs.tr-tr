---
title: IEnumDebugPrograms2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugPrograms2
helpviewer_keywords:
- IEnumDebugPrograms2
ms.assetid: 7fbb8fb7-db64-4546-a364-dc668430c8af
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d0277c316329e0adb763eb614f6d453a531781c7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53877477"
---
# <a name="ienumdebugprograms2"></a>IEnumDebugPrograms2
Bu arabirim geçerli hata ayıklama oturumunda çalışan programlar numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugPrograms2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE) tarafından DE ayıklanan programların listesini sağlamak için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Visual Studio çağrıları [EnumPrograms](../../../extensibility/debugger/reference/idebugprocess2-enumprograms.md) bu arabirimi elde edilir. [EnumPrograms](../../../extensibility/debugger/reference/idebugengine2-enumprograms.md) Visual Studio tarafından kullanılmaz.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugPrograms2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugprograms2-next.md)|Belirtilen bir sabit listesi sırası programlarında sayısını alır.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugprograms2-skip.md)|Bir numaralandırma sıralı programlarında belirtilen sayıda atlar.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugprograms2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugprograms2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugprograms2-getcount.md)|Program sayısını bir numaralandırıcı alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Visual Studio bu arabirime kullanır:  
  
-   Doldurma **modülleri** penceresi (çağırarak [EnumPrograms](../../../extensibility/debugger/reference/idebugprocess2-enumprograms.md) ve ardından arama [EnumModules](../../../extensibility/debugger/reference/idebugprogram2-enummodules.md) her programı'nda).  
  
-   Doldurma **iliştirme** listesi (çağırarak `IDebugProcess2::EnumPrograms` ve ardından arama [QueryInterface](/cpp/atl/queryinterface) her [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) bir almakiçinarabirimi[IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md) arabirimi).  
  
-   İşlemdeki her programda hata ayıklamak DEs listesini oluşturmak (kullanarak [GetEngineInfo](../../../extensibility/debugger/reference/idebugprogram2-getengineinfo.md)).  
  
-   Düzenle ve devam et (ENC) güncelleştirmeleri her program için geçerlidir (IDebugProcess2::EnumPrograms çağırarak ve ardından arama [GetENCUpdate](../../../extensibility/debugger/reference/idebugprogram2-getencupdate.md)).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumPrograms](../../../extensibility/debugger/reference/idebugengine2-enumprograms.md)   
 [EnumPrograms](../../../extensibility/debugger/reference/idebugprocess2-enumprograms.md)