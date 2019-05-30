---
title: IDebugProgram2::CauseBreak | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::CauseBreak
helpviewer_keywords:
- IDebugProgram2::CauseBreak
ms.assetid: 07d353fc-68ab-4297-a18f-3d3c7a80e121
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: a01b5982b4f747bd70c3a35bc0b7191bb54cd21b
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66311352"
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

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md)