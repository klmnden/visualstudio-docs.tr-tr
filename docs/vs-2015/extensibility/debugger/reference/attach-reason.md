---
title: ATTACH_REASON | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- ATTACH_REASON
helpviewer_keywords:
- ATTACH_REASON enumeration
ms.assetid: 159fb70b-a344-4ba6-9115-b7eaa16e228f
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b1805956ad9726a900d8425ac04a9215fcb70f65
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49189923"
---
# <a name="attachreason"></a>ATTACH_REASON
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir program düğüme iliştirmek için hata ayıklama altyapısı (DE) nedenini belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_ATTACH_REASON {   
   ATTACH_REASON_LAUNCH = 0x0001,  
   ATTACH_REASON_USER   = 0x0002,  
   ATTACH_REASON_AUTO   = 0x0003  
};  
typedef DWORD ATTACH_REASON;  
```  
  
```csharp  
public enum enum_ATTACH_REASON {   
   ATTACH_REASON_LAUNCH = 0x0001,  
   ATTACH_REASON_USER   = 0x0002,  
   ATTACH_REASON_AUTO   = 0x0003  
};  
```  
  
## <a name="members"></a>Üyeler  
 ATTACH_REASON_AUTO  
 İşlem şu anda hata ayıklama modunda olduğundan ekleyin.  
  
 ATTACH_REASON_LAUNCH  
 İşlem başlatıldığından ekleyin.  
  
 ATTACH_REASON_USER  
 Bir kullanıcı isteği nedeniyle ekleyin.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değerler için parametre olarak kullanılan [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) ve [iliştirme](../../../extensibility/debugger/reference/idebugprogramex2-attach.md) yöntemleri.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Ekleme](../../../extensibility/debugger/reference/idebugengine2-attach.md)   
 [Attach](../../../extensibility/debugger/reference/idebugprogramex2-attach.md)

