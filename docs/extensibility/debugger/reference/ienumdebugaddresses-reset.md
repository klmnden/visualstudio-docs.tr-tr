---
title: IEnumDebugAddresses::Reset | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugAddresses::Reset
helpviewer_keywords:
- IEnumDebugAddresses::Reset method
ms.assetid: 3a9d7f20-5bc6-4e13-8e91-5af4092e092f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 28819350dd0fe0c4cfb6fdc27fcd00aeb9456aea
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56710519"
---
# <a name="ienumdebugaddressesreset"></a>IEnumDebugAddresses::Reset
Bu yöntem, ilk öğe için sabit sıfırlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Reset(void);
```

```csharp
int Reset();
```

#### <a name="parameters"></a>Parametreler
 Hiçbiri

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem çağrıldığında sonra yapılan sonraki çağrıda [sonraki](../../../extensibility/debugger/reference/ienumdebugaddresses-next.md) numaralandırma ilk öğeyi döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md)
- [Next](../../../extensibility/debugger/reference/ienumdebugaddresses-next.md)