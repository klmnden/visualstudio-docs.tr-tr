---
title: IDebugPort2::GetPortRequest | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPort2::GetPortRequest
helpviewer_keywords:
- IDebugPort2::GetPortRequest
ms.assetid: 14abf847-0675-4fa8-872e-971e00c84224
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e8a103316a292c444a35b8c819968d98cda777b6
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678130"
---
# <a name="idebugport2getportrequest"></a>IDebugPort2::GetPortRequest
Daha önce (varsa) bağlantı noktası oluşturmak için kullanılan bağlantı noktası açıklamasını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetPortRequest( 
   IDebugPortRequest2** ppRequest
);
```

```csharp
int GetPortRequest( 
   out IDebugPortRequest2 ppRequest
);
```

#### <a name="parameters"></a>Parametreler
 `ppRequest`

 [out] Döndürür bir [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md) bağlantı noktası oluşturmak için kullanılan istek temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  Döndürür `E_PORT_NO_REQUEST` bir bağlantı noktası kullanarak oluşturulmamışsa bir [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md) bağlantı isteği.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)
- [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)