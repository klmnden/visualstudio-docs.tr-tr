---
title: IDebugPort2::GetPortSupplier | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPort2::GetPortSupplier
helpviewer_keywords:
- IDebugPort2::GetPortSupplier
ms.assetid: 7a7b0615-df6b-4726-ab35-39dfa1ebed8f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 0f3bca55ac7306b4b67e9456cf24e9a497fda422
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66209144"
---
# <a name="idebugport2getportsupplier"></a>IDebugPort2::GetPortSupplier
Bu bağlantı için bağlantı noktası sağlayıcısı alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetPortSupplier( 
   IDebugPortSupplier2** ppSupplier
);
```

```csharp
int GetPortSupplier( 
   out IDebugPortSupplier2 ppSupplier
);
```

## <a name="parameters"></a>Parametreler
`ppSupplier`\
[out] Döndürür bir [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) nesnesini temsil eden bir bağlantı noktası için bağlantı noktası sağlayıcısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)