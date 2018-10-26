---
title: IDebugProgram2::Attach | Microsoft Docs
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
- IDebugProgram2::Attach
helpviewer_keywords:
- IDebugProgram2::Attach
ms.assetid: de069fbf-a565-4905-b102-f5658c55aacd
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4c64b4839d2f16adfcf40b082d54f60a95d7a468
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49881646"
---
# <a name="idebugprogram2attach"></a>IDebugProgram2::Attach
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Programa ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Attach(   
   IDebugEventCallback2* pCallback  
);  
```  
  
```csharp  
int Attach(   
   IDebugEventCallback2 pCallback  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pCallback`  
 [in] Bir [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) hata ayıklama olayı bildirim için kullanılacak nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Aşağıdaki tabloda bazı olası hata kodları gösterilir.  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`E_ATTACH_DEBUGGER_ALREADY_ATTACHED`|Belirtilen program için hata ayıklayıcı zaten iliştirilmiş.|  
|`E_ATTACH_DEBUGGEE_PROCESS_SECURITY_VIOLATION`|Ekleme işlemi sırasında bir güvenlik ihlali oluştu.|  
|`E_ATTACH_CANNOT_ATTACH_TO_DESKTOP`|Bir masaüstü programına için hata ayıklayıcı eklenemiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama altyapısı (DE), hiçbir zaman bir programa eklemek için bu yöntemi çağırır. Programın adres alanında DE çalıştırıyorsa [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md) yöntemi çağrılır. Oturum hata ayıklama manager'ın içinde DE çalışır (SDM) adres alanı, [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi çağrılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)   
 [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md)   
 [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)

