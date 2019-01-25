---
title: IDebugMemoryBytes2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugMemoryBytes2
helpviewer_keywords:
- IDebugMemoryBytes2 interface
ms.assetid: d7647575-0e06-4190-88f5-ca40b82209a4
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 1e23588e8da41b981f372210def65fa34a7e55bf
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764234"
---
# <a name="idebugmemorybytes2"></a>IDebugMemoryBytes2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, belleğin bayt temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugMemoryBytes2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE) bayt cinsinden bellek temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugprogram2-getmemorybytes.md) sistem belleği erişim sağlamak için bu arabirimi döndürür. [GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md) ve [GetMemoryBytes](../../../extensibility/debugger/reference/idebugreference2-getmemorybytes.md) nesnenin bayt erişim sağlamak için bu arabirimi döndürür.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugMemoryBytes2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[ReadAt](../../../extensibility/debugger/reference/idebugmemorybytes2-readat.md)|Belirli bir konumda itibaren bayt dizisini okur.|  
|[WriteAt](../../../extensibility/debugger/reference/idebugmemorybytes2-writeat.md)|Yazar `dwCount` bayt cinsinden başlangıç `pStartContext`.|  
|[GetSize](../../../extensibility/debugger/reference/idebugmemorybytes2-getsize.md)|Bu arabirim tarafından temsil edilen belleğin bayt cinsinden boyutunu alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Özellikleri için bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) diziyi temsil eden arabirim sağlar bir `IDebugMemoryBytes2` , dizideki değerlere erişmek için arabirim.  
  
 Visual Studio'nun **bellek görünümü** çağrıları [GetMemoryBytes](../../../extensibility/debugger/reference/idebugprogram2-getmemorybytes.md) almak için bir `IDebugMemoryBytes2` sistem belleği erişmek için arabirim. Erişilecek adresi elde edilen adres olarak bellek görünüme girdiğiniz ifade ayrıştırma ve ardından kullanarak ayrıştırılmış ifade değerlendirme göre [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) almak için bir `IDebugProperty2` arabirimi. Bir çağrı [GetMemoryContext](../../../extensibility/debugger/reference/idebugproperty2-getmemorycontext.md) döndürür [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) , bellek adresi açıklar. Bu bellek bağlam geçirilerek [ReadAt](../../../extensibility/debugger/reference/idebugmemorybytes2-readat.md) ve [WriteAt](../../../extensibility/debugger/reference/idebugmemorybytes2-writeat.md).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugprogram2-getmemorybytes.md)   
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md)   
 [GetMemoryBytes](../../../extensibility/debugger/reference/idebugreference2-getmemorybytes.md)   
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)
