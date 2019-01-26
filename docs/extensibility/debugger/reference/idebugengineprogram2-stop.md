---
title: IDebugEngineProgram2::Stop | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugEngineProgram2::Stop
helpviewer_keywords:
- IDebugEngineProgram2::Stop
ms.assetid: 6e1c3d56-fb67-4a5b-80f9-8ee5131972bf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9e60b328ee13a47df9d7656c992f81e63cbbd2ed
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54983787"
---
# <a name="idebugengineprogram2stop"></a>IDebugEngineProgram2::Stop
Bu programa tüm iş parçacıkları durdurur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Stop(   
   void   
);  
```  
  
```csharp  
int Stop();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu program bir çok program ortamında ayıklanmakta olan bu yöntem çağrılır. Bu yöntem, bu programda başka bir programı durdurma olaydan alındığında çağrılır. Bu yöntemin uygulanmasını zaman uyumsuz olması gerekir; diğer bir deyişle, tüm iş parçacıkları bu yöntem döndürmeden önce durdurulması gerekir. Bu yöntemin uygulanmasını çağırmak kadar basit [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md) Bu program yöntemi.  
  
 Hata ayıklama olay yanıt olarak bu yöntem gönderilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)   
 [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md)