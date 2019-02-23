---
title: IDebugProgram2::CauseBreak | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::CauseBreak
helpviewer_keywords:
- IDebugProgram2::CauseBreak
ms.assetid: 07d353fc-68ab-4297-a18f-3d3c7a80e121
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 06b392dd10c364e746f592a4d0ffd9ac32ca7df9
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56720217"
---
# <a name="idebugprogram2causebreak"></a>IDebugProgram2::CauseBreak
Program yürütme sonraki durdurma isteği çalışma iş parçacığı girişimlerinin birini zaman.

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
 Bir [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) program sonraki kodu bu yöntemi çağrıldıktan sonra çalıştırmayı denediğinde, olay gönderilir.

 Programı durdurmak için mutlaka beklemenize gerek kalmadan yöntem hemen döner, bu zaman uyumsuz bir yöntemdir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md)