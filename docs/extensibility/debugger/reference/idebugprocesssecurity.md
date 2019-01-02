---
title: IDebugProcessSecurity | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugProcessSecurity interface
ms.assetid: 8a52ddca-bd99-49c0-9778-469dce7abd44
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7e34a93e73bd1c4c9b5e70f89d318c2db6a84f2b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53967962"
---
# <a name="idebugprocesssecurity"></a>IDebugProcessSecurity
`IDebugProcessSecurity` işleme iliştirdikten güvenli olduğunu kullanıcıyı uyarmak için bağlantı noktası sağlayıcısı tarafından uygulanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProcessSecurity : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProcessSecurity`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetUserName](../../../extensibility/debugger/reference/idebugprocesssecurity-getusername.md)|Kullanıcı adı bağlantı noktası tedarikçiden alır.|  
|[QueryCanSafelyAttach](../../../extensibility/debugger/reference/idebugprocesssecurity-querycansafelyattach.md)|Hata ayıklama işlemine iliştirme'güvenli olmayan bir kullanıcıyı uyarır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir uyarı gösterir ve kullanıcının olduğu iliştirmekte olduğunuz işlemin güvensiz kabul edilebilir iptal izin vermek için bu arabirimi uygulayın.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Bağlantı noktaları](../../../extensibility/debugger/ports.md)   
 [Bağlantı noktası sağlayıcıları](../../../extensibility/debugger/port-suppliers.md)   
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)