---
title: IDebugProgram2::EnumThreads | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::EnumThreads
helpviewer_keywords:
- IDebugProgram2::EnumThreads
ms.assetid: 0f2a8c51-1315-4c96-8aa1-6a937dc2a769
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: de5beb17fd0ffd3ca6f21c40ebdde85cc74225f4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53915419"
---
# <a name="idebugprogram2enumthreads"></a>IDebugProgram2::EnumThreads
Bir programda çalışan iş parçacıklarının listesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumThreads(   
   IEnumDebugThreads2** ppEnum  
);  
```  
  
```csharp  
int EnumThreads(   
   out IEnumDebugThreads2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md) iş parçacıklarının listesini içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)