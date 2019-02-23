---
title: IDebugPortSupplier2::RemovePort | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortSupplier2::RemovePort
helpviewer_keywords:
- IDebugPortSupplier2::RemovePort
ms.assetid: f5c1fbf2-9084-46f2-a682-7db963928df2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: db48cc82e16f071ec55493e98570c6969324bfda
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685752"
---
# <a name="idebugportsupplier2removeport"></a>IDebugPortSupplier2::RemovePort
Bir bağlantı noktası kaldırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT RemovePort( 
   IDebugPort2* pPort
);
```

```csharp
int RemovePort( 
   IDebugPort2 pPort
);
```

#### <a name="parameters"></a>Parametreler
 `pPort`

 [in] Bir [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) kaldırılacak bağlantı noktasını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem bağlantı noktasının bağlantı noktası tedarikçi iç etkin bağlantı noktalarını listeden kaldırır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)