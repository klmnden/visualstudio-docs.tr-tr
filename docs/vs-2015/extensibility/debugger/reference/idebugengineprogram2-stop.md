---
title: IDebugEngineProgram2::Stop | Microsoft Docs
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
- IDebugEngineProgram2::Stop
helpviewer_keywords:
- IDebugEngineProgram2::Stop
ms.assetid: 6e1c3d56-fb67-4a5b-80f9-8ee5131972bf
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b833dcab12fe4533e781154b90b8aceab7588c62
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49916640"
---
# <a name="idebugengineprogram2stop"></a>IDebugEngineProgram2::Stop
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu programa tüm iş parçacıkları durdurur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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

