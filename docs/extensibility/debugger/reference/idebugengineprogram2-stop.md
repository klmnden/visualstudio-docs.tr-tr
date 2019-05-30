---
title: IDebugEngineProgram2::Stop | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngineProgram2::Stop
helpviewer_keywords:
- IDebugEngineProgram2::Stop
ms.assetid: 6e1c3d56-fb67-4a5b-80f9-8ee5131972bf
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ba93c88eb3d7e996b2a5f19dda605653af090c94
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345210"
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

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)
- [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md)