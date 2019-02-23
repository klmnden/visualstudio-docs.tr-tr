---
title: IDebugEngine2::CauseBreak | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2::CauseBreak
helpviewer_keywords:
- IDebugEngine2::CauseBreak
ms.assetid: 17fe4698-b04e-4798-8412-80e0da60c387
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fa0d559887019a697b820a5a6c91f80b78c6b713
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678143"
---
# <a name="idebugengine2causebreak"></a>IDebugEngine2::CauseBreak
Tüm programları bu hata ayıklama altyapısı yürütme sonraki durdurmak için (DE) hata ayıklaması yapılan istekleri, iş parçacıkları birini çalıştırmayı dener.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CauseBreak( 
   void 
);
```

```csharp
int CauseBreak();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu zaman uyumsuz bir yöntemdir: bir [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) program bu yöntem çağrıldıktan sonra yürütülecek sonraki denediğinde olay gönderilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md)
- [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)