---
title: IDebugProcess2::EnumThreads | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess2::EnumThreads
helpviewer_keywords:
- IDebugProcess2::EnumThreads
ms.assetid: 05677385-7a7f-4545-8438-af00dde85db0
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9b6a1f7ab44666d88dd0ca5edc0aa55f418fdf4c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53900300"
---
# <a name="idebugprocess2enumthreads"></a>IDebugProcess2::EnumThreads
Bir işlemde çalışan tüm iş parçacıklarının listesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumThreads(  
   IEnumDebugThreads2** ppEnum  
);  
```  
  
```csharp  
int EnumThreads(  
   out IEnumDebugThreads2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md) tüm programlar işlemdeki tüm iş parçacıklarının listesini içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, her programda çalışan iş parçacıkları numaralandırır ve ardından bunları iş parçacığı bir işlem görünüme birleştirir. Tek bir iş parçacığı, birden çok programlarında çalışabilir; Bu yöntem yalnızca bir kez iş parçacığı numaralandırır.  
  
 Bu yöntem, çoğaltmaları olmadan işlem iş parçacıklarının listesini gösterir. Aksi takdirde, belirli bir programı çalışan iş parçacıkları listeleme için kullanın [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md)