---
title: IDebugThread2::GetLogicalThread | Microsoft Docs
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
- IDebugThread2::GetLogicalThread
helpviewer_keywords:
- IDebugThread2::GetLogicalThread
ms.assetid: bce6230e-41d4-49b7-a050-2dde5efb6805
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: eee8e8f205cb1dbc220c50dd1f7abd342c942483
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49284069"
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

