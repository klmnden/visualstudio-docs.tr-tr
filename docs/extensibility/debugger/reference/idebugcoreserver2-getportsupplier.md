---
title: IDebugCoreServer2::GetPortSupplier | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer2::GetPortSupplier
helpviewer_keywords:
- IDebugCoreServer2::GetPortSupplier
ms.assetid: acf181d4-ef42-4aa5-86f9-95fd5467ea31
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7ec665e3da8961b801c7e95efaee8bff3994b6b4
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66205621"
---
# <a name="idebugcoreserver2getportsupplier"></a>IDebugCoreServer2::GetPortSupplier
Belirli bir bağlantı noktası sağlayıcısı alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetPortSupplier( 
   REFGUID               guidPortSupplier,
   IDebugPortSupplier2** ppPortSupplier
);
```

```csharp
int GetPortSupplier( 
   ref Guid                guidPortSupplier,
   out IDebugPortSupplier2 ppPortSupplier
);
```

## <a name="parameters"></a>Parametreler
`guidPortSupplier`\
[in] Alınacak bağlantı noktası sağlayıcısı GUID.

`ppPortSupplier`\
[out] Döndürür bir [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) istenen bağlantı noktası sağlayıcısı temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)