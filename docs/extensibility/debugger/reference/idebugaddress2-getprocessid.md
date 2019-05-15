---
title: IDebugAddress2::GetProcessID | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugAddress2::GetProcessID
helpviewer_keywords:
- IDebugAddress2::GetProcessID method
ms.assetid: 2c18889d-074a-4b95-87b4-bf1a067f44ed
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: a12be8b3999639c69d479412e673b0e049629172
ms.sourcegitcommit: 77b4ca625674658d5c5766e684fa0e2a07cad4da
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65615145"
---
# <a name="idebugaddress2getprocessid"></a>IDebugAddress2::GetProcessID
Bu tarafından temsil edilen nesnenin sahibi olan işlemin Kimliğini alır. [IDebugAddress2](../../../extensibility/debugger/reference/idebugaddress2.md) arabirimi.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetProcessID (
   DWORD* pProcID
);
```

```csharp
int GetProcessID (
   out uint pProcID
);
```

## <a name="parameters"></a>Parametreler
`pProcID`\
[out] İşlem kimliği

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugAddress2](../../../extensibility/debugger/reference/idebugaddress2.md)