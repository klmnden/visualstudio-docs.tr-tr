---
title: IDebugPortRequest2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortRequest2
helpviewer_keywords:
- IDebugPortRequest2 interface
ms.assetid: 556e610d-7c4b-44a8-965a-76a9d02b601a
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: fa72ae9d2cfbe399c3507406875e9c692d18b678
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801924"
---
# <a name="idebugportrequest2"></a>IDebugPortRequest2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim bir bağlantı noktası açıklar. Bu açıklama, bağlantı noktası için bağlantı noktası sağlayıcısı eklemek için kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPortRequest2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Visual Studio, genellikle hata ayıklama bağlantı noktası bağlantı noktası sağlayıcısı alma işleminde bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim yöntemlere geçirilen [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md) hata ayıklama bağlantı oluşturmak için. Bir çağrı [GetPortRequest](../../../extensibility/debugger/reference/idebugport2-getportrequest.md) ilk başta bağlantı noktası oluşturmak için kullanılan istek temsil eden bu arabirimi döndürür.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortRequest2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetPortName](../../../extensibility/debugger/reference/idebugportrequest2-getportname.md)|Oluşturmak için bağlantı noktası adını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama altyapısı genellikle bağlantı noktası sağlayıcısı ile etkileşime girmez ve bu arabirim için herhangi bir kullanıma sahip olur.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)   
 [GetPortRequest](../../../extensibility/debugger/reference/idebugport2-getportrequest.md)
