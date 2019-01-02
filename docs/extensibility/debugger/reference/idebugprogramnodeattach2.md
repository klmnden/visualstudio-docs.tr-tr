---
title: IDebugProgramNodeAttach2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgramNodeAttach2
helpviewer_keywords:
- IDebugProgramNodeAttach2 interface
ms.assetid: 46b37ac9-a026-4ad3-997b-f19e2f8deb73
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: e212c195754fcab8d60beb3a6536606d6ce86054
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53851803"
---
# <a name="idebugprogramnodeattach2"></a>IDebugProgramNodeAttach2
Bir programı ilişkili programa ekleme girişimi bildirilmesini düğüme sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProgramNodeAttach2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirimi uygulayan aynı sınıf uygulanan [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) arabirimi iliştirme işlemi bildirim almak için ve iliştirme işlemi iptal etmek için bir fırsat sunar.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim çağırarak elde `QueryInterface` yönteminde bir [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) nesne. [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md) yöntemi çağrıldığında, önce [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi program düğüm ekleme işlemini durdurmak için bir şans verin.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Bu arabirim, aşağıdaki yöntemi uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md)|İlişkili programına iliştirir veya ekleme işlemi için erteler [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim kullanım dışı tercih edilen alternatif olan [Attach_V7](../../../extensibility/debugger/reference/idebugprogramnode2-attach-v7.md) yöntemi. Tüm hata ayıklama altyapıları ile her zaman yüklenir `CoCreateInstance` işlev, diğer bir deyişle, bunlar ayıklanan programa Adres alanının örneği oluşturulur.  
  
 Önceki bir uygulaması, `IDebugProgramNode2::Attach_V7` yöntemi yalnızca ayar `GUID` , ardından yalnızca ayıklanan programın [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md) yöntemi uygulanması gerekiyor.  
  
 Önceki bir uygulaması, `IDebugProgramNode2::Attach_V7` sağlanan geri arama arabirimini kullanılan yöntem ve ardından ilgili işlev uygulaması için taşınması gereken [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi ve `IDebugProgramNodeAttach2` arabirimi yok uygulanmalıdır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [Ekleme](../../../extensibility/debugger/reference/idebugengine2-attach.md)   
 [Attach_V7](../../../extensibility/debugger/reference/idebugprogramnode2-attach-v7.md)