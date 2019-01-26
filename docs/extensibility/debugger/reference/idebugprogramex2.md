---
title: IDebugProgramEx2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgramEx2
helpviewer_keywords:
- IDebugProgramEx2 interface
ms.assetid: 663359ed-635a-4539-addb-0cc52f19d1bd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c30be6fb9bd87972c3a3d186acc1fae9568ccc20
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55011968"
---
# <a name="idebugprogramex2"></a>IDebugProgramEx2
Bu arabirim, hata ayıklama Yöneticisi (SDM), bir programa ekledikten ve programla ilişkili program düğümünü Al oturum sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProgramEx2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı aynı nesne üzerinde bu arabirimi uygulayan [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) aynı anda tüm oturumları izlemek bağlantı noktası sağlayıcısı izin vererek bağlı durumdayken, bir programa ekledikten SDM izin vermek için arabirimi Program. Seçerse bu özel bağlantı noktası sağlayıcısı bu arabirim uygulayabilir.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 SDM çağrıları [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugProgram2` programlar ekli oturumları izlemek için bu arabirimi almak için arabirim.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramEx2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Attach](../../../extensibility/debugger/reference/idebugprogramex2-attach.md)|Bir program bir oturumuna ekler.|  
|[GetProgramNode](../../../extensibility/debugger/reference/idebugprogramex2-getprogramnode.md)|Bir programla ilişkili program düğümünü alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, SDM ve program özeldir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Portpriv.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)