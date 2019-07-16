---
title: IDebugThread2::GetLogicalThread | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugThread2::GetLogicalThread
helpviewer_keywords:
- IDebugThread2::GetLogicalThread
ms.assetid: bce6230e-41d4-49b7-a050-2dde5efb6805
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: f430ea7ba69ca55bc76543d853396e22b193cf02
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68153058"
---
# <a name="idebugthread2getlogicalthread"></a>IDebugThread2::GetLogicalThread
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama altyapısı, bu yöntemi uygulaması değil.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetLogicalThread(   
   IDebugStackFrame2*     pStackFrame,  
   IDebugLogicalThread2** ppLogicalThread  
);  
```  
  
```csharp  
int GetLogicalThread(   
   IDebugStackFrame2        pStackFrame,  
   out IDebugLogicalThread2 ppLogicalThread  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pStackFrame`  
 [in] Bir [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) yığın çerçevesini temsil eden nesne.  
  
 `ppLogicalThread`  
 [out] Döndürür bir `IDebugLogicalThread2` ilişkili mantıksal iş parçacığını temsil eden arabirim. Hata ayıklama altyapısı uygulama bu null bir değere ayarlamanız gerekir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Hata ayıklama altyapısı uygulamaları her zaman dönüş `E_NOTIMPL`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
