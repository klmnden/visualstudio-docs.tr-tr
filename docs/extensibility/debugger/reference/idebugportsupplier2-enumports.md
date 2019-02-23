---
title: IDebugPortSupplier2::EnumPorts | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortSupplier2::EnumPorts
helpviewer_keywords:
- IDebugPortSupplier2::EnumPorts
ms.assetid: 88b57fd2-eba1-44fa-bd34-cf2ad2b1ff87
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5b814c8097e001badafb93c27370ba5982eda48c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56703165"
---
# <a name="idebugportsupplier2enumports"></a>IDebugPortSupplier2::EnumPorts
Bağlantı noktası sağlayıcısı tarafından sağlanan tüm bağlantı noktalarının bir listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumPorts( 
   IEnumDebugPorts2** ppEnum
);
```

```csharp
int EnumPorts( 
   out IEnumDebugPorts2 ppEnum
);
```

#### <a name="parameters"></a>Parametreler
 `ppEnum`

 [out] Döndürür bir [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md) sağlanan bağlantı noktalarının bir listesini içeren nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)
- [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md)