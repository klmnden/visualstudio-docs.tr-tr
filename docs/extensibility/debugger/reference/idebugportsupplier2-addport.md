---
title: IDebugPortSupplier2::AddPort | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortSupplier2::AddPort
helpviewer_keywords:
- IDebugPortSupplier2::AddPort
ms.assetid: df491161-6bf3-4fcc-b478-b9ec88ec995f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5c674b73ad6ec45b1e388f62fbd3103afb5daedb
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678235"
---
# <a name="idebugportsupplier2addport"></a>IDebugPortSupplier2::AddPort
Bir bağlantı noktası ekler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT AddPort( 
   IDebugPortRequest2* pRequest,
   IDebugPort2**       ppPort
);
```

```csharp
int AddPort( 
   IDebugPortRequest2 pRequest,
   out IDebugPort2    ppPort
);
```

#### <a name="parameters"></a>Parametreler
 `pRequest`

 [in] Bir [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md) eklenecek bağlantı noktasını tanımlayan nesne.

 `ppPort`

 [out] Döndürür bir [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) bağlantı noktasını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, istenen bağlantı noktası hem de bağlantı noktası tedarikçi iç etkin bağlantı noktalarının listesine ekleyerek gerçekten oluşturur. [CanAddPort](../../../extensibility/debugger/reference/idebugportsupplier2-canaddport.md) yöntemi çağrıldığında önce olası zaman gecikmeleri önlemek için.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)
- [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [CanAddPort](../../../extensibility/debugger/reference/idebugportsupplier2-canaddport.md)