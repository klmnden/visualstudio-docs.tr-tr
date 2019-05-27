---
title: IDebugBreakpointRequest3::GetRequestInfo2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBreakpointRequest3::GetRequestInfo2
helpviewer_keywords:
- IDebugBreakpointRequest3::GetRequestInfo2
ms.assetid: 33942e4a-0a0a-49e8-a693-004954f6d38a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 58c313ebc56035d40d4743b9411c476434c82123
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66199765"
---
# <a name="idebugbreakpointrequest3getrequestinfo2"></a>IDebugBreakpointRequest3::GetRequestInfo2
Bu yöntem, bu kesme noktası istek tanımlayan kesme noktası isteği bilgilerini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetRequestInfo2(
   BPREQI_FIELDS      dwFields,
   BP_REQUEST_INFO2*  bBPRequestInfo
);
```

```csharp
int GetRequestInfo2(
   enum_BPREQI_FIELDS  dwFields,
   BP_REQUEST_INFO2[]  bBPRequestInfo
);
```

## <a name="parameters"></a>Parametreler
`dwFields`\
[in] Bayraklarının bir birleşimi [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md) hangi alanları belirlemek numaralandırma `pBPRequestInfo` doldurulacak olan.

`bBPRequestInfo`\
[out] [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapısına doldurulmasını.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu isteği öğesinden döndürülen çok daha fazla bilgi bulunmaktadır [GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugBreakpointRequest3](../../../extensibility/debugger/reference/idebugbreakpointrequest3.md)
- [GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md)
- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)
- [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md)