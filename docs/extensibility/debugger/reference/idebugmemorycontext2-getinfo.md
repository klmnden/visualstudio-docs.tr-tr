---
title: IDebugMemoryContext2::GetInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugMemoryContext2::GetInfo
helpviewer_keywords:
- GetInfo method
- IDebugMemoryContext2::GetInfo method
ms.assetid: 08c7f091-1816-4d64-8834-f9ecaac5c58d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 09ecbd655f67b3dcd79d237d6a710cd7003395fb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55007483"
---
# <a name="idebugmemorycontext2getinfo"></a>IDebugMemoryContext2::GetInfo
Alır bir [CONTEXT_INFO](../../../extensibility/debugger/reference/context-info.md) açıklanmaktadır bağlamın yapısı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetInfo(   
   CONTEXT_INFO_FIELDS dwFields,  
   CONTEXT_INFO*       pInfo  
);  
```  
  
```csharp  
int GetInfo(  
   enum_CONTEXT_INFO_FIELDS dwFields,   
   CONTEXT_INFO[]           pinfo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFields`  
 [in] Bayraklarının bir birleşimi [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md) hangi alanları gösteren numaralandırma [CONTEXT_INFO](../../../extensibility/debugger/reference/context-info.md) yapısı olan olacak şekilde doldurun.  
  
 `pInfo`  
 [out içinde] `CONTEXT_INFO` Girilir yapısının.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)   
 [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md)   
 [CONTEXT_INFO](../../../extensibility/debugger/reference/context-info.md)